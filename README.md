# **QR Project - Scan Gogh**

## **Team**
- **Gabreanu Răzvan-George** - Group 134, Series 13
- **Săpunaru Maia** - Group 134, Series 13
- **Mocanu Ruxandra-Ioana** - Group 134, Series 13

---

## **Description**
This project implements a system for generating and reading QR codes. The main menu offers two core functionalities:
1. **Generating a QR code**
2. **Reading a QR code**

---

## **Generating a QR Code**
The QR code generation process follows these steps:

1. Take the input character string from the user.
2. Convert the string into a binary sequence.
3. Apply the initial and final sequences to the binary string.
4. Split the binary string into blocks based on the number of characters.
5. Add error correction codes (**ECC - Error Correction Code**).
6. Rearrange bits according to the QR code structure.
7. Create a QR matrix (using `0` and `1`, corresponding to white and black colors).
8. Apply the necessary QR format, adding reserved corners and lines.
9. Insert the bit sequence into the QR matrix.
10. Apply the 8 possible masks and select the optimal one based on optimization criteria.
11. Apply the final formatting.
12. Convert the QR matrix into a **PNG** file.

---

## **Reading a QR Code**
The QR code reading process includes the following steps:

1. Resize the image to ensure each pixel can be accessed correctly.
2. Convert the image into a matrix containing only `0` and `1` values (**black/white**).
3. Identify the applied mask using decision bits.
4. Determine the QR code version for correct decoding.
5. Remove the applied mask.
6. Extract bits in a **zig-zag** order to retrieve data.
7. Convert the bit sequence into a final decoded **string**.

---

## **References**

### **General QR Code Guidelines:**
- [Creating a QR Code - Nayuki](https://www.nayuki.io/page/creating-a-qr-code-step-by-step)

### **Generating PNG Files from a Binary Matrix:**
- [Pillow - Convert to PNG](https://stackoverflow.com/questions/78913551/python-using-pillow-to-convert-any-format-to-png-any-way-to-speed-the-process)
- [GeeksforGeeks - Convert Numpy to Image](https://www.geeksforgeeks.org/convert-a-numpy-array-to-an-image/)

### **Generating Error Correction Codes (ECC):**
- [Reed-Solomon Codec](https://pypi.org/project/reedsolo/#basic-usage-with-high-level-rscodec-class)

### **QR Code Format Information:**
- [QR Code Format and Version](https://www.thonky.com/qr-code-tutorial/format-version-information)

### **Reading Image Pixels:**
- [StackOverflow - RGB pixel values](https://stackoverflow.com/questions/138250/how-to-read-the-rgb-value-of-a-given-pixel-in-python)
- [YouTube - Reading Image Pixels](https://www.youtube.com/watch?v=6Hk5KyiEktI)

### **QR Code Structure and Data Formatting:**
- [YouTube - Timing & Alignment Patterns](https://www.youtube.com/watch?v=pamazHwk0hg)
- [GeeksforGeeks - Convert Binary to String](https://www.geeksforgeeks.org/convert-binary-to-string-using-python/)

### **Finding the Optimal Mask for a QR Code:**
- [Reddit - How to Read QR Codes](https://www.reddit.com/r/LearnUselessTalents/comments/esidvc/the_simplest_guide_to_read_qr_codes/)
- [QR Mask Analysis Example](https://imgur.com/a/FvtpZ2o)

---

## **Video Explanation**
[https://www.youtube.com/watch?v=NIO0ZfSSZ34](https://www.youtube.com/watch?v=NIO0ZfSSZ34)

---
