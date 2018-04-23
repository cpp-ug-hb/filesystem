# Directories

---

### Remember: Safety First
* IO operations can fail.
* And they _will_ fail!
* Either...
  * throws `std::filesystem::filesystem_error` or...
  * returns `std::error_code` as output_parameter

---

### Safety First
Most functions have 2 signatures, one throwing and one `noexcept`

```cpp
bool create_directory( const std::filesystem::path& p );
bool create_directory( const std::filesystem::path& p,
                       std::error_code& ec ) noexcept;
```

---

### Information
* `exists( p )`
* `is_directory( p )`
* `current_path()`
* `temp_directory_path()`

---

### Creation
* `create_directory( p )` creates a directory in an existing path
* `create_directories( p )` creates a directory hierachy

---

### Manipulation
* `remove(p)`  delete a file or empty directory
* `remove_all(p)` delete a directory and everything inside
* `copy(from, to)`  - copy file or directory
* `rename(old_p, new_p)`

---

### Directory Listing (Iteration)
```cpp
for (auto &entry: fs::directory_iterator(p)) {
  // entry is a directory_entry const&
  // each file or directory in p, including "."
}
```

`std::filesytem::directory_entry` contains:
* `path()` relative to directory
* `status()`
* `is_regular_file()`, `is_directory()`, etc.

(see also: `recursive_directory_iterator`)
