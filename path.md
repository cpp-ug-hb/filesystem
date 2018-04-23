# Path

---

## The Path
* class `std::filesystem::path`
* like `std::string` but for paths

```cpp
using namespace std::filesystem;

path nothing {};
assert(nothing.empty() == true);

path bin = "/usr/bin";
path gcc = bin / "gcc";

std::cout << gcc << std::endl;

path p = "/";
p /= "opt";
path p2 = p / "gcc" / "7.3.0" / "bin";

```

---

### Path Constructors

* Default-, Copy and Move-Constructors
* From `string`, `string_view` or C-Style `const char*`
* From iterator range to char


Operators are **not** explicit.

---

### Path operators

* Copy- and Move-Assignment
*  `/`, `/=` or `append()` to join path
* `+=` or `concat()` to append text to a path

---

### Decomposition

```cpp
path p {"/usr/share/cppughb/README.md"};
```

* `p.root_directory() == "/"` or `"C:\\"`
* `p.relative_path() == "usr/share/cppughb/README.md"`
* `p.parent_path() == "/usr/share/cppughb"`
* `p.filename() == "README.md"`
* `p.stem() == "README"`
* `p.extension() == ".md"`

---

### Queries

```cpp
path p = "/usr/share/cppughb/README.md";
```

* `p.empty() == false`
* `p.has_*() == (not p.*().empty())`
* `p.is_absolute() == true`
* `p.is_relative() == false`

---

### Modifiers

```cpp
path p {"/usr/share/cppughb/README.md"};
```

* `p.clear()`
* `p.make_preferred() == "\\usr\\share\\cppughb\\README.md"` (on Windows)
* `p.remove_filename()`
* `p.replace_filename("LIESMICH.md")`
* `p.replace_extension(".txt")`
