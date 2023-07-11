# shodan_speaks

## Overview

System Shock 2 tribute test for Shodan face animation with audio logs.

## Tools

Make Art Talk - Wav2Lip Lip Sync Deepfake Google Collab Tutorial :

https://www.youtube.com/watch?v=Ic0TBhfuOrA

## Results

-Video 1: https://www.youtube.com/watch?v=hYgrpObU0v0

-Video 2: https://www.youtube.com/watch?v=AkpKw2BJQOo

-Shodan face detection: 
```
    -🟢cosplay photos have faces detected often
    -🔴game screenshots and drawings with Shodan kept failing
```
## Notes

-If you encounter error
```shell
cp: cannot stat '/content/gdrive/MyDrive/Wav2Lip/wav2lip_gan.pth': No such file or directory
```
when running
```shell
!cp -ri "/content/gdrive/MyDrive/Wav2Lip/wav2lip_gan.pth" /content/Wav2Lip/checkpoints/
```
make sure the file was downloaded correctly and modify the folder name punctuation to be
```shell
!cp -ri "/content/gdrive/MyDrive/Wav2lip/wav2lip_gan.pth" /content/Wav2Lip/checkpoints/
```

-If you encounter error
```python
TypeError: mel() takes 0 positional arguments but 2 positional arguments (and 3 keyword-only arguments) were given
```
when running
```python
!cd Wav2Lip && python inference.py --checkpoint_path checkpoints/wav2lip_gan.pth --face "../sample_data/test.mp4" --audio "../sample_data/test.wav"
```
then run 
```python
pip install librosa==0.8.0
```
as suggested from https://github.com/Rudrabha/Wav2Lip/issues/471#issuecomment-1512138768

-To reset the environment do the following in the navbar:
`Run > Reset all runtimes...``
as suggested from https://stackoverflow.com/a/47440626

-There is a periodic sound effect in the background that causes the face to talk. 
This sound could potentially be removed with a sound filter to make the lip sync more accurate.