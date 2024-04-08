# windows-python-standalone

## 構築環境

エディションWindows 11 Pro

バージョン23H2

OSビルド22631.3296

##   構築済みモデル
app/pythonフォルダーに格納済み（本資料の項目１～２で作成するもの）
上記をダウンロードして、項目３から実施でも可

## １．導入方法Windowsにzip版Pythonを導入

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

* libcrypto-1_1.dll
* libffi-7.dll
* libssl-1_1.dll
* LICENSE.txt
* pyexpat.pyd
* python.cat
* python.exe
* python3.dll
* python38.dll
* python38.zip
* python38._pth
* pythonw.exe
* select.pyd
* sqlite3.dll
* unicodedata.pyd
* vcruntime140.dll
* vcruntime140_1.dll
* winsound.pyd
* _asyncio.pyd
* _bz2.pyd
* _ctypes.pyd
* _decimal.pyd
* _elementtree.pyd
* _hashlib.pyd
* _lzma.pyd
* _msi.pyd
* _multiprocessing.pyd
* _overlapped.pyd
* _queue.pyd
* _socket.pyd
* _sqlite3.pyd
* _ssl.pyd

python.exeを実行することでpython環境を使用可能

ここに配置したものは、オリジナルとして使用はしない

## ２．スタンドアローン型の仮想python環境の構築

### オリジナルからスタンドアローン型の仮想python環境の機能を有したモデルを作成する

* 格納先作成

  ```
  mkdir C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv
  ```

上記に、オリジナル”C:\Users\work\app\python\python-3810\windows\origin\python-3.8.10-embed-amd64”から中身だけをコピーする

* コピー

  ```
  robocopy "C:\Users\work\app\python\python-3810\windows\origin\python-3.8.10-embed-amd64" "C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv" /E
  ```

  ディレクトリ: C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenvの中身

  ※オリジナルと同じ状態

Length Name

* libcrypto-1_1.dll
* libffi-7.dll
* libssl-1_1.dll
* LICENSE.txt
* pyexpat.pyd
* python.cat
* python.exe
* python3.dll
* python38.dll
* python38.zip
* python38._pth
* pythonw.exe
* select.pyd
* sqlite3.dll
* unicodedata.pyd
* vcruntime140.dll
* vcruntime140_1.dll
* winsound.pyd
* _asyncio.pyd
* _bz2.pyd
* _ctypes.pyd
* _decimal.pyd
* _elementtree.pyd
* _hashlib.pyd
* _lzma.pyd
* _msi.pyd
* _multiprocessing.pyd
* _overlapped.pyd
* _queue.pyd
* _socket.pyd
* _sqlite3.pyd
* _ssl.pyd

ここで仮想環境を実行できるモデルを作成していく

### 起動確認

* ターミナル（cmd等）で起動を確認

  ```
  C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\python.exe
  ```
* ログ

  ```
  C:\Users\work>C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\python.exe
  Python 3.8.10 (tags/v3.8.10:3d8993a, May  3 2021, 11:48:03) [MSC v.1928 64 bit (AMD64)] on win32
  >>>
  >>>
  ```

  コントロールZで抜ける

### バージョン確認

* ターミナル（cmd等）で起動を確認

  ```
  C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\python.exe -V
  ```
* ログ

  ```
  C:\Users\work>C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\python.exe -V
  Python 3.8.10
  ```

### モデル作成

仮想環境作成機能を有したモデルを構築するため、以下のモジュールをインストールする

