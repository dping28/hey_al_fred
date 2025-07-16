# Hey Alfred - microWakeWord Models

This repository contains custom-trained wake word models for the phrase "Hey Alfred." These models are designed for use with Home Assistant, ESPHome, and the `microWakeWord` component.

## Models

Three versions of the model are available. **Version 3 is the latest and most advanced model**, recommended for the best performance.

### Version 3: `hey_al_fred_v3` (Latest & Recommended)

This is the most advanced and highest-performing model, building on the lessons learned from V2. It was trained with a more complex structure and for a longer duration to maximize accuracy and reduce false activations.

*   **Training:** This version was trained for **120,000 steps** for maximum refinement.
*   **Model Structure:** Uses a more complex and balanced **mixed-kernel structure** (`[7], [7,9], [9,11], [11,13]`) for more precise sound recognition.
*   **Audio Clip Duration:** The audio clip length was fine-tuned to **1600ms** to ensure perfect compatibility with the advanced model structure.
*   **Performance:** Achieved a peak performance score of **99.87%** during validation, making it the most reliable model in this repository.
*   **Files:** `hey_al_fred_v3.tflite` and `hey_al_fred_v3.json`.

### Version 2: `hey_al_fred_v2`

This model was the first major improvement, trained with custom settings to enhance performance and resolve critical training errors.

*   **Training:** This version was trained for **80,000 steps**.
*   **Audio Clip Duration:** The audio clip length was set to **1940ms** to fix a compatibility issue with the model structure.
*   **Model Structure:** The model's "listening window" (kernel sizes) was simplified to a consistent `7, 7, 7, 7` structure for stability.
*   **Files:** `hey_al_fred_v2.tflite` and `hey_al_fred_v2.json`.

### Version 1: `hey_al_fred`

This is the original baseline model, created using the standard default settings from the `MicroWakeWord-Trainer-Docker` project.

*   **Training:** Default project settings.
*   **Files:** `hey_al_fred.tflite` and `hey_al_fred.json`.

## How to Use

To use these models, you will need to add the `.tflite` and `.json` files to your ESPHome configuration. Please refer to the official ESPHome `microWakeWord` documentation for instructions on how to integrate a custom model.

