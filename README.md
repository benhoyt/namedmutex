namedmutex.py, a simple ctypes wrapper for Win32 named mutexes
==============================================================

NamedMutex is a class for using Windows (Win32) named mutexes for system-wide
locks. For example, we use these to lock system-wide log files that multiple
processes can write to.

This has a similar API to `threading.Lock`, and can be used with Python's
`with` statement.

See the [source code](https://github.com/benhoyt/namedmutex/blob/master/namedmutex.py)
for more info!
