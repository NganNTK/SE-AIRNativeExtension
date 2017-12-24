## Build

Build command:

```bash
$adt -package -target ane VolumeController.ane extension.xml -swc VolumeController.swc -platform Android-ARM -C android . -platform default -C default . -platform iPhone-ARM -C ios .
```

### 1. Lưu ý với bản build AS3
Bản build AS3 cần có swf version nhỏ hơn hoặc bằng 14 bằng cách bổ sung compiler arguments:
``` 
    -swf-version=14
``` 
Nếu không sẽ xuất hiện lỗi sau khi build:
>Invalid swc file. The extension NameSpace requires the SWF version to be 14 or lower

### 2. Lưu ý với bản build iOS
>Lưu ý: Đảm bảo rằng bản build iOS phải dựa trên kiến trúc armv7 và arm64.

```bash
$lipo -info ./ios/libIOSVolumeLib.a
Architectures in the fat file: libANE-VolumeController.a are: armv7 arm64 
```

Nếu output là
```bash
$lipo -info ./ios/libIOSVolumeLib.a
Architectures in the fat file: libANE-VolumeController.a are: i386 x86_64 
```

Khi build bằng AIR SDK sẽ sinh ra lỗi:

```bash
$adt -package -target ane VolumeController.ane extension.xml -swc VolumeController.swc -platform Android-ARM -C android . -platform default -C default . -platform iPhone-ARM -C ios .
Error: Apple App Store allows only universal applications. "libIOSVolumeLib.a" is not a universal binary. Please change build settings in Xcode project to "Standard Architecture" to create universal library/framework.
```




