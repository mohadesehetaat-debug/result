<!DOCTYPE html>
<html lang="fa">
<head>
  <meta charset="UTF-8">
  <title>نتیجه تست رانندگی</title>
  <style>
    body {
      font-family: sans-serif;
      direction: rtl;
      background-color: #f5f5f5;
      padding: 40px;
      text-align: center;
    }
    .box {
      background-color: #800080;
      color: #fff;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 0 10px #aaa;
      max-width: 500px;
      margin: auto;
      font-size: 18px;
    }
  </style>
</head>
<body>

<div class="box" id="resultBox">
  <h2>در حال تحلیل شخصیت رانندگی شما...</h2>
</div>

<script>
window.onload = function() {
  const hash = window.location.hash;
  const score = parseInt(hash.substring(1));

  let resultText = "";

  if (isNaN(score)) {
    resultText = "امتیاز نامعتبر. لطفاً تست را دوباره انجام دهید.";
  } else if (score >= 1 && score <= 7) {
    resultText = "ماشین مناسب شما: BMW M3 یا Ford Mustang";
  } else if (score >= 8 && score <= 10) {
    resultText = "ماشین مناسب شما: Volkswagen Sedan یا Toyota Camry";
  } else if (score >= 11 && score <= 13) {
    resultText = "ماشین مناسب شما: Lexus RX یا Mercedes-Benz E-Class";
  } else if (score >= 14 && score <= 16) {
    resultText = "ماشین مناسب شما: Toyota Yaris یا Kia Picanto";
  } else if (score >= 17 && score <= 19) {
    resultText = "ماشین مناسب شما: Honda CR-V یا Hyundai Santa Fe";
  } else if (score >= 20 && score <= 22) {
    resultText = "ماشین مناسب شما: Mini Cooper یا Fiat 500";
  } else if (score >= 23 && score <= 28) {
    resultText = "ماشین مناسب شما: Tesla Model X یا Range Rover Evoque";
  } else {
    resultText = "امتیاز خارج از محدوده. لطفاً تست را دوباره انجام دهید.";
  }

  document.getElementById("resultBox").innerHTML = <h2>${resultText}</h2>;
};
</script>

</body>
</html>
