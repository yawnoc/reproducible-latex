# reproducible-latex

An attempt at reproducible builds in LaTeX.


## Compile

Run the bash script `./compile`.

This generates the following PDFs and computes their SHA-256 sums:
- `empty.pdf` (an empty A4 page)
- `nonempty.pdf` (a page-numbered but otherwise empty A4 page)
- `quick.pdf` (the quick brown fox jumps over the lazy dog)


## Resulting sha256sum incipits

`empty.pdf` appears to be reproducible.

`nonempty.pdf` appears to depend on the TeX distribution.

| `empty.pdf` | `nonempty.pdf` | `quick.pdf` | OS | Hardware | TeX distro | pdfTeX | kpathsea |
| - | - | - | - | - | - | - | - |
| 4a8a412 | 8addf1c | 0189e0b | Arch 5 | x86_64 | texlive-core 2020.57066-2 | 1.40.21 | 6.3.2 |
| 4a8a412 | 8c2080f | b7f7702 | Debian 10 | aarch64 | texlive-full 2018.20190227-2 | 1.40.19 | 6.3.1/dev |
| 4a8a412 | 8c2080f | | Debian 10 | x86_64 | texlive-full 2018.20190227-2 | 1.40.19 | 6.3.1/dev |
| 4a8a412 | fa2979b | 7917bca | Termux 0.112 | armv7l | texlive-full 20200406-4 | 1.40.21 | 6.3.2 |
| 4a8a412 | fa2979b | 7917bca | Windows 10 | x86_64 | TeX Live 2020/W32TeX | 1.40.21 | 6.3.2 |
