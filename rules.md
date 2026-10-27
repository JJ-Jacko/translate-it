# Rules

## Keep technical identifiers
Keep variable names, class names, package name, API names,
environment variable names, commands, and original log text unchanged.
### Few-Shot
EN -> SC (CN) / TC (HK)
#### Source
```python
text = "My number: 10099. My girl number: 10086"
```
#### ✔️ Correct
```python
text = "我的号码是：10099，我女友的是 10086"
```
```python
text = "我嘅電話號碼係：10099，我女朋友嘅係 10086"
```
#### ❌ Incorrect
```python
文本 = "我的号码是：10099，我女友的是 10086"
```
```python
文本 = "我嘅電話號碼係：10099，我女朋友嘅係 10086"
```

## Keep common English technical terms
Such as:
* `API`
* `Git`
* `Github`
* `CI/CD`

## Use natural Hong Kong Traditional Chinese
Use Traditional characters and local wording.
Do not just convert Simplified characters one by one.
Adjust the words and tone for Hong Kong readers.
### Few-Shot
SC (CN) -> TC (HK)
#### Source
请检查服务器日志，确认 API 请求是否超时。修复后重新部署到生产环境。
#### ✔️ Correct
* **Written Chinese + common English terms**:
請檢查伺服器日誌，確認 API request 是否逾時。修正後再部署至 production。
* **Written Cantonese + English**:
麻煩 check 下 server log，睇下 API request 有冇 timeout。修好之後再 deploy 上 production。
#### ❌ Incorrect
請檢查服務器日誌，確認 API 請求是否超時。修復後重新部署到生產環境。

## Do not over-localize
Do not turn every technical term into Cantonese or an uncommon Chinese word.
Accuracy, clarity, and consistency come first.
### Few-Shot
EN -> TC (HK)
* `Full-stack` -> ✔️ `Full-stack`
* `Full-stack` -> ❌ `全棧`
* `Full-stack Developer` -> ✔️ `Full-stack 工程師`
* `Full-stack Developer` -> ❌ `全棧工程師`
* `Web Scraping / Scraper / Crawler` -> ✔️ `Web Scraping / Scraper / Crawler`
* `Web Scraping / Scraper / Crawler` -> ❌ `(網絡)爬蟲`
