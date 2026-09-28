# AuraFlow Presentation Script & Recording Guidelines

## Slide 1: Introduction & Hook (Timing: 0:00 - 0:45)
- **Visuals:** Project Title Slide showcasing "AuraFlow" and the Snapdragon AI Lab badge logo asset.
- **Script:** "Hello judges. Today, I'm thrilled to present AuraFlow: a Privacy-First, NPU-Driven Desktop Automation and Task Synthesizer. In today's digital landscape, we are constantly forced to choose between the productivity power of AI and the complete exposure of our confidential workspace data to external clouds. AuraFlow eliminates this choice entirely. Designed natively for the Snapdragon-powered HP PC ecosystem, AuraFlow runs sophisticated language and speech models directly on system hardware. The result? Total privacy, sub-15-millisecond latency, and automated desktop orchestration that functions entirely offline."

## Slide 2: Vision & Core Problem (Timing: 0:45 - 1:45)
- **Visuals:** Conceptual comparison split screen showing chaotic cloud lag vs structured offline processing pipelines.
- **Script:** "Every time a cloud-based assistant parses your documents or logs a meeting transcription, it introduces security liabilities, network dependencies, and thermal performance throttling on standard hardware. AuraFlow shifts this entirely to edge architecture. By targeting the Snapdragon Hexagon NPU, we capture ambient user workflows, transcriptions, and command chains without sending a single byte to the web. By staying within the secure memory boundary of Windows on ARM, users maintain control over their data while eliminating battery drain."

## Slide 3: Technical Integration & Deep Dive (Timing: 1:45 - 3:15)
- **Visuals:** Technical block diagram tracing ONNX Runtime binding pipelines to the QNN Execution Provider.
- **Script:** "Let's review the technical stack. We didn't build a basic wrapper app. AuraFlow is built with hardware-accelerated code libraries. We leveraged the Qualcomm AI Hub to obtain highly optimized, INT4-quantized variants of the Phi-3-mini instruction set and Whisper audio parsing nodes. Using ONNX Runtime, we configured direct bindings to the QNNExecutionProvider. This allows the framework to bypass high-power GPU operational modes and run inference calculations natively inside the Hexagon Tensor Processor hardware layer, achieving minimal footprint execution."
