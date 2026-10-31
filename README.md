VoiceGuard AI — Complete Upgrade

Features

Existing pretrained voice detector: garystafford/wav2vec2-deepfake-voice-detector

Audio playback, waveform and signal characteristics

Model score breakdown and limitations

Downloadable PDF report

Session-only history with clear-history control

Optional speech-to-text using openai/whisper-tiny

Privacy notice and temporary-file cleanup

Windows setup

Extract this ZIP.

Open the extracted folder and check that app.py and requirements.txt are visible.

Click File Explorer's address bar, type cmd, press Enter.

Run: python -m pip install -r requirements.txt python -m streamlit run app.py

Open the localhost URL shown in the terminal (usually http://localhost:8501).

The first detector run downloads model files. Transcript generation downloads a second model. Keep internet on; these models require disk space and RAM.



Public deployment

Upload app.py, requirements.txt, and README.md to a GitHub repository.

Visit https://share.streamlit.io/ and sign in with GitHub.

Create app, choose repository, branch and app.py, then deploy.

Model downloads can make free cloud deployment slow or exceed available RAM. If it fails, use a host with more RAM or a managed inference endpoint.

Never commit API keys or private audio to a public repository.

Interpretation and privacy

Scores are raw softmax outputs, not calibrated probabilities. The model may not generalize to every language, speaker, device, codec, or synthesis method. False positives and false negatives are possible. Results are not proof of authenticity or identity. The app uses temporary files for decoding and attempts to delete them after processing. Session history is held in Streamlit session state, not written to a database by this code. This does not guarantee zero retention by the hosting provider, browser, OS, or network. Only upload recordings you have permission to analyze. Transcript uses Whisper Tiny, may mishear or hallucinate words, and is not used as proof of authenticity. Review the detector model card and license before public/commercial use: https://huggingface.co/garystafford/wav2vec2-deepfake-voice-detector

