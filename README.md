# ASL Alphabet Recognition using K-Nearest Neighbors (KNN)

## Overview

This project focuses on recognizing the American Sign Language (ASL) alphabet using a machine learning classification algorithm.

The dataset was obtained from Kaggle and contains images representing hand gestures for the English alphabet. The goal is to classify these images into their corresponding alphabet labels using the **K-Nearest Neighbors (KNN)** algorithm.

## Dataset

The dataset was sourced from Kaggle:

- **Dataset:** [ASL Alphabet Dataset](https://www.kaggle.com/datasets/grassknoted/asl-alphabet)
- **Total training images:** 87,000
- **Original image size:** 200 × 200 pixels
- **Preprocessed image size:** 28 × 28 pixels

Due to the dataset size and available computational resources, the images were resized from 200 × 200 to 28 × 28 pixels to reduce memory usage and computational costs.

## Project Workflow

### 1. Data Preprocessing

- Resized images from 200 × 200 to 28 × 28 pixels.
- Converted the image data into NumPy arrays for efficient processing.
- Prepared the features and labels for machine learning.

### 2. Train-Test Split

The dataset was split into two subsets:

- **80% — Training set**
- **20% — Test set**

This separation allows the model to be evaluated on data that was not used during training.

### 3. Observability and Validation

Throughout the preprocessing and modeling stages, validation checks and diagnostic techniques were used to improve observability, detect potential errors, and verify the integrity of the data and workflow.

### 4. Model Training

A K-Nearest Neighbors (KNN) classifier was trained using the training dataset.

- **Algorithm:** K-Nearest Neighbors (KNN)
- **Number of neighbors (k):** 5
- **Test accuracy:** 98%

### 5. Model Evaluation

The model was evaluated using multiple classification metrics to gain a more comprehensive understanding of its performance.

- **Accuracy:** Measures the proportion of correctly classified samples.
- **Precision:** Measures how many predictions for a class were correct.
- **Recall:** Measures how many actual samples of a class were correctly identified.
- **F1-score:** Provides a balance between precision and recall.
- **Confusion Matrix:** Shows the distribution of correct and incorrect predictions across classes.

## Results

The KNN classifier achieved **98% accuracy** on the test dataset.

In addition to accuracy, the F1-score and confusion matrix were used to investigate classification performance across different alphabet classes and identify potential misclassifications.

## Project Structure

```text
.
├── Test_dataset/
├── Train_dataset/
├── License
├── main.ipynb
├── README.md
├── x.npy
└── y.npy
```

- `Test_dataset/` — Test images.
- `Train_dataset/` — Training images.
- `License` — License information associated with the project.
- `main.ipynb` — Jupyter Notebook containing preprocessing, training, and evaluation.
- `README.md` — Project documentation.
- `x.npy` — NumPy array containing image features.
- `y.npy` — NumPy array containing the corresponding labels.

## Technologies Used

- Python
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook
- K-Nearest Neighbors (KNN)

## Future Improvements

- Experiment with different values of `k`.
- Compare KNN with other classification algorithms.
- Analyze class-specific performance using precision, recall, and F1-score.
- Explore dimensionality reduction and more efficient feature extraction.
- Investigate image augmentation and deep learning approaches such as Convolutional Neural Networks (CNNs).

## Acknowledgments

Special thanks to the dataset creator for making the ASL Alphabet dataset available on Kaggle.






# تشخیص حروف الفبای زبان اشاره آمریکایی با الگوریتم KNN

## معرفی پروژه

هدف این پروژه، تشخیص حروف الفبای زبان اشاره آمریکایی (ASL) با استفاده از الگوریتم‌های یادگیری ماشین است.

در این پروژه، از تصاویر حرکات دست برای آموزش یک مدل طبقه‌بندی استفاده شده است تا مدل بتواند حرف متناظر با هر تصویر را پیش‌بینی کند.

دیتاست مورد استفاده از وب‌سایت Kaggle تهیه شده است.

## دیتاست

- **منبع:** [ASL Alphabet Dataset در Kaggle](https://www.kaggle.com/datasets/grassknoted/asl-alphabet)
- **تعداد تصاویر:** ۸۷٬۰۰۰ تصویر
- **ابعاد اولیه تصاویر:** ۲۰۰ × ۲۰۰ پیکسل
- **ابعاد تصاویر پس از پیش‌پردازش:** ۲۸ × ۲۸ پیکسل

با توجه به حجم دیتاست و محدودیت منابع سخت‌افزاری سیستم، تصاویر از ابعاد ۲۰۰ × ۲۰۰ به ۲۸ × ۲۸ پیکسل تغییر اندازه داده شدند تا مصرف حافظه و هزینه محاسباتی کاهش یابد.

## مراحل اجرای پروژه

### ۱. پیش‌پردازش داده‌ها

در مرحله اول، تصاویر برای استفاده در الگوریتم یادگیری ماشین آماده شدند:

- تغییر اندازه تصاویر از ۲۰۰ × ۲۰۰ به ۲۸ × ۲۸ پیکسل
- تبدیل تصاویر به آرایه‌های NumPy
- آماده‌سازی ویژگی‌ها و برچسب‌ها برای آموزش مدل

### ۲. تقسیم دیتاست

داده‌های آماده‌شده به دو بخش آموزش و آزمون تقسیم شدند:

- **۸۰٪ داده‌ها:** مجموعه آموزش (Train Set)
- **۲۰٪ داده‌ها:** مجموعه آزمون (Test Set)

این تقسیم‌بندی امکان ارزیابی مدل را روی داده‌هایی فراهم می‌کند که در فرایند آموزش استفاده نشده‌اند.

### ۳. بررسی و اعتبارسنجی مراحل اجرا (Observability)

در طول مراحل پیش‌پردازش، آماده‌سازی داده‌ها و آموزش مدل، از بررسی‌ها و روش‌های اعتبارسنجی مختلف استفاده شد تا خطاهای احتمالی شناسایی شوند و از صحت اجرای مراحل اطمینان حاصل شود.

### ۴. آموزش مدل

برای طبقه‌بندی تصاویر از الگوریتم K-Nearest Neighbors (KNN) استفاده شد.

تنظیمات اصلی مدل:

- **الگوریتم:** K-Nearest Neighbors (KNN)
- **تعداد همسایه‌ها (k):** ۵
- **دقت مدل روی داده‌های آزمون:** ۹۸٪

### ۵. ارزیابی مدل

برای بررسی عملکرد مدل، از معیارهای مختلف ارزیابی طبقه‌بندی استفاده شد:

- **Accuracy:** نسبت پیش‌بینی‌های صحیح به کل پیش‌بینی‌ها
- **Precision:** نسبت پیش‌بینی‌های صحیح یک کلاس به کل پیش‌بینی‌های مثبت همان کلاس
- **Recall:** نسبت نمونه‌های صحیح شناسایی‌شده یک کلاس به کل نمونه‌های واقعی همان کلاس
- **F1-score:** معیاری برای ارزیابی هم‌زمان Precision و Recall
- **Confusion Matrix:** ماتریسی برای بررسی پیش‌بینی‌های صحیح و خطاهای طبقه‌بندی در کلاس‌های مختلف

استفاده از این معیارها کمک می‌کند عملکرد مدل از جنبه‌های مختلف بررسی شود و حروفی که مدل در تشخیص آن‌ها دچار اشتباه می‌شود، شناسایی شوند.

## نتایج

مدل KNN با مقدار `k=5` توانست روی مجموعه آزمون به دقت **۹۸٪** دست پیدا کند.

علاوه بر Accuracy، از معیار F1-score و ماتریس درهم‌ریختگی (Confusion Matrix) برای بررسی دقیق‌تر عملکرد مدل در کلاس‌های مختلف استفاده شد.

## ساختار پروژه

```text
.
├── Test_dataset/
├── Train_dataset/
├── License
├── main.ipynb
├── README.md
├── x.npy
└── y.npy
```

- `Test_dataset/` — شامل تصاویر مجموعه آزمون
- `Train_dataset/` — شامل تصاویر مجموعه آموزش
- `License` — فایل مربوط به اطلاعات مجوز
- `main.ipynb` — نوت‌بوک اصلی پروژه شامل مراحل پیش‌پردازش، آموزش و ارزیابی مدل
- `README.md` — مستندات پروژه
- `x.npy` — آرایه NumPy مربوط به ویژگی‌های تصاویر
- `y.npy` — آرایه NumPy مربوط به برچسب‌ها

## ابزارها و کتابخانه‌های استفاده‌شده

- Python
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## ایده‌هایی برای توسعه آینده

- بررسی عملکرد مدل با مقادیر مختلف `k`
- مقایسه KNN با الگوریتم‌های طبقه‌بندی دیگر
- تحلیل دقیق‌تر عملکرد هر کلاس با استفاده از Precision، Recall و F1-score
- بررسی روش‌های کاهش ابعاد و استخراج ویژگی
- بررسی روش‌های افزایش داده (Data Augmentation)
- پیاده‌سازی مدل‌های یادگیری عمیق، مانند شبکه‌های عصبی کانولوشنی (CNN)

## قدردانی

از تهیه‌کننده دیتاست ASL Alphabet به دلیل فراهم کردن این مجموعه داده در Kaggle سپاسگزارم.

**منبع دیتاست:** [ASL Alphabet Dataset — Kaggle](https://www.kaggle.com/datasets/grassknoted/asl-alphabet)


Dataset source: [ASL Alphabet Dataset — Kaggle](https://www.kaggle.com/datasets/grassknoted/asl-alphabet)
