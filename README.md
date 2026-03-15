# 🖼️🤖 Efficient Fine-Tuning of Vision-Language Models with LoRA & Quantization

This project demonstrates **parameter-efficient fine-tuning of large Vision-Language Models (VLMs)**, specifically **Qwen2-VL-7B-Instruct**, using **LoRA (Low-Rank Adaptation)** and **4-bit quantization**.  
The goal is to enable large multimodal models to understand and reason over **images and text**, even on modest hardware.

---

## 📖 Project Overview

Vision-Language Models are transformers trained to process both **text and images** simultaneously. They can perform tasks such as:

- Visual question answering  
- Image captioning  
- Chart reasoning and analysis  

This project focuses on fine-tuning these models **efficiently**, using techniques that reduce memory and computational requirements while maintaining high performance.

---
![thumbnail](img.png)

## 🎯 Objectives

1. Train a VLM to **reason over charts and visual data** using the ChartQA dataset.  
2. Implement **parameter-efficient fine-tuning** with LoRA adapters.  
3. Reduce GPU memory consumption via **4-bit quantization**.  
4. Provide a **reproducible pipeline** for training, evaluation, and inference of multimodal models.  

---

## 🏗️ Key Techniques

- **LoRA (Low-Rank Adaptation)**: Updates only small adapter layers in the model, keeping most parameters frozen, making training faster and more memory-efficient.  
- **4-bit Quantization**: Reduces memory usage and allows fine-tuning of large models on consumer GPUs without sacrificing significant accuracy.  
- **TRL SFTTrainer**: A supervised fine-tuning trainer optimized for large transformer models that handles evaluation, checkpointing, and batching automatically.  

---

## 📊 Dataset

The project uses the **ChartQA dataset**, which contains charts, corresponding questions, and answers. This allows the VLM to learn **visual reasoning** and **multimodal question answering**.

The data is formatted in a **chat-style structure**, where each sample includes:

- A system message describing the model’s task  
- A user message containing an image and a textual query  
- An assistant message containing the correct answer  

---

## 🚀 Workflow

1. **Dataset Preparation**: Format images and questions for model input.  
2. **Model Loading**: Load the pretrained Qwen2-VL-7B model with optional 4-bit quantization for GPU efficiency.  
3. **LoRA Adapter Integration**: Add low-rank adapters to the model for parameter-efficient training.  
4. **Data Collation**: Prepare batched inputs of text and images for the trainer.  
5. **Training**: Fine-tune the model using the TRL SFTTrainer with evaluation and checkpointing.  
6. **Inference**: Generate predictions on new chart or image-question samples.  
7. **Memory Management**: Clear GPU and system memory safely to support repeated experiments.  

---

## 💡 Key Benefits

- Fine-tuning large VLMs without the need for massive GPU clusters  
- Efficient training using LoRA and quantization  
- Adaptable to multiple multimodal tasks beyond ChartQA  
- Simplified pipeline for training, evaluation, and inference  

---

## 🔹 Potential Applications

- AI assistants that can **interpret images and answer questions**  
- Business intelligence dashboards that **analyze charts automatically**  
- Research tools for **visual reasoning and multimodal understanding**  
- Educational tools that explain **data visualizations** in natural language  

---

## 📚 References

- LoRA Paper: [Low-Rank Adaptation of Large Language Models](https://arxiv.org/abs/2106.09685)  
- BitsAndBytes Library: [Memory-efficient Quantization](https://github.com/TimDettmers/bitsandbytes)  
- Hugging Face VLM Cookbook: [Fine-Tuning VLMs](https://huggingface.co/learn/cookbook/en/fine_tuning_vlm_trl)  
- Qwen2-VL Models: [Hugging Face Model Hub](https://huggingface.co/Qwen)  

---

## 🌟 Conclusion

This project provides a **complete pipeline for efficiently fine-tuning large Vision-Language Models** on multimodal datasets.  
By combining **LoRA, quantization, and TRL**, researchers and developers can **train state-of-the-art multimodal AI models on limited hardware**, enabling a wide range of applications in visual reasoning, chart analysis, and AI-assisted understanding of images and text.
