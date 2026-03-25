# dash-streaming-video (FFmpeg + MPEG-DASH + Apache + Dash.js)

## System Overview
This project implements an MPEG-DASH workflow:
- Download HD videos
- Transcode to 1.5 Mbps / 2 Mbps / 4 Mbps using ffmpeg
- Package into DASH MPD + .m4s segments
- Host on Apache2
- Play on client VM using Dash.js player
- Network tests using iPerf3 and Linux traffic control (tc)

## Testbed
- Server VM: 192.168.56.2 (interface enp0s9)
- Client VM: 192.168.56.3 (interface enp0s9)

## Prerequisites (Server VM)
'''bash
sudo apt update
sudo apt install -y ffmpeg apache2 iperf3

