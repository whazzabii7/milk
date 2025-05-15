# MILK - Multi-Language Intelligent Linking & Compilation

**MILK** is an experimental build support system written in [**Lua**](https://luajit.org) with **C** as [ffi](https://luajit.org/ext_ffi.html),
using [**LuaJIT**](https://luajit.org) as its scripting engine to define flexible, powerful build rules. The Program is wrapped and embedded in a 
[**Rustshell**](https://www.rust-lang.org/) to compile the program into an executable. **MILK** is therefore a perfekt example of what is possible to build with **MILK**

> **Goal:** To create a fast, modular, cross-platform, multi-language build system with smart scripting capabilities.

---

## 🧠 Core Concept

At its heart, MILK separates **logic** from **tooling**. Instead of rigid configuration files like `Makefile` or `CMakeLists.txt`, MILK leverages **Lua scripts** to define build rules, steps, and behavior. Lua scripts allow for powerful custom build logic, dependency handling, and dynamic decisions.

The system itself is written entirely in **Zig** for maximum performance, control, and low overhead.

---

## 📦 Current Status

> 🚧 This project is in early development. Everything is still being implemented from scratch.

---

## ✅ Planned Features

- 🔄 **Multi-language build orchestration** (C, Zig, Lua, Rust, etc.)
- 🌳 **Project hierarchy as a Lua table**, auto-generated from folder/file structure
- 📤 Export hierarchy to **JSON** for tooling integration
- 🛠️ **Custom build/link rules** using Lua scripting
- 🧱 **Dynamic compilation & linking** decisions
- 📚 **Dependency management**: semi-automated through a declaration file
- ⚡ Ultra-fast build logic powered by **Zig** and **LuaJIT**
- 🔌 Easily extendable system for future tools or workflows

---

## 🚀 How It Works

1. **Write Lua build scripts** describing your project structure and logic.
2. MILK will parse these scripts and build the required project structure.
3. It uses the Lua API to generate a build graph and resolve compilation and linking steps.
4. Output and intermediate states can be logged or exported as JSON.
5. All rules are programmable: you can define exactly how each step behaves.

---

## 🔧 Requirements

- Nothing! (planned for now) 
  MILK **compiles LuaJIT directly into the binary**, so you don’t need any external Lua installation.

---

## 📌 To-Do (Development Roadmap)

- [ ] Initialize CLI interface
- [ ] Embed LuaJIT VM and API wrapper
- [ ] File parser & project hierarchy tree
- [ ] JSON export of project state
- [ ] Build rule evaluation engine
- [ ] Multi-language toolchain integration
- [ ] Dependency file format & loader
- [ ] First working demo build script
- [ ] Unit tests & project examples

---

## 📂 Planned Lua Syntax

It is planned to use mainly luas tables for configuration, but let the user use functions tho generate those tables.
Also the lua build files will get their own file extension.

