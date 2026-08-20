# AWS CloudFormationでCloud9を構築しよう
堀越 誠一朗（Wealthy Design株式会社）の提供する[AWS Cloud Formationテンプレート](https://github.com/s-horikoshi-public/CloudFormation-Template/tree/main)です。


1.  git cloneコマンド


    ```
    git clone -b waf-01 https://github.com/s-horikoshi-public/CloudFormation-Template.git
    ```


2.  環境


    akane というシステムの dev 環境を想定しています。
    同じ構成で違う環境を作成する場合は、{環境名}-parameters.jsonを別途作成します。


    ```
    akane (システム)
      ├── network (スタック)
      │   ├── dev-parameters.json (dev 環境のパラメータ)
      │   └── network.yml (CFnテンプレート)
      └── cloud9 (スタック)
          ├── dev-parameters.json (dev 環境のパラメータ)
          └── cloud9.yml (CFnテンプレート)
    ```


## AWS リソース構築内容
  1. networkスタック
