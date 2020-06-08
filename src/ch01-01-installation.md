## Instalasi

Langkah pertama adalah menginstall Rust. kita akan download Rust melalui `rustup`,
suatu alat lini perintah untuk mengatur versi Rust dan peralatan yang terasosiasikan.
Kamu akan membutuhkan koneksi internet untuk download.

> Catatan: Jika kamu memilih tidak menggunakan `rustup` untuk suatu alasan, silahkan
> melihat [halaman instalasi Rust](https://www.rust-lang.org/tools/install) untuk opsi lainnya

Langkah berikut ini adalah untuk menginstalasi versi stabil paling baru
dari kompiler Rust. Kestabilan Rust membuat jaminan bahwa seluruh contoh kode
yang dapat dikompilasi dibuku akan tetap dapat terkompilasi dengan versi Rust
yang lebih baru. Hasil output mungkin akan berbeda karena perbedaan versi, karena
Rust biasanya melakukan perbaikan pesan error dan peringatan/warning. Dengan kata lain,
versi yang baru, ataupun versi stabil dari Rust yang kamu install menggunakan
langkah ini harusnya berhasil bekerja seperti yang sesuai ekspetasi konten buku ini.

> ### Notasi Lini Perintah
> 
> Dalam bab ini dan sepanjang buku, kami akan memperlihatkan perintah yang digunakan
> dalam terminal. Lini yang kamu harus masukan akan dimulai dengan `$`. Kamu tidak
> perlu menuliskan karakter `$`; ini hanya mengindikasikan awalan dari setiap perintah.
> Lini yang tidak dimulai dengan `$` biasanya menampilkan output dari perintah sebelumnya.
> Untuk menambahkan, contoh spesifik seperti PowerShell akan menggunakan `>` daripada `$`.



### Installing `rustup` on Linux or macOS

If you’re using Linux or macOS, open a terminal and enter the following command:

```console
$ curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh
```

The command downloads a script and starts the installation of the `rustup`
tool, which installs the latest stable version of Rust. You might be prompted
for your password. If the install is successful, the following line will appear:

```text
Rust is installed now. Great!
```

Additionally, you’ll need a linker of some kind. It’s likely one is already
installed, but when you try to compile a Rust program and get errors indicating
that a linker could not execute, that means a linker isn’t installed on your
system and you’ll need to install one manually. C compilers usually come with
the correct linker. Check your platform’s documentation for how to install a C
compiler. Also, some common Rust packages depend on C code and will need a C
compiler. Therefore, it might be worth installing one now.

### Installing `rustup` on Windows

On Windows, go to [https://www.rust-lang.org/tools/install][install] and follow
the instructions for installing Rust. At some point in the installation, you’ll
receive a message explaining that you’ll also need the C++ build tools for
Visual Studio 2013 or later. The easiest way to acquire the build tools is to
install [Build Tools for Visual Studio 2019][visualstudio]. The tools are in
the Other Tools and Frameworks section.

[install]: https://www.rust-lang.org/tools/install
[visualstudio]: https://www.visualstudio.com/downloads/#build-tools-for-visual-studio-2019

The rest of this book uses commands that work in both *cmd.exe* and PowerShell.
If there are specific differences, we’ll explain which to use.

### Updating and Uninstalling

After you’ve installed Rust via `rustup`, updating to the latest version is
easy. From your shell, run the following update script:

```console
$ rustup update
```

To uninstall Rust and `rustup`, run the following uninstall script from your
shell:

```console
$ rustup self uninstall
```

### Troubleshooting

To check whether you have Rust installed correctly, open a shell and enter this
line:

```console
$ rustc --version
```

You should see the version number, commit hash, and commit date for the latest
stable version that has been released in the following format:

```text
rustc x.y.z (abcabcabc yyyy-mm-dd)
```

If you see this information, you have installed Rust successfully! If you don’t
see this information and you’re on Windows, check that Rust is in your `%PATH%`
system variable. If that’s all correct and Rust still isn’t working, there are
a number of places you can get help. The easiest is the #beginners channel on
[the official Rust Discord][discord]. There, you can chat with other Rustaceans
(a silly nickname we call ourselves) who can help you out. Other great
resources include [the Users forum][users] and [Stack Overflow][stackoverflow].

[discord]: https://discord.gg/rust-lang
[users]: https://users.rust-lang.org/
[stackoverflow]: https://stackoverflow.com/questions/tagged/rust

### Local Documentation

The installation of Rust also includes a copy of the documentation locally, so
you can read it offline. Run `rustup doc` to open the local documentation in
your browser.

Any time a type or function is provided by the standard library and you’re not
sure what it does or how to use it, use the application programming interface
(API) documentation to find out!
