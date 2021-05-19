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


## Generate pairwise diffs

Run the bash script `./makediffs`.


## Resulting sha256sum incipits

Only `empty.pdf` appears to be reproducible.

The others (`nonempty.pdf` and `quick.pdf`) depend on the TeX distribution.
For TeX Live, there are 3 cliques in terms of reproducibility so far:

<table>
  <tr>
    <th colspan="8">2019 Debian</th>
  </tr>
  <tr>
    <th><code>empty.pdf</code></th>
    <th><code>nonempty.pdf</code></th>
    <th><code>quick.pdf</code></th>
    <th>OS</th>
    <th>Hardware</th>
    <th>TeX distro</th>
    <th>pdfTeX</th>
    <th>kpathsea</th>
  </tr>
  <tr>
    <td>4a8a412</td>
    <td>8c2080f</td>
    <td>b7f7702</td>
    <td>Debian 10</td>
    <td>aarch64</td>
    <td>texlive-full 2018.20190227-2</td>
    <td>1.40.19</td>
    <td>6.3.1/dev</td>
  </tr>
  <tr>
    <td>4a8a412</td>
    <td>8c2080f</td>
    <td>b7f7702</td>
    <td>Debian 10</td>
    <td>x86_64</td>
    <td>texlive-full 2018.20190227-2</td>
    <td>1.40.19</td>
    <td>6.3.1/dev</td>
  </tr>
  <tr>
    <th colspan="8">2020 Linux</th>
  </tr>
  <tr>
    <th><code>empty.pdf</code></th>
    <th><code>nonempty.pdf</code></th>
    <th><code>quick.pdf</code></th>
    <th>OS</th>
    <th>Hardware</th>
    <th>TeX distro</th>
    <th>pdfTeX</th>
    <th>kpathsea</th>
  </tr>
  <tr>
    <td>4a8a412</td>
    <td>8addf1c</td>
    <td>0189e0b</td>
    <td>Arch 5</td>
    <td>x86_64</td>
    <td>texlive-core 2020.57066-2 + texlive-latexextra 2020.57067-1</td>
    <td>1.40.21</td>
    <td>6.3.2</td>
  </tr>
  <tr>
    <td>4a8a412</td>
    <td>8addf1c</td>
    <td>0189e0b</td>
    <td>Debian 11</td>
    <td>x86_64</td>
    <td>texlive-full 2020.20210202-3</td>
    <td>1.40.21</td>
    <td>6.3.2</td>
  </tr>
  <tr>
    <th colspan="8">2020 Not Linux</th>
  </tr>
  <tr>
    <th><code>empty.pdf</code></th>
    <th><code>nonempty.pdf</code></th>
    <th><code>quick.pdf</code></th>
    <th>OS</th>
    <th>Hardware</th>
    <th>TeX distro</th>
    <th>pdfTeX</th>
    <th>kpathsea</th>
  </tr>
  <tr>
    <td>4a8a412</td>
    <td>fa2979b</td>
    <td>7917bca</td>
    <td>macOS 10.15</td>
    <td>x86_64</td>
    <td>TeX Live 2020</td>
    <td>1.40.21</td>
    <td>6.3.2</td>
  </tr>
  <tr>
    <td>4a8a412</td>
    <td>fa2979b</td>
    <td>7917bca</td>
    <td>Termux 0.112</td>
    <td>armv7l</td>
    <td>texlive-full 20200406-4</td>
    <td>1.40.21</td>
    <td>6.3.2</td>
  </tr>
  <tr>
    <td>4a8a412</td>
    <td>fa2979b</td>
    <td>7917bca</td>
    <td>Windows 10</td>
    <td>x86_64</td>
    <td>TeX Live 2020/W32TeX</td>
    <td>1.40.21</td>
    <td>6.3.2</td>
  </tr>
</table>
