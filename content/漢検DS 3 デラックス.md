---
draft: false
---
==INTRO==
## Question Types
==the entirety of this table must be verified. note notes levels column does not go beyond level 2==
%% This table serves as a master copy for the actual table which is displayed with some decompilation-relevant metadata removed. 

| Hex ID | Type          | Answer Format                      | Input Type        | Key Fields                          | Notes / Levels                             | Question Count |
| ------ | ------------- | ---------------------------------- | ----------------- | ----------------------------------- | ------------------------------------------ | -------------- |
| 0x01   | かな（2択）        | 2-choice kana selection            | choice            | `prompt` `choices` `answer`             | Basic kana for kanji. Levels 10-8.         |                |
| 0x0A   | とめはね（2択）      | 2-choice stroke end (stop/hook)    | choice            | `prompt` `choices` `answer`             | Stroke detail judgment. Levels 10-7.       |                |
| 0x14   | 音訓判定（4択）      | 4-choice on/kun reading            | choice            | `prompt` `choices` `answer`             | Distinguish onyomi/kunyomi. Levels 9-2.    |                |
| 0x15   | 音訓判定（2択）      | 2-choice on/kun reading            | choice            | `prompt` `choices` `answer`             | Simplified version. Levels 10-5.           |                |
| 0x1E   | 筆順（数値）        | numeric stroke order               | numeric           | `prompt` `answer`         | Order strokes 1-N. Levels 10-5.            |                |
| 0x28   | 漢字選択（12択）     | 12-choice kanji pick               | choice            | `prompt` `choices` `answer`             | Many distractors. Levels 8-2.              |                |
| 0x29   | 同音・同訓異字       | homophone/homonym match            | multi_select/text | `prompt` `answer` `alt_answer`          | Pair same sound/meaning diffs. Levels 7-2. |                |
| 0x2A   | 漢字選択（5択）      | 5-choice kanji pick                | choice            | `prompt` `choices` `answer`             | Medium distractors. Levels 9-4.            |                |
| 0x2B   | 漢字選択（3択）      | 3-choice kanji pick                | choice            | `prompt` `choices` `answer`             | Few distractors. Levels 10-6.              |                |
| 0x32   | 誤字訂正          | misuse/misstroke correction        | text              | `prompt` `answer` `alt_answer`          | Fix wrong kanji in sentence. Levels 6-2.   |                |
| 0x3C   | 四字熟語（10択）     | 10-choice idiom                    | choice            | `prompt` `choices` `answer` `full_idiom` | 4-char idioms select. Levels 5-2.          |                |
| 0x3D   | 四字熟語（筆記2文字）   | idiom 2 missing chars              | text              | `prompt` `answer` `full_idiom`          | Partial writing. Levels 5-2.               |                |
| 0x3E   | 四字熟語（筆記）      | idiom writing                      | text              | `prompt` `answer` `full_idiom`          | Complete 4-char. Levels 4-2.               |                |
| 0x46   | 熟語の構成（5択）     | 5-choice compound breakdown        | choice            | `prompt` `choices` `answer`             | Parts of compounds. Levels 6-2.            |                |
| 0x47   | 熟語の構成（4択）     | 4-choice compound breakdown        | choice            | `prompt` `choices` `answer`             | Simplified. Levels 7-3.                    |                |
| 0x50   | 書き取り          | kanji writing from reading         | text              | `prompt` `answer` `reading`             | Dictation. Levels 10-2.                    |                |
| 0x5A   | 送りがな          | okurigana attachment               | text/choice       | `prompt` `answer`                      | Ruby rules. Levels 8-2.                    |                |
| 0x64   | 対義語・類義語       | antonym/synonym                    | choice/text       | `prompt` `choices` `answer`             | Word relations. Levels 7-2.                |                |
| 0x6E   | 読み            | reading selection/writing          | choice/text       | `prompt` `choices` `answer` `reading`    | Kanji to kana. Levels 10-2.                |                |
| 0x78   | 二字熟語（10択2連）   | 10-choice 2-pick                   | choice            | `prompt` `choices` `answer`             | 2-char compounds x2. Levels 6-2.           |                |
| 0x79   | 二字熟語（5択2連）    | 5-choice 2-pick                    | choice            | `prompt` `choices` `answer`             | Paired medium. Levels 7-3.                 |                |
| 0x7A   | 二字熟語（12択2連）   | 12-choice 2-pick                   | choice            | `prompt` `choices` `answer`             | Paired hard. Levels 5-2.                   |                |
| 0x82   | 画数（数値）        | numeric stroke count               | numeric           | `prompt` `answer`                      | Count strokes. Levels 10-6.                |                |
| 0x8C   | 部首識別（10択ひらがな） | 10-choice radical (hiragana)       | choice            | `prompt` `choices` `answer`             | Radical name kana. Levels 9-4.             |                |
| 0x8D   | 部首識別（10択漢字）   | 10-choice radical (kanji)          | choice            | `prompt` `choices` `answer`             | Radical kanji. Levels 8-3.                 | 0              |
| 0x8E   | 部首（4択）        | 4-choice radical pick              | choice            | `prompt` `choices` `answer`             | Basic radical ID. Levels 10-7.             |                |
| 0x8F   | 部首＋読み→漢字（筆記）  | radical + reading to kanji (write) | text              | `prompt` `answer` `reading`             | Compose from parts. Levels 7-2.            |                |
| 0x90   | 部首（3択）        | 3-choice radical pick              | choice            | `prompt` `choices` `answer`             | Easy radical. Levels 10-8.                 |                |
| 0xBE   | 表外の読み         | non-joyo readings                  | text/choice       | `prompt` `answer` `reading`             | Rare readings. Levels 4-2.                 |                |
| 0xC8   | 書き換え・旧字体      | old to new font conversion         | text              | `prompt` `answer` `alt_answer`          | Kyūjitai ↔ Shinjitai. Levels 3-2.          |                |
%%

