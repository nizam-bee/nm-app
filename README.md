<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>FFAM AI Tool by Nizam</title>
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
</head>
<body class="bg-gray-100 text-gray-800 font-sans">

  <header class="text-center py-6 bg-purple-600 text-white shadow">
    <h1 class="text-3xl font-bold">FFAM AI Tool</h1>
    <p class="text-sm mt-1">Create Android apps with AI – by Nizam</p>
  </header>

  <main class="max-w-xl mx-auto mt-10 px-4">
    <label class="block mb-2 font-semibold text-lg">Enter your app idea:</label>
    <textarea id="prompt" rows="4" class="w-full p-3 rounded border" placeholder="e.g. Create OTT app with Premium plans"></textarea>

    <button onclick="generatePreview()" class="mt-4 w-full bg-purple-600 text-white p-3 rounded hover:bg-purple-700">
      Generate App
    </button>

    <div id="preview" class="mt-6 p-4 bg-white rounded shadow hidden">
      <h2 class="font-bold text-lg mb-2">🧠 AI App Preview</h2>
      <p id="previewText" class="text-sm text-gray-700">...</p>
      <a id="downloadBtn" href="#" class="mt-4 inline-block bg-green-600 text-white p-3 rounded hover:bg-green-700">⬇️ Download .AAB</a>
    </div>
  </main>

  <footer class="text-center py-4 mt-10 text-sm text-gray-500">
    Made with ❤️ by Nizam · FFAM.ai · 2025
  </footer>

  <script>
    function generatePreview() {
      const idea = document.getElementById('prompt').value.toLowerCase();
      const preview = document.getElementById('preview');
      const previewText = document.getElementById('previewText');
      const downloadBtn = document.getElementById('downloadBtn');

      let link = "#";
      let desc = "Default NM App";

      if (idea.includes("ott")) {
        link = "https://pixeldrain.com/u/9qshg1zM"; // sample OTT .aab
        desc = "Includes Home, Watch Movies, Premium plans";
      } else if (idea.includes("quiz")) {
        link = "https://pixeldrain.com/u/x13u47or"; // sample quiz .aab
        desc = "Includes quiz questions, score system";
      } else {
        link = "https://pixeldrain.com/u/gj0d9vLT"; // default NM App
        desc = "Default NM App bundle with language info";
      }

      previewText.innerText = "✅ " + desc;
      downloadBtn.href = link;
      preview.classList.remove("hidden");
    }
  </script>

</body>
</html>
