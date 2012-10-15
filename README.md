namedmutex.py, a simple ctypes wrapper for Win32 named mutexes
==============================================================

NamedMutex is a class for using Windows (Win32) named mutexes for system-wide
locks. For example, we use these to lock system-wide log files that multiple
processes can write to.

This has a similar API to `threading.Lock`, and can be used with Python's
`with` statement.

For example:

```python
with namedmutex.NamedMutex('get_dir_mutex'):
    latest_dir = get_latest_dir()
    os.rename(latest_dir, latest_dir + '-processing')
```

See the [source code](https://github.com/benhoyt/namedmutex/blob/master/namedmutex.py)
for more info!
