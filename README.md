# QR Code GAN for Cybersecurity

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1AhF_VN1qXZfo22PK3dfa4lUWoTt429pP?usp=drive_link)
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-red.svg)](https://pytorch.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## Overview

A Generative Adversarial Network (GAN) implementation that generates functional QR codes indistinguishable from real ones while maintaining scannability. This project demonstrates potential cybersecurity vulnerabilities in QR-based authentication systems.

**Key Achievement:** 100% scan success rate on generated QR codes that decode to the target message.

## 🎯 Project Objectives

- Train a DCGAN to generate synthetic QR codes that fool discriminator networks
- Ensure generated QR codes scan successfully on smartphones
- Maintain embedded message integrity ("CyberSec_Masters_GAN_Project_2025")
- Demonstrate adversarial AI capabilities for cybersecurity research

## 🏗️ Architecture

### Generator Network
- **Input:** 100-dimensional noise vector
- **Output:** 64x64 grayscale QR code
- **Architecture:** 4-layer transpose convolutional network with batch normalization
- **Parameters:** ~1.5M

### Discriminator Network
- **Input:** 64x64 QR code image
- **Output:** Real/fake classification
- **Architecture:** 4-layer convolutional network with LeakyReLU
- **Parameters:** ~800K

## 📊 Results

| Metric | Value |
|--------|-------|
| **Scan Success Rate** | 100% |
| **Generated Samples** | 64/64 functional |
| **Training Epochs** | 300 |
| **Training Time** | ~30 minutes |
| **Discriminator Accuracy** | 50% (balanced) |

## 🚀 Quick Start

### Run in Google Colab (Recommended)
Click the "Open in Colab" badge above to run the complete notebook with free GPU access.

### Local Installation
```bash
# Clone repository
git clone https://github.com/yourusername/qr-gan.git
cd qr-gan

# Install dependencies
pip install torch torchvision
pip install qrcode[pil] pyzbar
pip install opencv-python-headless
pip install numpy matplotlib tqdm
```

## 📁 Project Structure

```
qr-gan/
├── Section 1: Environment Setup & Imports
├── Section 2: Original QR Code Creation
├── Section 3: Dataset Generation (2000 samples)
├── Section 4: GAN Architecture Definition
├── Section 5: Loss Functions & Training Setup
├── Section 6: Training Loop (300 epochs)
└── Section 7: Results Analysis & Visualization
```

## 🔬 Technical Approach

1. **Dataset Creation:** Generated 2000 QR code variations using augmentation (rotation, noise, brightness)
2. **Custom Loss Function:** Balanced adversarial loss with structural preservation (weight: 0.1)
3. **Training Strategy:** Alternating discriminator/generator updates with periodic validation
4. **Quality Control:** Real-time QR scanning validation during training

## ⚠️ Security Implications

This project demonstrates that adversarial AI can:
- Generate functional QR codes that pass standard validation
- Potentially bypass QR-based security systems
- Create untraceable fake QR codes for:
  - Payment systems
  - Authentication tokens
  - Digital COVID passes
  - Event tickets

## 📈 Key Findings

- **Mode Collapse:** The GAN converged on highly reliable patterns rather than diverse variations, mimicking real-world attack scenarios
- **Perfect Functionality:** 100% scan success demonstrates the vulnerability of QR validation systems
- **Structural Loss Critical:** Experiments showed QR functionality requires domain-specific constraints (structural loss weight between 0.1-0.3)

## 🛠️ Technologies Used

- **PyTorch** - Deep learning framework
- **DCGAN** - Deep Convolutional GAN architecture
- **OpenCV** - Image processing
- **pyzbar** - QR code scanning validation
- **Google Colab** - GPU-accelerated training

## 📚 References

- Goodfellow et al. (2014) - Generative Adversarial Networks
- Radford et al. (2015) - Unsupervised Representation Learning with DCGANs
- QR Code ISO/IEC 18004:2015 Standard

## 🤝 Contributing

This project was developed for educational purposes in cybersecurity research. Contributions and discussions about defensive measures are welcome.

## ⚖️ Disclaimer

This project is for educational and research purposes only. The techniques demonstrated should not be used for malicious purposes or to compromise security systems.

## 📝 License

MIT License - See [LICENSE](LICENSE) file for details

## 👤 Author

**[Your Name]**
- Portfolio: [yourportfolio.com](https://yourportfolio.com)
- LinkedIn: [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
- GitHub: [@yourusername](https://github.com/yourusername)

---

*Developed as part of AI for Cybersecurity Masters Course Project (2025)*