* pip（Pythonのパッケージを管理するためのツール）※オリジナルには入っていないため

  [pip · PyPI](https://pypi.org/project/pip/)
* virtualenv（Pythonの開発環境を仮想化するツール）

  [virtualenv · PyPI](https://pypi.org/project/virtualenv/)

  virtualenv:
  virtualenv はPythonの外部パッケージで、Pythonの標準ライブラリには含まれていません1。
  別途インストールが必要ですが、Python 2およびPython 3の両方で使用できます。
  標準ライブラリに依存しないため、より広範な環境で動作し、柔軟性を提供します。
  高度なオプションとカスタマイズが可能で、さまざまなシナリオに適した設定ができます。
  要するに、venv はPython 3.3以降の標準ライブラリで提供されており、シンプルで基本的な仮想環境管理を行うのに適しています。一方、virtualenv はPython 2およびPython 3の両方で使用でき、より多くのカスタマイズオプションを提供し、さまざまな環境で動作するため、より柔軟です。どちらを選ぶかは、プロジェクトの要件と開発環境に依存します。

#### pipインストール

* 格納先作成

  ```
  mkdir C:\Users\work\app\python\pip-origin
  ```
* ダウンロードするときは、pipのバージョンは24.0だったため以下を作成

  ```
  mkdir C:\Users\work\app\python\pip-origin\pip-24.0
  ```
* pip ファイルを次のURL先からダウンロード

  [https://bootstrap.pypa.io/get-pip.py](https://bootstrap.pypa.io/get-pip.py)

  ダウンロードしたファイル get-pip.py を以下に配置

  `C:\Users\work>C:\Users\work\app\python\pip-origin\pip-24-0`

#### モデルにインストール

* ターミナルでコマンド実行

  ```
  C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\python.exe C:\Users\work\app\python\pip-origin\pip-24.0\get-pip.py
  ```

これにより、pipがインストールされ、必要に応じてSetuptoolsとwheelもインストールされます

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

#### モデルにインストールされた確認

以下フォルダに作成されたことを確認

`C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\`{`ここにインストールされる}`

インストールされるもの

* Lib
* Scripts

#### import siteを有効化

そのままだとpipが正しく起動しないため、[pythonの展開パス]\python38._pth を編集して

 import site の行を有効化する。

```python38._pth
python38.zip
.

# Uncomment to run site.main() automatically
import site
```

#### pipモジュールインストール確認

* ターミナル（cmd等）で確認

  ```
  C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\Scripts\pip.exe -V
  ```
* ログ

  ```
  C:\Users\work>C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\Scripts\pip.exe -V
  pip 24.0 from C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\lib\site-packages\pip (python 3.8)
  ```

#### virtualenvインストール

* ターミナルからコマンドを実行しインストール（virtualenv==20.25.1）

  ```
  C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\Scripts\pip.exe install virtualenv==20.25.1
  ```
* ログ

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

* ターミナル（cmd等）で確認

  ```
  C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\Scripts\pip.exe list

  ```
* ログ

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

## ３．仮想環境の構築

”オリジナル”→”スタンドアローン型の仮想python環境の機能を有したモデル”と今まで作成してきた。

作成したモデルから、仮想環境を作成していく。

```
・関係

origin
└─windows-python-standalone
   ├─仮想環境1
   ├─仮想環境2
   └─仮想環境3
```

ここで作成する環境は、フォルダで独立している（パッケージ独立）

* 仮想環境1
* 仮想環境2
* 仮想環境3

### 仮想環境作成

開発プロジェクトフォルダ作成

```
mkdir C:\Users\work\project-app
```

#### 仮想環境1作成（virtualProject1）

* 作成

  `{もととなるpythonのスタンドアローンのpython.exe} -m virtualenv {仮想環境配置場所}`

  ```
  C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\python.exe -m virtualenv "C:\Users\work\project-app\virtualProject1"
  ```


※本レポジトリのapp/pythonをダウンロードした場合は以下のコマンドで実施。後の説明は読み替えてください。
  ```
  {ダウンロードして配置した場所}\app\python\python-3810\windows\branch\python-3810-virtualenv\python.exe -m virtualenv "C:\Users\work\project-app\virtualProject1"
  ```

  
* ログ

  ```
  C:\Users\work\project-app>C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\python.exe -m virtualenv "C:\Users\work\project-app\virtualProject1"
  created virtual environment CPython3.8.10.final.0-64 in 213ms
    creator CPython3Windows(dest=C:\Users\work\project-app\virtualProject1, clear=False, no_vcs_ignore=False, global=False)
    seeder FromAppData(download=False, pip=bundle, setuptools=bundle, wheel=bundle, via=copy, app_data_dir=C:\Users\work\AppData\Local\pypa\virtualenv)
      added seed packages: pip==24.0, setuptools==69.1.1, wheel==0.42.0
    activators BashActivator,BatchActivator,FishActivator,NushellActivator,PowerShellActivator,PythonActivator
  ```

virtualProject1が作成される

```
C:\Users\work\project-app>cd virtualProject1

C:\Users\work\project-app\virtualProject1>tree ./
フォルダー パスの一覧
ボリューム シリアル番号は A4E1-12C1 です
C:\USERS\WORK\PROJECT-APP\VIRTUALPROJECT1
├─Lib
│  └─site-packages
│      ├─pip
│      │  ├─_internal
│      │  │  ├─cli
│      │  │  │  └─__pycache__
│      │  │  ├─commands
│      │  │  │  └─__pycache__
│      │  │  ├─distributions
│      │  │  │  └─__pycache__
│      │  │  ├─index
│      │  │  │  └─__pycache__
│      │  │  ├─locations
│      │  │  │  └─__pycache__
│      │  │  ├─metadata
│      │  │  │  ├─importlib
│      │  │  │  └─__pycache__
│      │  │  ├─models
│      │  │  │  └─__pycache__
│      │  │  ├─network
│      │  │  │  └─__pycache__
│      │  │  ├─operations
│      │  │  │  ├─build
│      │  │  │  │  └─__pycache__
│      │  │  │  ├─install
│      │  │  │  │  └─__pycache__
│      │  │  │  └─__pycache__
│      │  │  ├─req
│      │  │  │  └─__pycache__
│      │  │  ├─resolution
│      │  │  │  ├─legacy
│      │  │  │  ├─resolvelib
│      │  │  │  └─__pycache__
│      │  │  ├─utils
│      │  │  │  └─__pycache__
│      │  │  ├─vcs
│      │  │  │  └─__pycache__
│      │  │  └─__pycache__
│      │  ├─_vendor
│      │  │  ├─cachecontrol
│      │  │  │  ├─caches
│      │  │  │  │  └─__pycache__
│      │  │  │  └─__pycache__
│      │  │  ├─certifi
│      │  │  │  └─__pycache__
│      │  │  ├─chardet
│      │  │  │  ├─cli
│      │  │  │  ├─metadata
│      │  │  │  └─__pycache__
│      │  │  ├─colorama
│      │  │  │  └─tests
│      │  │  ├─distlib
│      │  │  │  └─__pycache__
│      │  │  ├─distro
│      │  │  ├─idna
│      │  │  │  └─__pycache__
│      │  │  ├─msgpack
│      │  │  │  └─__pycache__
│      │  │  ├─packaging
│      │  │  │  └─__pycache__
│      │  │  ├─pkg_resources
│      │  │  │  └─__pycache__
│      │  │  ├─platformdirs
│      │  │  │  └─__pycache__
│      │  │  ├─pygments
│      │  │  │  ├─filters
│      │  │  │  │  └─__pycache__
│      │  │  │  ├─formatters
│      │  │  │  ├─lexers
│      │  │  │  │  └─__pycache__
│      │  │  │  ├─styles
│      │  │  │  │  └─__pycache__
│      │  │  │  └─__pycache__
│      │  │  ├─pyparsing
│      │  │  │  ├─diagram
│      │  │  │  └─__pycache__
│      │  │  ├─pyproject_hooks
│      │  │  │  ├─_in_process
│      │  │  │  │  └─__pycache__
│      │  │  │  └─__pycache__
│      │  │  ├─requests
│      │  │  │  └─__pycache__
│      │  │  ├─resolvelib
│      │  │  │  └─compat
│      │  │  ├─rich
│      │  │  │  └─__pycache__
│      │  │  ├─tenacity
│      │  │  │  └─__pycache__
│      │  │  ├─tomli
│      │  │  │  └─__pycache__
│      │  │  ├─truststore
│      │  │  ├─urllib3
│      │  │  │  ├─contrib
│      │  │  │  │  ├─_securetransport
│      │  │  │  │  └─__pycache__
│      │  │  │  ├─packages
│      │  │  │  │  ├─backports
│      │  │  │  │  └─__pycache__
│      │  │  │  ├─util
│      │  │  │  │  └─__pycache__
│      │  │  │  └─__pycache__
│      │  │  ├─webencodings
│      │  │  └─__pycache__
│      │  └─__pycache__
│      ├─pip-24.0.dist-info
│      ├─pkg_resources
│      │  ├─extern
│      │  └─_vendor
│      │      ├─importlib_resources
│      │      ├─jaraco
│      │      │  └─text
│      │      ├─more_itertools
│      │      ├─packaging
│      │      └─platformdirs
│      ├─setuptools
│      │  ├─command
│      │  ├─compat
│      │  ├─config
│      │  │  └─_validate_pyproject
│      │  ├─extern
│      │  ├─_distutils
│      │  │  └─command
│      │  └─_vendor
│      │      ├─importlib_metadata
│      │      ├─importlib_resources
│      │      ├─jaraco
│      │      │  └─text
│      │      ├─more_itertools
│      │      ├─packaging
│      │      └─tomli
│      ├─setuptools-69.1.1.dist-info
│      ├─wheel
│      │  ├─cli
│      │  └─vendored
│      │      └─packaging
│      ├─wheel-0.42.0.dist-info
│      ├─_distutils_hack
│      │  └─__pycache__
│      └─__pycache__
└─Scripts
```

* 実行確認

  ```
  C:\Users\work\project-app\virtualProject1\Scripts\python.exe
  ```
* ログ（コントロールZで抜ける）

  ```
  C:\Users\work\project-app\virtualProject1>C:\Users\work\project-app\virtualProject1\Scripts\python.exe
  Python 3.8.10 (tags/v3.8.10:3d8993a, May  3 2021, 11:48:03) [MSC v.1928 64 bit (AMD64)] on win32
  Type "help", "copyright", "credits" or "license" for more information.
  >>>
  >>>
  ```
* ピップバージョン確認

```
C:\Users\work\project-app\virtualProject1\Scripts\pip3.exe -V
```

* ログ

```
C:\Users\work\project-app\virtualProject1>C:\Users\work\project-app\virtualProject1\Scripts\pip3.8.exe -V
pip 24.0 from C:\Users\work\project-app\virtualProject1\lib\site-packages\pip (python 3.8)
```

* ピップリスト確認

  ```
  C:\Users\work\project-app\virtualProject1\Scripts\pip3.8.exe list
  ```
* ログ

```
C:\Users\work\project-app\virtualProject1>C:\Users\work\project-app\virtualProject1\Scripts\pip3.8.exe list
Package    Version
---------- -------
pip        24.0
setuptools 69.1.1
wheel      0.42.0
```

作成されたことが確認できた

#### 仮想環境2作成（virtualProject2）

仮想環境1と同様に作成

* 作成

  `{python.exe} -m virtualenv {仮想環境配置場所}`

  ```
  C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\python.exe -m virtualenv "C:\Users\work\project-app\virtualProject2"
  ```
* ログ

  ```
  C:\Users\work\project-app>C:\Users\work\app\python\python-3810\windows\branch\python-3810-virtualenv\python.exe -m virtualenv "C:\Users\work\project-app\virtualProject2"
  created virtual environment CPython3.8.10.final.0-64 in 210ms
    creator CPython3Windows(dest=C:\Users\work\project-app\virtualProject2, clear=False, no_vcs_ignore=False, global=False)
    seeder FromAppData(download=False, pip=bundle, setuptools=bundle, wheel=bundle, via=copy, app_data_dir=C:\Users\work\AppData\Local\pypa\virtualenv)
      added seed packages: pip==24.0, setuptools==69.1.1, wheel==0.42.0
    activators BashActivator,BatchActivator,FishActivator,NushellActivator,PowerShellActivator,PythonActivator
  ```

virtualProject2が作成される

```
C:\Users\work\project-app>cd virtualProject2

C:\Users\work\project-app\virtualProject2>

C:\Users\work\project-app\virtualProject2>tree ./
フォルダー パスの一覧
ボリューム シリアル番号は A4E1-12C1 です
C:\USERS\WORK\PROJECT-APP\VIRTUALPROJECT2
├─Lib
│  └─site-packages
│      ├─pip
│      │  ├─_internal
│      │  │  ├─cli
│      │  │  ├─commands
│      │  │  ├─distributions
│      │  │  ├─index
│      │  │  ├─locations
│      │  │  ├─metadata
│      │  │  │  └─importlib
│      │  │  ├─models
│      │  │  ├─network
│      │  │  ├─operations
│      │  │  │  ├─build
│      │  │  │  └─install
│      │  │  ├─req
│      │  │  ├─resolution
│      │  │  │  ├─legacy
│      │  │  │  └─resolvelib
│      │  │  ├─utils
│      │  │  └─vcs
│      │  └─_vendor
│      │      ├─cachecontrol
│      │      │  └─caches
│      │      ├─certifi
│      │      ├─chardet
│      │      │  ├─cli
│      │      │  └─metadata
│      │      ├─colorama
│      │      │  └─tests
│      │      ├─distlib
│      │      ├─distro
│      │      ├─idna
│      │      ├─msgpack
│      │      ├─packaging
│      │      ├─pkg_resources
│      │      ├─platformdirs
│      │      ├─pygments
│      │      │  ├─filters
│      │      │  ├─formatters
│      │      │  ├─lexers
│      │      │  └─styles
│      │      ├─pyparsing
│      │      │  └─diagram
│      │      ├─pyproject_hooks
│      │      │  └─_in_process
│      │      ├─requests
│      │      ├─resolvelib
│      │      │  └─compat
│      │      ├─rich
│      │      ├─tenacity
│      │      ├─tomli
│      │      ├─truststore
│      │      ├─urllib3
│      │      │  ├─contrib
│      │      │  │  └─_securetransport
│      │      │  ├─packages
│      │      │  │  └─backports
│      │      │  └─util
│      │      └─webencodings
│      ├─pip-24.0.dist-info
│      ├─pkg_resources
│      │  ├─extern
│      │  └─_vendor
│      │      ├─importlib_resources
│      │      ├─jaraco
│      │      │  └─text
│      │      ├─more_itertools
│      │      ├─packaging
│      │      └─platformdirs
│      ├─setuptools
│      │  ├─command
│      │  ├─compat
│      │  ├─config
│      │  │  └─_validate_pyproject
│      │  ├─extern
│      │  ├─_distutils
│      │  │  └─command
│      │  └─_vendor
│      │      ├─importlib_metadata
│      │      ├─importlib_resources
│      │      ├─jaraco
│      │      │  └─text
│      │      ├─more_itertools
│      │      ├─packaging
│      │      └─tomli
│      ├─setuptools-69.1.1.dist-info
│      ├─wheel
│      │  ├─cli
│      │  └─vendored
│      │      └─packaging
│      ├─wheel-0.42.0.dist-info
│      └─_distutils_hack
└─Scripts
```

* 実行確認

  ```
  C:\Users\work\project-app\virtualProject2\Scripts\python.exe
  ```
* ログ（コントロールZで抜ける）

  ```
  C:\Users\work\project-app\virtualProject2>C:\Users\work\project-app\virtualProject2\Scripts\python.exe
  Python 3.8.10 (tags/v3.8.10:3d8993a, May  3 2021, 11:48:03) [MSC v.1928 64 bit (AMD64)] on win32
  Type "help", "copyright", "credits" or "license" for more information.
  >>>
  >>>
  ```
* ピップバージョン確認

```
C:\Users\work\project-app\virtualProject2\Scripts\pip3.exe -V
```

* ログ

```
C:\Users\work\project-app\virtualProject2>C:\Users\work\project-app\virtualProject2\Scripts\pip3.8.exe -V
pip 24.0 from C:\Users\work\project-app\virtualProject2\lib\site-packages\pip (python 3.8)
```

* ピップリスト確認

  ```
  C:\Users\work\project-app\virtualProject2\Scripts\pip3.8.exe list
  ```
* ログ

```
C:\Users\work\project-app\virtualProject2>C:\Users\work\project-app\virtualProject2\Scripts\pip3.8.exe list
Package    Version
---------- -------
pip        24.0
setuptools 69.1.1
wheel      0.42.0
```

作成されたことが確認できた

## ４．仮想環境の開発手順

仮想環境１での開発手順を記述する（仮想環境２も同様）

### 仮想環境のアクティベート

* ターミナルで実行

```
C:\Users\work\project-app\virtualProject1\Scripts\activate
```

* ログ

```
C:\Users\work>C:\Users\work\project-app\virtualProject1\Scripts\activate

(virtualProject1) C:\Users\work>
(virtualProject1) C:\Users\work>
```

(virtualProject1) C:\Users\work>　のように仮想環境が起動する

作業が終了したら、仮想環境をディアクティベートで抜ける

```
C:\Users\work>C:\Users\work\project-app\virtualProject1\Scripts\activate

(virtualProject1) C:\Users\work>
(virtualProject1) C:\Users\work>
(virtualProject1) C:\Users\work>deactivate
C:\Users\work>
```

### 仮想環境１にパッケージをインストール

* ターミナル（cmd等）で確認

  ```
  C:\Users\work\project-app\virtualProject1\Scripts\pip.exe list

  ```
* ログ

  ```
  C:\Users\work>C:\Users\work\project-app\virtualProject1\Scripts\pip3.8.exe list
  Package    Version
  ---------- -------
  pip        24.0
  setuptools 69.1.1
  wheel      0.42.0
  ```
* 適当なパッケージをインストール（tqdm）

```
C:\Users\work>C:\Users\work\project-app\virtualProject1\Scripts\pip3.8.exe install tqdm
Collecting tqdm
  Downloading tqdm-4.66.2-py3-none-any.whl.metadata (57 kB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 57.6/57.6 kB ? eta 0:00:00
Collecting colorama (from tqdm)
  Downloading colorama-0.4.6-py2.py3-none-any.whl.metadata (17 kB)
Downloading tqdm-4.66.2-py3-none-any.whl (78 kB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 78.3/78.3 kB ? eta 0:00:00
Downloading colorama-0.4.6-py2.py3-none-any.whl (25 kB)
Installing collected packages: colorama, tqdm
Successfully installed colorama-0.4.6 tqdm-4.66.2

C:\Users\work>
C:\Users\work>C:\Users\work\project-app\virtualProject1\Scripts\pip3.8.exe list
Package    Version
---------- -------
colorama   0.4.6
pip        24.0
setuptools 69.1.1
tqdm       4.66.2
wheel      0.42.0
```

* コマンドでインストールされているものを確認

```
C:\Users\work\project-app\virtualProject1\Scripts\pip3.8.exe freeze
```

```
C:\Users\work>C:\Users\work\project-app\virtualProject1\Scripts\pip3.8.exe freeze
colorama==0.4.6
tqdm==4.66.2
```

tqdmとcoloramaがインストールされていた

### 仮想環境２でパッケージのインストール状況を確認

```
C:\Users\work>C:\Users\work\project-app\virtualProject2\Scripts\pip3.8.exe list
Package    Version
---------- -------
pip        24.0
setuptools 69.1.1
wheel      0.42.0
```

```
C:\Users\work>C:\Users\work\project-app\virtualProject2\Scripts\pip3.8.exe freeze

C:\Users\work>

```

tqdmとcoloramaはインストールされていないことから、環境は分かれていることが確認できた。

## ５．パスの設定

python実行時のコマンドが長すぎて使いにくいので、パスを通す

* pythonコマンド
* pipコマンド

### 仮想環境１を使用する場合（仮想環境２で開発する際は切り替える）

**（仮想環境２で開発する際は、切替る。切り替えないと、仮想環境１にパッケージがインストールされてしまうことが発生する）**


* ユーザ環境変数のPathに以下を追加
  ※%USERPROFILE%\AppData\Local\Microsoft\WindowsAppsより上（前）に記述

```
C:\Users\work\project-app\virtualProject1\Scripts
```

#### pythonコマンド確認

* ログ

```
C:\Users\work>python -V
Python 3.8.10

C:\Users\work>where python
C:\Users\work\project-app\virtualProject1\Scripts\python.exe
C:\Users\work\AppData\Local\Microsoft\WindowsApps\python.exe
```

C:\Users\work\project-app\virtualProject1\Scripts\python.exeが

C:\Users\work\AppData\Local\Microsoft\WindowsApps\python.exeより先に表示されていること

#### pipコマンド確認

* ログ

```
C:\Users\work>pip3.8 -V
pip 24.0 from C:\Users\work\project-app\virtualProject1\lib\site-packages\pip (python 3.8)

C:\Users\work>where pip3.8
C:\Users\work\project-app\virtualProject1\Scripts\pip3.8.exe
C:\Users\work\app\python\python3.8.10\python-3.8.10-embed-amd64\Scripts\pip3.8.exe
```

C:\Users\work\project-app\virtualProject1\Scripts\pip3.8.exeが

C:\Users\work\app\python\python3.8.10\python-3.8.10-embed-amd64\Scripts\pip3.8.exeより先に表示されていること


パスが通っていることを確認できた

### 仮想環境１にアクティベートして入る

* ログ

```
C:\Users\work>cd project-app

C:\Users\work\project-app>cd virtualProject1

C:\Users\work\project-app\virtualProject1>.\Scripts\activate

(virtualProject1) C:\Users\work\project-app\virtualProject1>
(virtualProject1) C:\Users\work\project-app\virtualProject1>
```


### １０．その他参考

[Pythonではパッケージ管理ツールpipを含まない仮想環境を作ることができる。◯か☓か](https://nikkie-ftnext.hatenablog.com/entry/create-python-virtual-environments-without-pip)
