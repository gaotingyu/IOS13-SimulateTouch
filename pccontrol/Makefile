export THEOS_DEVICE_IP = 192.168.0.6

include $(THEOS)/makefiles/common.mk

TWEAK_NAME = pccontrol

pccontrol_FILES = Tweak.xm SocketServer.xm Touch.xm Screen.xm Task.xm Process.xm AlertBox.xm Common.xm Record.xm Play.xm Window.xm Popup.xm TemplateMatch.xm ScreenMatch.xm Toast.xm Image.xm ColorPicker.xm UIKeyboard.xm DeviceInfo.xm
pccontrol_CFLAGS = -Wno-error -Wno-module-import-in-extern-c -fobjc-arc
pccontrol_FRAMEWORKS = UIKit opencv2 AssetsLibrary AVFoundation CoreMedia CoreVideo
pccontrol_ARCHS = arm64e arm64 armv7
#pccontrol_CCFLAGS = -std=c++11

pccontrol_PRIVATE_FRAMEWORKS = IOKit
pccontrol_LIBRARIES = substrate

include $(THEOS_MAKE_PATH)/tweak.mk

after-install::
	install.exec "killall -9 SpringBoard"

