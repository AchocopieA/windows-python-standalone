# windows-python-standalone

スタンドアローン型の仮想python環境の構築

## 構築環境

エディションWindows 11 Pro

バージョン23H2

OSビルド22631.3296

## 導入方法Windowsにzip版Pythonを導入

[参考1](https://suzulang.com/windows-zip-python/)、[参考2](https://qiita.com/subebe/items/fb2749f2cd9a197e161c#:~:text=Windows%2010%E3%81%ABZIP%E7%89%88Python%E3%81%A8pip%E3%82%92%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%AB%201%20%E5%88%9D%E3%82%81%E3%81%AB%20Windows%E3%81%A7Python%E3%82%92%E4%BD%BF%E3%81%84%E3%81%9F%E3%81%84%E3%81%91%E3%81%A9%E4%BD%99%E8%A8%88%E3%81%AA%E3%82%82%E3%81%AE%E3%81%AF%E5%85%A5%E3%82%8C%E3%81%A6%E3%81%8F%E3%82%8C%E3%82%8B%E3%81%AA%E3%81%A8%E3%81%84%E3%81%86%E7%A7%81%E5%90%91%E3%81%91%E3%81%AE%E8%A8%98%E4%BA%8B%E3%81%A7%E3%81%99%E3%80%82%20%E5%A4%9A%E5%88%86%E6%99%AE%E9%80%9A%E3%81%AB%E3%82%A4%E3%83%B3%E3%82%B9%E3%83%88%E3%83%BC%E3%83%A9%E3%81%A7%E3%82%82%E3%81%9D%E3%82%93%E3%81%AA%E3%81%AB%E5%85%A5%E3%82%8B%E3%82%82%E3%81%AE%E3%81%AF%E5%A4%89%E3%82%8F%E3%82%89%E3%81%AA%E3%81%84%E3%81%A8%E6%80%9D%E3%81%86%E3%80%82%202%20Python%E3%81%AEZIP%E7%89%88%E3%82%92%E3%83%80%E3%82%A6%E3%83%B3%E3%83%AD%E3%83%BC%E3%83%89,6%20pip%E3%81%AE%E3%83%91%E3%82%B9%E3%82%92%E9%80%9A%E3%81%99%20...%207%20import%20site%E3%82%92%E6%9C%89%E5%8A%B9%E5%8C%96%20...%20%E3%81%9D%E3%81%AE%E4%BB%96%E3%81%AE%E3%82%A2%E3%82%A4%E3%83%86%E3%83%A0)

サイトからインストール　[ダウンロード](https://www.python.org/downloads/windows/)

* ダウンロードのリストから、Python 3.8.10を探す
* [Python Release Python 3.8.10 | Python.org](https://www.python.org/downloads/release/python-3810/)
* Download Windows embeddable package (64-bit)をインストールする

> Python 3.8.10 - May 3, 2021
> Note that Python 3.8.10 cannot be used on Windows XP or earlier.
>
> Download Windows installer (64-bit)
> Download Windows installer (32-bit)
> Download Windows help file
> Download Windows embeddable package (64-bit)
> Download Windows embeddable package (32-bit)

### 格納先ディレクトリを作成

ここで作成するディレクトリはpython環境のソースを格納する場所となる。

```
mkdir C:\Users\work\app
mkdir C:\Users\work\app\python
```

### 各バージョンごとの格納先を作成

Python 3.8.10用を作成

```
mkdir C:\Users\work\app\python\python-3810
```

### 各OSごとのオリジナルの格納先を作成

* windows

```
mkdir C:\Users\work\app\python\python-3810\windows
mkdir C:\Users\work\app\python\python-3810\windows\origin
```

* macOS

```
mkdir C:\Users\work\app\python\python-3810\mac
mkdir C:\Users\work\app\python\python-3810\mac\origin
```

* Source（ソース）

```
mkdir C:\Users\work\app\python\python-3810\source
mkdir C:\Users\work\app\python\python-3810\source\origin
```

### 各OSごとのオリジナルから派生したものの格納先を作成

* windows

```
mkdir C:\Users\work\app\python\python-3810\windows\branch
```

* macOS

```
mkdir C:\Users\work\app\python\python-3810\mac\branch
```

* Source（ソース）

```
mkdir C:\Users\work\app\python\python-3810\source\branch
```

### インストールしたpythonを格納

今回はWindows版

インストールしたpython-3.8.10-embed-amd64.zipをオリジナルの格納先に格納

展開もしておく

```
・zip格納
C:\Users\work\app\python\python-3810\windows\origin\python-3.8.10-embed-amd64.zip

・展開ファイル格納
C:\Users\work\app\python\python-3810\windows\origin\python-3.8.10-embed-amd64
```

Length Name

---

libcrypto-1_1.dll
libffi-7.dll
libssl-1_1.dll
LICENSE.txt
pyexpat.pyd
python.cat
python.exe
python3.dll
python38.dll
python38.zip
python38._pth
pythonw.exe
select.pyd
sqlite3.dll
unicodedata.pyd
vcruntime140.dll
vcruntime140_1.dll
winsound.pyd
_asyncio.pyd
_bz2.pyd
_ctypes.pyd
_decimal.pyd
_elementtree.pyd
_hashlib.pyd
_lzma.pyd
_msi.pyd
_multiprocessing.pyd
_overlapped.pyd
_queue.pyd
_socket.pyd
_sqlite3.pyd
 _ssl.pyd

---

python.exeを実行することでpython環境を使用可能

ここに配置したものは、オリジナルとして使用はしない

## スタンドアローン型の仮想python環境の構築

### オリジナルからスタンドアローン型の仮想python環境の機能を有したモデルを作成する

* 格納先作成

`mkdir C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv`

上記に、オリジナル”C:\Users\work\app\python\python-3810\windows\origin\python-3.8.10-embed-amd64”から中身だけをコピーする

* コピー

```bash
robocopy "C:\Users\work\app\python\python-3810\windows\origin\python-3.8.10-embed-amd64" "C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv" /E
```

ディレクトリ: C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenvの中身。

オリジナルと同じ状態

Length Name

---

libcrypto-1_1.dll
libffi-7.dll
libssl-1_1.dll
LICENSE.txt
pyexpat.pyd
python.cat
python.exe
python3.dll
python38.dll
python38.zip
python38._pth
pythonw.exe
select.pyd
sqlite3.dll
unicodedata.pyd
vcruntime140.dll
vcruntime140_1.dll
winsound.pyd
_asyncio.pyd
_bz2.pyd
_ctypes.pyd
_decimal.pyd
_elementtree.pyd
_hashlib.pyd
_lzma.pyd
_msi.pyd
_multiprocessing.pyd
_overlapped.pyd
_queue.pyd
_socket.pyd
_sqlite3.pyd
 _ssl.pyd

---

ここで仮想環境を実行できるモデルを作成していく

### 起動確認

ターミナル（cmd等）で起動を確認

```
C:\Users\work>C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\python.exe
Python 3.8.10 (tags/v3.8.10:3d8993a, May  3 2021, 11:48:03) [MSC v.1928 64 bit (AMD64)] on win32
>>>
>>>
```

コントロールZで抜ける

### バージョン確認

```
C:\Users\work>C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\python.exe -V
Python 3.8.10
```

### モデル作成

仮想環境作成機能を有したモデルを構築するため、以下のモジュールをインストールする

* pip（ｘｘｘｘｘｘ）※オリジナルには入っていないため
* virtualenv（仮想化環境作成機能）

#### pipインストール

* 格納先作成
  `mkdir C:\Users\work\app\python\pip-origin`

  ダウンロードするときは、pipのバージョンは24.0だったため以下を作成

  `mkdir C:\Users\work\app\python\pip-origin\pip-24.0`

pip ファイルを次のURL先からダウンロードします。

[https://bootstrap.pypa.io/get-pip.py](https://bootstrap.pypa.io/get-pip.py)

ダウンロードしたファイル get-pip.py を `C:\Users\work>C:\Users\work\app\python\pip-origin\pip-24-0`に配置する

#### モデルにインストールする

ターミナルでコマンド実行

```
$ C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\python.exe C:\Users\work\app\python\pip-origin\pip-24.0\get-pip.py
```

これにより、pipがインストールされ、必要に応じてSetuptoolsとwheelもインストールされます。

* ログ

  ```
  C:\Users\work>C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\python.exe C:\Users\work\app\python\pip-origin\pip-24.0\get-pip.py
  Collecting pip
    Using cached pip-24.0-py3-none-any.whl.metadata (3.6 kB)
  Collecting setuptools
    Using cached setuptools-69.2.0-py3-none-any.whl.metadata (6.3 kB)
  Collecting wheel
    Using cached wheel-0.43.0-py3-none-any.whl.metadata (2.2 kB)
  Using cached pip-24.0-py3-none-any.whl (2.1 MB)
  Using cached setuptools-69.2.0-py3-none-any.whl (821 kB)
  Using cached wheel-0.43.0-py3-none-any.whl (65 kB)
  Installing collected packages: wheel, setuptools, pip
    WARNING: The script wheel.exe is installed in 'C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\Scripts' which is not on PATH.
    Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
    WARNING: The scripts pip.exe, pip3.8.exe and pip3.exe are installed in 'C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\Scripts' which is not on PATH.
    Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
  Successfully installed pip-24.0 setuptools-69.2.0 wheel-0.43.0

  ```

C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\に以下のフォルダが作成されている。

* Lib
* Scripts

### import siteを有効化

そのままだとpipが正しく起動しないので[pythonの展開パス]\python38._pth を編集して import site の行を有効化する。

```python38._pth
python38.zip
.

# Uncomment to run site.main() automatically
import site
```

### pipモジュールインストール確認

ターミナル（cmd等）で確認

```
C:\Users\work>C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\python.exe
Python 3.8.10 (tags/v3.8.10:3d8993a, May  3 2021, 11:48:03) [MSC v.1928 64 bit (AMD64)] on win32
```


#### virtualenvインストール

ターミナルから以下コマンドを実行しインストール

```
C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\Scripts\pip.exe install virtualenv==20.25.1
```

ログ

```
C:\Users\work>C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\Scripts\pip.exe list
Package    Version
---------- -------
pip        24.0
setuptools 69.2.0
wheel      0.43.0

C:\Users\work>C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\Scripts\pip.exe install virtualenv==20.25.1
Collecting virtualenv==20.25.1
  Using cached virtualenv-20.25.1-py3-none-any.whl.metadata (4.4 kB)
Collecting distlib<1,>=0.3.7 (from virtualenv==20.25.1)
  Using cached distlib-0.3.8-py2.py3-none-any.whl.metadata (5.1 kB)
Collecting filelock<4,>=3.12.2 (from virtualenv==20.25.1)
  Using cached filelock-3.13.3-py3-none-any.whl.metadata (2.8 kB)
Collecting platformdirs<5,>=3.9.1 (from virtualenv==20.25.1)
  Using cached platformdirs-4.2.0-py3-none-any.whl.metadata (11 kB)
Using cached virtualenv-20.25.1-py3-none-any.whl (3.8 MB)
Using cached distlib-0.3.8-py2.py3-none-any.whl (468 kB)
Using cached filelock-3.13.3-py3-none-any.whl (11 kB)
Using cached platformdirs-4.2.0-py3-none-any.whl (17 kB)
Installing collected packages: distlib, platformdirs, filelock, virtualenv
  WARNING: The script virtualenv.exe is installed in 'C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\Scripts' which is not on PATH.
  Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
Successfully installed distlib-0.3.8 filelock-3.13.3 platformdirs-4.2.0 virtualenv-20.25.1
```


#### virtualenvインストール確認

ターミナル（cmd等）で確認

```
C:\Users\work>C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\Scripts\pip.exe list
Package      Version
------------ -------
distlib      0.3.8
filelock     3.13.3
pip          24.0
platformdirs 4.2.0
setuptools   69.2.0
virtualenv   20.25.1
wheel        0.43.0
```


以上でモデル作成は完了
