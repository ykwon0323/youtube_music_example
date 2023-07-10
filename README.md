# YouTube 음원 추출기
참고
https://bebutae.tistory.com/17


~~~ shell
# youtube 음원추출을 위한 라이브러리
pip install youtube_dl

# GUI 만들어주는 라이브러리 tkinter
pip install tk

# webm -> mp3 변환 라이브러리
pip install ffmpeg 이거했는데 안돼서

brew install ffmpeg 이거 하니깐 되었음
~~~





## Error

### 1
~~~ log
Unable to download webpage: <urlopen error [SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed: unable to get local issuer certificate (_ssl.c:1002)>
~~~

Solve
Once upon a time I stumbled with this issue. If you're using macOS go to Macintosh HD > Applications > Python3.6 folder (or whatever version of python you're using) > double click on "Install Certificates.command" file. :D

### 2
How To Fix yt_dlp Error: Unable to extract uploader id

Solve
~~~ shell
python3 -m pip install --force-reinstall https://github.com/yt-dlp/yt-dlp/archive/master.tar.gz
~~~

~~~ python
import yt_dlp as youtube_dl
~~~

~~~ shell
python3 -m pip install yt-dlp==2023.02.17.334
~~~ 

### 3 
~~~ log
ffprobe or avprobe not found. Please install one
~~~

Make sure you have the latest version for youtube-dl:
sudo youtube-dl -U

After that you can solve this problem by installing the missing ffmpeg.

Ubuntu and debian:
sudo apt-get install ffmpeg

macOS:
brew install ffmpeg

Windows:
choco install ffmpeg