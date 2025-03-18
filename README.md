# Audio and Image Encryption/Decryption Project

This project demonstrates encryption and decryption techniques using Python. It includes two Jupyter notebooks:

1. **Image Encryption/Decryption**: Encrypts and decrypts an image file using AES (CBC mode) with a derived key from a password.
2. **Audio Decryption and Playback**: Reads a decrypted WAV audio file, visualizes its waveform, and plays it back.

The project leverages cryptographic libraries like `pycryptodome` and audio processing libraries like `scipy` and `sounddevice`.


## Usage

### Image Encryption/Decryption
- **Notebook**: `image_encryption_decryption.ipynb`
- **Description**: Encrypts an image file (`Warframe0002.jpg`) using AES in CBC mode with a key derived from a password via PBKDF2, then decrypts it.
- **Steps**:
  1. Open the notebook in Jupyter.
  2. Ensure the `pics/Warframe0002.jpg` file exists in the specified directory.
  3. Run all cells:
     - A 256-bit AES key is generated using the password `"mysecret"` and a random salt.
     - The image is encrypted to `encrypt.jpg.enc`.
     - The encrypted file is decrypted to `decyptImage.jpg` (saved to the default path: `c:\Users\madhu\Documents\image\decrypt\decrypt.jpg` unless modified).
- **Output**:
  - The derived key is printed (e.g., `b'dP\xd4\x1d...'`).
  - Encrypted and decrypted files are created in the specified locations.

### Audio Decryption and Playback
- **Notebook**: `audio_decryption_playback.ipynb`
- **Description**: Reads a decrypted WAV file, plots its waveform, and plays the audio.
- **Steps**:
  1. Open the notebook in Jupyter.
  2. Ensure `decrypted_audio_file.wav` exists in the root directory (this file is assumed to be pre-decrypted).
  3. Run all cells:
     - The audio data is read using `scipy.io.wavfile`.
     - A plot of the waveform is displayed (titled "Decrypted Audio Plot").
     - The audio is played using `sounddevice`.
- **Output**:
  - A matplotlib plot of the audio waveform.
  - Audio playback through your system's speakers.

## Dependencies
Install these packages using `pip`:
- `pycryptodome` (for AES encryption)
- `scipy` (for WAV file handling)
- `numpy` (for numerical operations)
- `matplotlib` (for plotting)
- `sounddevice` (for audio playback)

```bash
pip install pycryptodome scipy numpy matplotlib sounddevice
