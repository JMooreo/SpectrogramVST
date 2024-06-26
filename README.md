Demo Video (click to view on YouTube)

[![Demo video](images/example_reassignment.gif)](https://www.youtube.com/watch?v=_9qX5OIP9nE)


# Context / Background
- I was inspired by this [video](https://www.youtube.com/watch?v=8J4LE9UpxYU) from Au5 (Austin) which talks about Spectrograms and the problems with FFT resolution in the low end. Austin goes on to talk about the [Spectral Reassignment method](https://arxiv.org/pdf/0903.3080) which outlines the math and equations for reassigning the energy of the frequency bands closer to the center of mass.
- [This 2016 paper](https://ltfat.org/notes/ltfatnote044.pdf) explains how to do it in a real-time case
- [Librosa](https://librosa.org/doc/latest/generated/librosa.reassigned_spectrogram.html#librosa.reassigned_spectrogram) is a Python library for audio processing that implements reassigned spectrograms
- I'm doing this becuase I want more C++ and desktop app development experience under my belt.

# Why it matters
As an EDM producer myself, I have always struggled with this problem with spectrograms. The trade-off between time and frequency resolution has been solved (since 2009!) but lots of industry-level, $100+ plugins still only provide basic FFT spectrograms which don't really help visualize spectral information.
Quality tools like this are really important for producers who literally can't hear the frequencies or whose low end it misrepresented because the headphones or speakers they use can't produce them accurately. Because of that, I plan to build this and give it away for free, as long as that doesn't conflict with the JUCE Terms of Service.


# Installation
The source code can be cloned built with [Projucer](https://juce.com/) in your favorite IDE.
I plan to create builds for download in the future

# To-do
## MVP
- [X] Take at least one channel of input and draw a spectrogram on the screen
- [X] Use a log scale to display the spectrogram
- [X] Use the reassignment equations to redistribute the energy of the original FFT
- [X] It builds and runs in a Ableton 10 Standard

## Nice to have
- [X] Add de-speckling
- [X] Add FFT size dropdown
- [ ] Resizable screen
- [ ] Hover to view frequency and note name
