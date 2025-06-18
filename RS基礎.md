# Cisco IOS 学習メモ（テスト対策）

---

## 1. コンフィギュレーション（設定）の保存と初期化

### Cisco IOS 設定ファイル

- **startup-config**：
  - 保存場所：
    - Router：NVRAM
    - Switch：フラッシュメモリなどの**不揮発性メモリ**
  - 電源を入れると自動で読み込まれる
- **running-config**：
  - 現在動作中の設定
  - 電源を落とすと消去される（**揮発性メモリ**）

---

## Cisco IOS の基本情報

- **コンソールケーブル**：D-Sub9pin（メス）to LAN（RJ45）
- **USB変換ケーブル**：D-Sub9pin（オス）to USB-A
- **vty (virtual teletype)**：
  - LAN経由で別機器を経由してアクセス
- **IOS（Internetwork Operating System）**：
  - CLIベースのOS、コマンド入力で操作

---

## 1. Tera Term 操作

### 基本操作

- **コピー・ペースト**：`Ctrl + C` / `Ctrl + V`不可、**右クリックで貼り付け**
- **接続方法**
  - Router：表の緑端子（小さい方）
  - Switch：裏の上端子（大きい方）
- **接続手順**
  - Tera Term 起動 → **[シリアル]選択 → OK**
  - Router：コードが出たら「NO」→ `Enter` → `Router>` 表示でOK
  - Switch：`Enter` → `Switch>` 表示でOK
- **Tera Term 設定**
  - 設定 → シリアルポート：
    - 速度：9600
    - データ：8bit
    - パリティ：none
    - ストップビット：1bit
    - フロー制御：none
    - 送信遅延：10, 20

---

## モード一覧

| モード名                   | プロンプト | コマンド                       |
|----------------------------|------------|--------------------------------|
| ユーザEXECモード           | `>`        | `enable` → 特権EXECモードへ     |
| 特権EXECモード             | `#`        | `configure terminal`            |
| グローバルコンフィグモード | `(config)#`| `interface`や`hostname`など設定 |
| インターフェースモード     | `(config-if)#` | ポートごとの設定               |

---

## よく使うコマンド

- `#show running-config`：現在の設定確認
- `#copy running-config startup-config`：設定を保存
- `#erase startup-config`：初期化
- `#reload`：再起動
- `(config)#hostname [name]`：デバイス名変更
- `(config)#no hostname`：初期名に戻す
- `#show ?`：コマンドヘルプ
- `(config)#do [コマンド]`：設定モードでも実行可能

---

## 2. Switchの起動と基本設定（P.36)

- **モジュール型スイッチ**：
  - 自由度は高いが高価
  - 必要に追うおじて各種モジュールを組み合わせられる
- **固定型スイッチ**：
  - 安価だが拡張性低い
  - シャーシにモジュールが固定されている
- **RPSコネクタ**：
  - 冗長電源（今回は未実装）
- **アップリンク／ダウンリンク**：
  - 見た目は同じ、接続先の階層が違うだけ
  - 機器のヒエラルキーから下位の機器につなぐか上位の機器につなぐかの違い
### MACアドレステーブル確認

- `#show mac address-table`
