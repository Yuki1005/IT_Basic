## Server仮想化

- 藤本さん　仮想化オンプレ/Cloud設計構築 
- 村上さん　仮想化オンプレ/Cloud設計構築 -> バックアップSW
- 尾崎さん　仮想化 -> DELL設計構築

---

### 目的

- Server仮想化/VMware製品の基礎知識習得
- 仮想Serverのイメージを持つ
- Serverを仮想マシンにするメリット
  - リソースを無駄なく使える
  - メンテナンスしやすく障害対応できる（vMotion, HA)
- デメリット
  - 構成が複雑
  - 障害時の切り分けが大変

---

### 1. Serverの仮想化とは

- コンピュータリソースをSWで抽象化して論理的に利用する技術
- リソースの柔軟性、SW上からのコンポーネント一元管理など自由度の大幅向上が見込める

|名| 特徴|略語|
|------|------|-----|
|Server仮想化|物理マシンに搭載されたHWリソースを抽象化|`SDC`：Software Difined Compute|
|Storage仮想化|HDDなどの記憶媒体を抽象化|`SDS`：Software Difined Storage|
|NW仮想化|物理NWを抽象化|`SDN`：Software Difined Network|
|Client仮想化|Server仮想化技術をお応用してClient端末のデスクトップ環境を抽象化||

<br>

- `Hypervisor`：物理マシンのHWリソースを抽象化し、複数のOSがリソースを共有して利用できるよう管理するSW
  - 主なServer仮想化製品(当社はすべて取り扱い有)：
  - `ESXi(VMware社)` `Hyper-V(Windows OS標準機能)` `AHV(Nutanix社)` `HVM(HPE社 Ubuntu(Linux)KVM)`

#### 物理マシンとAppの構成（一般的）

- 物理Server一台にAppを一つ動かす
  - デメリット：`拡張による機器コスト増` `管理維持コスト増` `構築コスト増` `高スペックを最大限に活用不可`
- 物理Server一台にAppをnつ動かす
  - あまりない、一つのOSが落ちるとすべてのAppが落ちてしまう
- Server仮想化、物理Server一台にHypervisorをかまして1:1の仮想Serverをnつたてる
  - メリット：`1台のOSがクラッシュしてもほかのOSは正常に稼働`
 
