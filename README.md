# Ml-Agents for Unity for Beginners

これはUnityで強化学習を行うことができる公式のツールセットの使い方のハンズオンの資料です。


次のようなステップで進めて行きます。

1. 公式のML-Agentsのプロジェクトをダウンロード
2. 諸々必用なもののインストール
3. ML-Agentsの仕組み
4. 学習済みのサンプルを動かす
5. サンプルで学習を体験する
6. 簡単な学習環境を作る

## 1. 公式のML-Agentsのプロジェクトをダウンロード

Unity公式の強化学習ツールML-Agentsのバージョン0.13のページ（ https://github.com/Unity-Technologies/ml-agents/tree/release_13 ）に行き、
このプロジェクトを自分のPCにクローン/ダウンロードします。

gitがインストールされている環境であれば次のようなコマンドでクローンができます。

git clone --branch release_13 https://github.com/Unity-Technologies/ml-agents.git

## 2. 諸々必用なもののインストール

基本公式のインストールページに沿って進めます。

https://github.com/Unity-Technologies/ml-agents/blob/release_13_docs/docs/Installation.md

今回はステップ１でダウンロードしたプロジェクトを利用するので、次のようなステップで必用なインストールを完了させます。

### 2-1. Unity 2018.4以上をUnity Hubを介してインストール

Unity 2018.4以上を利用します。ハンズオンでは2018.4.32f1を利用します。

### 2-2. Python 3.6.1以上をインストール（Anaconda推奨）

Python3.6.1以上をインストールしてください。Ancondaで環境を作るのがおすすめです。

https://www.anaconda.com/products/individual

のページに行って64bit用のインストーラを利用してインストールしてください。
インストールが終わったらPythonのバーチャル環境を3.6.1以上で作ります。

### 2-3. PyTorchのインストール（Windowsのみ）

Windowsの場合は個別にPythonのPyTorchパッケージをインストールする必用があります。
利用するPython環境で次のようなコマンドでインストールしてください。

```
pip3 install torch~=1.7.1 -f https://download.pytorch.org/whl/torch_stable.html
```

### 2-3. mlagents Pythonパッケージのインストール

Pythonの環境に次のようなコマンドでmlagentsのパッケージをインストールします。

```
pip3 install mlagents
```
## 3. ML-Agentsの仕組み

ML-Agentsを使うことによってエージェントと呼ばれるNPC（ノンプレイヤーキャラクター）の動きを環境とのインタラクションを通じて自身が最適な行動を行うための強化学習を行うことができます。

基本的には次のような流れで強化学習が行われます。

 - 観察（Observations）： エージェントから見て、自身の行動に関係のある環境の情報を観察します。例えば、エージェントが指定の場所にたどりつくことが目標だとすると、その指定の場所までの距離などが観察対象になりえます。
 - 行動（Actions）: エージェントが目標に達するための行動をします。例えばエージェントが指定の場所にたどり着くためにある方向に歩くなどが行動の一つの例となります。
 - 報酬（Reward Signals）: エージェントがどの程度最適な行動をしたかを測るための数値が報酬となります。報酬を与えるタイミングはいつでも大丈夫です。

以上の３つの要素を用意するだけで強化学習を始めることが可能です。これらの要素で強化学習を行うことで、基本的には報酬を多くもらえるような行動を観察から推測して行うことができるようにするのが強化学習ということになります。

## 4. 学習済みのサンプルを動かす

すでに用意されている学習済みのサンプルを動かしてみます。
ML-Agents/Examplesフォルダの中にあるシーンを試していきます。

## 5. サンプルで学習を体験する

公式のGetting Startedに沿ってサンプルシーンの学習を体験します。
https://github.com/Unity-Technologies/ml-agents/blob/release_13_docs/docs/Getting-Started.md

## 6. 簡単な学習環境を作る

公式のMaking a New Learning Environmentに沿って簡単な強化学習環境を作って見ます。
https://github.com/Unity-Technologies/ml-agents/blob/release_13_docs/docs/Learning-Environment-Create-New.md
