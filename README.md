# Drummy-NSynth

Drummy-NSynth is a project that uses TensorFlow and NSynth to generate new drum sounds from existing samples based on user-defined parameters. For example, you can create a new drum hit by combining 20% of one sound, 60% of another, and 20% of a third sound. The project consists of blending audio files and using a pre-trained NSynth model to generate new sounds.

## Todo

The checkpoint size needs to be reduced using my own drum sounds so it can be used in a web app.  It was trained on 30 gigs of waves and the checkpoint is a gig.


## Project Structure

- `blend_sounds.py`: Script for generating new drum sounds using NSynth with weighted blending.
- `requirements.txt`: File listing the required Python packages.
- `samples/`: Directory containing subdirectories for different drum sounds.

## Setup

1. **Install Dependencies**:
   - Install the required Python packages using pip:
     ```sh
     pip install -r requirements.txt
     ```

2. **Download the NSynth Model**:
   - Download the pre-trained NSynth model from the Magenta GitHub repository or the official website.
   - Place the model files in the appropriate directory.

3. **Create Samples Directory**:
   - Create a `samples` directory with subdirectories for different drum sounds. For example:
     ```
     samples/
     ├── kick/
     │   ├── 909/
     │   │   └── 909.wav
     │   └── Croup/
     │       └── 909.wav
     ├── snare/
     │   ├── Acoustic/
     │   │   └── snare.wav
     │   └── Electronic/
     │       └── snare.wav
     └── ...
     ```
   - You can use your own sample library by placing your WAV files in the appropriate directories.

4. **Generate New Drum Sounds with NSynth**:
   - Run the `generate_nsynth_sound.py` script to generate new drum sounds using NSynth with weighted blending. The generated drum sound will be saved to `generated_audio.wav`:
     ```sh
     python generate_nsynth_sound.py
     ```

## Requirements

- TensorFlow
- Librosa
- Soundfile

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for details.