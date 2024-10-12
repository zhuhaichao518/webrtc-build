# webrtc-build

webrtc build scripts

## Build Tools

Use dart-lang to build cross-platform compilation [tools](tools).

python3 run.py build macos_arm64 --debug

# Windows
代理不行的时候
gclient llvm版本不对：手动下载然后拷贝到src\third_party\llvm-build\Release+Asserts
创建文件 cr_build_revision
内容：llvmorg-19-init-8091-gab037c4f-1（gclient时的版本）
然后按照libwebrtc的教程去build. 不要再跑gclient了 否则build文件夹会有报错信息

gclint
LASTCHANGE.committime 拷贝到 webrtc\src\build\util
自己cd过去build

gn gen G:\\webrtc_new\\webrtc-build\\build\\_build\\windows_x86_64\\debug\\webrtc --args="target_os=\"win\" target_cpu=\"x64\" is_component_build=false is_clang=true is_debug=true rtc_use_h264=true ffmpeg_branding=\"Chrome\" rtc_include_tests=false rtc_build_examples=false libwebrtc_desktop_capture=true" --ide=vs2022

git clone https://github.com/webrtc-sdk/libwebrtc
自己去仓库里走一遍
gn gen G:\\webrtc_new\\webrtc-build\\build\\_build\\windows_x86_64\\debug\\webrtc --args="target_os=\"win\" target_cpu=\"x64\" is_component_build=false is_clang=true is_debug=true rtc_use_h264=true ffmpeg_branding=\"Chrome\" rtc_include_tests=false rtc_build_examples=false libwebrtc_desktop_capture=true" --ide=vs2022