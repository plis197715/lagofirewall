# lagofirewall


## install

```
$ sudo apt-get install jq
$ git clone https://github.com/hibitomo/lagofirewall
$ cd lagofirewall
$ git clone https://github.com/hibitomo/ofctl_script
$ cd scripts/db2rules
$ make
$ cd ../..
```

## Usage


```
$ cd lagofirewall
$ ryu-manager lagofirewall.py /path/to/ryu/app/ofctl_rest.py
```

Add filter rules

```
$ ./add_rule [priority] [IP_src] [IP_dst] [tcp|udp] [Pt_src] [Pt_dst] [drop|accept]
$ ./add_rule 100 192.168.10.0/24 0.0.0.0/0 tcp 0:65535 80:80 drop
```

Delete filter rules

```
$ ./del_rule [priority] [IP_src] [IP_dst] [tcp|udp] [Pt_src] [Pt_dst] [drop|accept]
$ ./del_rule 100 192.168.10.0/24 0.0.0.0/0 tcp 0:65535 80:80
```
