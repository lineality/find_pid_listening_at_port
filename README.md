## find_pid_listening_at_port


# Method 1
```
$ sudo ss -lptn 'sport = :80'
```

# Method 2
```
$ sudo lsof -n -i :80 | grep LISTEN
```

# Method 3
```
$ sudo nethogs

$ kill -9 <PID #####>
```
