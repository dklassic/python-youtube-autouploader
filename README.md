# python-youtube-autouploader
A super dirty implementation of Python-based YouTube automatic uploader

## Overview
This is a very dirty implementation of YouTube autouploader. A by product of a current project I'm working with.

The use case of this particular script is to automatically upload:

- Video file
- Thumbnail
- Multilanguage title and description
- Multilanguage subtitle

User simply needed to indicate the name of the file, the script will automatically locate the existence of other optional file (.srt for sub; .jpg for thumbnail), and seek title and description in an Excel(.xlsx).

Example:

```
python youtubeUpload.py --name="test"
```

in this case, the uploader will automatically seek:

- test.mp4 for video upload
- test.xlsx for title and description
- test.[ket].srt for subtitle
- test.jpg for thumbnail

Since this is build on my personal project, currently the script is hard coded with zh_Hant, th srt setting, but it should be fairly easy for others to modify for their own usage.

Also note the cells of Excel spreadsheet read by the script, which B8 is currently the ENG Title, and B10+B11+B12 will serve as description.
