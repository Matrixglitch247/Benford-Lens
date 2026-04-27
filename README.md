# BenfordLens — AI Image Authenticity Detector

A free, browser-based tool that detects AI-generated images using **Benford's Law applied to DCT frequency coefficients**.

🔗 **Live tool:** [your-Matrixglitch247.github.io/Benford-Lens](https://Matrixglitch247.github.io/Benford-Lens)

---

## How it works

Real photographs are captured from the physical world through a lens. Their DCT (Discrete Cosine Transform) frequency coefficients follow **Benford's Law** — a mathematical principle stating that leading digits in naturally occurring data appear with a specific logarithmic frequency (digit 1 ≈ 30.1%, digit 2 ≈ 17.6%, down to digit 9 ≈ 4.6%).

AI-generated images, synthesised rather than captured, deviate from this distribution in measurable ways. This tool quantifies that deviation using 8 statistical metrics and returns a synthetic probability score.

## Features

- **100% private** — analysis runs entirely in your browser, no images are uploaded anywhere
- **Interpretable** — see exactly which digits deviated and by how much
- **8 statistical metrics** — chi-squared, KL divergence, mean absolute deviation, KS statistic, kurtosis, skewness, digit-1 excess ratio, Pearson correlation
- **Adaptive sharpening** — handles blurry and low-texture images intelligently
- **Community feedback** — thumbs up/down on every result to track real-world accuracy

## Academic basis

This implementation is based on:

> Bonettini, N., Bestagini, P., Milani, S., & Tubaro, S. (2020). *On the use of Benford's Law to detect GAN-generated images*. ICPR 2020. [arxiv.org/abs/2004.07682](https://arxiv.org/abs/2004.07682)

Also informed by Fu, Shi & Su (2007) on Generalised Benford's Law for JPEG forensics.

## Limitations

- Statistical estimate only — not a definitive classification
- Heavily blurred images, extreme JPEG compression, and screenshots can affect accuracy
- Best used alongside other forensic methods
- Modern high-quality AI generators (especially those that mimic photographic noise) are harder to detect

## Usage

No installation needed. Open `index.html` in any browser, or visit the live link above.

## License

MIT — free to use, modify, and share.
