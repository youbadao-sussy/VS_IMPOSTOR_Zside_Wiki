# Create DLC Folder
DLCは、非ビルド形式のmodと同じくmodsフォルダーで管理されます。

## 最初のフォルダ構成
最低限必要なフォルダです。
``` mermaid
flowchart LR
    mods --> dlc[my_dlc]

    dlc --> char[characters]
    dlc --> conf[config]
    dlc --> data[data]
    dlc --> imag[image]
    dlc --> song[songs]
    dlc --> week[weeks]
    dlc ==> dmeta[(dlc.json)]
    dlc ==> dhead{header.png}
    dlc ==> dicon{icon.png}
```

## dlcのmetadataを作成
`dlc.json`は、DLC Menuに表示されるDLCの顔のようなものです。

例として、Jorsawsee's Spike DLCの`dlc.json`の中身を見てみましょう。

```json
{
    "name": "Jorsawsee's Spike",
    "version": "1.0.0",
    "api_version": "1.0.0",
    "color": "#C300FF",
    "credits": [
        {
            "header": "Developer",
            "people": [
                {"name": "Youbadao", "desc": "Director, Artist, Animater, Musician and Programmer", "link": "https://x.com/Youba_mint"},
                {"name": "Shikumiro", "desc": "Artist and Animater", "link": "https://x.com/shikumiro7"},
                {"name": "Teru Yamane", "desc": "Musician", "link": ""}
            ]
        }
    ]
}
```

* `name`: DLC Menuに表示されるdlc名。
* `version`: DLCのバージョン。
* `api_version`: modのapiバージョン。メジャーアップデートにより変更される可能性がある。
* `color`: DLC Menuの背景のカラー。
* `credits`: DLC制作に直接的・間接的に関わった人々を記入するための場所。
  * `header`: グループ分け用のヘッダー。
  * `people`: DLC制作に直接的・間接的に関わった人々。
    * `name`: ニックネーム。
    * `desc`: その人のdlc制作に関連する説明等。
    * `link`: その人のサイトやブログ、活動場所等のリンク。

## 最終的なフォルダ及びファイル
これは全てを追加した後のフォルダ構成です。まだここまでは必要ないかも。
```mermaid
flowchart LR
    
  top(mods) --> dlc[my_dlc]

  dlc --> char[characters]
  dlc --> conf[config]
  dlc --> crew[crewmates]
  dlc --> evet[custom_events]
  dlc --> noty[custom_notetypes]
  dlc --> nost[custom_notestyles]
  dlc --> data[data]
  dlc --> imag[images]
  dlc --> musc[music]
  dlc --> scrp[scripts]
  dlc --> shad[shaders]
  dlc --> song[songs]
  dlc --> soun[sounds]
  dlc --> stge[stages]
  dlc --> vdeo[videos]
  dlc --> week[weeks]
  dlc ==> dmeta[(dlc.json)]
  dlc ==> dhead{header.png}
  dlc ==> dicon{icon.png}

  char --> cfld[charname]
  cfld ==> cmeta[(data.json)]
  cfld ==> cscrp[[script.lua/hx]]

  conf --> csmc[cosmicube]
  conf --> cfdi[dialogue]
  conf --> lang[languages]
  conf --> pets[pets]
  conf ==> crwbd[(crew_body_style.json)]
  conf ==> fmeta[(freeplay.json)]
  conf ==> inchr[include_char.txt]
  conf ==> maint[(mainmenu.json)]
  conf ==> stmeta[(settings.json)]

  csmc --> csmc_incl[cube_name]
  csmc ==> csmc_meta[(cube_name.json)]
  csmc_incl ==> csmc_item[item_name]

  cfdi --> boxes ==> dibox_meta[(textbox_name.json)]
  cfdi --> speaker ==> ditlk_meta[(talker_name.json)]

  lang ==> ldata[(lang_name.lang)]

  pets --> pfld[pet_name]
  pfld ==> pmeta[(data.json)]
  pets ==> pscrp[[script.lua/hx]]

  crew --> crfl[crew_name]
  crfl ==> crmet[(data.json)]
  crfl ==> crscr[[script.lua/hx]]

  evet ==> emeta[(event_name.txt)]
  evet ==> edata[[event_name.lua/hx]]

  noty ==> ntmet[(type_name.txt)]
  noty ==> ntscr[[type_name.lua/hx]]

  nost ==> stmeta[(style_name.json)]

  data --> sdfl[song_name]
  sdfl ==> sdata[(song_name.json)]
  sdfl ==> sscrp[[script.json]]
  sdfl ==> sdial[(dialogue.json)]

  imag --> characters --> ifld_char[char_name] ==> img_char{img_path}
  imag --> ifld_crew[crewmates] ==> img_crew{img_path}
  imag --> dialogue --> ifld_talk[character] ==> img_talk{img_path}
  imag --> bg --> name ==> img_bg{images}

  musc --> menu[menu_theme]
  musc ==> ur_msc[music_name.ogg/wav]
  menu ==> thm_meta[(metadata.json)]
  menu ==> thm_file{theme_name.ogg/wav}
```