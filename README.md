# Speaker_Recognition_System

# Speaker Recognition System - TMS320C6713 DSK Implementation

## Overview

This project implements a speaker recognition system using the TMS320C6713 DSK board. The system aims to identify or verify speakers based on their voice characteristics. The project encompasses hardware setup, software development using Code Composer Studio (CCS) and MATLAB, and the implementation of Mel-Frequency Cepstral Coefficients (MFCC) for feature extraction.

## Table of Contents

1.  Problem Definition & Design Specifications
2.  Introduction
3.  Principle of Speaker Recognition
4.  Literature Survey
5.  Hardware Composition of the Kit (TMS320C6713 DSK)
6.  Software Description (CCS 5.3.0, Audacity)
7.  Speech Feature Extraction Process (MFCC)

## 1. Problem Definition & Design Specifications

### Problem Definition

The objective is to develop a system capable of identifying a speaker from a collection of audio data recorded over time. Applications include video conferencing, access control, and fraud detection.

### Design Specifications

-   **Hardware:**
    -   TMS320C6713 DSK board (225 MHz, floating-point DSP, EDMA Controller, AIC23 Stereo Codec)
-   **Software:**
    -   MATLAB 2015b
    -   Code Composer Studio v5.3

## 2. Introduction

Speaker recognition is the process of automatically recognizing a speaker based on their voice. It involves training and testing phases to build and compare speaker models.

## 3. Principle of Speaker Recognition

Speaker recognition can be:

-   **Text-independent:** Recognizes speakers regardless of what they say.
-   **Text-dependent:** Recognizes speakers based on specific phrases.

The system consists of feature extraction and feature matching modules.

-   **Speaker Identification:** Determining which speaker's voice is present.
-   **Speaker Verification:** Confirming if a speaker's claimed identity is correct.

## 4. Literature Survey

Various institutions and companies have developed speaker recognition systems. The choice between fixed-point and floating-point processors is crucial, with the TMS320C6713 being a floating-point DSP.

## 5. Hardware Composition of the Kit (TMS320C6713 DSK)

### Key Features

-   TMS320C6713 DSP
-   AIC23 stereo codec
-   DIP switches and LEDs
-   CPLD registers

### Processor Description

-   Floating-point DSP with VLIW architecture
-   Dual register files and functional units
-   Load/store architecture

## 6. Software Description (CCS 5.3.0, Audacity)

### Code Composer Studio (CCS) 5.3.0

-   Integrated development environment for DSP programming.
-   Includes compiler, debugger, and project manager.
-   Installation and project setup instructions are provided.
-   Connection of dsk6713 with CCS is described.

### Audacity

-   Used to convert audio files from .mp3 to .wav format for MATLAB compatibility.

## 7. Speech Feature Extraction Process (MFCC)

### Introduction

-   Converts speech waveforms into parametric representations.
-   Short-time spectral analysis is used.

### MFCC Processor

-   Mimics human ear behavior.
-   Steps include framing, windowing, FFT, power spectrum calculation, and Mel-frequency wrapping.

#### Framing

-   Splits the audio signal into uniform frames.

#### Windowing

-   Reduces spectral leakage using a Hamming window.

#### Fast Fourier Transform (FFT)

-   Converts time-domain frames to the frequency domain.

#### Power Spectrum of the Signal

-   Calculates the power of the frequency domain.

#### Mel-Frequency Wrapping

-   Applies triangular filters using the Mel frequency scale.

## Usage

1.  **Hardware Setup:** Connect the TMS320C6713 DSK to your computer.
2.  **Software Installation:** Install CCS 5.3.0 and MATLAB 2015b.
3.  **Audio File Conversion:** Use Audacity to convert audio files to .wav format.
4.  **CCS Project Setup:** Create a new project in CCS, configure the linker and compiler settings.
5.  **Code Development:** Implement the MFCC algorithm and speaker recognition logic in CCS.
6.  **Testing:** Load and debug the code on the TMS320C6713 DSK.
7.  **MATLAB Integration:** use the .wav files with matlab for further processing, if neccesary.

## Dependencies

-   TMS320C6713 DSK board
-   Code Composer Studio v5.3
-   MATLAB 2015b
-   Audacity

