<!DOCTYPE html>
<html lang="uz">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Anatomiya Tarjimon</title>
  <style>
    body {
      font-family: sans-serif;
      text-align: center;
      padding: 20px;
      background: #f2f2f2;
    }
    input, button {
      font-size: 18px;
      padding: 10px;
      margin: 10px;
      width: 80%;
    }
    .result {
      margin-top: 20px;
      font-size: 20px;
      color: green;
    }
  </style>
</head>
<body>
  <h2>Anatomiya Tarjimon (UZ / RU / EN → LATIN)</h2>

  <input id="termInput" placeholder="So‘z kiriting..." />
  <button onclick="translate()">Tarjima qil</button>

  <div class="result" id="output"></div>

  <script>
    const dictionary = {
      // Uzbek
      "tizza": "patella",
      "barmoq": "digitus",
      "elka": "humerus",
      "tizza qopqog'i": "patella",

      // Ruscha
      "колено": "patella",
      "палец": "digitus",
      "плечо": "humerus",

      // Inglizcha
      "knee": "patella",
      "finger": "digitus",
      "shoulder": "humerus"
    };

    function translate() {
      const input = document.getElementById("termInput").value.trim().toLowerCase();
      const translation = dictionary[input];
      const output = document.getElementById("output");
      if (translation) {
        output.innerText = `Lotincha: ${translation}`;
      } else {
        output.innerText = "So‘z topilmadi";
      }
    }
  </script>
</body>
</html>