| Type          | Answer Format                      | Input Type        | Key Fields                               | Notes / Levels                             | Question Count |
| ------------- | ---------------------------------- | ----------------- | ---------------------------------------- | ------------------------------------------ | -------------- |
| かな（2択）        | 2-choice kana selection            | choice            | `prompt` `choices` `answer`              | Basic kana for kanji. Levels 10-8.         |                |
| とめはね（2択）      | 2-choice stroke end (stop/hook)    | choice            | `prompt` `choices` `answer`              | Stroke detail judgment. Levels 10-7.       |                |
| 音訓判定（4択）      | 4-choice on/kun reading            | choice            | `prompt` `choices` `answer`              | Distinguish onyomi/kunyomi. Levels 9-2.    |                |
| 音訓判定（2択）      | 2-choice on/kun reading            | choice            | `prompt` `choices` `answer`              | Simplified version. Levels 10-5.           |                |
| 筆順（数値）        | numeric stroke order               | numeric           | `prompt` `answer`                        | Order strokes 1-N. Levels 10-5.            |                |
| 漢字選択（12択）     | 12-choice kanji pick               | choice            | `prompt` `choices` `answer`              | Many distractors. Levels 8-2.              |                |
| 同音・同訓異字       | homophone/homonym match            | multi_select/text | `prompt` `answer` `alt_answer`           | Pair same sound/meaning diffs. Levels 7-2. |                |
| 漢字選択（5択）      | 5-choice kanji pick                | choice            | `prompt` `choices` `answer`              | Medium distractors. Levels 9-4.            |                |
| 漢字選択（3択）      | 3-choice kanji pick                | choice            | `prompt` `choices` `answer`              | Few distractors. Levels 10-6.              |                |
| 誤字訂正          | misuse/misstroke correction        | text              | `prompt` `answer` `alt_answer`           | Fix wrong kanji in sentence. Levels 6-2.   |                |
| 四字熟語（10択）     | 10-choice idiom                    | choice            | `prompt` `choices` `answer` `full_idiom` | 4-char idioms select. Levels 5-2.          |                |
| 四字熟語（筆記2文字）   | idiom 2 missing chars              | text              | `prompt` `answer` `full_idiom`           | Partial writing. Levels 5-2.               |                |
| 四字熟語（筆記）      | idiom writing                      | text              | `prompt` `answer` `full_idiom`           | Complete 4-char. Levels 4-2.               |                |
| 熟語の構成（5択）     | 5-choice compound breakdown        | choice            | `prompt` `choices` `answer`              | Parts of compounds. Levels 6-2.            |                |
| 熟語の構成（4択）     | 4-choice compound breakdown        | choice            | `prompt` `choices` `answer`              | Simplified. Levels 7-3.                    |                |
| 書き取り          | kanji writing from reading         | text              | `prompt` `answer` `reading`              | Dictation. Levels 10-2.                    |                |
| 送りがな          | okurigana attachment               | text/choice       | `prompt` `answer`                        | Ruby rules. Levels 8-2.                    |                |
| 対義語・類義語       | antonym/synonym                    | choice/text       | `prompt` `choices` `answer`              | Word relations. Levels 7-2.                |                |
| 読み            | reading selection/writing          | choice/text       | `prompt` `choices` `answer` `reading`    | Kanji to kana. Levels 10-2.                |                |
| 二字熟語（10択2連）   | 10-choice 2-pick                   | choice            | `prompt` `choices` `answer`              | 2-char compounds x2. Levels 6-2.           |                |
| 二字熟語（5択2連）    | 5-choice 2-pick                    | choice            | `prompt` `choices` `answer`              | Paired medium. Levels 7-3.                 |                |
| 二字熟語（12択2連）   | 12-choice 2-pick                   | choice            | `prompt` `choices` `answer`              | Paired hard. Levels 5-2.                   |                |
| 画数（数値）        | numeric stroke count               | numeric           | `prompt` `answer`                        | Count strokes. Levels 10-6.                |                |
| 部首識別（10択ひらがな） | 10-choice radical (hiragana)       | choice            | `prompt` `choices` `answer`              | Radical name kana. Levels 9-4.             |                |
| 部首識別（10択漢字）   | 10-choice radical (kanji)          | choice            | `prompt` `choices` `answer`              | Radical kanji. Levels 8-3.                 | 0              |
| 部首（4択）        | 4-choice radical pick              | choice            | `prompt` `choices` `answer`              | Basic radical ID. Levels 10-7.             |                |
| 部首＋読み→漢字（筆記）  | radical + reading to kanji (write) | text              | `prompt` `answer` `reading`              | Compose from parts. Levels 7-2.            |                |
| 部首（3択）        | 3-choice radical pick              | choice            | `prompt` `choices` `answer`              | Easy radical. Levels 10-8.                 |                |
| 表外の読み         | non-joyo readings                  | text/choice       | `prompt` `answer` `reading`              | Rare readings. Levels 4-2.                 |                |
| 書き換え・旧字体      | old to new font conversion         | text              | `prompt` `answer` `alt_answer`           | Kyūjitai ↔ Shinjitai. Levels 3-2.          |                |
# Level Overview
The below table covers the number of questions available per level of study, the number of different sections (questions types)^[note that multiple sections may have identical question types, for example reading]

