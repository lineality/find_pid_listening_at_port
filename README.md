## find_pid_listening_at_port

Once you find the pid (process ID) of, for example, the unresponsive server listening at a port, 
use one of these two to end the process.
```
$ kill -9 <PID #####>
or
# kill SIGKILL <PID #####>
```


# Method 1
```
$ sudo ss -lptn 'sport = :80'
$ kill -9 <PID #####>
```

# Method 2
```
$ sudo lsof -n -i :80 | grep LISTEN
$ kill -9 <PID #####>
```

# Method 3
```
$ sudo nethogs
$ kill -9 <PID #####>
```
