# Hey Alfred - microWakeWord Models

This repository contains two custom-trained wake word models for the phrase "Hey Alfred." These models are designed for use with ESPHome and the microWakeWord component.

Models
There are two versions of the model available. Version 2 is the recommended model for use.

***Version 1: hey_al_fred***

This is the original model and was created using the standard, default settings provided in the MicroWakeWord-Trainer-Docker project. It serves as a good baseline but may be less optimized than Version 2.

Training: Default project settings.

Files: `hey_al_fred.tflite` and `hey_al_fred.json`.

***Version 2: hey_al_fred_v2 (Recommended)***

This model was trained with specific custom settings to improve performance and stability. The key adjustments were made to ensure the model trained successfully without errors.

Training: This version was trained for 80,000 steps for more robust learning.

Audio Clip Duration: The audio clip length was set to 1940ms. This specific length was chosen to ensure the audio data was perfectly compatible with the final model conversion process, fixing a critical AssertionError.

Model Structure: The model's internal "listening window" (its kernel sizes) was simplified to use a consistent 7, 7, 7, 7 structure. This created a more stable and predictable model, which was crucial for a successful build.

Files: `hey_al_fred_v2.tflite` and `hey_al_fred_v2.json`.

How to Use
To use these models, you will need to add the .tflite and .json files to your ESPHome configuration. Please refer to the official ESPHome microWakeWord documentation for instructions on how to integrate a custom model.
