
# ED Flutter Screen Recorder

Screen recorder plugin for Flutter. It currently only works on Android operating system. IOS operating system will be supported in the near future.


[![pubdev](https://img.shields.io/badge/pub-de__screen__recorder-blue)]()

[!["Buy Me A Coffee"](https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png)](https://www.buymeacoffee.com/erendemir)
## Usage/Examples

```dart
import 'package:screen_recorder/screen_recorder.dart';

ScreenRecorder? screenRecorder;
Map<String, dynamic>? _response;

@override
void initState() {
    super.initState();
    screenRecorder = ScreenRecorder();
}

Future<void> startRecord({required String fileName}) async {
    var startResponse = await screenRecorder?.startRecordScreen(
        fileName: "Eren",
        audioEnable: false,
    );
}
Future<void> stopRecord() async {
    var stopResponse = await screenRecorder?.stopRecord();
}

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text("Screen Recording Debug"),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            Text("File: ${(_response?['file'] as File?)?.path}"),
            Text("Status: ${(_response?['success']).toString()}"),
            Text("Event: ${_response?['eventname']}"),
            Text("Progress: ${(_response?['progressing']).toString()}"),
            Text("Message: ${_response?['message']}"),
            Text("Video Hash: ${_response?['videohash']}"),
            Text("Start Date: ${(_response?['startdate']).toString()}"),
            Text("End Date: ${(_response?['enddate']).toString()}"),
            ElevatedButton(onPressed: () => startRecord(fileName: "eren"), child: const Text('START RECORD')),
            ElevatedButton(onPressed: () => stopRecord(), child: const Text('STOP RECORD')),
          ],
        ),
      ),
    );
  }
```

  
## Resources used within the plugin

HBRecorder
Lightweight screen and audio recording Android library. 
[URL](https://github.com/HBiSoft/HBRecorder)

Watcher

A file system watcher. [URL](https://pub.dev/packages/watcher)

UUID

Simple, fast generation of RFC4122 UUIDs. [URL](https://pub.dev/packages/uuid)

Path Provider

A Flutter plugin for finding commonly used locations on the filesystem. [URL](https://pub.dev/packages/path_provider)


  
## Features

- Custom Audio Record
- Custom Video Frame
- Custom File Name


  
## Feedback

If you have any feedback, please contact us at erndemir.1@gmail.com.

  
## Roadmap

- IOS operating system support.

- Code optimization.

  