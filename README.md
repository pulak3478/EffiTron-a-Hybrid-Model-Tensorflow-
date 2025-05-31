📚 EffiTron: Hybrid CNN-Transformer Architecture for Multi-Class Image Classification
EffiTron combines the powerful local feature extraction capabilities of EfficientNetB0 with the global contextual understanding of a Transformer Encoder. This hybrid model is designed for robust and efficient multi-class image classification tasks.

🏗️ Architecture Summary
EffiTron integrates:

EfficientNetB0 Backbone – Captures local spatial features.

Transformer Encoder Layers – Extracts global contextual relationships from reshaped feature sequences.

Dense Classifier – Outputs final class probabilities.
🔬 Notation
Symbol	Description
𝐼 ∈ ℝᴴ×ᵂ×ᶜ	Input image
𝐹 ∈ ℝʰ×ʷ×ᵈ	Feature map from EfficientNetB0
𝑇 ∈ ℝ(ʰ⋅ʷ)×ᵈ	Reshaped sequence
𝑑	Feature depth (1280 for EfficientNetB0)
𝑁	Number of classes
𝐿	Number of Transformer layers
𝐻	Number of attention heads

🧮 Parameter Calculation
EfficientNetB0 Output: 𝐹 ∈ ℝ⁷×⁷×¹²⁸⁰ (parameters ~5.3M)

Transformer Encoder Parameters:

For 1 layer (H=4, f=256): ~7.1M

For 2 layers: ~14.2M

Final Dense Layer:
≈
1280
×
𝑁
+
𝑁
≈1280×N+N
