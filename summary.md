# Summary

---


### What's included?
* `std::filesystem::path`
  * explicit path type, vs. std::string
  * manipulation of paths
* File and Directory access
  * copy, rename, remove, ...
  * exits, type, status, size, ...
  * directory iteration

---

### What's missing?

---

### Temporary Files and Directories
* Atomically create a unique file name or directory
* Like the Linux command `tempfile` or `mktemp`
* or `tmpfile()` from `<stdio.h>` or `mkstemp(...)` from `<stdlib.h>`

```bash
~$ tempfile
/tmp/filevyLcbf
~$ mktemp -d
/tmp/tmp.Mtt52jXKCo
~$ ls -ld /tmp/filevyLcbf /tmp/tmp.Mtt52jXKCo
-rw------- 1 finn finn    0 Feb 11 22:22 /tmp/filevyLcbf
drwx------ 2 finn finn 4096 Feb 11 22:23 /tmp/tmp.Mtt52jXKCo
```

---

### What's more?

---

# More Documentation
* http://en.cppreference.com/w/cpp/filesystem/path
* http://www.boost.org/doc/libs/1_66_0/libs/filesystem/doc/reference.html

---

### End
Thank you for your Attention.
