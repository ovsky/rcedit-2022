# ![icon](https://i.postimg.cc/XvGmRwG8/icon-rcedit.png) RCEdit'22 - Electron Source Editor

**A powerful command-line tool for editing Windows executable resources, modernized for 2022+**

> ✨ Reimagined and rebuilt with **Visual Studio 2022** and **.NET 7.0** for today's standards

---

## 🎯 What is RCEdit'22?

RCEdit'22 is a full modernization of the legendary `rcedit` tool, bringing this Windows resource editing powerhouse into the modern era. Whether you're developing Electron applications or working with Windows executables, RCEdit'22 provides a streamlined CLI for managing:

- **🎨 Icons & Resources** - Update application icons and embedded resources
- **📌 Version Information** - Control file and product version strings  
- **🔐 Manifest Settings** - Manage execution levels and application manifests
- **⚡ Everything at Once** - Batch modify multiple properties in a single command

### Why "2022"?

The original `rcedit` served the community well, but it was built on legacy standards. This modernized fork elevates the entire project to contemporary development practices:

✅ Built with **Visual Studio 2022**  
✅ Powered by **.NET 7.0**  
✅ Full CLI compatibility maintained  
✅ Ready for modern development workflows  

---

## 🚀 Quick Start

### Building the Project

```bash
# Clone the repository
git clone https://github.com/ovsky/rcedit-2022.git
cd rcedit-2022

# Open and build with Visual Studio 2022
# OR use modern .NET CLI
dotnet build rcedit.sln
```

### Common Usage

**Set application icon:**
```bash
rcedit "app.exe" --set-icon "icon.ico"
```

**Update version information:**
```bash
rcedit "app.exe" --set-file-version "1.0.0" --set-product-version "1.0.0"
```

**Modify version properties:**
```bash
rcedit "app.exe" --set-version-string "ProductName" "My Application"
```

**Get version information:**
```bash
rcedit "app.exe" --get-version-string "FileVersion"
```

**Set execution level:**
```bash
rcedit "app.exe" --set-requested-execution-level "requireAdministrator"
```

**Apply manifest:**
```bash
rcedit "app.exe" --application-manifest "./manifest.xml"
```

**Combine multiple operations:**
```bash
rcedit "app.exe" --set-icon "icon.ico" --set-file-version "2.0.0" --set-requested-execution-level "asInvoker"
```

---

## 📚 Documentation

### Help Command
```bash
rcedit -h
```

### Version String Properties

Any MSDN [Version String Resource](https://msdn.microsoft.com/en-us/library/windows/desktop/aa381058(v=vs.85).aspx) property is supported:

Common properties include: `Comments`, `CompanyName`, `FileDescription`, `FileVersion`, `InternalName`, `LegalCopyright`, `OriginalFilename`, `ProductName`, `ProductVersion`

### Execution Levels

Set the [requested execution level](https://msdn.microsoft.com/en-us/library/6ad1fshk.aspx#Anchor_9) in the manifest:

- `asInvoker` - Run with current user privileges
- `highestAvailable` - Request highest available privileges  
- `requireAdministrator` - Require administrator rights

---

## 📦 Downloads

Prebuilt binaries are available in the **AppVeyor CI artifacts**. Check the [build status](https://ci.appveyor.com/project/zcbenz/rcedit/branch/master) for the latest releases.

---

## 📋 Regenerating Solution Files

If you've modified the GYP files, regenerate the solution:

```bash
# 1. Ensure GYP is installed (clone from Chromium if needed)
# https://chromium.googlesource.com/external/gyp

# 2. Regenerate solution files
gyp rcedit.gyp --depth .
```

---

## 📖 Technology Stack

![C++](https://img.shields.io/badge/C++-96.4%25-blue?style=flat-square&logo=cplusplus)
![Python](https://img.shields.io/badge/Python-1.9%25-yellow?style=flat-square&logo=python)
![C](https://img.shields.io/badge/C-1.7%25-gray?style=flat-square&logo=c)

Built with modern tooling for **Visual Studio 2022** and **.NET 7.0+**

---

## 📜 License & Credits

Original `rcedit` repository: https://github.com/electron/rcedit

This modernized fork maintains compatibility while bringing the project to 2022+ standards.

---

**Made with ❤️ for modern Windows development**
