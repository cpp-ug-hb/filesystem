# History


---

### C++98 - C++14: No filesystem API
* Only `<fstream>` to create/write files
* Platform API (POSIX, Win32, ...)

---

### Boost.Filesystem
* Introduced in Boost 1.30.0 (March 2003)
* Current version: 3
* Compatible to C++98 or later
* Base for Standatization in C++17
* http://www.boost.org/doc/libs/1_66_0/libs/filesystem/doc/index.htm


Note: Version 4 might be changed to reflact C++17 std::filesstem

---

### C++17: std::filesystem
* Standatized but not widely avaiable
* Header: `<filesystem>`
* Namespace: `std::filesystem`
* Not in GCC 7.3, but in trunk
* Not in clang 5.0
* Not in MSVC 19 - 2017
* http://en.cppreference.com/w/cpp/filesystem

---

### experimental/filesystem
* Pre-Standard implementation of the new API
* Header: `<experimental/filesystem>`
* Namespace: `std::experimental::filesystem`
* Available in GCC 5.3
* Available in clang 5.0
* Available in MSVC 19 - 2017

---

### Differences
* Mostly identical.
* Various details changed between Boost.Filesystem and std::filesystem.
* https://stackoverflow.com/a/46271698
