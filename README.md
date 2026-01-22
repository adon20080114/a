<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>課題管理アプリ</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <link rel="stylesheet" href="style.css">
  <script src="script.js" defer></script>
</head>
<body>

<div class="app">
  <h1>課題管理アプリ 📚</h1>

  <div class="form">
    <input id="title" placeholder="課題名">

    <select id="type">
      <option value="school">学校の課題</option>
      <option value="self">自主学習（塾など）</option>
    </select>

    <select id="subject">
      <option value="">教科</option>
      <option>論国</option><option>文国</option><option>古探</option>
      <option>数Ⅱ・Ⅲ</option><option>数C</option>
      <option>英Ⅱ</option><option>論表</option>
      <option>化学</option><option>物理</option><option>生物</option>
      <option>日本史</option><option>世界史</option><option>公共</option>
      <option>保健体育</option><option>家庭科</option>
      <option>その他</option>
    </select>

    <input id="due" type="date">
    <textarea id="detail" placeholder="メモ"></textarea>
    <button id="add">追加</button>
  </div>

  <div class="tabs">
    <button class="tab active" data-view="list">一覧</button>
    <button class="tab" data-view="month">月</button>
    <button class="tab" data-view="done">提出済</button>
  </div>

  <div id="month-nav" class="month-nav hidden">
    <button id="prev">←</button>
    <span id="month-label"></span>
    <button id="next">→</button>
  </div>

  <div id="content"></div>
</div>

<div id="modal" class="modal hidden">
  <div class="modal-box">
    <h2>課題を編集</h2>
    <input id="m-title">
    <input id="m-due" type="date">
    <textarea id="m-detail"></textarea>
    <button id="save">保存</button>
    <button id="close">×</button>
  </div>
</div>

</body>
</html>

