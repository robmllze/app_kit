
### CREATING SNIPPETS IN VS CODE

https://code.visualstudio.com/docs/editor/userdefinedsnippets

### READING A WEB FILE
```dart
import 'dart:html';

Future<String> readWebFile(final String path) {
  return Future<String>(() async {
    final _request = await HttpRequest.request(path);
    final _response = _request.response;
    return _response as String;
  });
}
```

### WRITING TO A FILE
```dart
Future<void> writeToFile(final String file, final String data) {
  return File(file).openWrite()
  ..write(data)
  ..close();
}
```