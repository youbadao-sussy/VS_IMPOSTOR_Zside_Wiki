# Boyfriend (Zside)

<!-- 折りたたみ可能なコンテンツ -->
<details>
  <summary style="cursor: pointer; font-weight: bold;">Boyfriend</summary>
    <div align="center">
<body>
<img id="mainImage" src="" alt="" style="max-width: 30%; height: auto;">

<div class="controls">
  <button id="prtBtn" style="background-color: #acacac; color: white; padding: 0.5rem 1rem; border: none; border-radius: 4px; cursor: pointer;">Portrait</button>
  <button id="idlBtn" style="background-color: #acacac; color: white; padding: 0.5rem 1rem; border: none; border-radius: 4px; cursor: pointer;">Idle</button>
</div>

<script>
  // 画像データ配列（ファイル名とaltテキスト）
  const images = [
    { src: "img/BF.svg", alt: "Portrait" },
    { src: "img/Week1__Default.svg", alt: "Default" }
  ];

  let currentIndex = 0; // 現在の画像インデックス
  const mainImage = document.getElementById("mainImage");
  const prtBtn = document.getElementById("prtBtn");
  const idlBtn = document.getElementById("idlBtn");

  // 画像を表示する関数
  function updateImage(index) {
    mainImage.src = images[index].src;
    mainImage.alt = images[index].alt;
    mainImage.style = images[index].style;
  }

  // 初期表示
  updateImage(currentIndex);

  // Normalボタン
  prtBtn.addEventListener("click", () => {
    currentIndex = 0; // 最初なら最後に戻る
    updateImage(currentIndex);
  });

  // 「次へ」ボタン
  idlBtn.addEventListener("click", () => {
    currentIndex = 1; // 最後なら最初に戻る
    updateImage(currentIndex);
  });
</script>

</body>

<table style="border-collapse: collapse; width: 100%;">
    <tbody>
        <tr style="background-color: #f9f9f9;">
            <td style="border: 1px solid #bbbbbb; padding: 8px;">別名</td>
            <td style="border: 1px solid #bbbbbb; padding: 8px;">
                BF
            </td>
        </tr>
        <tr style="background-color: #f9f9f9;">
            <td style="border: 1px solid #bbbbbb; padding: 8px;">人間関係</td>
            <td style="border: 1px solid #bbbbbb; padding: 8px;">
                Girlfriend (彼女) <br>
                Pico (元彼)
            </td>
        </tr>
        <tr style="background-color: #249bfd; font-weight: bold;">
            <td colspan="2" style="border: 1px solid #bbbbbb; padding: 8px;">伝記情報</td>
        </tr>
        <tr style="background-color: #f9f9f9;">
            <td style="border: 1px solid #bbbbbb; padding: 8px;">性的指向</td>
            <td style="border: 1px solid #bbbbbb; padding: 8px;">
                バイセクシュアル
            </td>
        </tr>
        <tr style="background-color: #f9f9f9;">
            <td style="border: 1px solid #bbbbbb; padding: 8px;">キルカウント</td>
            <td style="border: 1px solid #bbbbbb; padding: 8px;">
                0
            </td>
        </tr>
        <tr style="background-color: #f9f9f9;">
            <td style="border: 1px solid #bbbbbb; padding: 8px;">デスカウント</td>
            <td style="border: 1px solid #bbbbbb; padding: 8px;">
                0
            </td>
        </tr>
        <tr style="background-color: #249bfd; font-weight: bold;">
            <td colspan="2" style="border: 1px solid #bbbbbb; padding: 8px;">物理的特徴</td>
        </tr>
        <tr style="background-color: #f9f9f9;">
            <td style="border: 1px solid #bbbbbb; padding: 8px;">種族</td>
            <td style="border: 1px solid #bbbbbb; padding: 8px;">
                人間 <br>
                クルーメイト
            </td>
        </tr>
        <tr style="background-color: #f9f9f9;">
            <td style="border: 1px solid #bbbbbb; padding: 8px;">性別</td>
            <td style="border: 1px solid #bbbbbb; padding: 8px;">
                男性
            </td>
        </tr>
        <tr style="background-color: #f9f9f9;">
            <td style="border: 1px solid #bbbbbb; padding: 8px;">カラー</td>
            <td style="border: 1px solid #bbbbbb; padding: 8px;">
                オレンジ
            </td>
        </tr>
        <tr style="background-color: #f9f9f9;">
            <td style="border: 1px solid #bbbbbb; padding: 8px;">バイザーの色</td>
            <td style="border: 1px solid #bbbbbb; padding: 8px;">
                普通 (薄水色)
            </td>
        </tr>
        <tr style="background-color: #249bfd; font-weight: bold;">
            <td colspan="2" style="border: 1px solid #bbbbbb; padding: 8px;">出演</td>
        </tr>
        <tr style="background-color: #f9f9f9;">
            <td style="border: 1px solid #bbbbbb; padding: 8px;">所有者</td>
            <td style="border: 1px solid #bbbbbb; padding: 8px;">
                Youbadao (and Funkin' Zside Team)
            </td>
        </tr>
        <tr style="background-color: #f9f9f9;">
            <td style="border: 1px solid #bbbbbb; padding: 8px;">作成者</td>
            <td style="border: 1px solid #bbbbbb; padding: 8px;">
                Pasy-kun
            </td>
        </tr>
        <tr style="background-color: #f9f9f9;">
            <td style="border: 1px solid #bbbbbb; padding: 8px;">声優</td>
            <td style="border: 1px solid #bbbbbb; padding: 8px;">
                Kawai Sprite (Funkin' Crew Inc.)
            </td>
        </tr>
    </tbody>
</table>

</details>


Boyfriendはラッパーで、VS Impostor Zsideの主人公です。
