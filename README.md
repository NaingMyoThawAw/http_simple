**Example:**
**Dart Code:**

```markdown
```dart
// [response] will be either [YourSuccessResponseModel] or [ErrorCodeAndMessage]
final dynamic response = await parseAPIResponse<YourSuccessResponseModel>(
      response: post(
        tag: 'forgotPasswordRequestOTP',
        url: AppData.forgotPasswordRequestOtpURL,
        body: jsonEncode(body),
      ),
      fromJson: YourSuccessResponseModel.fromJson,
      onFailure: (ErrorCodeAndMessage error) {
        // TODO
      },
      onSuccess: (YourSuccessResponseModel success) {
        // TODO
      },
      defaultErrorMessage: 'This default error message will be used when the error cannot be detected.',
    );
