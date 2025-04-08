<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Interactive BioBloom</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    .modal {
      display: none;
    }
    .modal.active {
      display: flex;
    }
  </style>
</head>
<body class="bg-pink-50 text-gray-800">

  <!-- Header -->
  <header class="bg-white shadow p-6 text-center">
    <h1 class="text-3xl font-bold text-pink-700">BioBloom🌸</h1>
    <p class="text-gray-500">Beautifully made with love and creativity</p>
  </header>

  <!-- Gallery Section -->
  <main class="p-8 grid gap-6 grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4">
    <!-- Item -->
    <div class="bg-white p-4 rounded-lg shadow hover:shadow-lg transition cursor-pointer" onclick="openModal('craft1.jpg', 'Woven Basket')">
      <img src="craft1.jpg" alt="Craft 1" class="rounded mb-2 w-full h-48 object-cover">
      <h2 class="font-semibold text-lg">Woven Basket</h2>
      <p class="text-sm text-gray-600">Handcrafted with natural fibers.</p>
      <button class="mt-2 bg-pink-600 text-white px-3 py-1 rounded hover:bg-pink-700">Buy Now</button>
    </div>

    <!-- Item 2 -->
    <div class="bg-white p-4 rounded-lg shadow hover:shadow-lg transition cursor-pointer" onclick="openModal('craft2.jpg', 'Clay Pot')">
      <img src="craft2.jpg" alt="Craft 2" class="rounded mb-2 w-full h-48 object-cover">
      <h2 class="font-semibold text-lg">Clay Pot</h2>
      <p class="text-sm text-gray-600">Earthy tones with a rustic finish.</p>
      <button class="mt-2 bg-pink-600 text-white px-3 py-1 rounded hover:bg-pink-700">Buy Now</button>
    </div>

    <!-- Item 3 -->
    <div class="bg-white p-4 rounded-lg shadow hover:shadow-lg transition cursor-pointer" onclick="openModal('craft3.jpg', 'Beaded Jewelry')">
      <img src="craft3.jpg" alt="Craft 3" class="rounded mb-2 w-full h-48 object-cover">
      <h2 class="font-semibold text-lg">Beaded Jewelry</h2>
      <p class="text-sm text-gray-600">Colorful and unique accessories.</p>
      <button class="mt-2 bg-pink-600 text-white px-3 py-1 rounded hover:bg-pink-700">Buy Now</button>
    </div>
  </main>

  <!-- Image Modal -->
  <div id="modal" class="modal fixed inset-0 bg-black bg-opacity-60 justify-center items-center z-50">
    <div class="bg-white rounded-lg p-6 max-w-md text-center relative">
      <button onclick="closeModal()" class="absolute top-2 right-2 text-gray-500 hover:text-red-500 text-xl">&times;</button>
      <img id="modalImg" src="" alt="" class="w-full h-60 object-cover rounded mb-4">
      <h2 id="modalTitle" class="text-xl font-semibold mb-2"></h2>
      <button class="bg-pink-600 text-white px-4 py-2 rounded hover:bg-pink-700">Buy Now</button>
    </div>
  </div>

  <!-- Footer -->
  <footer class="bg-white text-center p-4 mt-10 text-sm text-gray-500">
    © 2025 BioBloom. All rights reserved.
  </footer>

  <!-- JS Script -->
  <script>
    function openModal(imgSrc, title) {
      document.getElementById('modal').classList.add('active');
      document.getElementById('modalImg').src = imgSrc;
      document.getElementById('modalTitle').textContent = title;
    }

    function closeModal() {
      document.getElementById('modal').classList.remove('active');
    }
  </script>

</body>
</html>