| Metric                    |       10級 |           9級 |          8級 |                   7級 |     6級 |     5級 |     4級 |     3級 |    準2級 |     2級 |    準1級 |     1級 |
| ------------------------- | --------: | -----------: | ----------: | -------------------: | -----: | -----: | -----: | -----: | -----: | -----: | -----: | -----: |
| Question Count            |     $2,850$ |        $3,150$ |       $4,799$ |                $5,760$ |  $5,415$ |  $5,760$ |  $5,750$ |  $5,750$ |  $5,458$ |  $5,509$ |    $929$ |    $951$ |
| Cumulative Question Count |           |        $6,000$ |      $10,799$ |               $16,559$ | $21,974$ | $27,734$ | $33,484$ | $39,234$ | $44,629$ | $50,201$ | $51,130$ | $52,081$ |
| Section Count             |         8 |            7 |           8 |                   11 |     11 |     11 |     10 |     10 |     10 |     10 |     10 |      9 |
| 読み (0x6E)                 | 900 (32%) |  1,200 (38%) | 1,919 (40%) |                    ● |      ● |      ● |      ● |      ● |      ● |      ● |      ● |      ● |
| 書き取り (0x50)               | 900 (32%) |    750 (24%) | 1,440 (30%) |                    ● |      ● |      ● |      ● |      ● |      ● |      ● |      ● |      ● |
| Numerics                  |       600 |          300 |         480 |                    ● |      ● |      ● |      ● |      ● |      ● |      ● |      ● |      ● |
| Introduced Types          |       対義語 | とめはね<br>部　　首 |        送りがな | 漢字選択<br>音　　訓<br>二字熟語 |      ● |      ● |      ● |      ● |      ● |      ● |      ● |      ● |
Type Frequency: (generated by AI - completely wrong) (table incomplete - was copied from a level breakdown table below)
読み　　　████████░░░░░░░░░░░░ 40%
書き取り　██████░░░░░░░░░░░░░░ 30%
画数　　　████░░░░░░░░░░░░░░░░ 20%
部首　　　████░░░░░░░░░░░░░░░░ 20%
送りがな　█░░░░░░░░░░░░░░░░░░░ 5%
# Todo
- [ ] work out why some sections are repeated. Should those sections be merged in the below tables or not? Why?
# Level Breakdown
## Level 10

