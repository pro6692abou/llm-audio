# llm-audio

Whisper transcription, translation, and TTS in a single C++ header.

## Features
- Transcribe audio files (mp3, wav, m4a, ogg, webm) via OpenAI Whisper
- Translate audio to English
- Text-to-speech with 6 voices and 4 formats
- Single-header, C++17, namespace `llm`

## Quick Start
```cpp
#define LLM_AUDIO_IMPLEMENTATION
#include "llm_audio.hpp"

llm::TranscribeConfig cfg{ .api_key = "sk-..." };
auto result = llm::transcribe("audio.mp3", cfg);
std::cout << result.text;
```

## API
```cpp
TranscribeResult transcribe(const std::string& filepath, const TranscribeConfig&);
TranscribeResult transcribe_bytes(const std::vector<uint8_t>&, const std::string& filename, const TranscribeConfig&);
void             text_to_speech(const std::string& text, const std::string& output_path, const TTSConfig&);
std::vector<uint8_t> text_to_speech_bytes(const std::string& text, const TTSConfig&);
```

## Build
```bash
cmake -B build && cmake --build build
```
Requires libcurl (vcpkg: `vcpkg install curl`).

## License
MIT — Mattbusel, 2026

## See Also

| Repo | Purpose |
|------|---------|
| [llm-stream](https://github.com/Mattbusel/llm-stream) | SSE streaming |
| [llm-cache](https://github.com/Mattbusel/llm-cache) | Response caching |
| [llm-cost](https://github.com/Mattbusel/llm-cost) | Token cost estimation |
| [llm-retry](https://github.com/Mattbusel/llm-retry) | Retry + circuit breaker |
| [llm-format](https://github.com/Mattbusel/llm-format) | Markdown/code formatting |
| [llm-embed](https://github.com/Mattbusel/llm-embed) | Embeddings + cosine similarity |
| [llm-pool](https://github.com/Mattbusel/llm-pool) | Connection pooling |
| [llm-log](https://github.com/Mattbusel/llm-log) | Structured logging |
| [llm-template](https://github.com/Mattbusel/llm-template) | Prompt templates |
| [llm-agent](https://github.com/Mattbusel/llm-agent) | Tool-use agent loop |
| [llm-rag](https://github.com/Mattbusel/llm-rag) | Retrieval-augmented generation |
| [llm-eval](https://github.com/Mattbusel/llm-eval) | Output evaluation |
| [llm-chat](https://github.com/Mattbusel/llm-chat) | Multi-turn chat |
| [llm-vision](https://github.com/Mattbusel/llm-vision) | Vision/image inputs |
| [llm-mock](https://github.com/Mattbusel/llm-mock) | Mock LLM for testing |
| [llm-router](https://github.com/Mattbusel/llm-router) | Model routing |
| [llm-guard](https://github.com/Mattbusel/llm-guard) | Content moderation |
| [llm-compress](https://github.com/Mattbusel/llm-compress) | Prompt compression |
| [llm-batch](https://github.com/Mattbusel/llm-batch) | Batch processing |
| [llm-audio](https://github.com/Mattbusel/llm-audio) | Audio transcription/TTS |
| [llm-finetune](https://github.com/Mattbusel/llm-finetune) | Fine-tuning jobs |
| [llm-rank](https://github.com/Mattbusel/llm-rank) | Passage reranking |
| [llm-parse](https://github.com/Mattbusel/llm-parse) | HTML/markdown parsing |
| [llm-trace](https://github.com/Mattbusel/llm-trace) | Distributed tracing |
| [llm-ab](https://github.com/Mattbusel/llm-ab) | A/B testing |
| [llm-json](https://github.com/Mattbusel/llm-json) | JSON parsing/building |
