# Unhandled Exception during JSON Decoding in Dart

This repository demonstrates a common error in Dart applications: failing to handle exceptions that can occur during JSON decoding using the `jsonDecode` function. The `bug.dart` file contains code with insufficient error handling, while `bugSolution.dart` provides a corrected version with improved exception management.

## Problem

The original code lacks comprehensive error handling when processing JSON responses from network requests.  A `FormatException` could occur if the response from the API isn't valid JSON.  This leads to an unhandled exception and application crashes.

## Solution

The improved code includes a `try-catch` block specifically to catch `FormatException` during JSON decoding.  It also includes checks for HTTP status codes to handle network errors and logs error messages to the console for debugging purposes.  This makes the application more robust and less prone to unexpected crashes.