# Yolo V5 v8

## 1.まず理解しておくこと
### エポック数（epoch）とステップ数（step）の違い、バッチサイズとは【初級 深層学習講座】

https://tech.aru-zakki.com/deeplearning-epoch-step-batchsize/

#### 機械学習におけるバッチサイズとは？決め方や注意点を解説

https://www.tryeting.jp/column/6047/

## 2.インストールと学習
### Yolov5を独自のデータでトレーニングする

https://qiita.com/john-rocky/items/60af264e3e60f2bc0eb7

#### Yolov5のインストール
```
git clone https://github.com/ultralytics/yolov5  # clone
cd yolov5
pip install -r requirements.txt
```
#### トレーニング

以下を指定してトレーニング・スクリプトを開始します。
```
python train.py --img 640 --batch 16 --epochs 3 --data coco128.yaml --weights yolov5s.pt
引数は以下のとおりです。

・画像サイズ（正方形の縦横）
・トレーニング・バッチ数（一度にモデルに入力するデータ数）
・エポック（何回トレーニング・ループを回すか）
・データ構成ファイル・パス（上記で作った構成ファイル）
・事前トレーニング済み重み（一般的なデータセットで学習された重みを用いる）

*事前トレーニング済みの重みを用いずに、１からランダムな重みでトレーニングするときは
--weights '' --cfg yolov5s.yaml
と引数を指定することもできますが、ランダムな重みからの学習は非推奨となっています。

事前トレーニング済みの重みは公式リポジトリから入手できます。
```
### YOLOv8で学習→物体検出】楽に学習データを用意して好きなものを検出してみよう

https://qiita.com/ysv/items/2bc7fe4f927fa2c10156


## 推論
### YOLOv5 で物体検出をしてみよう  Windows

https://rinsaka.com/python/yolov5/index.html#google_vignette

### OpenCVとYOLOv5を使って動画切り抜きをしてみる

https://qiita.com/smiler5617/items/c8a0925373eaa89e2aae

## アノテーション
#### Roboflow (30000円/月、フリーのは使えない)

https://roboflow.com/annotate?ref=ultralytics



#### Pytorchでモデルの保存と読み込み

https://tzmi.hatenablog.com/entry/2020/03/05/222813

#### 第5回：PyTorch hubまとめとYouTube動画の物体検出

https://tt-tsukumochi.com/archives/1933

#### 物体検出 YOLOv5のオプションまとめ

https://zenn.dev/gotty/articles/6bd35b25cf3bd9

#### YOLOv5を用いた物体検出

https://avinton.com/academy/object-detection-using-yolov5/

#### OpenCVのdnnモジュールのクラス分類で信頼度を[0.0-1.0]にする

https://qiita.com/UnaNancyOwen/items/dc0a3c3afce60cd81d2f

#### PyTorch Hub

https://docs.ultralytics.com/yolov5/tutorials/pytorch_hub_model_loading/











