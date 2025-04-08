# Panduan Penulisan Tesis/Skripsi/Disertasi dengan LaTeX

![LaTeX Logo](https://upload.wikimedia.org/wikipedia/commons/9/92/LaTeX_logo.svg)

Repository ini berisi template dan panduan sederhana untuk penulisan karya ilmiah (tesis, skripsi, atau disertasi) menggunakan LaTeX.

## 📋 Daftar Isi
- [Instalasi LaTeX](#-instalasi-latex)
  - [Windows](#windows)
  - [macOS](#macos)
  - [Linux](#linux)
  - [Online (Overleaf)](#online-overleaf)
- [Struktur Dokumen](#-struktur-dokumen)
- [Kompilasi Dokumen](#-kompilasi-dokumen)
- [Referensi dan Bibliografi](#-referensi-dan-bibliografi)
- [Tips dan Trik](#-tips-dan-trik)
- [Kontribusi](#-kontribusi)

---

## 💻 Instalasi LaTeX

### Windows
1. **MikTeX** (Recommended)
   - Download installer dari [miktex.org](https://miktex.org/download)
   - Pilih versi `64-bit` atau `32-bit` sesuai sistem
   - Ikuti wizard instalasi, pilih opsi `Install missing packages on-the-fly`

2. **TeX Live** (Full distribution)
   - Download dari [tug.org/texlive](https://www.tug.org/texlive/)
   - Jalankan `install-tl-windows.bat`

3. **Editor**:
   - [TeXstudio](https://www.texstudio.org/) (Recommended)
   - [VS Code](https://code.visualstudio.com/) dengan ekstensi LaTeX Workshop

### macOS
1. **MacTeX** (Full distribution)
   - Download dari [tug.org/mactex](https://www.tug.org/mactex/)
   - File `.pkg` > 4GB (termasuk editor TeXShop)

2. **Alternatif**:
   - Via Homebrew
   - `brew install --cask mactex`

3. **Editor**:
   - TeXShop (Bawaan MacTeX)
   - VS Code dengan LaTeX Workshop

### Linux

1. **TeX Live** (Full distribution)
   
    Debian/Ubuntu
   
    `sudo apt install texlive-full`

    Fedora
   
    `sudo dnf install texlive-scheme-full`

    Arch Linux
   
    `sudo pacman -S texlive-most texlive-lang`

3. **Editor**:
   - TeXmaker
   - VS Code dengan LaTeX Workshop

### Online (Overleaf)

Buka overleaf.com

Buat akun gratis (atau login via institusi)

---

## 🛠 Kompilasi Dokumen

**Cara dasar:**

```bash
pdflatex main.tex
bibtex main.aux
pdflatex main.tex
pdflatex main.tex
```

**Menggunakan Makefile:**

```bash
make all
```

**Overleaf:**

- Klik tombol **Recompile** otomatis

---

## 📚 Referensi dan Bibliografi

**Contoh entri dalam `bibliography.bib`:**

```bibtex
@book{knuth1984texbook,
  title={The TeXbook},
  author={Knuth, Donald E.},
  year={1984},
  publisher={Addison-Wesley}
}
```

**Sitasi dalam teks:**

```latex
Menurut \cite{knuth1984texbook}, LaTeX adalah...
```

---

## 💡 Tips dan Trik

- Gunakan **Version Control (Git)** untuk men-track perubahan
- Bagi dokumen menjadi beberapa file (per bab)
- Gunakan **Label** untuk referensi silang:

```latex
\label{chap:pendahuluan}
```

- Kompres gambar sebelum dimasukkan:

```bash
convert image.png -quality 80 image-compressed.jpg
```

---

## 🤝 Kontribusi

- Fork repository ini
- Buat branch baru:

```bash
git checkout -b fitur-baru
```

- Commit perubahan:

```bash
git commit -am 'Tambahkan fitur'
```

- Push ke branch:

```bash
git push origin fitur-baru
```

- Buat **Pull Request** ke repository utama

