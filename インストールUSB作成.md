## イメージファイルから、インストール用USBを作成する方法

***対象機器が事前に稼働していた場合はアクティベーションファイルを保存しておくこと***


### 手順
1. 192.168.3.173のデスクトップからClonzillaをUSBにコピー<br>
~/デスクトップ/Clonzila_template/* を USBのルートへコピー（ルートに「BAFFALO」フォルダとかあってもそのまま残しておく）
2. USBの以下にバックアップで取得したファイルをコピー<br>
USB : home/partimag/Recovery-Image/ 配下に、バックアップで取得したSSDの該当フォルダから全ファイルをコピー
3. USB : boot/grub/grub.cfg の確認<br>
192.168.3.173のデスクトップにある以下と比較し筐体にあったファイルに合わせて修正
- grub.cfg_nvme01　← Cube 2nd用（diff デスクトップ/grub.cfg_nvme01 /media/USBメモリ/boot/grub/grub.cfgで差分確認） ← 2ndの場合
- grub.cfg_sda　　　← Cube Pro用（diff デスクトップ/grub.cfg_sda /media/USBメモリ/boot/grub/grub.cfgで差分確認） ← Proの場合
4. 上記終わったら、Cube 2nd 、Cube Pro にUSBを差して、自動インストールできるか確認<br>（USBを挿してリブートしたら何もしないでインストールされるか確認）
5. インストール後、簡易動作確認<br>（OCR読み取り/csv保存、非定型読み取り/csv保存、Sorter実行/csv保存を実行）
