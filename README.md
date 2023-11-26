# Vision Transformer(ViT)
このプログラムはCIFAR-10データセットをVision Transformer(ViT)モデルを使って訓練するためのプログラムです。
## プログラムの概要

モデルの訓練: train 関数はモデルの訓練を行い、バリデーションデータに対するパフォーマンスを監視しながら、適切な時点で訓練を早期終了します。

学習率の探索: islearnrate_search 引数に基づき、異なる学習率でモデルを訓練し、最適な学習率を見つけ出します。

## プログラムの実行方法
1. 依存ライブラリのインストール：必要なライブラリをインストールします。
```
pip install -r requirements.txt
```
2. プログラムの実行
```
python train.py --epochs <学習回数> --learning_rate <学習率> --patience <早期終了パラメータ> --islearnrate_search <学習率探索> --seed <シード> --batch <バッチサイズ>
```
### 引数の説明
--epochs: エポック数（訓練の反復回数）

--learning_rate: 学習率（デフォルトは0.001）

--patience: 早期終了のための耐性回数（バリデーションロスが改善しない場合の訓練継続エポック数）

--islearnrate_search: 学習率の探索を行うかどうか（'true' または 'false'）

--seed: 乱数生成のためのシード

--batch: バッチサイズ
### プログラムの応用
このプログラムは、カスタムデータセットや異なるモデルアーキテクチャにも適用可能です。必要に応じて、モデルの構造やデータ処理の部分を変更することで、様々な画像分類タスクに対応できます。