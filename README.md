# MySpeech2Myspeech

> Takes what you say and makes it sound unbearably sophisticated.

A Google Colab pipeline that:
1. **Transcribes** a voice message using OpenAI Whisper
2. **Rewrites** the text in pompous, 19th-century academic German using Claude
3. **Synthesizes** the result back in your own voice using XTTS v2

## Demo

Input:
> "Hey, also ich habe heute einige Zeit damit verbracht, dass ich an so einem Programm programmiert habe..."

Output:
> "In der zeitlichen Konfiguration des heutigen Tages habe ich mich der elaborierten Konzeptualisierung und subsequenten Implementation eines computertechnologischen Instrumentariums gewidmet..."

## Requirements

- Google Colab with GPU (T4 is sufficient)
- An [Anthropic API Key](https://console.anthropic.com/)
- A voice message (`message.wav`)
- 1–3 short voice samples of yourself for cloning (`*.wav`, ~10–30 sec each)

## Usage

1. Open the notebook in Colab
2. Add your Anthropic API key to Colab Secrets as `claude-key`
3. Run the installation cell
4. Upload your `message.wav` and voice samples when prompted
5. Run the pipeline cells

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/clemens71/REPONAME/blob/main/fancy_voice.ipynb)

## Tech Stack

- [OpenAI Whisper](https://github.com/openai/whisper) — speech-to-text
- [Anthropic Claude](https://www.anthropic.com/) — text rewriting
- [Coqui XTTS v2](https://github.com/coqui-ai/TTS) — voice cloning TTS
- [pydub](https://github.com/jiaaro/pydub) — audio processing

## Notes

- The notebook also contains an alternative version using [Qwen2.5-3B](https://huggingface.co/Qwen/Qwen2.5-3B-Instruct) as a local LLM instead of Claude