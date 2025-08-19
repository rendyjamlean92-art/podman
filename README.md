# 🚀 Tutorial Dasar Menggunakan Podman

## 🔹 Apa itu Podman?

Podman (Pod Manager) adalah sebuah container engine open-source yang digunakan untuk membuat, mengelola, dan menjalankan container serta pod. Podman memiliki fungsi yang mirip dengan Docker, namun dengan keunggulan utama yaitu bersifat daemonless (tidak membutuhkan daemon yang berjalan di background) dan mendukung mode rootless, sehingga container dapat dijalankan tanpa hak akses root. Hal ini membuat Podman lebih aman serta fleksibel digunakan di berbagai sistem operasi, termasuk Linux, macOS, dan Windows.

Selain itu, Podman memiliki integrasi konsep pod secara bawaan, mirip dengan Kubernetes, di mana beberapa container dapat berjalan dalam satu lingkungan jaringan yang sama. Perintah Podman juga kompatibel dengan perintah Docker, sehingga pengguna yang terbiasa dengan Docker dapat dengan mudah beralih tanpa banyak penyesuaian. Karena sifatnya yang ringan, aman, dan mendukung arsitektur mirip Kubernetes, Podman banyak digunakan untuk pengembangan, pengujian, hingga implementasi aplikasi berbasis container di lingkungan produksi.

Podman (**Pod Manager**) adalah _container engine_ mirip **Docker** tetapi:

- Tidak membutuhkan **daemon** (lebih ringan).
- Bisa berjalan tanpa root (`rootless container`).
- Mendukung kompatibilitas dengan **Docker CLI** (`alias docker=podman`).

---

## 🔹 Tutorial Dan Instalasi Podman

### Ubuntu / Debian

```bash
sudo apt update
sudo apt -y install podman
```

### macOS (menggunakan Homebrew)

```bash
brew install podman
```

### Windows

1. **Download Podman**

   - Unduh installer Podman dari GitHub:  
     [Podman Windows Installer](https://github.com/containers/podman/releases)
   - Pilih file `.msi` terbaru sesuai arsitektur (x64/ARM64).

2. **Instalasi**

   - Jalankan file `.msi` → ikuti wizard instalasi.
   - Setelah selesai, buka **PowerShell** atau **Command Prompt**.

3. **Inisialisasi Podman Machine**
   Karena Windows tidak bisa jalan langsung seperti Linux, buat VM dulu:
   ```powershell
   podman machine init
   podman machine start
   ```
## 🔹 Cek versi
```
podman --version
```
## 🔹 Menjalankan Container
```
podman run -d -p 8080:80 nginx
```
## 🔹 Melihat Container
```
podman ps
podman ps -a  
```
## 🔹 Menghentikan & Menghapus Container
```
podman stop <container_id>
podman rm <container_id>
```
## 🔹 Build Image dengan Podman
```
podman build -t myapp .
podman run -d -p 5000:5000 myapp

```


