<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Đổi Delta</title>

  <style>
    body {
      margin: 0;
      min-height: 100vh;
      background: #0b0d10;
      color: white;
      font-family: Arial, sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 20px;
    }

    .box {
      width: 100%;
      max-width: 420px;
      background: #15181d;
      padding: 30px;
      border-radius: 18px;
      box-sizing: border-box;
    }

    h1 {
      text-align: center;
      margin-bottom: 10px;
    }

    .sub {
      text-align: center;
      color: #aaa;
      margin-bottom: 25px;
    }

    label {
      display: block;
      margin-bottom: 8px;
    }

    input {
      width: 100%;
      padding: 14px;
      box-sizing: border-box;
      border-radius: 10px;
      border: 1px solid #444;
      background: #0e1115;
      color: white;
      font-size: 16px;
      margin-bottom: 15px;
    }

    button {
      width: 100%;
      padding: 14px;
      border: none;
      border-radius: 10px;
      background: #f59e0b;
      color: black;
      font-size: 16px;
      font-weight: bold;
    }

    #message {
      text-align: center;
      margin-top: 18px;
      color: #fbbf24;
    }

    .info {
      text-align: center;
      color: #888;
      font-size: 13px;
      margin-top: 25px;
    }
  </style>
</head>

<body>

  <div class="box">

    <h1>DELTA REDEEM</h1>

    <div class="sub">
      Nhập mã phần thưởng của bạn
    </div>

    <label for="code">
      Mã redeem
    </label>

    <input
      id="code"
      type="text"
      placeholder="VD: DELTA-XXXX-XXXX"
    >

    <button onclick="redeemCode()">
      ĐỔI CODE
    </button>

    <div id="message"></div>

    <div class="info">
      Đây là bản demo.<br>
      Không nhập mật khẩu hoặc thông tin tài khoản.
    </div>

  </div>

  <script>
    function redeemCode() {

      var code = document.getElementById("code").value.trim();
      var message = document.getElementById("message");

      if (code === "") {
        message.textContent = "⚠️ Vui lòng nhập mã.";
        return;
      }

      message.textContent = "⏳ Đang kiểm tra mã...";

      setTimeout(function() {
        message.textContent =
          "ℹ️ Đây là bản demo, chưa kết nối hệ thống redeem thật.";
      }, 1000);

    }
  </script>

</body>
</html>
