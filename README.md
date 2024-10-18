# Lambda API Example

## 概要
このプロジェクトは、AWS LambdaとAPI Gatewayを使用して「Hello, World!」APIを構築するためのサンプルです。

## デプロイ手順
1. AWS Lambda関数を作成し、以下のコードを追加します。
   ```python
   def lambda_handler(event, context):
       return {
           'statusCode': 200,
           'body': 'Hello, World!'
       }
