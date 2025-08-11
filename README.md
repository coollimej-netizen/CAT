<!doctype html>
<html lang="ko">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>세로 3장 이미지</title>
  <style>
    :root {
      --max-width: 420px;
    }

    body {
      font-family: system-ui, -apple-system, "Segoe UI", Roboto, "Noto Sans KR", "Apple SD Gothic Neo", "Malgun Gothic", sans-serif;
      display: flex;
      justify-content: center;
      padding: 24px;
      background: #f7f7f7;
      margin: 0;
    }

    .stack {
      width: 100%;
      max-width: var(--max-width);
      display: flex;
      flex-direction: column;
      gap: 16px;
    }

    .item {
      position: relative;
      overflow: hidden;
      border-radius: 8px;
      box-shadow: 0 6px 18px rgba(0,0,0,0.08);
      background: #ddd;
    }

    .item img {
      width: 100%;
      height: auto;
      display: block;
    }

    .caption {
      position: absolute;
      left: 12px;
      bottom: 12px;
      padding: 6px 10px;
      background: rgba(0,0,0,0.45);
      color: white;
      font-size: 14px;
      border-radius: 6px;
      backdrop-filter: blur(4px);
    }

    @media (max-width: 420px) {
      .item img { height: auto; }
    }
  </style>
</head>
<body>
  <div class="stack">
    <div class="item">
      <img src="자는.jpg" alt="이미지 1 설명" />
      <div class="caption">같이 자기</div>
    </div>

    <div class="item">
      <img src="노는.jpg" alt="이미지 2 설명" />
      <div class="caption">같이 놀기</div>
    </div>

    <div class="item">
      <img src="TV.jpg" alt="이미지 3 설명" />
      <div class="caption">같이 TV 보기</div>
    </div>
  </div>
</body>
</html>