| Section | Hex ID | Type    | Input   | Questions | Slug         |
| ------- | ------ | ------- | ------- | --------- | ------------ |
| 0       | 0x6E   | 読み      | text    | 600       | yomi         |
| 1       | 0x82   | 画数（数値）  | numeric | 300       | kakusuu      |
| 2       | 0x1E   | 筆順（数値）  | numeric | 300       | hitsujun     |
| 3       | 0x6E   | 読み      | text    | 300       | yomi         |
| 4       | 0x01   | かな（2択）  | choice  | 150       | kana-2choice |
| 5       | 0x50   | 書き取り    | text    | 450       | kakitori     |
| 6       | 0x64   | 対義語・類義語 | text    | 300       | tai-rui      |
| 7       | 0x50   | 書き取り    | text    | 450       | kakitori     |
## Level 9

| #   | Hex ID   | Type         | Input   | Questions | Slug            |
| --- | -------- | ------------ | ------- | --------- | --------------- |
| 0   | 0x6E     | 読み           | text    | 900       | yomi            |
| 1   | 0x82     | 画数（数値）       | numeric | 300       | kakusuu         |
| 2   | 0x6E     | 読み           | text    | 300       | yomi            |
| 3   | 0x64     | 対義語・類義語      | text    | 300       | tai-rui         |
| 4   | 0x8F | 部首+読み→漢字（筆記） | text    | 300       | bushu-yomi-kaki |
| 5   | 0x0A | とめはね（2択）     | choice  | 300       | tomehane        |
| 6   | 0x50     | 書き取り         | text    | 750       | kakitori        |
## Level 8

