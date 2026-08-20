# AWS CloudFormationでLambda Layerを使用したSlack通知定期実行Lambdaを構築しよう
堀越 誠一朗（Wealthy Design株式会社）の提供する[AWS Cloud Formationテンプレート](https://github.com/s-horikoshi-public/CloudFormation-Template/tree/main)です。


1.  git cloneコマンド


    ```
    git clone -b lambda-01 https://github.com/s-horikoshi-public/CloudFormation-Template.git
    ```


2.  環境


    akane というシステムの dev 環境を想定しています。
    同じ構成で違う環境を作成する場合は、{環境名}-parameters.jsonを別途作成します。


    ```
    akane (システム)
      ├── lambda (スタック)
      │     ├── code
      │     │     └── getEC2InfoToSlack.py (S3アーティファクトソース)
      │     ├── code-lambda-getEC2InfoToSlack.zip (S3アーティファクト)
      │     ├── delete_artifact.dev.sh (S3アーティファクト削除シェル)
      │     ├── dev-parameters.json (dev 環境のパラメータ)
