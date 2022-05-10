# YouTube 頻道 新影片自動撥放器

此專案部屬在 Heroku 上，因使用免費方案，第一次載入 Heroku 需開機約 3~5 秒 [連結](http://youtube-new-video-auto-player.herokuapp.com/).

## 專案簡介

### 專案概念

平時在使用 YouTube 時，因為訂閱太多頻道與推薦影片太雜，時常需要自己到想看的頻道查看是否有上新影片，或是一不留神就一部又一部的看著推薦影片，花掉了許多寶貴時間。

因此我做了這個網站來嘗試解決這個問題，並練習 `React` 與 [其他相關套件](###使用的技能)


網站的主要功能是幫您檢查訂閱頻道是否有新影片，並集合成列表讓您觀看。其中「搜尋頻道」與「檢查是否有新影片」兩個功能需要透過 YouTube API 取得 ( 寫在後端 Express 中 )

### 基本功能

* 您可以在網站中搜尋並訂閱 YouTube 的頻道，網頁會自動整理頻道的最新一部影片，集合成播放清單。

* 網頁依照播放清單的順序播放影片，您也可以點擊播放清單的影片改變播放順序。

* 當您看完影片或是點擊右下角的「把此影片從清單中刪除」，影片便會從清單中被移除。下次該頻道有新影片便會再加入清單。

>YouTube API 每天大概只有 100 次的配額，因此我限制每個頻道至少每 8 小時更新一次，
並且在主頁右上角，點擊「預覽模式」按鈕，則會出現假資料來方便查看網頁的大致切版。



### 使用的技能

* React
主要分成三個元件「SideBar」、「VideoBar」、「VideoPlayer」構成
├─api
├─components
│  ├─infoPage
│  ├─sideBar
│  │  ├─channelItem
│  │  ├─channelList
│  │  └─searchBlock
│  ├─userAssistance
│  │  ├─infoButton
│  │  └─previewButton
│  ├─videoBar
│  │  └─videoItem
│  └─videoPlayer
└─redux
    ├─previewReducer
    ├─subscriptArrayReducer
    └─updateArrayReducer

* Redux


* react-router-dom

123

* axios

123

* styled-components

123

* express

123