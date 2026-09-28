# AuraFlow: Privacy-First NPU-Driven Desktop Automation and Task Synthesizer

## 1. Executive Summary
AuraFlow is an ultra-low latency, zero-cloud context intelligence and task orchestration framework engineered specifically for the Snapdragon-powered HP PC ecosystem. By executing quantized LLMs and audio-processing models entirely on-device via the Snapdragon Hexagon NPU, AuraFlow breaks the reliance on cloud infrastructure. This completely eliminates data privacy exposures, reduces power consumption, and ensures system snappiness during continuous background orchestration.

## 2. Core Capabilities
- **Zero-Cloud Privacy Framework:** All desktop scraping, text synthesis, and local action routing happen within the system memory boundary. No telemetry or data payloads leave the local HP PC machine.
- **Cross-Application Task Orchestration:** Synthesizes user intent from text or voice commands into deterministic, native desktop automation sequences (file routing, application launch, and inter-process communication).
- **On-Device Audio Intelligence:** Locally captures and indexes ambient meeting streams using quantized speech-to-text models, transforming raw sound arrays into actionable text highlights instantly.

## 3. Technical Implementation & Qualcomm Tech Stack
- **Target Platform:** Snapdragon-powered HP PCs running Windows 11 on ARM.
- **Models Used (Qualcomm AI Hub Compiled):** 
  - Text Processing: `Phi-3-mini-4k-instruct-onnx` (Quantized to INT4 for optimal NPU memory footprint).
  - Audio Transcription: `Whisper-Base-En` (ONNX format optimized for Snapdragon Neural Processing SDK).
- **Execution Target:** ONNX Runtime utilizing the `QNNExecutionProvider` (Qualcomm Neural Network execution provider) to directly target the Hexagon NPU via the HTP backend drivers (`libQnnHtp.so` / `QnnHtp.dll`).
- **Memory Footprint:** Configured to consume under 2.8 GB of unified system memory during peak concurrent processing pipelines, preserving resources for standard foreground operations.

## 4. Evaluation Criteria Alignment
- **Technical Implementation:** Achieves hardware-level acceleration by directly loading ONNX files via the QNN Execution Provider.
- **Application Use Case & Innovation:** Transitions workflow automation from passive cloud scripts to proactive, privacy-isolated local agents.
- **Deployment & Accessibility:** Fully packaged as a native client app for Windows on ARM, making advanced AI completely offline-accessible.
- **Presentation & Documentation:** Transparent architecture blueprints, clean modular codebase, and thorough deployment validation routines.
