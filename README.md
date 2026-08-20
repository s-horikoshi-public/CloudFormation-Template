# AWS CloudFormationでS3にSPA(React)を構築しよう
堀越 誠一朗（Wealthy Design株式会社）の提供する[AWS Cloud Formationテンプレート](https://github.com/s-horikoshi-public/CloudFormation-Template/tree/main)です。


1.  git cloneコマンド


    ```
    git clone -b s3-01 https://github.com/s-horikoshi-public/CloudFormation-Template.git
    ```


2.  環境


    akane というシステムの dev 環境を想定しています。
    同じ構成で違う環境を作成する場合は、{環境名}-parameters.jsonを別途作成します。


    ```
    akane (システム)
      ├── app (Reactアプリ)
      └── s3 (スタック)
          ├─ s3.yml (CFnテンプレート)
          └─ dev-parameters.json (dev 環境のパラメータ)
    ```


## AWS リソース構築内容
  1. s3スタック
      - s3バケット (akane-dev-s3-reacts)
