# Files

---

### Safety First
* IO operations can fail.
* And they _will_ fail!
* Either...
  * throws `std::filesystem::filesystem_error` or...
  * returns `std::error_code` as output_parameter

---

### Safety First
Most functions have 2 signatures, one throwing and one `noexcept`

```cpp
bool exists( const std::filesystem::path& p );
bool exists( const std::filesystem::path& p,
             std::error_code& ec ) noexcept;
```

---

### File Information
* `exists(p)`
* `file_size(p)`
* `is_empty(p)`, `is_regular_file()`, ...
* links, permissions, mtime, status, ...

---

### Read/Write with <fstream>
* `std::fstream(const char*, mode)` (since C++98)
* `std::fstream(std::string const&, mode)` (since C++11)
* `std::fstream(std::filesystem::path const&, mode)` (since C++17)

---

### Rename, Copy, Etc..
* `copy(from, to)`  - copy file or directory
* `copy_file(from, to)` - copy file only
* `rename(old_p, new_p)`
* `remove(p)`, `remove_all(p)`
