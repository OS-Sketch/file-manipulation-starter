# File Manipulation

[![build](../../actions/workflows/build.yml/badge.svg)](../../actions/)
[![Language: Python](https://img.shields.io/badge/Language-Python-blue.svg)](https://www.python.org/)
[![Language: Go](https://img.shields.io/badge/Language-Go-blue.svg)](https://go.dev/)
[![Commits: Conventional](https://img.shields.io/badge/Commits-Conventional-blue.svg)](https://www.conventionalcommits.org/en/v1.0.0/)
[![Discord](https://img.shields.io/discord/1013818801281839184?logo=discord)](https://discord.gg/9VfCdqffu6)

## Introduction

This project introduces the steps that you must take to implement, build, and
run a program in Go programming languages that manipulates files on the file
system. You will learn how to use Makefiles to automatically build programs and
copy their binaries to a suitable directory. The programs that you implement
will demonstrate the use of conditional logic, the extraction and processing of
command-line arguments, and the steps needed to read from and write to files.

## Seeking Assistance

Even though the course instructor will have covered all of the concepts central
to this project before you start to work on it, please note that not every
detail needed to successfully complete the assignment will have been covered
during prior classroom sessions. This is by design as an important skill that
you must practice as you explore the depth and breadth in the field of operating
systems. If you have questions about this project, please schedule a meeting
with the course instructor during office hours.

## Project Overview

After cloning this repository to your computer, please take the following
steps:

### Program Setup

Some of the source code for this project inspired by the content of the [OSTEP
book](http://pages.cs.wisc.edu/~remzi/OSTEP/intro.pdf). Please make sure that
you read chapters 2, 4, and 5 and to the slides on the course web site for more
information about these programs!

- Make sure that you have installed the following programs on your laptop:
  - Gcc toolchain, especially the `make` command for running Makefiles.
  - Go programming language
  - C programming language
- Use the `cd` command to change into the directory for this repository.
- Review the `Makefile` in the `project/golang/` directory to see the targets
  for the version of this project implemented in the Go programming language.
- The provided `Makefile` will work on the Linux and MacOS operating systems
  and, additionally, on GitHub Actions and inside of the OS-Sketch Docker
  container. You may need to revise portions of these `Makefile`s so that they
  work correctly on the Windows operating system.
- To build the Go program you need to run the following commands from the
  respective `golang/` directory: `make copy` to build the `bin/copy` binary.
- If you are still learning more about the Go programming language you can refer
  to the tutorials that are available on the [Go](https://go.dev/) and [Go by
  Example](https://gobyexample.com/) web sites.
- Remember, it is not necessary for you to take a "build" step for the Python
  program since the `python` interpreter will run the program without a
  compilation step.

### Program Implementation

When you run the Go implementation of the `copy` program with the command
`./project/golang/bin/copy files source.txt files destination.txt` it will
produce the following output:

```text
Source Path: files/source.txt

Destination Path: files/destination.txt

Completed the copy from the source to the destination.
```

When you run the Python implementation of the `copy` program with the command
`python project/pylang/copy.py files source.txt files destination.txt` it will
produce the following output, which is the same as the output of the `copy`
program implemented in Go.

```text
Source Path: files/source.txt

Destination Path: files/destination.txt

Completed the copy from the source to the destination.
```

Please note that these programs will work with any type of text files that
already exist in the source and destination directories. As such, you are
encouraged to try the program with a wide variety of input text files of
different sizes. With that said, you can initially ensure that your program is
running correctly by using the `source.txt` and `destination.txt` files provided
in the `files` directory of your GitHub repository. After running the version of
the program implemented in either Go or Python, you check the `destination.txt`
file to confirm that it now contains the contents of the `source.txt` file and
that the contents of the `source.txt` file remain unchanged. Finally, it is
worth noting that both of the programs should produce an error message when they
are run with a filename, such as `source1.txt`, that does not exist in a
specified directory, as in the following output example:

```text
Source Path: files/source1.txt

Destination Path: files/destination.txt

Cannot copy due to incorrect source or destination path
```

As you implement both the Go and Python versions of the `copy` program, you
should create them in such as a way so as to ensure that they operate correctly
while only using the packages that are a part of the languages main libraries.
This means that your program should not use an external dependencies from
either other GitHub repositories or packages published in a package index like
PyPI. With that said, you are welcome to implement your programs while using
any of the packages that ship with the programming language.

### Project Reflection

As you work on this project, you should regularly take time to reflect on the
steps that you are taking and why you are taking them. Each time you run a
program you should think about the inputs, outputs, and behavior of that
program, jotting down notes to help you remember these insights. When you are
writing Python and Go programs, please reserve time to reflect on the features
of the language that you are learning and how the languages are similar to and
different from each other. Finally, as you complete this project, make sure that
you reflect on your own strengths and weaknesses and how you can improve in
advance of the next project.

### Automated Assessment

Please review the following notes about the way in which your project will be
automatically assess in GitHub Actions:

- If you have already installed the
  [GatorGrade](https://github.com/GatorEducator/gatorgrade) program that runs
  the automated grading checks provided by
  [GatorGrader](https://github.com/GatorEducator/gatorgrader) you can, from the
  repository's base directory, run the automated grading checks by typing
  `gatorgrade --config config/gatorgrade.yml`.
- You may also review the output from running GatorGrader in GitHub Actions.
- Don't forget to provide all of the required responses to the technical writing
  prompts in the `writing/reflection.md` file.
- Please make sure that you completely delete the `TODO` markers and their
  labels from all of the provided source code. This means that instead of only
  deleting the `TODO` marker from the code you should delete the `TODO`
  marker and the entire prompt and then add your own comments to demonstrate
  that you understand all of the source code in this project.
- Please make sure that you also completely delete the `TODO` markers and their
  labels from every line of the `writing/reflection.md` file. This means that
  you should not simply delete the `TODO` marker but instead delete the entire
  prompt so that your reflection is a document that contains polished technical
  writing that is suitable for publication on your professional web site.
