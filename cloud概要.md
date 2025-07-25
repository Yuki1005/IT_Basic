## Cloud概要

[1. Cloudとは](#Cloudとは)

[2. Cloudの特徴](#Cloudの特徴)

[3. Cloud利用のメリット](#Cloud利用のメリット)

[4. Cloudのサービスモデル](#Cloudのサービスモデル)

[5. Cloudの実装モデル](#Cloudの実装モデル)

[6. Cloud利用におけるポイント](#Cloud利用におけるポイント)



##### 課題

[_1. ワーク1](#個人ワーク+グループワーク1)


---

### 目的
- Cloudの基本的な概要を知る
- Cloudに関する用語や機能を知る
- 技術的な内容ではなく、Cloudのイメージをつかむ

--- 

### Cloudとは

- ITリソースではなく**利用形態**
- Cloud Computingの正式名称
- インターネット経由で必要な時必要な分だけ利用することができる `自分で用意する必要がない`

#### 主な事業者名

| 事業社| 名|
| --- | -----|
| Microcoft | Microsoft Azure|
|Amazon | Amazon Web Services|
|Google | Google Cloud|

#### 従来型オンプレミスとの違い

|名|特徴|イメージ|ライトユーザー目線|
|---- | ----|-----|----|
|Cloud|`自社でもたない` `サービスとして利用`|カーシェア |`利用効率：高`|
| オンプレミス | `自社で運用`　`組織の資産として所有` `社内ネットワークを通して利用`|自家用車|`利用効率：低い`|



---

### Cloudの特徴

`オンデマンド/セルフサービス`：サービス業者を介さずネット経由で調達/設定/構築を行うことができる

`ブロードNWアクセス`：様々なデバイスからいつでもどこでもアクセスができる

`リソース共有`：DCのリソースを仮想化し複数のユーザが共有する形態

`急速な拡張`：必要に応じてリソースを迅速に拡大縮小できるため急激な需要変化に対応できる

`計測可能なサービス`：従量課金制

`サービスモデル`：IaaS, PaaS, SaaS の3つにサービスが分類される

`実装モデル`：プラットフォームの所有権/運用責任などの違いに応じてPublic, Private, Hybrid, Communityの4つに分類される


#### 料金モデル

|名|特徴|
|------|------|
|従量課金制|`利用した分だけ料金が発生` `時間/通信料/使用料などに応じ請求金額が変動`|
|固定制/予約制/リザーブ|`一定額をあらかじめ払うことで割引利用` `事業者ごとにリソースに上限や違いあり`|
|オークション制/スポット|`余剰リソースを格安で利用可能` `なくなった場合強制的に中断`|

---

### Cloud利用のメリット

#### 経済性

||メリット|デメリット|
|------|----|-----|
|Cloud|`高コスパ` `初期投資不要`| `過剰投資`|
|オンプレ|`機器購入時の割引` |`余剰リソースの発生`|

- Cloudを利用するとITリソースを資産として所有する必要がない

-  `運用人件費` `IT機器費` `電力/設備費` の削減が期待できる

<br>

 #### 柔軟性

 ||メリット|デメリット|
|------|----|-----|
|Cloud|`高い拡張性` | `Customizeの制限`|
|オンプレ|`Customize性` |`低い拡張性`|


- **用語**

  - スケールアップ：スペックを上げること
  - スケールダウン：スペックを下げること
  - スケールアウト：台数を増やして処理を分担させること
  - スケールイン：台数を減らしてコストを削減すること

- 時間ごとの需要に応じてServer台数を変更調整できる

<br>

 #### 可用性

 Avalability：システムが継続して稼働できる能力のこと

 ||メリット|デメリット|
|------|----|-----|
|Cloud|`障害時もサービス継続可能` | `Cloud事業者のシステム障害`|
|オンプレ|`リソースの完全コントロール` |`高コストと複雑な設計`|


 SLA(Service Level Agreement(%))と呼ばれる基準にて保障される

 |SLA|習慣ダウンタイム|月間ダウンタイム|年間ダウンタイム|
 |----|-----|----|-----|
 |99%|1.68 h |7.2 h | 3.65 days|
 |99.9%| 10.1 min | 43.2 min | 8.76 h|
 |99.99%|5 min | 21.6 min | 4.38 h |
 |99.999%| 6 sec | 25.9 sec | 5.26 min|

<br>

  #### 迅速性


 ||メリット|デメリット|
|------|----|-----|
|Cloud|`短時間で構築` | `パフォーマンス低下時に対処不可`|
|オンプレ|`パフォーマンス低下時に対処可能` |`構築準備に大幅な時間を要す`|


---

### 個人ワーク+グループワーク1

- 現状
  - 自社サーバによるオンプレ環境を運用中
  - 夜間のアクセス増加時のパフォーマンス低下
  - Server管理人員不足
  - 設備の老朽化
  - 費用が気になる

- Cloudとは
  - インターネットを通じてサービスを利用する形態
  - オンプレミスとは異なり必要な時に必要な分だけ利用することが可能
  - 場所を選らばず使用可能で手軽に拡張できる
  
 
- Cloud導入メリット
  - 需要のある時間帯に台数を調整できる柔軟性
  - 利用者にあった料金モデル
  - リソースを資産として所有しないため運用人件費、維持費の削減を見込める

- Cloud導入デメリット
  - 自由にSW,HWを選定できない
  - 事業者のシステム障害、パフォーマンス低下時自分たちで改善できない


---

### Cloudのサービスモデル

役割や責任の分担を定義したもの

<br>

|名|例え|特徴|代表的なサービス|
|----|---|------|------|
|SaaS|コンビニでお弁当を買う|業務用SWの機能をインターネット経由でサービスとして利用できる|`Zoom` `BOX`|
|PaaS|スーパーで買ってきた材料で作る|AppやDB実行用のプラットフォームをインターネット経由で利用できる|`Google App Engine` `Salesforce Platform`|
|IaaS|土地を借りて自分で育てた材料で作る|HWリソースをインターネット経由で利用できる|`Microsoft Azure` `Amazon Web Services`|

<br>

- `SaaS`：
  - Software as a Service
  - インストールやセットアップなく、ブラウザやSWを通じて即座に利用可能
  - アプリケーション層まで完全にサービス化して提供
- `PaaS`：
  - Platform as a Service
  - 開発環境を用意するにあたり管理作業を大幅に簡略化し即座に着手できる
  - HW - MW層までを提供
- `IaaS`：
  - Infrastructure as a Service
  - ユーザーが物理的なHW機器類を購入することなく必要な分を必要な時に利用できる
  - OS、HWリソースを提供

---

### Cloudの実装モデル

|実装モデル|説明|
|-----|-----|
|Public Cloud|サービス利用者が不特定多数の`組織 ` `企業` `個人` であるモデル|
|Private Cloud|サービスの利用者が`特定の組織内`に限定されるモデル|
|Community Cloud|サービスの利用者が`特定の共同体`に限定されるモデル|
|Hybrid Cloud|複数の実装モデルを組み合わせてCloud間の相互運用性、連携性を高めたモデル|

<br>

- Public Cloud：
  - Cloud事業者が所有するDC内のリソース上で一般企業や個人がCloudサービスを利用できるモデル
  - メリット
    - `HW/SW運用管理不要` `地理的制約がなくどこからでもアクセス` `低コスト`
  - デメリット
    - `障害発生時コントロール不可`
- Private Cloud：
  - ほかのユーザと独立した閉じられた環境下でCloudサービスを利用できるモデル
  - メリット
    - `高セキュリティ` `高プライバシー` `柔軟性`
  - デメリット
    - `Publicに比べ費用や運用負荷が高い`
- Hybrid Cloud：
  - 複数の実装モデルを組み合わせてCloud間の相互運用性や連携性を高めたモデル
  - 定常的なものをオンプレミスで、ピーク時需要に応じてCloudリソースを活用することができる
  - メリット
    - `コスト効率` `柔軟性`
  - デメリット
    - `環境の複雑性` `設計難易度の向上`
   

--- 

### Cloud利用におけるポイント

|利用シナリオ|課題|効果|
|-------|-------|------|
|既存の基幹システムの移行/更改|IT資産の所有による運用コスト抑制|コスト削減|
|DR(ディザスタリカバリ)環境の構築|災害時のサービス停止|BCP(事業継続計画)対策による災害時のサービス継続|
|ECサイトの更改|繁忙期に合わせた構成による運用コストの肥大化|アクセスピーク時にリソースを自動的に拡張|
|開発/PoC(概念実証)環境を構築|環境利用をやめる想定のため資産にしたくない<br>開発環境を早く構築/利用したいがServer調達と構築に時間がかかる|早期の利用開始/終了|


#### Cloud by Default

- 政府が推奨するCloudサービス利用にかかる基本方針

- Step0：検討準備
  - 活用にあたりCloud化の対象となるサービスや業務情報を明確化してメリット/コストの検討を行う
- Step1：SaaS（Public Cloud)の利用検討：
  - 検討を踏まえPublicで提供されている場合には利用検討/サービス選定
- Step2：SaaS（Private Cloud)の利用検討：
  - Private利用推奨の場合、各府省の共通システムやプラットフォーム、基板などから提供されるサービスを選定
- Step3：IaaS/PaaS（Public Cloud)の利用検討：
  - SaaSが利用困難/導入にあたってのコスト面などのメリットがない場合検討
- Step4：IaaS/PaaS（Private Cloud)の利用検討：
  - Publicでは扱えない情報を管理したり独自小規模システムの構築の場合検討


#### 留意点

- 事業者起因の障害が発生した場合
  - 主要サービスごとにSLAが定められている
  - SLAに満たない稼働率となった場合、サービスの稼働率に応じた減額対応のみを行う
  - もしCloud上のシステムが止まり損失が企業側に発生しても事業者側は機会損失には関与しない
<br>
- HWのライフサイクルを考慮する必要はなくなるがシステムで使われているSWのライフサイクルに合わせたバージョンアップが必要
- Cloudサービス拠点が海外の場合、各国の法律などの制限によりデータのやり取りで制約が発生する場合あり


---

### Cloudサービス

- 仮想Server
  - HWのリソースをSW的に分割して提供するCloudにおけるもっとも基本となるサービス
  - ユーザー操作用の管理画面から数分 - 数十分程度で構築/起動できる
  - OSイメージを内包した形での構築が可能
  - リージョン：地理的に離れている独立した地域単位
  - AZ：リージョン内の複数のDCから構築されるインフラ設備の単位
- オートケース
  - 仮想Serverやサービスにかかる負荷を監視しトラフィック量やリソース使用率を基準にServer台数を増減させる機能
- 仮想ネットワーク
  - Cloudに自分専用のネットワークを構築できるサービス
  - 基本的な考えはオンプレミスと同様　-> サブネットを使用しネットワークの管理単位を分割
- ロードバランサー
  - アクセス処理を分散させることで大量のアクセスに対応したシステムを構築可能
  - 複数台のServerで構成することから可用性の向上にもつながる
- Storage
  - 仮想的なStorageサービス
  - データ形式や単位に応じた形で利用できる
  - 保存容量は基本無制限で使用に応じた従来課金制

<br>

||ブロックStorage|ファイルStorage|オブジェクトStorage|
|-----|-----|------|------|
|単位|ブロック単位でのアクセス|ファイル単位でのアクセス|オブジェクト単位でのアクセス|
|特徴|高速なデータ転送|階層構造でのデータ管理<br>アクセス制御や属性情報を直感的に管理|更新頻度が少ないデータや大量のデータの保管に使用|
|利用シーン|DBや仮想マシンの起動ディスク|ファイル共有やバックアップ、ドキュメント|静的コンテンツの配信やアーカイブ|
|プロトコル|`iSCSI` `FC`|`CIFS` `NFS` `SMB`|`HTTP(S)` `REST`|


 
