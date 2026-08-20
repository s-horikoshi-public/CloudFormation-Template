# AWS CloudFormationでCloudFormationエンドポイントを使用したEC2インスタンスを構築しよう
堀越 誠一朗（Wealthy Design株式会社）の提供する[AWS Cloud Formationテンプレート](https://github.com/s-horikoshi-public/CloudFormation-Template/tree/main)です。


1.  git cloneコマンド


    ```
    git clone -b vpc-endpoint-02 https://github.com/s-horikoshi-public/CloudFormation-Template.git
    ```


2.  環境


    akane-cfn というシステムの all 環境を想定しています。
    同じ構成で違う環境を作成する場合は、{環境名}-parameters.jsonを別途作成します。


    ```
    akane-cfn (システム)
      ├─ network (スタック)
      |   ├─ network.yml (CFnテンプレート)
      |   └─ all-parameters.json (all 環境のパラメータ)
      ├─ instance-cfn (スタック)
      |   ├─ instance-cfn.yml (CFnテンプレート)
      |   └─ all-parameters.json (all 環境のパラメータ)
      └─ endpoint-cfn (スタック)
