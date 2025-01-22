
## The Server's Identity

Find the **hostname** of the server.


## Steps

Use the `strings` command and `grep` to find the keyword `localhost` and `hostname`

```bash
strings capture2.pcapng | grep -i "localhost" | grep -i "hostname"
```

We will get something like this:

```bash
var environment = {"is_cockpit_client":false,"page":{"connect":true,"require_host":false,"allow_multihost":true},"logged_into":[],"hostname":"localhost.localdomain","os-release":{"NAME":"Rocky Linux","ID":"rocky","PRETTY_NAME":"Rocky Linux 9.5 (Blue Onyx)","CPE_NAME":"cpe:/o:rocky:rocky:9::baseos","ID_LIKE":"rhel centos fedora"},"CACertUrl":"/ca.cer"};
        "Hostname": "localhost",
        "DefaultHostname": "localhost",
        "Hostname": "localhost",
        "DefaultHostname": "localhost",

```

We can see that the host name is:

```bash
  "hostname": "localhost.localdomain"
```

Hence, the falg is:

```bash
  KCTF{localhost.localdomain}
```



