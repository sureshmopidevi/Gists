# Debug Messages

#### Type of Error message
```swift
    enum TypeOfError: String {
        case error
        case warning
        case caution
        case emptyData
        case other
        case success
    }

    func debugMessage(type: TypeOfError, message: String, line: Int, function: String) {
        switch type {
        case .error:
            print("🔴 Error: \(message) , method: \(function) , line: \(line) ")
        case .caution:
            print("☢️ Caution: \(message) , method: \(function) , line: \(line) ")
        case .warning:
            print("⚠️ Warning: \(message) , method: \(function) , line: \(line) ")
        case .emptyData:
            print("🗑 Empty data: \(message) , method: \(function) , line: \(line) ")
        case .success:
            print("✅ Success Message: \(message) , method: \(function) , line: \(line) ")
        case .other:
            print("🌀\(message) , method: \(function) , line: \(line) ")
        }
    }
```

```swift
self.debugMessage(type: .error, message: error.localizedDescription, line: #line, function: #function)
```
