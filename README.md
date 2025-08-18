# 🚀 Tutorial Dasar Menggunakan Podman

## 🔹 Apa itu Podman?

Podman (**Pod Manager**) adalah _container engine_ mirip **Docker** tetapi:

- Tidak membutuhkan **daemon** (lebih ringan).
- Bisa berjalan tanpa root (`rootless container`).
- Mendukung kompatibilitas dengan **Docker CLI** (`alias docker=podman`).

---

## 🔹 Instalasi Podman

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
