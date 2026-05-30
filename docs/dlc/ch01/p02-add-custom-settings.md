# カスタム設定を作成する
Psych Engineには、`settings.json`という、mod専用の設定を作ることが出来るものがあります。
これは、このmodの制作環境である`Psychness Engine`でも引き継がれているため、このmodのdlcでも使えるようになっています。

## 作成
`config`フォルダに`settings.json`を作成。
以下のような物を中に記入してください。
```json
[
	{
		"save": "testbool",
		"name": "Test Bool Option",
		"type": "bool",
		"description": "This is a test bool option",
		"value": true
	},
	{
		"save": "testnumber",
		"name": "Test Number Option",
		"type": "float",
		"description": "This is a test number option",
		"value": 5,
	
		"min": 0,
		"max": 10,
		"step": 1,

		"decimals": 1,
		"scroll": 5
	},
	{
		"save": "teststring",
		"name": "Test String Option",
		"type": "string",
		"description": "This is a test string option",
		"value": "Sun",
		"format": "%vday",

		"options": ["Sun", "Mon", "Tues", "Wednes", "Thurs", "Fri", "Satur"]
	},
	{
		"save": "testkey",
		"name": "Test Custom Key",
		"type": "keybind",
		"keyboard": "T",
		"gamepad": "RIGHT_TRIGGER"
	}
]
```

* `save`: その設定のid。
* `name`: その設定の名前。
* `type`: その設定の種類。全部で6つあります。
  * `bool`: `true`(有効)か`false`(無効)か、つまりオンオフを切り替えることが出来る。
  * `int`: 小数点を含まない数字。
  * `float`: 小数点を含む数字。
  * `percent`: `float`と同義ですが、実際の数値に100をかけられたものになっています。
    * たとえば、名目上の最大数値が`110`の場合、実際の数値は`1.1`です。
  * `string`: 選択式の設定の場合に、数値の代わりとして文字をつけたいときに使用します。
  * `keybind`: キーの割り当て設定。

ここから先の項目は、`type`の選択によって変わります。

### `bool`
* `description`: 設定の説明。
* `value`: デフォルトの値。

### `int`, `float`, `percent`
* `description`: 設定の説明。
* `min`: 最低値。
* `max`: 最高値。
* `step`: 一回の動作で増加する値。

#### `float`, `percent`のみ
* `decimals`: 小数点の桁数。
* `scroll`: 左右どちらかを押しっぱなしにした時に変化する数値の速度。

### `string`
* `description`: 設定の説明。
* `value`: デフォルトの値。
* `format`: ちょっとよくわからんかった。
* `options`: 選択可能な文字の配列。

### `keybind`
* `keyboad`: キーボード入力のデフォルトのキー割り当て。
* `gamepad`: ゲームパッド(コントローラー)入力のデフォルトのキー割り当て。

## `id`の取得方法
Psych Engine (Psychness Engine)では、HaxeやLuaを使って設定を取得するための関数が用意されています。
[こちら](https://shadowmario.github.io/psychengine.lua/pages/savedata.html)をご覧ください。