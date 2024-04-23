# yt-tldr
懶得看 YouTube，直接整理重點給你！

這個 Bash Script 會自動下載 YouTube 影片的字幕或音訊，並使用 Whisper 和 ollama 產生影片內容摘要。

## 功能

- 根據提供的 YouTube 影片 URL，自動下載影片的字幕（如果有的話）或音訊
- 如果找到字幕，則提取字幕文字並保存到輸出檔案中
- 如果找不到字幕，則下載影片的音訊，使用 Whisper 進行語音轉錄，產生逐字稿
- 使用 ollama 對逐字稿進行摘要，產生影片內容摘要並保存到摘要檔案中

## 使用方法

1. 確保已安裝以下：
   - [yt-dlp](https://github.com/yt-dlp/yt-dlp)：用於下載 YouTube 影片的字幕或音訊
   - [Whisper](https://github.com/openai/whisper)：用於進行語音轉錄
   - [ollama](https://github.com/OllieStanley/ollama)：用於生成摘要（腳本中使用 llama3 模型）

2. 將腳本下載到本機，並賦予執行權限：
   ```
   chmod +x yt-tldr.sh
   ```

3. 執行腳本，並提供 YouTube 影片的 URL 作為參數：
   ```
   ./yt-tldr.sh <YouTube_URL>
   ```

4. 腳本將自動下載字幕或音訊，產生逐字稿和摘要，並將結果保存到以影片 ID 命名的檔案中。

## 注意事項

- 這個腳本只是作者個人使用的工具，可能存在 bug 或功能不完善的情況。
- 歡迎自行修改和改進腳本以滿足個人需求。
