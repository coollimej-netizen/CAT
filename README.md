<!doctype html>
<html lang="ko">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>세로 3장 이미지</title>
  <style>
    :root {
      --max-width: 420px; /* 전체 컨테이너 최대 너비 (원하면 변경) */
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
      gap: 16px; /* 이미지 사이 간격 */
    }

    .item {
      position: relative;
      overflow: hidden;
      border-radius: 8px;
      box-shadow: 0 6px 18px rgba(0,0,0,0.08);
      background: #ddd;
    }

    /* 이미지가 컨테이너에 맞추어 자동으로 잘림 없이 채움 */
    .item img {
      width: 100%;
      height: 280px; /* 각 이미지 높이 (원하면 변경 또는 min-height 사용) */
      object-fit: cover;
      display: block;
    }

    /* 이미지 위에 올라가는 텍스트 스타일 */
    .caption {
      position: absolute;
      left: 12px;
      top: 12px;
      padding: 6px 10px;
      background: rgba(0,0,0,0.45);
      color: white;
      font-size: 14px;
      border-radius: 6px;
      backdrop-filter: blur(4px);
    }

    /* 반응형: 작은 화면에서는 높이를 줄임 */
    @media (max-width: 420px) {
      .item img { height: 200px; }
    }
  </style>
</head>
<body>
  <div class="stack">
    <!-- 1번 이미지: src에 파일명 또는 URL 넣으세요 -->
    <div class="item">
      <img src="자는.jpg.png" alt="이미지 1 설명" />
      <div class="caption">같이 자기</div>
    </div>

    <!-- 2번 이미지 -->
    <div class="item">
      <img src="노는.jpg.png" alt="이미지 2 설명" />
      <div class="caption">같이 놀기</div>
    </div>

    <!-- 3번 이미지 -->
    <div class="item">
      <img src="TV.jpg.png" alt="이미지 3 설명" />
      <div class="caption">같이tv보기</div>
    </div>
  </div>
</body>
</html>
