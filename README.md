# OpenShift Update Graph Viewer

This repository is based on the work made by @ctron in https://github.com/ctron/openshift-update-graph.

On top of his work, this repository adds a proxy to get OpenShift update channels from GitHub and adds the posibility to get the update graph directly from a public/self-managed Cincinnati instance.

## How to use it

1. Build the main.go 
```
$ go build main.go 
```

2. Run the main.go
```
$ go run main.go 
```

3. Point your browser to http://127.0.0.1:8080


## Output samples of the CLI

1. Display the help
```
$ ./main -h
Options:

  -h, --help                 display help information
  -v                         Version
      --port[=8080]          Default port of communication
      --ipaddr[=127.0.0.1]   Default IPaddr
```
2. Query the version 
```
$ ./main -v
v0.0.2
```
3. Usage with different ports and ipaddres
```
$ ./main --port 8080 --ipaddr 0.0.0.0
2021/12/14 22:33:29 Starting OpenShift Update Graph v0.0.2
2021/12/14 22:33:29 Listening on 0.0.0.0:808

$ ./main --port 8443 --ipaddr 127.0.0.1
2021/12/14 22:46:37 Starting OpenShift Update Graph v0.0.2
2021/12/14 22:46:37 Listening on 127.0.0.1:8443
```
