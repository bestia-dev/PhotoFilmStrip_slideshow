<!-- markdownlint-disable MD041 -->
[//]: # (auto_md_to_doc_comments segment start A)

# PhotoFilmStrip_slideshow  

[//]: # (auto_cargo_toml_to_md start)

**Slideshows from my travels are easy to make with PhotoFilmStrip**  
***version: 1.0.0 date: 2024-07-19 author: [bestia.dev](https://bestia.dev) repository: [GitHub](https://github.com/bestia-dev/PhotoFilmStrip_slideshow)***  

[//]: # (auto_cargo_toml_to_md end)

 ![pre_alpha](https://img.shields.io/badge/pre_alpha-red)

 [![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/bestia-dev/PhotoFilmStrip_slideshow/blob/master/LICENSE)
 ![PhotoFilmStrip_slideshow](https://bestia.dev/webpage_hit_counter/get_svg_image/275848160.svg)

Hashtags: #tutorial #slideshow #photofilmstrip  
My projects on GitHub are more like a tutorial than a finished product: [bestia-dev tutorials](https://github.com/bestia-dev/tutorials_rust_wasm).

## Workflow

[PhotoFilmStrip](https://www.photofilmstrip.org/en/features/) has a great simple UI to make slideshows. I use it to make videos of my travels.  
First I choose a song as a background. That defines the duration of the video.  
Then I add around 40 images. PhotoFilmStrip adds some random animations to every image. That's ok.  
The duration of the image is automatically calculated to fill the song duration. Great.  
I then add subtitles to every image. Eventually, I can modify the animation and change the order of the images.  
The UI is so easy, that even my wife likes to use it.  
Finally, PhotoFilmStrip renders the slideshow as a mp4 file and the subtitles as a srt file. That is fine, but...

I prefer to have the subtitles embedded in the video, so every video player will show them exactly how I want it. I encountered a lot of odd problems with separated `srt` files in different video players online and offline.  
I use `ffmpeg` in Debian to do that.

```bash
ffmpeg -i "MexicoCity.mkv" -vf subtitles="MexicoCity.srt:force_style='FontSize=32'" "MexicoCity_srt.mp4"
```

To install `ffmpeg`:

```bash
sudo apt install ffmpeg
```

## Open-source and free as a beer

My open-source projects are free as a beer (MIT license).  
I just love programming.  
But I need also to drink. If you find my projects and tutorials helpful, please buy me a beer by donating to my [PayPal](https://paypal.me/LucianoBestia).  
You know the price of a beer in your local bar ;-)  
So I can drink a free beer for your health :-)  
[Na zdravje!](https://translate.google.com/?hl=en&sl=sl&tl=en&text=Na%20zdravje&op=translate) [Alla salute!](https://dictionary.cambridge.org/dictionary/italian-english/alla-salute) [Prost!](https://dictionary.cambridge.org/dictionary/german-english/prost) [Nazdravlje!](https://matadornetwork.com/nights/how-to-say-cheers-in-50-languages/) 🍻

[//bestia.dev](https://bestia.dev)  
[//github.com/bestia-dev](https://github.com/bestia-dev)  
[//bestiadev.substack.com](https://bestiadev.substack.com)  
[//youtube.com/@bestia-dev-tutorials](https://youtube.com/@bestia-dev-tutorials)  

[//]: # (auto_md_to_doc_comments segment end A)
