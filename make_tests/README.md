# Make Tests フォルダ

> 美容室エージェントのMake連携テスト関連ファイル

**作成日**: 2026-05-10  
**テスト対象**: 美容室予約相談エージェント  

## 📁 ファイル構成

### 🔧 [shop_agent.md](shop_agent.md)
- **内容**: 美容室エージェントの設定
- **店主プロフィール**: 登戸の美容室オーナー  
- **AIミッション**: 予約整理・悩み特定・接客アドバイス

### 💬 [customer_line.md](customer_line.md)  
- **内容**: 顧客からのLINE相談メッセージ
- **ケース**: パサパサ・広がりの悩み
- **特徴**: 静かな接客希望

### 📊 [customer_analysis.md](customer_analysis.md)
- **内容**: 顧客分析結果と接客アドバイス
- **構成**: スプレッドシート用データ + 5年後を見据えた提案
- **店主こだわり**: 誤魔化さない根本改善アプローチ

## 🔗 Make連携テスト

### Webhookエンドポイント
```
https://hook.eu1.make.com/4goajnimdn8gulcue5m76coh47mg3ynr
```

### テスト実行コマンド
```python
# 基本送信形式
payload = {
    "timestamp": "2026-05-10T12:00:00",
    "client_name": "顧客名", 
    "post_content": "相談内容"
}
```

### テスト結果サマリー
- **Threadsテスト**: 3投稿 ✓
- **美容室テスト**: 8回送信 ✓  
- **成功率**: 100% (11/11回)

## 🎯 使用方法

1. **[shop_agent.md](shop_agent.md)** で店主設定を確認
2. **[customer_line.md](customer_line.md)** でテスト用相談内容を参照
3. **[customer_analysis.md](customer_analysis.md)** で期待される分析結果を確認
4. Make Webhookにテストデータを送信して動作確認

---
*美容室エージェント開発・テスト用ファイル群*