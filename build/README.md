## Build

Build command:

```bash
$adt -package -target ane VolumeController.ane extension.xml -swc VolumeController.swc -platform Android-ARM -C android . -platform default -C default . -platform iPhone-ARM -C ios .
```

>Lưu ý: Đảm bảo rằng bản build iOS phải dựa trên kiến trúc armv7 và arm64.

```bash
$lipo -info ./ios/libIOSVolumeLib.a
Architectures in the fat file: libANE-VolumeController.a are: armv7 arm64 
```

Nếu output là
```bash
$lipo -info ./ios/libIOSVolumeLib.a
Architectures in the fat file: libANE-VolumeController.a are: armv7 arm64 
```

Khi build bằng AIR SDK sẽ sinh ra lỗi:

```bash
$adt -package -target ane VolumeController.ane extension.xml -swc VolumeController.swc -platform Android-ARM -C android . -platform default -C default . -platform iPhone-ARM -C ios .
Error: Apple App Store allows only universal applications. "libIOSVolumeLib.a" is not a universal binary. Please change build settings in Xcode project to "Standard Architecture" to create universal library/framework.
```




