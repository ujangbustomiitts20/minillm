# llama.cpp - Manual Build Guide

Panduan ini menjelaskan cara menginstal dan menggunakan `llama.cpp` langsung dari GitHub dengan build manual menggunakan `CMake`.

---

##  Keunggulan Instalasi Manual

- Build langsung dari source resmi (paling fleksibel dan up-to-date)
- Mendapatkan semua binary CLI (`main`, `quantize`, `llama-server`, dll)
- Bisa mengatur fitur build seperti dukungan CUDA, Metal, atau HuggingFace
- Cocok untuk modifikasi kode sumber dan eksperimen lanjutan

---

## ⚙️ Build Options

| Fitur                         | Flag Build               | Default Value     | Keterangan                                                                    |
|------------------------------|--------------------------|-------------------|--------------------------------------------------------------------------------|
| Build Mode                   | `CMAKE_BUILD_TYPE`       | `Release`         | Build dalam mode optimal, bukan debug                                         |
| HuggingFace Support (libcurl)| `LLAMA_CURL`             | `ON`              | Aktif jika `libcurl` tersedia, bisa dimatikan                                |
| CLI Tools                    | `LLAMA_BUILD_TOOLS`      | `ON`              | Build tools seperti `main`, `quantize`, dll                                   |
| Contoh Program               | `LLAMA_BUILD_EXAMPLES`   | `ON`              | Build contoh kode: `chat`, `embedding`, dll                                   |
| HTTP API Server              | `LLAMA_BUILD_SERVER`     | `ON` (standalone) | Build `llama-server` untuk REST API                                           |
| GPU NVIDIA (CUDA)           | `GGML_CUDA`              | `OFF`             | Aktifkan dengan `-DGGML_CUDA=ON`                                              |
| Mac GPU M1/M2 (Metal)        | `GGML_METAL`             | `OFF`             | Aktifkan dengan `-DGGML_METAL=ON`                                             |

---


