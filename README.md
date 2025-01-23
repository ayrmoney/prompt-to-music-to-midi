# prompt-to-music-to-midi
Experimental prototype for Text to Music to MIDI generation, built using open source models.

> Prompt "Drum loop of..." → Base Model (MusicGen-Large / MusicGen-Small) → Drum loop audio in .wav → Convert to MIDI (OaF-Drums)

Using MusicGen-Small model is free using the HuggingFace inference API, but you need to have a HuggingFace account and get an API token. The MusicGen-Large model is not available in Inference API, but you can deploy it by creating an Endpoint in HuggingFace (you may refer to my fork for the `handler`: https://huggingface.co/ayrmoney/musicgen-large).

If you want to try out the prototype, some points to keep in mind:
1. Requires python 3.7 (**NOT** higher) since the magenta model (OaF-Drums) depends on it & hasn't been updated (creating a conda env works).
2. Install all dependencies refering to the first block of the notebook.
3. Replace `HF_TOKEN` in `Pipeline V0.ipynb` (second block) with your own huggingface token.