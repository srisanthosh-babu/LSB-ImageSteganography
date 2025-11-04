````markdown
# 🧩 LSB Image Steganography in C

## 📘 Overview
This project implements **Image Steganography using the Least Significant Bit (LSB) technique** in the C programming language.  
It allows users to **hide secret text data inside BMP images** and later **decode it back** accurately — without any visible changes to the image.

Through efficient bitwise operations and file handling, the project demonstrates how information can be securely embedded within digital media.

---

## ⚙️ Features
- 🔒 Hide secret text files inside BMP images using LSB substitution.
- 🧠 Retrieve the hidden message accurately through decoding.
- 📂 Modular structure for clarity:
  - `encode.c / encode.h` – Handles embedding of secret data.
  - `decode.c / decode.h` – Extracts and reconstructs hidden data.
  - `types.h` – Contains user-defined types, enums, and status codes.
  - `common.h` – Defines the `MAGIC_STRING` identifier.
  - `main.c` – Command-line driver for encoding and decoding.
- 🧮 Demonstrates concepts of bitwise manipulation, file I/O, and data security.

---

## 🚀 Usage

### **Encoding**
Hide a secret text file inside a BMP image:
```bash
./a.out -e source.bmp secret.txt stego.bmp
````

If no output filename is given, a default `default.bmp` is created.

### **Decoding**

Extract the hidden message from an encoded BMP:

```bash
./a.out -d stego.bmp output.txt
```

If no output filename is given, the result is saved as `output.txt`.

---

## 🧱 Project Structure

```
├── encode.c
├── encode.h
├── decode.c
├── decode.h
├── types.h
├── common.h
├── main.c
└── README.md
```

---

## 🔍 How It Works

1. **Encoding Phase**

   * Copies the BMP header.
   * Embeds a magic string for verification.
   * Hides file extension, file size, and actual secret data in the pixel LSBs.
2. **Decoding Phase**

   * Verifies magic string.
   * Extracts the extension, size, and data bits.
   * Reconstructs the hidden file accurately.

---

## 🧠 Concepts Demonstrated

* Bitwise operations and masking
* File handling and binary I/O
* Information hiding and data security fundamentals
* Modular C programming and clean design

---

## 🧑‍💻 Author

**Srisanthosh**
*Electronics Engineer | Embedded Systems Enthusiast*
📧 Feel free to connect or share feedback!

---

## 🪶 License

This project is released under the **MIT License** – free to use, modify, and distribute with proper attribution.

```

---

```
