![Real-Time Face Mask Detection](assets/banner.svg)

> A video system that finds each face and shows whether the person is wearing a mask.

**Training project · IoT & Computer Vision track**  
**Tools:** Python, TensorFlow/Keras, OpenCV

## The challenge

Checking mask use by hand does not scale in busy places. This project applies a small trained model to every face in a video.

## The data

A labelled image set with two classes: 1,314 training images and 194 test images, resized to 150×150.

## How it works

![How it works](assets/pipeline.svg)

1. Trained a custom CNN on 1,314 images, with 194 images held out for testing.
2. Used a Haar Cascade to find faces in each video frame.
3. Classified every face, and drew the result on the video.

## A closer look

- **Model:** four convolution and pooling blocks with dropout, then dense layers.
- **Training:** batch size 16, for 10 epochs.
- **Live use:** a Haar Cascade finds faces, then each one goes through the classifier.

## Key decisions

- A classic face detector keeps the live pipeline simple, and leaves the decision to the trained model.

## Results

| Measure | Result |
|---|---|
| Training images | **1,314** |
| Test images | **194** |
| Classes | **Mask, no mask** |

## Programming skills

- Python programming
- Designing and training a CNN in Keras
- Loading image data in batches
- Saving and reusing trained models
- Real-time video processing with OpenCV
- Face detection with Haar Cascades

## Good to know

- The notebook did not keep a final accuracy score, so no accuracy is claimed here.

## What I would do next

- Record test accuracy and a confusion matrix.
- Replace the Haar Cascade with a modern face detector, for side views.

<details dir="rtl"><summary><strong>بالعربي: كشف الكمامة في الوقت الفعلي</strong></summary>

نظام يجد الوجوه في الفيديو ويحدد لكل وجه هل يرتدي كمامة، بشبكة عصبية دُرّبت على 1,314 صورة.

**ملاحظة:** لم يُحفظ رقم الدقة النهائي، لذلك لا نذكر دقة.

**المهارات البرمجية:** Python programming، Designing and training a CNN in Keras، Loading image data in batches، Saving and reusing trained models، Real-time video processing with OpenCV، Face detection with Haar Cascades.

الكود خاص، وهذه الصفحة تعرض فكرة المشروع وطريقة عمله ونتائجه.

</details>


---

**About the source code:** the code for this project is private. This page presents what it does, how it works, and its results. To talk about the work, contact me through my [GitHub profile](https://github.com/SamerAlTaki97).
