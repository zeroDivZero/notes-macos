# `FileDocument`

```swift
protocol FileDocument
```

Type to serialize document to and from file. To store document as value type, create type conforming to `FileDocument` and implement the required methods and properties:

* `readableContentTypes`: list of content types that document can read from.
* `writableContentTypes`: optional if list of content types that document can write to is different from read.
* Load document from file in `init(configuration:)` initializer.
* Store document to file by serializing content in `fileWrapper(configuration:)`.

Conforming type should be thread-safe. SwiftUI calls protocol's methods on background thread. Don't use that thread to perform UI updates. Use it only to serialize and deserialize document data.
