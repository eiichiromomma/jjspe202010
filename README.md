# はじめてのPythonとOpenCVによる画像処理
ここで公開するipynbおよび画像は精密工学会誌2020年10月号「はじめての精密工学」と連動した内容となっています。
また，OpenCVを主として[画像処理100本ノック](https://yoyoyo-yo.github.io/Gasyori100knock/)を出来るだけ簡潔に解く方法についても掲載しています。

## 環境構築
channelはdefaults, conda-forgeを利用した。installしたパッケージは下記の通り。
* python = 3.7
* NumPy = 1.18 (Pythonで数値計算を効率良く行うためのパッケージでOpenCVも強く依存していて，画像データはNumPyのndarray(N-d Array)である)
* pillow = 7.1 (PIL (Python Imaging Library)からforkした画像処理パッケージでOpenCVとの間でのやりとりには変換が必要。メジャーバージョンが上がって間も無いので6.xを入れておいた方がトラブルが少ない)
* SciPy = 1.4 (NumPyをベースとした科学的な計算向けのパッケージ)
* Notebook(Jupyter Notebook) = 6.0 (文章とソースコードを混在して記述できる仕組み)
* Matplotlib = 3.2 (2-Dなプロット用パッケージ)
* scikit-image = 0.17 (SciPyのサードパーティ拡張の一つで画像処理用パッケージ)
* jupyter_nbextensions_configurator = 0.4 (Notebookの拡張設定)
* py-opencv = 4.2 (OpenCVのPython I/F)

condaコマンドが使える場合は下記で仮想環境が構築・利用できる
```bash
conda create -n jjspe202010 -c conda-forge python=3.7 numpy pillow scipy notebook matplotlib scikit-image jupyter_nbextensions_configurator py-opencv
conda activate jjspe202010
```

## このrepositoryについて
* 実際に確認した内容に基いて記述していますが，環境の違いにより意図せぬ動作をする場合があります
* 記載されている文章，ソース，画像等で出典の記載されていない物の著作権は門馬英一郎に帰属します
* 研究，教育目的に於いては，出典を明記すれば自由に利用して構いません
* 商用利用を目的とする場合にはメール等でご連絡下さい
