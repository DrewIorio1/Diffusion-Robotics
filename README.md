# Diffusion-Robotics
A collection of resources and papers on Diffusion Models and Robotics using diffusion

## 📚 Diffusion Model Resources

### **Diffusion Resources**  
*Vikash Sehwag*  
GitHub Pages 2023. [[Blog](https://vsehwag.github.io/blog/2023/2/all_papers_on_diffusion.html)] [[Code](https://github.com/VSehwag/minimal-diffusion)]  
20 Feb 2023

---

### **Sora by OpenAI (Video Diffusion Engine)**  
*OpenAI*  
Announced Feb 2024. [[Link](https://openai.com/sora)]  
Feb 2024

---

## 📘 Diffusion Papers

**Understanding Diffusion Models: A Unified Perspective** \
*Calvin Luo* \
arXiv 2022. [[Paper](https://arxiv.org/abs/2208.11970)] \
25 Aug 2022
Key Formulas - 
1. Forward Diffusion Process : q(xt∣xt−1)=N(xt;1−βtxt−1,βtI)
1.1. Where xt = noisy trajectory at timestep t
1.2.       βt  = variance schedule controlling how much noise is added per step

2. Reverse Deffusion Process: Formula - 125
2.1. Where ϵθ = network predicting the noise at step t
2.2        θ = learnable parameters
---

### **Denoising Diffusion Probabilistic Models (DDPM)**  
*Jonathan Ho, Ajay Jain, Pieter Abbeel*  
NeurIPS 2020. [[Paper](https://arxiv.org/abs/2006.11239)]  
15 Jun 2020

Key Formulas : 
1. Forward Diffusion Process : q(xt∣xt−1)=N(xt;1−βtxt−1,βtI)
1.1. Where xt = noisy trajectory at timestep t
1.2.       βt  = variance schedule controlling how much noise is added per step


---

### **Score-Based Generative Modeling through Stochastic Differential Equations**  
*Yang Song, Jascha Sohl-Dickstein, et al.*  
ICLR 2021. [[Paper](https://arxiv.org/abs/2011.13456)]  
24 Nov 2020

Key Formulas :
1.Forward Diffusion Process
  1.1 q(xt∣ xt−1) = N (xt;√αtx0,(1 − αt)I);
  1.2. xt = noisy sample at step t
  1.3. βt  =  variance schedule
2. **DDIM Reverse Process**

First, predict the original clean image \( \hat{x}_0 \) from \( x_t \):

\[
\hat{x}_0(x_t, t) = \frac{x_t - \sqrt{1 - \alpha_t} \, \epsilon_\theta(x_t, t)}{\sqrt{\alpha_t}}
\]

Then, update from \( x_t \) to \( x_{t-1} \) (deterministic DDIM case, \( \sigma_t = 0 \)):

\[
x_{t-1} = \sqrt{\bar{\alpha}_{t-1}} \, \hat{x}_0(x_t, t) + \sqrt{1 - \bar{\alpha}_{t-1}} \, \epsilon_\theta(x_t, t)
\]

Where:
- \( \epsilon_\theta(x_t, t) \) is the predicted noise at step \(t\)
- \( \alpha_t = 1 - \beta_t \)
- \( \bar{\alpha}_t = \prod_{s=1}^t \alpha_s \)


---

### **Denoising Diffusion Implicit Models (DDIM)**  
*Jiaming Song, Chenlin Meng, Stefano Ermon*  
ICLR 2021. [[Paper](https://arxiv.org/abs/2010.02502)]  
6 Oct 2020

---

### **Imagen: Photorealistic Text-to-Image Generation with Deep Language Understanding**  
*Chitwan Saharia et al. (Google Research)*  
arXiv 2022. [[Paper](https://arxiv.org/abs/2205.11487)]  
22 May 2022

---

### **Hierarchical Text-Conditional Image Generation with CLIP Latents (DALL·E 2)**  
*OpenAI*  
Open Access 2022. [[Research](https://openai.com/research/dall-e-2)]  
Apr 2022

---

### **High-Resolution Image Synthesis with Latent Diffusion Models**  
*Robin Rombach et al.*  
CVPR 2022. [[Paper](https://arxiv.org/abs/2112.10752)]  
20 Dec 2021

Introduced Latent Diffusion, enabling high-resolution generation with reduced computational cost. Backbone of Stable Diffusion.

---

### **ControlNet: Adding Conditional Control to Text-to-Image Diffusion Models**  
*Lvmin Zhang, Maneesh Agrawala (Stanford)*  
arXiv 2023. [[Paper](https://arxiv.org/abs/2302.05543)]  
10 Feb 2023


---

### **Diffusion Policies: Visuomotor Decision Making via Diffusion Probabilistic Models**  
*Alex Ichter et al. (Stanford, Google DeepMind)*  
ICLR 2023. [[Paper](https://arxiv.org/abs/2209.07245)]  
15 Sep 2022

---

### **Video Diffusion Models**  
*Jonathan Ho et al.*  
arXiv 2024. [[Paper](https://arxiv.org/abs/2304.08818)]  
17 Apr 2023


---

### **Consistency Models**  
*Yang Song, Diederik Kingma, et al.*  
NeurIPS 2023. [[Paper](https://arxiv.org/abs/2303.01469)]  
3 Mar 2023

---

### **AudioLM: A Language Modeling Approach to Audio Generation**  
*Google Research*  
NeurIPS 2023. [[Paper](https://arxiv.org/abs/2209.03143)]  
7 Sep 2022



---
