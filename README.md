# reproducible-latex

An attempt at reproducible builds in LaTeX.


## Generate PDFs

Run the bash script `./makepdfs`.

This generates the following PDFs,
copies them into their respective directories,
and computes their SHA-256 sums:
- `empty.pdf` (an empty A4 page)
- `nonempty.pdf` (a page-numbered but otherwise empty A4 page)
- `quick.pdf` (the quick brown fox jumps over the lazy dog)


## Resulting sha256sum incipits

Only `empty.pdf` appears to be reproducible.

The others (`nonempty.pdf` and `quick.pdf`) depend on the TeX distribution.

| `empty.pdf` | `nonempty.pdf` | `quick.pdf` | OS | Hardware | TeX distro | pdfTeX | kpathsea |
| - | - | - | - | - | - | - | - |
| 4a8a412 | 8addf1c | 0189e0b | Arch 5 | x86_64 | texlive-core 2020.57066-2 + texlive-latexextra 2020.57067-1 | 1.40.21 | 6.3.2 |
| 4a8a412 | 8c2080f | b7f7702 | Debian 10 | aarch64 | texlive-full 2018.20190227-2 | 1.40.19 | 6.3.1/dev |
| 4a8a412 | 8c2080f | b7f7702 | Debian 10 | x86_64 | texlive-full 2018.20190227-2 | 1.40.19 | 6.3.1/dev |
| 4a8a412 | fa2979b | 7917bca | Termux 0.112 | armv7l | texlive-full 20200406-4 | 1.40.21 | 6.3.2 |
| 4a8a412 | fa2979b | 7917bca | Windows 10 | x86_64 | TeX Live 2020/W32TeX | 1.40.21 | 6.3.2 |
