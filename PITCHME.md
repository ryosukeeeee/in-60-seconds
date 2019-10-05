<!-- 1枚目：タイトルスライド -->
# Slackアプリ All Timesについて

<!-- 2枚目 -->
---
@snap[north span-40]
### きっかけ
@snapend

@snap[center]
@fa[slack fa-2x]に#timesが多すぎる
@snapend

<!-- 3枚目 -->
---
@title[Slackスクリーンショット]

@img[span-100 position_center](assets/img/slack_home-original.png)

<!-- 4枚目 -->
+++
@title[Slackスクリーンショット]

@img[span-100](assets/img/slack_home-original-2.png)

<!-- 5枚目 -->
---?color=white
@title[ディストラクタ]

@snap[midpoint span-100 cite]
> 「集中力を削ぐものを、心理学では『ディストラクター』といいます。視界の隅で動くものなど、目に入ってくるものが最も人間の注意力を奪うのですが、工事現場の騒音など、耳から入ってくるものもディストラクターの一種だと考えることができます」
@snapend

@snap[south-east text-03]
cited from [集中力の高め方を心理学者が伝授「ディストラクター」をなくすこと](https://news.livedoor.com/article/detail/10669129/)
@snapend

<!-- 6枚目 -->
---?color=linear-gradient(90deg, white 50%, #D6DBB6 50%)
@title[All Timesの紹介]
@snap[north-east text-center span-50]
### 特徴
@snapend

@snap[west span-30]
![ICON](assets/img/all_times_icon.png)
@snapend

@snap[east span-50]
- ユーザのアイコンで表示
- スレッド形式
@snapend


<!-- 7枚目 -->
---
@title[フロー図]

@snap[center text-center span-100 position_center]
![FLOW](assets/img/all_times_usecase.png)
@snapend

<!-- 7-1 -->
+++

@snap[center text-center span-100]
![FLOW](assets/img/all_times_usecase-1.png)
@snapend

<!-- 7-2 -->
+++

@snap[center text-center span-100]
![FLOW](assets/img/all_times_usecase-2.png)
@snapend

<!-- 7-3 -->
+++

@snap[center text-center span-100]
![FLOW](assets/img/all_times_usecase-3.png)
@snapend

<!-- 7-4 -->
+++

@snap[center text-center span-100]
![FLOW](assets/img/all_times_usecase-4.png)
@snapend

<!-- 7-5 -->
+++

@snap[center text-center span-100]
![FLOW](assets/img/all_times_usecase-5.png)
@snapend

<!-- 7-6 -->
+++

@snap[center text-center span-100]
![FLOW](assets/img/all_times_usecase-6.png)
@snapend

---
@title[event]

@snap[north span-100 text-09]
イベントが発生したときに
送られてくるJSON（一部抜粋）
@snapend

@snap[center]
```json
{
  'token': '********',
  'api_app_id': '********',
  'event': {
    'type': 'message',
    'text': '増税対応お疲れさまでした',
    'user': 'UKDKXN543',
    'channel': 'CP2BU7SCC',
    'ts': '1570282631.000200',
    'team': 'TKT6H65TQ',
  },
  'type': 'event_callback',
  'authed_users': ['UNND549UZ']
}
```
@snapend

@snap[south span-100 text-gray text-08]
@[2-3](tokenとapi_app_idで正当なリクエストか検証)))
@[4-11](発生したイベントに関する情報)
@[5](発生したイベントのタイプ。これはメッセージが投稿されたとき。)
@[6](投稿されたメッセージ内容)
@[7](メッセージを投稿した人の **ID** )
@[8](メッセージを投稿されたチャンネルの **ID** )
@snapend

---
@title[EventHandlerの処理]

@snap[north span-100]
### eventHandlerのお仕事
@snapend


@snap[west span-100]
@ul[list-spaced-bullets text-08]
- チャンネルIDからチャンネル名（ex. times_bengal_cat）を取得
- ユーザーのIDからユーザー名とアイコンのURLを取得
- #all_timesに当日の投稿がすでにあるか調べる
- ある→スレッド形式で投稿
- ない→チャンネル名を投稿し、スレッド形式でメッセージを投稿
@ulend
@snapend

---

@title[feature work]

@snap[north span-100]
### まだ実装されていない機能
@snapend

@snap[west span-100]
@ul[list-spaced-bullets text-09]
- ファイルアップロードイベントの転送
- メッセージ内のURLを展開
@ulend
@snapend


<!-- 最後のスライド -->
---

@snap[center text-18]
Have a good slack life @fa[slack]
@snapend
