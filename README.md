# Video Transcribing and Translation with subtitling
Video transcriber and translator using Amazon Translate, Transcribe and Polly

Inspired by AWS Machine Learning Blog: [Create video subtitles with translation using machine learning]

## Amazon Transcribe
[Amazon Transcribe] uses advanced deep learning technologies to recognize speech in audio files or video files and transcribe them into text.

## Amazon Translate
[Amazon Translate] is neural machine translation service that delivers fast, high-quality, and affordable language translation. It uses deep learning models to deliver more accurate and more natural sounding translations.

## Amazon Polly
[Amazon Polly] is a cloud service that leverages AI/ML technology to synthesize text into lifelike speech.

## Prerequisite
- Python 2.7.15
- ImageMagic
- s3 bucket

## Python Packages
```sh
$ pip install awscli
$ pip install boto3
$ pip install requests
$ pip install moviepy
``` 

## How to use

#### For help and argument descriptions check help section

```sh
$ python translatevideo.py -h
```

#### For generating only srt files with translations

```sh
python translatevideo.py \
       -r us-east-1 \
       -ib test-transcript-er \
       -if hiroshima-speech-edited.mp4 \
       -ol es de
```

#### For generating audio/video files along with translations and subtitle

```sh
python translatevideo.py \
       -r us-east-1 \
       -ib test-transcript-er \
       -if hiroshima-speech-edited.mp4 \
       -ol es de \
       -av true \
       -ofn edited \
       -ob test-transcript-er \
       -oft mp4
```

#### Supported Translations
- es - Spanish
- de - German
- cmn - Chinese, Mandarin
- da - Danish
- nl - Dutch
- fr - French
- is - Icelandic
- it - Italian
- ja - Japanese
- ko - Korean
- nb - Norwegian
- pl - Polish
- pt - Portuguese
- ro - Romanian
- ru - Russian
- sv - Swedish
- tr - Turkish
- cy - Welsh

## Contribute

Contributions are welcome, be it feedback, bug reports, documentation, translation, research or code. Feel free to work
on any of the [open issues], just leave a comment that you're working on one to avoid duplicated work.

## Do you have further questions or feedback or having problems?

Feel free to open an issue on our issue tracker, but please:
- Provide details to reproduce the issue
- Traceback / Logs would be helpful
File an issue at https://github.com/md-farhan-memon/video-translator-amazon-translate/issues/new


[Create video subtitles with translation using machine learning]: <https://aws.amazon.com/blogs/machine-learning/create-video-subtitles-with-translation-using-machine-learning/>
[Amazon Transcribe]: <https://docs.aws.amazon.com/transcribe/latest/dg/what-is-transcribe.html>
[Amazon Translate]: <https://docs.aws.amazon.com/translate/latest/dg/what-is.html>
[Amazon Polly]: <https://docs.aws.amazon.com/polly/latest/dg/what-is.html>
[open issues]: <https://github.com/md-farhan-memon/video-translator-amazon-translate/issues?utf8=%E2%9C%93&q=is%3Aissue+is%3Aopen+>
