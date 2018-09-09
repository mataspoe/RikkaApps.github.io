# 一切看起來正常，但重新導向完全不起作用。

在“開發者設定”中檢查 log 是否開啟。

另外，據使用者反饋，在 Huawei EMUI 上 log 預設關閉 log。如果你在使用 EMUI，請自行查詢如何在 EMUI 上開啟 log。

# 開啟重新導向後程式先前建立的檔案會被自動移動嗎？

不會。內建儲存中建立的檔案並沒有所有者，因此無法實現自動移動，你可以手動移動或刪除那些檔案。

# 開啟了重新導向的應用會被自動授予儲存權限，這是正常情況嗎？

是的。在應用執行中授予儲存權限將導致重新導向失效，因此強制自動授予。

# 被重新導向的程式仍會產生檔案。

受原理所限，重新導向執行必定**可能**晚於被重定向程式本身邏輯。使用 [增強模組](https://rikka.app/storage_redirect/docs/zh-TW/?doc=%E5%A2%9E%E5%BC%B7%E6%A8%A1%E7%B5%84) 以解決該問題。

此外，若程式使用系統“下載管理器”下載檔案，受原理所限，下載的檔案將無法被重新導向。此問題未來可能會藉助增強模組解決。

# 無法在被重新導向程式內找到檔案。

請先閱讀 [關於重新導向](https://rikka.app/storage_redirect/docs/zh-TW/?doc=關於重新導向)。

若檔案不在“非重新導向資料夾”內，請將其移動至“非重新導向資料夾”中或更改“非重新導向資料夾”設定。

如已確定設定無誤但仍無法找到檔案，請嘗試清除程式資料（可選？），從程式詳情詳情關閉再開啟該程式的儲存權限。

# 無法從被重新導向程式開啟檔案。

> 例項：「微信」的「用其他程式開啟」會提示找不到檔案。

這是由於被重新導向程式設計上的問題，直接將檔案路徑傳遞給其他程式，對其他程式來說該路徑是錯誤的，因此無法找到。

對於該問題，請使用 [連結](https://rikka.app/storage_redirect/docs/zh-TW/?doc=關於連結) 功能來解決。
  
新增正確的規則後，當有新檔案時就會發送通知，此時只需點選通知開啟檔案即可。（大多數流行程式都已有使用者提交的規則，直接新增即可）

> 例項：“微信”中正確開啟接收的檔案的方式
>
> ![正確開啟方式](./../en/images/open_with_0.png)

此外還可以通過系統的“檔案”程式（DocumentUI）找到檔案。

> 例項：使用“檔案”程式找到收到的檔案
>
> ![“檔案”程式](./../en/images/open_with_1.png)

# 無法分享至被重新導向程式

這是由於被重新導向程式（可能也包括分享的程式）設計上的問題。

請下載我們的 [Bridge](https://play.google.com/store/apps/details?id=moe.shizuku.bridge) 程式，使用他的“轉發分享”功能來解決這個問題。（也可能等待我們提供另外的解決方案）