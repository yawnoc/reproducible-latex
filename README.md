# reproducible-latex

An attempt at reproducible builds in LaTeX.


## Compile

Run the bash script `./compile`.

This generates the following PDFs and computes their SHA-256 sums:
- `empty.pdf` (an empty A4 page)
- `nonempty.pdf` (a page-numbered but otherwise empty A4 page)


## Results for `empty.pdf`

| OS | Hardware | TeX distro | pdfTeX | kpathsea | sha256sum incipit |
| - | - | - | - | - | - |
| Android Termux 0.112 | armv7l | texlive-full 20200406-4 | 1.40.21 | 6.3.2 | 4a8a412 |
| Linux Debian 10 | aarch64 | texlive-full 2018.20190227-2 | 1.40.19 | 6.3.1/dev | 4a8a412 |


## Results for `nonempty.pdf`

| OS | Hardware | TeX distro | pdfTeX | kpathsea | sha256sum incipit |
| - | - | - | - | - | - |
| Linux Debian 10 | aarch64 | texlive-full 2018.20190227-2 | 1.40.19 | 6.3.1/dev | 8c2080f |
| Android Termux 0.112 | armv7l | texlive-full 20200406-4 | 1.40.21 | 6.3.2 | fa2979b |
