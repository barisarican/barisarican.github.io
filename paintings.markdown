---
layout: default
title: Paintings
---
<a href="/index.html" class="inline-block mb-6 text-blue-600 hover:text-blue-800">
  ← Home
</a>
<h1 class="text-3xl font-bold mb-8 text-center">Paintings 🖼️</h1>

<div class="flex flex-col gap-8 items-center">
  {% for painting in site.paintings %}
    <div class="w-full max-w-xl bg-[#feeeee] shadow-md rounded-2xl overflow-hidden">
      <div class="p-6 text-center">
        <h2 class="text-2xl font-semibold mb-4">{{ painting.title }}</h2>
        {% if painting.images[1]%}
        <img src="{{ painting.images[1] }}" alt="{{ painting.title }}" class="rounded brightness-125">
        {% endif %}
        <a href="{{ painting.url }}" class="inline-block px-6 py-2 bg-blue-600 text-white rounded hover:bg-blue-700 transition m-8 animate-bounce">
          Show me 👀  
        </a>
      </div>
    </div>
  {% endfor %}
</div>