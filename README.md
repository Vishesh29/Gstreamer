# Gstreamer

sudo apt-get install libgstreamer1.0-dev libgstreamer-plugins-base1.0-dev libgstreamer-plugins-bad1.0-dev gstreamer1.0-plugins-base gstreamer1.0-plugins-good gstreamer1.0-plugins-bad gstreamer1.0-plugins-ugly gstreamer1.0-libav gstreamer1.0-doc gstreamer1.0-tools gstreamer1.0-x gstreamer1.0-alsa gstreamer1.0-gl gstreamer1.0-gtk3 gstreamer1.0-qt5 gstreamer1.0-pulseaudio

pkg-config --cflags --libs gstreamer-1.0

git clone https://gitlab.freedesktop.org/gstreamer/gst-docs

cd Downloads/gst-docs/examples/tutorials

gcc basic-tutorial-1.c -o basic-tutorial-1 `pkg-config --cflags --libs gstreamer-1.0`

./basic-tutorial-1

gst-inspect-1.0 --gst-version     ->1.16

gst-launch-1.0 -v v4l2src ! decodebin ! videoconvert ! videoscale ! videorate ! video/x-raw,framerate=1/10 ! jpegenc ! multifilesink location=snapshot-%05d.jpg


