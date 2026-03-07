# llm-audio

Single-header C++17 library for OpenAI Whisper transcription, translation, and TTS.

- Single-header C++17, namespace `llm`, stb-style `#ifdef LLM_LLM_AUDIO_IMPLEMENTATION` guard
- MIT License — Mattbusel, 2026
- No `/WX` in CMakeLists (avoids C4702 on MSVC)
- Examples use `std::getenv("OPENAI_API_KEY")` for credentials
