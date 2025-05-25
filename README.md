# 🧠 Augmented Reality using Planar Homographies

This is a **computer vision project** focused on implementing an **Augmented Reality (AR)** system from scratch using **planar homographies**. The project showcases how traditional computer vision techniques can be used to augment real-world video with synthetic content, without relying on modern AR toolkits.

---

## 🎯 Objective

The main objective is to overlay each frame of a source video (`ar_source.mov`) onto a **book** visible in a target video (`book.mov`) — creating an illusion that the book is displaying dynamic content.

---

## 📦 Project Breakdown

### 🔹 Part 1: Point Correspondence and Homography Estimation
- Detect and manually select or automatically extract matching points between two planar views.
- Estimate the **homography matrix (H)** using Direct Linear Transformation (DLT) and RANSAC for robustness.

### 🔹 Part 2: Image Warping
- Warp the source image/video frames using the estimated homography.
- Ensure geometric alignment of the warped frame to the target surface (the book).

### 🔹 Part 3: Augmented Reality Application
- Iterate over frames in `book.mov`.
- For each frame:
  - Compute homography
  - Warp the `ar_source.mov` frame
  - Overlay it onto the book region
- Generate and save the resulting AR video.

---

## 🎥 Demo Input

- 📘 `book.mov` – Video of a book in real-world environment.
- 🔺 `ar_source.mov` – Synthetic video content to be projected on the book.

---

## 💻 Technologies Used

- Python
- OpenCV
- NumPy
- Homography estimation (DLT, RANSAC)
- Video I/O and image processing

---

## 🧪 Key Concepts

- **Planar Homography**: Mapping between two views of the same planar surface.
- **Perspective Warping**: Aligning content to a different viewpoint.
- **Augmented Reality (AR)**: Overlaying computer-generated content onto real-world scenes in a context-aware manner.

---

## 📁 Project Structure
📁 augmented-reality/
┣ 📄 README.md ← Project overview and documentation

┣ 📓 augmented_reality.ipynb ← Homography + AR implementation

┣ 📹 book.mov ← Real-world video with a book

┣ 📹 ar_source.mov ← Synthetic video to be projected on the book
