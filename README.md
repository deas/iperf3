# iperf3 for k8s

Usage example:

```
➜  ~ kubectl -n iperf3 get svc
NAME     TYPE           CLUSTER-IP       EXTERNAL-IP    PORT(S)          AGE
iperf3   LoadBalancer   10.247.254.169   10.168.0.177   5201:32373/TCP   89m
➜  ~ iperf3 -c 10.168.0.177 -V -f K
iperf 3.7
Linux chuck 5.4.0-37-generic #41-Ubuntu SMP Wed Jun 3 18:57:02 UTC 2020 x86_64
Control connection MSS 1360
Time: Fri, 17 Jul 2020 06:14:25 GMT
Connecting to host 10.168.0.177, port 5201
      Cookie: swfgik5xsn6zo5lni6pq6i3sdj3pgxjk4ffo
      TCP MSS: 1360 (default)
[  5] local 172.20.39.15 port 51246 connected to 10.168.0.177 port 5201
Starting Test: protocol: TCP, 1 streams, 131072 byte blocks, omitting 0 seconds, 10 second test, tos 0
[ ID] Interval           Transfer     Bitrate         Retr  Cwnd
[  5]   0.00-1.00   sec  5.13 MBytes  5256 KBytes/sec    0    315 KBytes       
[  5]   1.00-2.00   sec  5.43 MBytes  5555 KBytes/sec    0    562 KBytes       
[  5]   2.00-3.00   sec  5.30 MBytes  5430 KBytes/sec    0    792 KBytes       
[  5]   3.00-4.00   sec  5.12 MBytes  5243 KBytes/sec    0   1.03 MBytes       
[  5]   4.00-5.00   sec  6.13 MBytes  6275 KBytes/sec    0   1.27 MBytes       
[  5]   5.00-6.00   sec  3.75 MBytes  3839 KBytes/sec    0   1.51 MBytes       
[  5]   6.00-7.00   sec  5.00 MBytes  5120 KBytes/sec    0   1.75 MBytes       
[  5]   7.00-8.00   sec  5.00 MBytes  5120 KBytes/sec    0   1.99 MBytes       
[  5]   8.00-9.00   sec  5.00 MBytes  5120 KBytes/sec    0   2.23 MBytes       
[  5]   9.00-10.00  sec  5.00 MBytes  5120 KBytes/sec    0   2.47 MBytes       
- - - - - - - - - - - - - - - - - - - - - - - - -
Test Complete. Summary Results:
[ ID] Interval           Transfer     Bitrate         Retr
[  5]   0.00-10.00  sec  50.9 MBytes  5208 KBytes/sec    0             sender
[  5]   0.00-10.51  sec  50.2 MBytes  4893 KBytes/sec                  receiver
CPU Utilization: local/sender 0.7% (0.0%u/0.7%s), remote/receiver 0.1% (0.0%u/0.1%s)
snd_tcp_congestion cubic
rcv_tcp_congestion cubic

iperf Done.
➜  ~ 
```
