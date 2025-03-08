<div align="center">
  <h1>LLVM Builds for the Metal Programming Language</h1>
  
  <p>
    <a href="https://github.com/metallang/llvm-builds/actions?query=workflow%3A%22Build%22">
      <img src="https://github.com/metallang/llvm-builds/workflows/Build/badge.svg" alt="Build Status">
    </a>
    <a href="https://github.com/metallang/llvm-builds/blob/master/LICENSE">
      <img src="https://img.shields.io/github/license/metallang/llvm-builds.svg" alt="License">
    </a>
  </p>

</div>

<hr/>

> Go along your path, this is a dangerous place.

This repository contains a small `build.sh` (or `build.ps1` for Windows 
PowerShell) script that builds LLVM. The version of LLVM is defined in the CI script.
The build is run by [Github
Actions](https://github.com/metallang/llvm-builds/actions) on 4
platforms: Linux (Ubuntu, amd64 and aarch64), Darwin (macOS), and Windows.
Builds are attached to [Github releases as
assets](https://github.com/metallang/llvm-builds/releases).

## Prebuilds

<table>
  <thead>
    <tr>
      <th>LLVM version</th>
      <th>Architecture</th>
      <th>Platform</th>
      <th>Package</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="6">20</td>
      <td rowspan="3">amd64</td>
      <td>Darwin</td>
      <td><a href="https://github.com/metallang/llvm-builds/releases/download/20.x/llvm-darwin-amd64.tar.xz">download</a></td>
    </tr>
    <tr>
      <td>Linux</td>
      <td><a href="https://github.com/metallang/llvm-builds/releases/download/20.x/llvm-linux-amd64.tar.xz">download</a></td>
    </tr>
    <tr>
      <td>Windows</td>
      <td><a href="https://github.com/metallang/llvm-builds/releases/download/20.x/llvm-windows-amd64.tar.xz">download</a></td>
    </tr>
    <tr>
      <td rowspan="2">aarch64</td>
      <td>Linux</td>
      <td><a href="https://github.com/metallang/llvm-builds/releases/download/20.x/llvm-linux-aarch64.tar.xz">download</a></td>
    </tr>
    <tr>
      <td>Darwin</td>
      <td><a href="https://github.com/metallang/llvm-builds/releases/download/20.x/llvm-darwin-aarch64.tar.xz">download</a></td>
    </tr>
      </tr>
      <td>riscv64</td>
      <td>Linux</td>
      <td><a href="https://github.com/metallang/llvm-builds/releases/download/20.x/llvm-linux-riscv64.tar.xz">download</a></td>
      <tr>
    <tr>
      <td rowspan="6">19</td>
      <td rowspan="3">amd64</td>
      <td>Darwin</td>
      <td><a href="https://github.com/metallang/llvm-builds/releases/download/19.x/llvm-darwin-amd64.tar.xz">download</a></td>
    </tr>
    <tr>
      <td>Linux</td>
      <td><a href="https://github.com/metallang/llvm-builds/releases/download/19.x/llvm-linux-amd64.tar.xz">download</a></td>
    </tr>
    <tr>
      <td>Windows</td>
      <td><a href="https://github.com/metallang/llvm-builds/releases/download/19.x/llvm-windows-amd64.tar.xz">download</a></td>
    </tr>
    <tr>
      <td rowspan="2">aarch64</td>
      <td>Linux</td>
      <td><a href="https://github.com/metallang/llvm-builds/releases/download/19.x/llvm-linux-aarch64.tar.xz">download</a></td>
    </tr>
    <tr>
      <td>Darwin</td>
      <td><a href="https://github.com/metallang/llvm-builds/releases/download/19.x/llvm-darwin-aarch64.tar.xz">download</a></td>
    </tr>
      </tr>
      <td>riscv64</td>
      <td>Linux</td>
      <td><a href="https://github.com/metallang/llvm-builds/releases/download/19.x/llvm-linux-riscv64.tar.xz">download</a></td>
      <tr>
  </tbody>
</table>

## LLVM configuration

The following configuration is the one used for all actual prebuilds:

| Options | Value |
|-|-|
| `clang` | enabled |
| `docs` | not included |
| `examples` | not included |
| `go_tests` | not included |
| `lld` | enabled |
| `optimized_tablegen` | enabled |
| `targets_to_build` | `X86` + `AArch64` |
| `terminfo` | disabled |
| `tests` | not included |
| `tools` | included |
| `utils` | not included |
| `zlib` | disabled |

# License

The entire project is under the MIT License. Please read [the `LICENSE` file][license].


[license]: https://github.com/metallang/llvm-builds/blob/master/LICENSE
