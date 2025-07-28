# WearGAN - AI Powered Personalized Styling


This project leverages advanced Generative Adversarial Networks (GANs) to generate high-quality, realistic fashion images directly from textual descriptions.

# Key Features:

- **Text-to-Image Synthesis**: Utilizes a text-conditioned GAN to translate natural language prompts into corresponding fashion images.
- **Semantic Alignment with CLIP**: Integrates CLIP (Contrastive Language-Image Pre-training) embeddings to ensure the generated images semantically match the input text descriptions. The model was trained on the DressCodePromptSketch dataset to learn rich, style-specific representations.

# Advanced GAN Architecture:

- The Generator uses Residual Adaptive Instance Normalization (AdaIN) blocks to effectively modulate style based on text embeddings.
- The Discriminator employs Spectral Normalization and a WGAN-GP loss function to stabilize training and improve output quality.
- High-Resolution Upscaling: Employs Real-ESRGAN, a state-of-the-art super-resolution model, to upscale the generated 128x128 images to a sharper 256x256 resolution.
- Performance: Achieved a CLIPScore of 0.71, indicating strong text-image alignment, and an Inception Score of 6.12, reflecting high image quality and diversity.

# Usage

- The model is trained to take a textual prompt (e.g., "A red off-shoulder gown with golden lace") and generate a corresponding fashion image. The generation pipeline is as follows:
- A text prompt is encoded into a semantic vector using CLIP.
- The GAN's generator uses this vector to synthesize a 128x128 pixel image.
- The final image is upscaled to 256x256 pixels using Real-ESRGAN for enhanced detail.

# Future Enhancements

- Native High-Resolution Generation: Integrate architectures capable of generating 256x256 or 512x512 images directly, reducing reliance on post-processing upscaling.
- Multi-Modal Conditioning: Extend the model to accept a combination of inputs, such as text, sketches, and specific attributes (color, pattern, etc.).
- Interactive Design Interface: Develop a user-friendly UI that allows for iterative refinement of generated designs by adjusting text prompts or sketches in real-time.
- 3D Garment Modeling: Expand the 2D image generation capabilities into 3D modeling for applications in virtual try-ons and digital fashion.


