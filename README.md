# image-sharpening-knowledge-distillation
Image sharpening using knowledge distillation with Real-ESRGAN teacher and custom student

🗂️ Overview:

Image Sharpening with Knowledge Distillation is a deep learning approach that leverages a powerful teacher model (Real-ESRGAN) and a lightweight student CNN to enhance degraded or low-resolution images. The goal is to distill the high-fidelity sharpening capability of the teacher into a smaller, faster student that can run efficiently on limited hardware.

This project demonstrates the use of:

Super-resolution,

Perceptual Loss,

Knowledge Distillation,

High-to-low image translation,

and is built to showcase how advanced deep learning methods can improve image quality in real-world scenarios like restoration, upscaling, or detail enhancement.

✅ Key Features:

🔬 Teacher Model (Real-ESRGAN):

Uses the Anime6B variant for high-quality upscaling.

Pre-trained on diverse datasets.

Provides sharp, super-resolved images as ground truth for the student.

👨‍🎓 Student Model:

Lightweight custom CNN with PixelShuffle upscaling blocks.

Trained to mimic the teacher’s output using L1 Loss and Perceptual Loss.

Designed for efficient deployment with reduced compute needs.

🔁 Knowledge Distillation:

Degraded images are enhanced by the teacher.

The student learns to reproduce the teacher’s output.

Combines pixel-wise loss with feature-level perceptual loss for better sharpness.

🗂️ Data:

Uses the DIV2K dataset (high-res images).

Includes custom degradation pipeline to create realistic blurred inputs.

📏 Evaluation Metrics:

PSNR (Peak Signal-to-Noise Ratio),

SSIM (Structural Similarity Index).

⚙️ Technology Stack:

Language: Python 3.x;

Frameworks/Libraries: PyTorch, OpenCV, PIL, torchvision, Real-ESRGAN;

Notebook: Google Colab (GPU-accelerated);

Dataset: DIV2K (High Resolution Images).

🚀 Usage:

1️⃣ Clone the Repository:

bash    Copy    Edit

git clone https://github.com/yourusername/ImageSharpening-KD.git

cd ImageSharpening-KD

2️⃣ Run on Google Colab:

Open the ImageSharpeningKD.ipynb notebook.

Follow the step-by-step cells.

Connect to a GPU runtime.

3️⃣ Mount Drive:

Store your trained student model (student_model.pth) in Google Drive for persistence.

4️⃣ Train:

The notebook automatically downloads DIV2K.

Runs the degradation pipeline.

Trains the student with knowledge distillation.

5️⃣ Evaluate:

Visualizes degraded, student, and teacher outputs.

Computes PSNR, SSIM for objective quality.

🎯 Conclusion:

Image Sharpening with Knowledge Distillation demonstrates how you can replicate large high-capacity models with efficient smaller ones — bridging the gap between high-performance and real-world deployment.
The pipeline can be adapted for other image enhancement tasks, integrated into apps, or extended with new architectures.
