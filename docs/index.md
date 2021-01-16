# 21Stepで体得 Vue.jsハンズオン (StepUp! 選書) 関連情報

## 初版訂正情報

### 誤植
現時点で初版において見つかっている誤植です 😰
* p192 2番目のサンプルコード内  
× `import { defineComponent, reactive, toRef }`  
○ `import { defineComponent, reactive, toRefs }`  
* p291 2番目のサンプルコード `calender-event.ts`  
  ×
  ```JavaScript
  import {
    CalendarEventDetail,
    CalendarEventTodayDetail
  } from "@/store/calendar-event.d";
  ```
  ○
  ```JavaScript
  import {
    CalendarEventDetail,
    CalendarEventTodayDetail
  } from "@/store/calendar-event.model";
  ```
* p390 脚注<85>  
URL記述の直前に半角カギ括弧「[ 」の抜け

### Vuetifyドキュメント
ドキュメント改定の影響で、Vuetify2.xの日本語版のURLが変更になりました。

* p282 脚注<44>  
https://vuetifyjs.com/ja/getting-started/quick-start/  
↓  
https://v2.vuetifyjs.com/ja/getting-started/quick-start/

* p283 脚注<46>  
https://vuetifyjs.com/ja/customization/a-la-carte/  
↓  
https://v2.vuetifyjs.com/ja/customization/a-la-carte/

* p285 脚注<48>  
https://vuetifyjs.com/ja/introduction/frequently-asked-questions/#typescript-に追加したとき、-error-could-not-find-a-declaration-file-for-module-vuetify-lib-というエラーが表示されてしまいます  
↓  
https://v2.vuetifyjs.com/ja/introduction/frequently-asked-questions/#typescript-に追加したとき、-error-could-not-find-a-declaration-file-for-module-vuetify-lib-というエラーが表示されてしまいます

* p297 脚注<50>  
https://vuetifyjs.com/ja/getting-started/pre-made-layouts/  
↓  
https://v2.vuetifyjs.com/ja/getting-started/pre-made-layouts/

* p314 脚注<57>  
https://vuetifyjs.com/ja/examples/layouts/centered  
↓  
https://v2.vuetifyjs.com/ja/examples/layouts/centered/

## サンプルアプリケーションについて

### axiosの脆弱性

サンプルアプリケーションで使っている `axios` のバージョンには、`proxy`オプションを使った際の脆弱性が報告されています。  
https://github.com/advisories/GHSA-4w2v-q235-vp99  
稼働環境で利用する場合は `axios` のバージョンを `0.21.1` 以降に上げてください。