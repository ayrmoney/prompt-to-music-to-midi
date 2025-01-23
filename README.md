# prompt-to-music-to-midi
Experimental prototype for Text to Music to MIDI generation, built using open source models.

![image](https://github.com/user-attachments/assets/f9c4da0b-05a6-4d94-9653-4056f3fd3532)

> Prompt "Drum loop of..." → Base Model (MusicGen-Large / MusicGen-Small) → Drum loop audio in .wav → Convert to MIDI (OaF-Drums)

Using MusicGen-Small model is free using the HuggingFace inference API, but you need to have a HuggingFace account and get an API token. The MusicGen-Large model is not available in Inference API, but you can deploy it by creating an Endpoint in HuggingFace (you may refer to my fork for the `handler`: https://huggingface.co/ayrmoney/musicgen-large).

If you want to try out the prototype, some points to keep in mind:
1. Requires python 3.7 (**NOT** higher) since the magenta model (OaF-Drums) depends on it & hasn't been updated (creating a conda env works).
2. Install all dependencies refering to the first block of the notebook.
3. Replace `HF_TOKEN` in `Pipeline V0.ipynb` (second block) with your own huggingface token.

### Example:

Prompt: "Cinematic taiko drum loop with a release tail at 125 BPM. Drum Loops, Japanese Traditional"

MusicGen-Large output (uploaded as .mp4 since GitHub doesn't support .mp3 or .wav):

https://github.com/user-attachments/assets/40569f9e-ab48-479f-a8a3-6c65b10dce6d

OaF-Drums (MIDI file, but played with Clean Back drums):

https://github.com/user-attachments/assets/0ea44875-511f-4e91-aba2-da89104646b2
