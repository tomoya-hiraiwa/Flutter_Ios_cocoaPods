# Flutter_Ios_cocoaPods

## エラー内容

```
Warning: CocoaPods not installed. Skipping pod install. CocoaPods is used to retrieve the iOS and macOS platform side's plugin code that responds to your plugin usage on the Dart side.
Without CocoaPods, plugins will not work on iOS or macOS. For more info, see https://flutter.dev/platform-plugins To install see https://guides.cocoapods.org/using/getting-started.html#installation for instructions.

Exception: CocoaPods not installed or not in valid state.
```

## 対処法

### 1.Homebrewのインストール

・mac本体のターミナルに以下入力

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

・パスワードを入力

・インストール終了後、パスを通す

```
Add Homebrew to ~ に続く部分をコピぺしてreturn
```

・インストールが正常に終了したかを確認

```
brew help
```

実行した時に、ずらずらっとレスポンスが帰ってきていればOK

### 2.cocoapodsのインストール

```
brew install cocoapods
```

を実行する

・インストール終了後、

```
flutter doctor
```
を実行(android studiodのターミナルでもOK,一度再起動しておく)

・インストール前はXcodeのところに❌が表示されていたが、インストールできていれば、

```
[✓] Xcode - develop for iOS and macOS (Xcode 14.3.1)
```

のようになっているはず。

・再度、エミュレータを起動し問題がないことを確認
