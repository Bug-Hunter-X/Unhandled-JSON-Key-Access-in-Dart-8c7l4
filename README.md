# Unhandled JSON Key Access in Dart

This example demonstrates a common error in Dart when handling JSON responses: accessing a key that might not exist in the JSON data.  The code includes a `try-catch` block to handle the `NullPointerException` but doesn't explicitly check for the key's existence before accessing it.  The solution provides a more robust way to handle this scenario.

## Bug Report
The `bug.dart` file contains the buggy code.  It makes a network request, parses the JSON response, and then attempts to access a key (`jsonData['someKey']`) without checking if the key exists. If `someKey` is absent, a runtime error occurs.