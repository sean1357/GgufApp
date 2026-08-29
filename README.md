📋 GGUF Model Manager - Program Summary
🎯 Purpose
A Windows Forms desktop application for managing and interacting with GGUF format AI models (LLaMA, DeepSeek, Qwen, etc.). It allows users to download models from Hugging Face, manage them locally, and chat with them using LLamaSharp.

🔧 Key Features
1. Model Management (Settings Tab)
Hugging Face Integration: Search and scan repositories for GGUF files

Download Models: Download GGUF models directly from Hugging Face

Local Browsing: Browse local folders to add existing GGUF/BIN/ONNX models

GPU Detection: Automatically detects GPU (AMD/NVIDIA) with VRAM info

Model Search: Quick search filters for popular model families:

All Models, Llama, DeepSeek, Qwen, Gemma, Mistral, Phi, Mixtral, Falcon, GPT-NeoX, CodeLlama, Vicuna, WizardLM, Zephyr, StarCoder, Granite

2. Chat Interface (Chat Tab)
Prompt Input: Rich text box for entering questions/prompts

Generate Responses: Send prompts to loaded models and get AI responses

Live Streaming: Responses appear incrementally as they're generated

Model Info Panel: Shows currently loaded model and token count

Real-time Clock: Displays current time

3. Advanced Settings
Context Size: Adjust the model's context window (512-32768 tokens)

Temperature: Control response randomness (0-2)

Repetition Penalty: Prevent repetitive outputs (1-2)

Top P: Nucleus sampling for response diversity

Max Tokens: Limit response length

4. Visual Features
Dark/Light Themes: Toggle between dark and light modes

Button Hover Effects: Visual feedback on button hover

Progress Bar: Download progress indicator

Status Log: Real-time status updates

Professional UI: Clean, modern interface with proper anchoring

🛠️ Technical Stack
Component	Technology
Framework	Windows Forms (.NET)
LLM Engine	LLamaSharp (C# bindings for llama.cpp)
GPU Support	ComputeSharp (DirectX 12/11, Vulkan)
API Client	Hugging Face REST API
GPU Detection	WMI + Registry
HTTP Client	HttpClient with proxy support
JSON Parsing	System.Text.Json
📁 File Structure
text
GgufApp/
├── Form1.cs              # Main logic (500+ lines)
├── Form1.Designer.cs     # UI layout (400+ lines)
└── Namespace: GgufApp
🚀 Core Workflows
Download Model Flow
Enter Hugging Face repo (e.g., TheBloke/Llama-2-7B-GGUF)

Click "Scan" → Lists all .gguf files

Select a file → "Download" button enabled

Choose save location → Progress bar shows download status

Chat Flow
Browse/Download a .gguf model file

Select model from dropdown

Enter prompt in chat box

Click "Generate" → Model loads (if not already)

Response streams in real-time

Token counter shows usage

Theme Toggle
Click "🌓 Theme" → Switches between dark/light

All UI elements update instantly

State persists until toggled again
