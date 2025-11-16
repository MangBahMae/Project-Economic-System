#2025 11 15
GPT로 주식 웹사이트 만듦

#2025 11 16
// 가격 업데이트 함수 (간단 랜덤 변동)
function updatePrice() {
  // -5% ~ +5% 사이 랜덤 변동
  const changeRate = (Math.random() * 0.4) - 0.2;
  let newPrice = Math.round(price * (1 + changeRate));

  // 최소/최대 가격 제한 (원하는 대로 조정 가능)
  if (newPrice < 10) newPrice = 10;
  if (newPrice > 10000) newPrice = 10000;

  price = newPrice;
}

## 가격제한 제외하고 가격이 내려가도 음수가 되지않고 소수점으로 끝없이 나눠지는 형식으로 변경, 서킷브레이크 도입

## 터미널에만 가격변동 서킷브레이크 표시> 웹페이지에도 표시되게 변경
