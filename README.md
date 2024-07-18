_如果你想要知道如何將markdown檔案中的圖片換成網路連結，可以參考根目錄下的「如何上傳markdown圖片.md」_

### 以下是新版文章上傳與上tags方式：
現行方案：將tags放在markdown檔案中，所有文章在同一資料夾

[範例文章](https://github.com/NCU-FRESH/2024-blog/blob/main/Posts/%E6%96%B0%E7%89%880704%E7%AF%84%E4%BE%8B%E8%B2%BC%E6%96%87.md?plain=1)

請將「檔案名稱」設為「貼文名稱」，例如：貼文1.md

請將「所有」文章都放在根目錄下的「Posts資料夾」

所有上傳的文章請遵守以下格式：

一、在所有檔案前面，新增yaml資料(可以理解為metadata)

_Example：_

\-\-\-

title: "新版0704範例貼文"

tags: ["我只是測試", "這裡是放Tags", "拜託別自己亂創tag"]

date: 2024-07-03

\-\-\-

#### yaml資料有幾個規則：

a. 他包在兩行的三個減號中

b. 他必須在檔案第一行

#### title, tags, date 的說明：

- title：文章的標題
- tags：文章的tags，像是Life, Mustread，在引號裡面，用逗號隔開，文字要雙引號。範例檔案的"我只是測試", "這裡是放Tags", "拜託別自己亂創tag" 都是一個 tag，請確保你使用的tag都有在下方的表出現
- date：你更新或上傳這篇文章的日期


### 重要
以上這些都很重要，你填錯或亂填都會讓文章抓不到

你上傳的md檔案，所有引用的連結都必須是「網路連結」，而不是「相對路徑」

這技術目前目前可行，但不代表之後不會出問題，所以上傳具有yaml資料的md檔前，請先「備份」原始的md檔案(不含yaml的)，以防之後出問題解決之便。

## 目前認可的tags
(若有不足，歡迎提出)(請不要包含中文)

Information(最新消息)

Blog,
Life, Study, Entertainment, Department, QA

Mustread,
Undergraduate(大學部), Graduate(研究所)

Instruction(入學須知), Counseling(新生輔導), Learning(學習資訊), Dormitory(宿舍相關)

###### 筆記
入學須知第一篇必須是 學士班註冊通知
第二篇必須是學雜費繳費

新生輔導第一篇必須是新生營
