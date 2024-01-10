# Project Documentation with Doxygen

## Introduction

This README provides guidelines on how to generate and customize a Doxyfile for your project using Doxygen. Doxygen is a documentation generator and is used to create documentation from annotated source code.

## Prerequisites

- Doxygen (1.8.13 or later recommended). Install it from [Doxygen's website](http://www.doxygen.nl/download.html) or use package managers like `apt` on Linux, `brew` on macOS, or `choco` on Windows.

## Generating a Doxyfile

To generate a default Doxyfile, run the following command in your project's root directory:

```bash
doxygen -g
```

This command creates a file named Doxyfile in the current directory with the default configuration.

## Customizing the Doxyfile

After generating the Doxyfile, you should customize it to suit your project. Key fields to update include:

1. Project Name: Set your project's name.

```makefile
PROJECT_NAME           = "Your Project Name"
```

2. Version Number: Specify the current version of your project.

```makefile
PROJECT_NUMBER         = "1.0"
```

3. Source Directories: Indicate where your source files are located.

```css
INPUT                  = ./src
```

4. Output Directory: Specify where the generated documentation should be placed.

```bash
OUTPUT_DIRECTORY       = ./docs
```

5. Generate HTML: Enable HTML documentation.

```makefile
GENERATE_HTML          = YES
```

6. Generate LaTeX: Enable/disable LaTeX documentation output.

```makefile
GENERATE_LATEX         = NO
```

7. EXTRACT_ALL: If set to YES, all classes and members will be included in the documentation.

```makefile
EXTRACT_ALL            = YES
```

8. Source Browser: If set to YES, a source code browser will be included.

```makefile
SOURCE_BROWSER         = YES
```

9. File Patterns: Fine-tune the file patterns if needed.

```makefile
FILE_PATTERNS          = *.c *.cpp *.java *.py
```

10. Exclude Patterns: Exclude directories or files from the documentation.

```javascript
EXCLUDE_PATTERNS       = */test/*
```

## Running Doxygen

After customizing the Doxyfile, generate the documentation by running:

```bash
doxygen Doxyfile
```

The generated documentation can be found in the directory specified by OUTPUT_DIRECTORY.
