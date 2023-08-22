依赖：
```
$ go mod tidy
```

测试输入输出：
```
gohangout.exe --config test/test_stdin_stdout.yml
```

测试tcp输入：
```
gohangout.exe --config test/test_tcp_stdout.yml
```

tcp测试：
```
lenovo@DESKTOP-V4UHF0P MINGW32 /d/GoProject/gohangout-1.9.14 (master)
$ nc -h
[v1.12 NT http://eternallybored.org/misc/netcat/]
connect to somewhere:   nc [-options] hostname port[s] [ports] ...
listen for inbound:     nc -l -p port [options] [hostname] [port]
options:
        -d              detach from console, background mode

        -e prog         inbound program to exec [dangerous!!]
        -g gateway      source-routing hop point[s], up to 8
        -G num          source-routing pointer: 4, 8, 12, ...
        -h              this cruft
        -i secs         delay interval for lines sent, ports scanned
        -l              listen mode, for inbound connects
        -L              listen harder, re-listen on socket close
        -n              numeric-only IP addresses, no DNS
        -o file         hex dump of traffic
        -p port         local port number
        -r              randomize local and remote ports
        -s addr         local source address
        -t              answer TELNET negotiation
        -c              send CRLF instead of just LF
        -u              UDP mode
        -v              verbose [use twice to be more verbose]
        -w secs         timeout for connects and final net reads
        -z              zero-I/O mode [used for scanning]
port numbers can be individual or ranges: m-n [inclusive]

lenovo@DESKTOP-V4UHF0P MINGW32 /d/GoProject/gohangout-1.9.14 (master)
$ nc -l -p 8002


lenovo@DESKTOP-V4UHF0P MINGW32 /d/GoProject/gohangout-1.9.14 (master)
$ nc 127.0.0.1 8089
{"a": 1}
{"a": 22}
{"a": 22, "name": "莫南"}
{"a": 22, "name": "莫南"}
{"a": 22, "name": "莫南"}

lenovo@DESKTOP-V4UHF0P MINGW32 /d/GoProject/gohangout-1.9.14 (master)
$
```