| #   | Hex ID | Type         | Input   | Questions | Slug            |
| --- | ------ | ------------ | ------- | --------- | --------------- |
| 0   | 0x6E   | 読み           | text    | 1,439     | yomi            |
| 1   | 0x82   | 画数（数値）       | numeric | 480       | kakusuu         |
| 2   | 0x64   | 対義語・類義語      | text    | 240       | tai-rui         |
| 3   | 0x8F   | 部首+読み→漢字（筆記） | text    | 480       | bushu-yomi-kaki |
| 4   | 0x50   | 書き取り         | text    | 480       | kakitori        |
| 5   | 0x5A   | 送りがな         | text    | 240       | okurigana       |
| 6   | 0x6E   | 読み           | text    | 480       | yomi            |
| 7   | 0x50   | 書き取り         | text    | 960       | kakitori        |
Type Frequency: (generated by AI - completely wrong)
読み　　　████████░░░░░░░░░░░░ 40%
書き取り　██████░░░░░░░░░░░░░░ 30%
画数　　　████░░░░░░░░░░░░░░░░ 20%
部首　　　████░░░░░░░░░░░░░░░░ 20%
送りがな　█░░░░░░░░░░░░░░░░░░░ 5%
## Level 7
| #   | Hex ID | Type       | Input   | Questions | Slug            |
| --- | ------ | ---------- | ------- | --------- | --------------- |
| 0   | 0x6E   | 読み         | text    | 960       | yomi            |
| 1   | 0x6E   | 読み         | text    | 480       | yomi            |
| 2   | 0x2B   | 漢字選択（3択）   | choice  | 480       | kanji-sentaku-3 |
| 3   | 0x82   | 画数（数値）     | numeric | 480       | kakusuu         |
| 4   | 0x15   | 音訓判定（2択）   | choice  | 480       | onkun-2choice   |
| 5   | 0x64   | 対義語・類義語    | text    | 240       | tai-rui         |
| 6   | 0x5A   | 送りがな       | text    | 336       | okurigana       |
| 7   | 0x8F   | 部首+読み→漢字   | text    | 480       | bushu-yomi-kaki |
| 8   | 0x50   | 書き取り       | text    | 384       | kakitori        |
| 9   | 0x79   | 二字熟語（5択2連） | choice  | 480       | niji-5x2        |
| 10  | 0x50   | 書き取り       | text    | 960       | kakitori        |
## Level 6
| #     | Hex ID   | Type          | Input   | Questions | Slug                 |
| ----- | -------- | ------------- | ------- | --------- | -------------------- |
| 0     | 0x6E     | 読み            | text    | 960       | yomi                 |
| 1     | 0x5A     | 送りがな          | text    | 240       | okurigana            |
| 2 | 0x90 | 部首（3択）    | choice  | 135   | bushu-3          |
| 3     | 0x82     | 画数            | numeric | 480       | kakusuu              |
| 4 | 0x47 | 熟語の構成（4択） | choice  | 480   | jukugo-kousei-4  |
| 5 | 0x3E | 四字熟語（筆記）  | text    | 480   | yoji-jukugo      |
| 6     | 0x64     | 対義語・類義語       | text    | 480       | tai-rui              |
| 7 | 0x28 | 漢字選択（12択） | choice  | 288   | kanji-sentaku-12 |
| 8     | 0x14     | 音訓判定（4択）      | choice  | 480       | onkun-4choice        |
| 9     | 0x50     | 書き取り          | text    | 432       | kakitori             |
| 10    | 0x50     | 書き取り          | text    | 960   | kakitori             |
## Level 5
| #   | Hex ID | Type          | Input   | Questions | Slug            |
| --- | ------ | ------------- | ------- | --------- | --------------- |
| 0   | 0x6E   | 読み            | text    | 960       | yomi            |
| 1   | 0x8C   | 部首識別（10択ひらがな） | choice  | 480       | bushu-10h       |
| 2   | 0x82   | 画数            | numeric | 480       | kakusuu         |
| 3   | 0x5A   | 送りがな          | text    | 240       | okurigana       |
| 4   | 0x14   | 音訓判定（4択）      | choice  | 480       | onkun-4choice   |
| 5   | 0x3E   | 四字熟語（筆記）      | text    | 480       | yoji-jukugo     |
| 6   | 0x64   | 対義語・類義語       | text    | 480       | tai-rui         |
| 7   | 0x78   | 二字熟語（10択2連）   | choice  | 240       | niji-10x2       |
| 8   | 0x46   | 熟語の構成（5択）     | choice  | 480       | jukugo-kousei-5 |
| 9   | 0x50   | 書き取り          | text    | 480       | kakitori        |
| 10  | 0x50   | 書き取り          | text    | 960       | kakitori        |
## Level 4
| #   | Hex ID | Type      | Input  | Questions | Slug            |
| --- | ------ | --------- | ------ | --------- | --------------- |
| 0   | 0x6E   | 読み        | text   | 1,440     | yomi            |
| 1   | 0x2A   | 漢字選択（5択）  | choice | 720       | kanji-sentaku-5 |
| 2   | 0x29   | 同音・同訓異字   | choice | 240       | douon-dokunji   |
| 3   | 0x46   | 熟語の構成（5択） | choice | 470       | jukugo-kousei-5 |
| 4   | 0x8E   | 部首（4択）    | choice | 480       | bushu-4         |
| 5   | 0x64   | 対義語・類義語   | text   | 480       | tai-rui         |
| 6   | 0x5A   | 送りがな      | text   | 240       | okurigana       |
| 7   | 0x3E   | 四字熟語（筆記）  | text   | 480       | yoji-jukugo     |
| 8   | 0x32   | 誤字訂正      | text   | 240       | goji-teisei     |
| 9   | 0x50   | 書き取り      | text   | 960       | kakitori        |
## Level 3
Identical to Level 4?

