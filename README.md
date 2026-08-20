# AWS CloudFormationで2層ネットワークを構築しよう
堀越 誠一朗（Wealthy Design株式会社）の提供する[AWS Cloud Formationテンプレート](https://github.com/s-horikoshi-public/CloudFormation-Template/tree/main)です。


1.  git cloneコマンド


    ```
    git clone -b network-01 https://github.com/s-horikoshi-public/CloudFormation-Template.git
    ```


2.  環境


    akane というシステムの dev 環境を想定しています。
    同じ構成で違う環境を作成する場合は、{環境名}-parameters.jsonを別途作成します。


    ```
    akane (システム)
      └─ network (スタック)
          ├─ network.yml (CFnテンプレート)
          └─ dev-parameters.json (dev 環境のパラメータ)
    ```


## AWS リソース構築内容
  - VPC (10.0.0.0/16)
  - Publicサブネット1 (10.0.1.0/24)
  - Publicサブネット2 (10.0.2.0/24)
  - Privateサブネット1 (10.0.11.0/24)
  - Privateサブネット2 (10.0.12.0/24)
