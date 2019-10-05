<!-- 1枚目：タイトルスライド -->
# Slackアプリ All Timesについて

<!-- 2枚目 -->
---
@snap[north span-40 h3-black]
### きっかけ
@snapend

@snap[center]
@fa[slack fa-2x]に#timesが多すぎる
@snapend

<!-- 3枚目 -->
---
@title[Slackスクリーンショット]

@img[span-100](assets/img/slack_home-original.png)

<!-- 4枚目 -->
---
@title[Slackスクリーンショット]

@img[span-100](assets/img/slack_home-original-2.png)

<!-- 4枚目 -->
---
@title[ディストラクタ]

@snap[midpoint span-100 cite]
> 「集中力を削ぐものを、心理学では『ディストラクター』といいます。視界の隅で動くものなど、目に入ってくるものが最も人間の注意力を奪うのですが、工事現場の騒音など、耳から入ってくるものもディストラクターの一種だと考えることができます」
@snapend

@snap[south-east text-03]
cited from [集中力の高め方を心理学者が伝授「ディストラクター」をなくすこと](https://news.livedoor.com/article/detail/10669129/)
@snapend

---


@title[Customize Slide Layout]

@snap[west span-50]
## Customize the Layout
@snapend

@snap[center]
![IMAGE](assets/img/presentation.png)
@snapend

@snap[south span-100 text-white]
Snap Layouts let you create custom slide designs directly within your markdown.
@snapend

---
@title[Add A Little Imagination]

@snap[north-west h4-white]
#### And start presenting...
@snapend

@snap[west span-55]
@ul[list-spaced-bullets text-white text-09]
- You will be amazed
- What you can achieve
- *With a little imagination...*
- And **GitPitch Markdown**
@ulend
@snapend

@snap[east span-45]
@img[shadow](assets/img/conference.png)
@snapend

---

@snap[north-east span-100 text-pink text-06]
Let your code do the talking!
@snapend

```sql zoom-18
CREATE TABLE "topic" (
    "id" serial NOT NULL PRIMARY KEY,
    "forum_id" integer NOT NULL,
    "subject" varchar(255) NOT NULL
);
ALTER TABLE "topic"
ADD CONSTRAINT forum_id
FOREIGN KEY ("forum_id")
REFERENCES "forum" ("id");
```

@snap[south span-100 text-gray text-08]
@[1-5](You can step-and-ZOOM into fenced-code blocks, source files, and Github GIST.)
@[6,7, zoom-13](Using GitPitch live code presenting with optional annotations.)
@[8-9, zoom-12](This means no more switching between your slide deck and IDE on stage.)
@snapend


---?image=assets/img/presenter.jpg

@snap[north span-100 h2-white]
## Now It's Your Turn
@snapend

@snap[south span-100 text-06]
[Click here to jump straight into the interactive feature guides in the GitPitch Docs @fa[external-link]](https://gitpitch.com/docs/getting-started/tutorial/)
@snapend
