---
title: Automatic Speech Recognition using Segments
type: templates
category: Audio/Speech Processing
cat: audio-speech-processing
order: 303
meta_title: Automatic Speech Recognition using Segments Data Labeling Template
meta_description: Template for audio transcription for automatic speech recognition segmentation use cases with Label Studio for your machine learning and data science projects.
---



<img src="/images/templates/automatic-speech-recognition-using-segments.png" alt="" class="gif-border" width="552px" height="408px" />

Listen to an audio file and segment it, then transcribe the contents of each segment in natural language, performing speech recognition using segments.

## Interactive Template Preview

<div id="main-preview"></div>

## Labeling Configuration

```html
<View>
  <Labels name="labels" toName="audio">
    <Label value="Speech" />
    <Label value="Noise" />
  </Labels>
  <AudioPlus name="audio" value="$audio"/>
  <TextArea name="transcription" toName="audio"
            rows="2" editable="true"
            perRegion="true" required="true" />
</View>
```

## About the labeling configuration

All labeling configurations must be wrapped in [`View`](/tags/view.html) tags.

```html
<View>
    <!--Use the Labels control tag to allow annotators to highlight portions
    of the audio that represent different types of noise-->
  <Labels name="labels" toName="audio">
    <Label value="Speech" />
    <Label value="Noise" />
  </Labels>
<!--Use the AudioPlus object tag to display a waveform of audio that can be labeled-->
  <AudioPlus name="audio" value="$audio"/>
<!--Use the TextArea control tag to prompt annotators to provide a transcript-->
  <TextArea name="transcription" toName="audio"
            rows="2" editable="true"
            perRegion="true" required="true" />
</View>
```


## Enhance this template

## Related tags

- [AudioPlus](/tags/audioplus.html)
- [Audio](/tags/audio.html)
- [Labels](/tags/labels.html)
- [TextArea](/tags/textarea.html)