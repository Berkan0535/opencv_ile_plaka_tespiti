##README
#TR
# OpenCV ile Basit Plaka Tespiti

Bu proje, Python ve OpenCV kütüphanesi kullanarak bir görüntü üzerindeki araç plakasını tespit etmek için geliştirilmiş basit bir bilgisayarlı görü uygulamasıdır.

## 📝 Proje Açıklaması

Kod, `plaka.jpg` adlı görüntü dosyasını işler ve görüntü işleme tekniklerini kullanarak plaka olabilecek dikdörtgen alanları tespit etmeye çalışır.

Uygulanan adımlar sırasıyla şunlardır:
1.  Görüntü gri tonlamalı olarak okunur.
2.  Gürültüyü azaltmak için **Gaussian Blur** filtresi uygulanır.
3.  **Canny Kenar Tespiti** algoritması ile görüntüdeki kenarlar bulunur.
4.  Kenarlardan yola çıkarak **konturlar (dış hatlar)** tespit edilir.
5.  Bulunan konturlar; en-boy oranı, alan, genişlik ve yükseklik gibi geometrik özelliklerine göre filtrelenir.
6.  Plaka kriterlerine uyan konturların etrafı yeşil bir dikdörtgen ile işaretlenir ve sonuç görüntülenir.

## 🛠️ Kullanılan Teknikler ve Kütüphaneler

* **Python 3**
* **OpenCV** (`opencv-python`): Görüntü işleme fonksiyonları için (Görüntü okuma, GaussianBlur, Canny, findContours, rectangle).
* **NumPy**: OpenCV için temel bir gereksinimdir.

## 🚀 Nasıl Çalıştırılır?

1.  Bu repoyu klonlayın veya dosyaları indirin:
    ```bash
    git clone [REPO_URL]
    ```

2.  Gerekli kütüphaneleri yükleyin:
    ```bash
    pip install opencv-python numpy
    ```

3.  Proje dizininde `plaka.jpg` adında bir görüntü olduğundan emin olun (veya koddaki `cv2.imread` satırını kendi dosya adınızla değiştirin).

4.  Jupyter Notebook'u çalıştırın:
    ```bash
    jupyter notebook opencv_ile_plaka_tespiti.ipynb
    ```
    Veya Python betiği olarak çalıştırıyorsanız:
    ```bash
    python dosya_adi.py
    ```
_______________________________________________________________________________________________________________________________________________________________________________________________________________________________
#EN
# Simple License Plate Detection with OpenCV

This project is a simple computer vision application developed using Python and the OpenCV library to detect a vehicle license plate in an image.

## 📝 Project Description

The code processes an image file named `plaka.jpg` and attempts to detect rectangular areas that could be license plates using image processing techniques.

The steps applied are as follows:
1.  The image is read in grayscale.
2.  A **Gaussian Blur** filter is applied to reduce noise.
3.  Edges in the image are found using the **Canny Edge Detection** algorithm.
4.  **Contours (outlines)** are detected based on the edges.
5.  The found contours are filtered based on geometric properties such as aspect ratio, area, width, and height.
6.  Contours that meet the license plate criteria are marked with a green rectangle, and the result is displayed.

## 🛠️ Technologies and Libraries Used

* **Python 3**
* **OpenCV** (`opencv-python`): For image processing functions (Image reading, GaussianBlur, Canny, findContours, rectangle).
* **NumPy**: A fundamental requirement for OpenCV.

## 🚀 How to Run

1.  Clone this repository or download the files:
    ```bash
    git clone [REPO_URL]
    ```

2.  Install the necessary libraries:
    ```bash
    pip install opencv-python numpy
    ```

3.  Ensure there is an image named `plaka.jpg` in the project directory (or change the `cv2.imread` line in the code to your own file name).

4.  Run the Jupyter Notebook:
    ```bash
    jupyter notebook opencv_ile_plaka_tespiti.ipynb
    ```
    Or, if running as a Python script:
    ```bash
    python file_name.py
    ```
