goprocinfo
===================

/proc information parser for Go, includes a fix for older kernels

Usage
---------------

```go
import linuxproc "github.com/nlacey/goprocinfo/linux"

stat, err := linuxproc.ReadStat("/proc/stat")
if err != nil {
    t.Fatal("stat read fail")
}

for _, s := range stat.CPUStats {
    // s.User
    // s.Nice
    // s.System
    // s.Idle
    // s.IOWait
}

// stat.CPUStatAll
// stat.CPUStats
// stat.Processes
// stat.BootTime
// ... etc
```


Reference
------------

* http://www.mjmwired.net/kernel/Documentation/filesystems/proc.txt
