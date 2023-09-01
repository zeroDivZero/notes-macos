# INTRO

![Document App](/assets/DocumentApp/document-app.png)

In generated `Document` Swift file:

```swift
extension UTType {
    static var exampleText: UTType {
        UTType(importedAs: "com.example.plain-text")
    }
}
```

informs system which file type(s) this app supports. Can select from predefined or customize.

Also creates type conforming to `FileDocument` to handle reading/writing of document.

In generated `App` Swift file, entry point of app is specified. Uses `DocumentGroup` to create one window per document, allowing multiple documents opened at once.

In `ContentView.swift`, `TextEditor` is used, since by default this is multi-document, text-editing app.
