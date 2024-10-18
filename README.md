# Lambda API Example

## 概要
このプロジェクトは、AWS LambdaとAPI Gatewayを使用して「Hello, World!」APIを構築するためのサンプルです。

## デプロイ手順
1. **AWS Lambda関数**を作成し、以下のコードを追加します。

    ```python
    def lambda_handler(event, context):
        return {
            'statusCode': 200,
            'body': 'Hello, World!'
        }
    ```

2. **API Gateway**で**REST API**を作成し、**GETメソッド**を設定して、作成したLambda関数をトリガーに設定します。

3. **APIをデプロイ**し、エンドポイントURLを取得します。

---

## テスト方法
以下の`curl`コマンドを使用して、APIが正常に動作することを確認します。

```bash
curl -X GET https://<api-id>.execute-api.<region>.amazonaws.com/dev


## 無料利用枠について
Lambda:
月間 100万件のリクエストまで無料
合計 400,000 GB-秒の実行時間が無料
API Gateway:
REST API の場合、月間 100万件の呼び出しまで無料
