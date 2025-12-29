# Weather-GAN
🌦️ WeatherGAN – Conditional Adverse Weather Image Translation

WeatherGAN is a conditional GAN for translating clear road scenes into foggy and rainy conditions.

The model focuses on realistic weather effects while preserving the underlying scene structure.

🗂️ Datasets
This project uses real-world driving datasets as clear-weather inputs:

📌 Cityscapes Dataset

📌 Indian Driving Dataset (IDD)

• These datasets contained only clear weather images. Corresponding synthetic dataset for rain and fog by augmentation.

🧠 Approach

The system learns a residual-based Pix2Pix image translation strategy:

• The generator takes a clear image and a weather condition as input

• It predicts a weather-specific residual

• The residual is added to the conditioned weather image to produce the final output


This design allows:

• Better preservation of scene geometry

• Controlled intensity of weather effects

• Stable multi-domain training within a single model


🏗️ Architecture

• Generator: U-Net–style architecture with skip connections and residual learning

• Discriminator: PatchGAN discriminator

A single generator is trained to handle multiple weather conditions.

📊 Results

The model:

• Produces realistic fog with reduced visibility

• Adds rain streaks and lighting changes

• Preserves object layout, roads, and buildings


<img width="1920" height="1080" alt="Screenshot (133)" src="https://github.com/user-attachments/assets/f06118dc-4408-4484-9d85-f429086731a6" />


🔧 Key Learnings

• Residual learning improves structural consistency in image translation

• Conditional GANs can effectively handle multiple weather domains

• Multi-domain translation does not require separate models per condition


📌 Future Work

• Extend to night-time and snow conditions

• Improve rain streak realism
• Evaluate impact on downstream perception tasks
