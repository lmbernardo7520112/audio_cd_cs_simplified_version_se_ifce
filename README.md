# 🗣️ Voice Command Recognition on Raspberry Pi Pico W 🎙️

A TinyML project for embedded voice command recognition on the Raspberry Pi Pico W.

## 💡 Overview

This project explores the implementation of a voice command recognition system on the Raspberry Pi Pico W microcontroller. Leveraging the device's low cost, flexibility, and limited resource capabilities, we've created a streamlined system capable of processing audio signals and performing inference using pre-trained machine learning models. 🚀

This project is divided into two main phases:

*   **Phase 1: Proof of Concept** - Demonstrating the end-to-end audio processing pipeline using synthetic audio samples.
*   **Phase 2: Enhanced Realism** - Improving robustness and accuracy by integrating real-world audio data and refined feature extraction techniques.

## ✨ Key Features

*   **Embedded Implementation:** Runs directly on the Raspberry Pi Pico W, eliminating the need for cloud processing.
*   **Low Resource Footprint:** Optimized algorithms and model architecture for resource-constrained devices.
*   **Real-time Performance:**  Designed for real-time voice command recognition.
*   **Clear Feedback:** Provides visual and auditory feedback on command recognition success. ✅
*   **Simulated Environment:** Developed and tested within the Wokwi online simulator for easy experimentation. 💻

## 🛠️ Technologies Used

*   **Raspberry Pi Pico W:** Microcontroller for audio processing and inference. 🍓
*   **C:** Programming language for firmware development. ⚙️
*   **TensorFlow Lite Micro:**  Framework for deploying optimized machine learning models.
*   **Wokwi:** Online simulator for embedded systems. 🌐
*   **MFCC (Mel-Frequency Cepstral Coefficients):** Feature extraction technique for audio analysis. 🎶
*   **TinyML:** Machine learning on embedded devices. 🧠

## ⚙️ How It Works

The voice command recognition system follows these steps:

1.  **Audio Acquisition:** The system captures audio from a microphone (simulated in the Wokwi environment).
2.  **Feature Extraction:** Mel-Frequency Cepstral Coefficients (MFCCs) are extracted from the audio signal to capture relevant acoustic characteristics.
3.  **Neural Network Inference:** A pre-trained neural network processes the MFCCs and predicts the spoken command.
4.  **Feedback:** The system provides feedback to the user through an LED (visual) and a buzzer (auditory), confirming the recognized command.


## 🚀 Getting Started

Unfortunately, this project can't be directly cloned and run without a Raspberry Pi Pico W or Wokwi account. However you can follow the methodology, and adapt the source to your own project.

1.  **Prerequisites:**
    *   Raspberry Pi Pico W
    *   Wokwi Account (optional, for simulation)
    *   Basic knowledge of C programming.
    *   Raspberry Pi Pico C/C++ SDK installed and configured on your development machine.

2.  **Setup:**
    *   (For Wokwi simulation): Create a free account at [wokwi.com](https://wokwi.com/) and clone the source code to use in the environment.

3.  **Build the Firmware:**

4.  **Flash the Firmware:** Connect the Raspberry Pi Pico W to your computer and flash the compiled firmware.

5.  **Test and Experiment:** Speak the pre-defined commands ("go", "stop", "up", "down", "left", "right") and observe the system's feedback.

## 📂 Project Structure

├── main.c # Main source code file
├── diagram.json # Wokwi simulator configuration
├── model_data_modelo_simplificado.h # Pre-trained neural network weights
├── test_audio_samples.h # Real audio samples for testing
└── ...

## 📈 Performance and Results

The initial version of the system achieved a recognition accuracy of **88%** in a controlled environment. The project improved upon this by using prerecorded auido samples and reducing the neural network. However some problems were identified:

*   Overflow on Softmax
*   Prediction Concentrated

These will be addressed in the future for increasing the robustness and precise system.

## 🗺️ Roadmap

*   Address overflows in the Softmax function to improve stability.
*   Implement techniques to improve the model's generalization to a wider range of speakers and environments.
*   Explore data augmentation techniques to increase the robustness of the model.
*   Evaluate and compare different model architectures to optimize performance.
*   Implement noise reduction algorithms to improve recognition accuracy in noisy environments. (Work in progress)

## 🤝 Contributions

Contributions to this project are welcome! Feel free to submit bug reports, feature requests, or pull requests.


## ✍️ Author

*   Leonardo Maximino Bernardo

## 🔗 Useful Links

*   **Wokwi Simulation:** [https://wokwi.com/projects/420983118254131201](https://wokwi.com/projects/420983118254131201)
*   **Second Version**: [https://wokwi.com/projects/420267737999434753](https://wokwi.com/projects/420267737999434753)
*   **Raspberry Pi Pico C/C++ SDK Documentation:** [https://datasheets.raspberrypi.com/picow/pico-2-w-schematic.pdf](https://datasheets.raspberrypi.com/picow/pico-2-w-schematic.pdf)
*   **Mini Speech Commands Dataset:** (if applicable) [https://www.tensorflow.org/tutorials/audio/simple\_audio?hl=pt-br](https://www.tensorflow.org/tutorials/audio/simple_audio?hl=pt-br)

