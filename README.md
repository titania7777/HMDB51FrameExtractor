# HMDB51 Frame Extractor with ray
this frame extractor supports optical flow(dense optical flow) also

## Requirements

*   ray>=0.8.7
*   opencv-python>=4.4.0.44

## Usage
example
```
$ wget --no-check-certificate http://serre-lab.clps.brown.edu/wp-content/uploads/2013/10/hmdb51_org.rar
$ mkdir HMDB51_videos
$ unrar e hmdb51_org.rar ./HMDB51_videos
$ cd ./HMDB51_videos
$ for file in *.rar; do unrar x "$file"; rm -rf "$file"; done
$ cd ..
$ python frame_extractor.py --videos-path ./HMDB51_videos --frames-path ./HMDB51_frames --num-cpus 8
```

extract only frames
```
frame_extractor.py --videos-path /path/to/videos --frames-path /path/to/save --num-cpus /number/of/cpus
```

extract only optical flows
```
frame_extractor.py --videos-path /path/to/videos --flows-path /path/to/save --num-cpus /number/of/cpus --flow-mode
```