| #   | Hex ID | Type      | Input  | Questions | Slug            |
| --- | ------ | --------- | ------ | --------- | --------------- |
| 0   | 0x6E   | 読み        | text   | 1,440     | yomi            |
| 1   | 0x2A   | 漢字選択（5択）  | choice | 720       | kanji-sentaku-5 |
| 2   | 0x29   | 同音・同訓異字   | choice | 240       | douon-dokunji   |
| 3   | 0x46   | 熟語の構成（5択） | choice | 470       | jukugo-kousei-5 |
| 4   | 0x8E   | 部首（4択）    | choice | 480       | bushu-4         |
| 5   | 0x64   | 対義語・類義語   | text   | 480       | tai-rui         |
| 6   | 0x5A   | 送りがな      | text   | 240       | okurigana       |
| 7   | 0x3E   | 四字熟語（筆記）  | text   | 480       | yoji-jukugo     |
| 8   | 0x32   | 誤字訂正      | text   | 240       | goji-teisei     |
| 9   | 0x50   | 書き取り      | text   | 960       | kakitori        |
## Level Pre-2
| #   | Hex ID | Type      | Input  | Questions | Slug            |
| --- | ------ | --------- | ------ | --------- | --------------- |
| 0   | 0x6E   | 読み        | text   | 1,440 | yomi            |
| 1   | 0x8E   | 部首（4択）    | choice | 188       | bushu-4         |
| 2   | 0x2A   | 漢字選択（5択）  | choice | 720   | kanji-sentaku-5 |
| 3   | 0x46   | 熟語の構成（5択） | choice | 470       | jukugo-kousei-5 |
| 4   | 0x29   | 同音・同訓異字   | choice | 240       | douon-dokunji   |
| 5   | 0x64   | 対義語・類義語   | text   | 480       | tai-rui         |
| 6   | 0x5A   | 送りがな      | text   | 240       | okurigana       |
| 7   | 0x3E   | 四字熟語（筆記）  | text   | 480       | yoji-jukugo     |
| 8   | 0x32   | 誤字訂正      | text   | 240       | goji-teisei     |
| 9   | 0x50   | 書き取り      | text   | 960   | kakitori        |
## Level 2
| #   | Hex ID | Type        | Input  | Questions | Slug            |
| --- | ------ | ----------- | ------ | --------- | --------------- |
| 0   | 0x6E   | 読み          | text   | 1,440     | yomi            |
| 1   | 0x8E   | 部首（4択）      | choice | 239       | bushu-4         |
| 2   | 0x46   | 熟語の構成（5択）   | choice | 470       | jukugo-kousei-5 |
| 3   | 0x3D   | 四字熟語（筆記2文字） | text   | 480       | yoji-kaki       |
| 4   | 0x3C   | 四字熟語（10択）   | choice | 240       | yoji-imi        |
| 5   | 0x64   | 対義語・類義語     | text   | 480       | tai-rui         |
| 6   | 0x50   | 書き取り        | text   | 480       | kakitori        |
| 7   | 0x32   | 誤字訂正        | text   | 240       | goji-teisei     |
| 8   | 0x5A   | 送りがな        | text   | 240       | okurigana       |
| 9   | 0x50   | 書き取り        | text   | 1,200     | kakitori        |
## Level Pre-1
| #   | Hex ID | Type     | Input | Qs  | Slug            |
| --- | ------ | -------- | ----- | --- | --------------- |
| 0   | 0x6E   | 読み       | text  | 284 | yomi            |
| 1   | 0x6E   | 読み（訓読み）  | text  | 86  | kunyomi         |
| 2   | 0x6E   | 書き取り（熟語） | text  | 77  | kakitori-jukugo |
| 3   | 0xBE   | 表外の読み    | text  | 29  | hyougai-yomi    |
| 4   | 0xC8   | 書き換え・旧字体 | text  | 37  | kakikae         |
| 5   | 0x32   | 誤字訂正     | text  | 29  | goji-teisei     |
| 6   | 0x3D   | 四字熟語     | text  | 77  | yoji-kaki       |
| 7   | 0x50   | 書き取り     | text  | 142 | kakitori        |
| 8   | 0x64   | 対義語・類義語  | text  | 72  | tai-rui         |
| 9   | 0x50   | 書き取り２    | text  | 96  | kakitori-2      |
## Level 1
| #   | Hex ID | Type    | Input | Qs  | Slug          |
| --- | ------ | ------- | ----- | --- | ------------- |
| 0   | 0x6E   | 読み      | text  | 313 | yomi          |
| 1   | 0x50   | 書き取り    | text  | 167 | kakitori      |
| 2   | 0x50   | 国字      | text  | 33  | kokuji        |
| 3   | 0x50   | 故事・諺    | text  | 39  | koji-kotowaza |
| 4   | 0x3D   | 四字熟語    | text  | 70  | yoji-kaki     |
| 5   | 0x6E   | 熟字訓・当て字 | text  | 72  | juku-ate      |
| 6   | 0x6E   | 音訓読み    | text  | 84  | onkun         |
| 7   | 0x64   | 対義語・類義語 | text  | 77  | tai-rui       |
| 8   | 0x50   | 書き取り２   | text  | 96  | kakitori-2    |
## Key Insights from L10
- **Duplicate sections** (読み x2, 書き取り x2): Real exams mix for variety.
- **Dominant types**: 書き取り (900 total), 読み (900 total)—focus here for 63% coverage.
- **file_slug**: Perfect for routing (`/practice/10/yomi`, `/practice/10/kakitori`).
### Quick Filters
- **Choice-based** (fast drills): 0x01, 0x0A, 0x14-0x15, 0x28, 0x2A-0x2B, 0x3C, 0x46-0x47, 0x64, 0x6E, 0x78-0x7A, 0x8C-0x8E, 0x90.
- **Writing** (pen skills): 0x29, 0x32, 0x3D-0x3E, 0x50, 0x5A, 0x8F, 0xBE, 0xC8.
- **Numeric**: 0x1E, 0x82.