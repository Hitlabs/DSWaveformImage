DSWaveformImage
===============

DSWaveformImage and DSWaveformImageView offer a simple drop-in solution to generate
and render waveform images from audio files in iOS.

Usage
-----

To create a UIImage:

```objc
NSURL *audioURL = [[NSBundle mainBundle] URLForResource:@"example_sound" withExtension:@"m4a"];
UIImage *waveformImage = [DSWaveformImage waveformForAssetAtURL:audioURL
                                                          color:[UIColor redColor]
                                                           size:CGSizeMake(500, 300)
                                                          scale:2.0 // retina
                                                          style:DSWaveformStyleFull];
```

To create a UIImageView:

```objc
NSURL *audioURL = [[NSBundle mainBundle] URLForResource:@"example_sound" withExtension:@"m4a"];
self.waveformImageView = [[DSWaveformImageView alloc] initWithFrame:CGRectMake(0, 0, 500, 300)];
[self.waveformImageView setAudioURL:audioURL];
```
