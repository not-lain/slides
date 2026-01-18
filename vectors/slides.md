---
theme: seriph
background: https://github.com/not-lain/slides/blob/main/vectors/public/orbit.png?raw=true
title: Welcome to Slidev
info: |
  ## Chonkie and qdrant
  Vector Search and Python Runner.

  Learn more at [chonkie.ai](https://chonkie.ai)
class: text-center
drawings:
  persist: false
transition: slide-left
duration: 20min
---

<style>
@keyframes neon-gradient {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}

.slidev-layout {
  background: linear-gradient(
    -45deg,
    #0a0a1a,
    #1a0a15,
    #2d1033,
    #1a0a2d,
    #150a1a,
    #1a0a15
  );
  background-size: 400% 400%;
  animation: neon-gradient 15s ease infinite;
}
</style>

<div
  v-motion
  :initial="{ y: -50, opacity: 0 }"
  :enter="{ y: 0, opacity: 1, transition: { duration: 800 } }"
  class="backdrop-blur-xl bg-white/10 p-8 rounded-2xl border border-violet-400/30 shadow-2xl"
>

# Chonkie 🦛

</div>

<div
  v-motion
  :initial="{ y: 50, opacity: 0 }"
  :enter="{ y: 0, opacity: 1, transition: { delay: 300, duration: 800 } }"
  class="text-xl mt-4"
>

Building RAG pipelines with chonkie

</div>

<div
  v-motion
  :initial="{ scale: 0, opacity: 0 }"
  :enter="{ scale: 1, opacity: 1, transition: { delay: 800, duration: 500 } }"
  @click="$slidev.nav.next"
  class="mt-12 py-1"
  hover:bg="white op-10"
>
  Start chonking ... <carbon:arrow-right />
</div>

<div
  v-motion
  :initial="{ x: 100, opacity: 0 }"
  :enter="{ x: 0, opacity: 1, transition: { delay: 1200, duration: 600 } }"
  class="abs-br m-6 text-xl"
>

  <a href="https://github.com/chonkie-inc/chonkie" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

<style scoped>
h1 {
  text-shadow:
    0 0 20px rgba(220, 36, 76, 0.8),
    0 0 40px rgba(183, 53, 143, 0.5),
    0 0 60px rgba(133, 71, 255, 0.3);
  filter: drop-shadow(0 0 15px rgba(220, 36, 76, 0.7));
}

.backdrop-blur-xl {
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
}
</style>

---
transition: fade-out
---
# Who Are We?

Chonkie is an AI company specializing in building tools related to RAG.
We are a team of 3 dedicated engineers.

<div grid="~ cols-3 gap-8" class="mt-8">

<div
  v-motion
  :initial="{ y: 50, opacity: 0 }"
  :enter="{ y: 0, opacity: 1, transition: { delay: 200, duration: 600 } }"
  class="text-center"
>
  <img
    src="https://avatars.githubusercontent.com/u/205269431?v=4"
    class="w-32 h-32 rounded-full mx-auto mb-4 border-4 border-transparent hover:border-blue-400 transition-all duration-300 transform hover:scale-110"
  />
  <div class="text-xl font-bold">🎨 Shreyash Nigam</div>
  <a href="https://github.com/shreyash-chonkie" target="_blank" class="text-sm opacity-75 hover:opacity-100">@shreyash-chonkie</a>
</div>

<div
  v-motion
  :initial="{ y: 50, opacity: 0 }"
  :enter="{ y: 0, opacity: 1, transition: { delay: 400, duration: 600 } }"
  class="text-center"
>
  <img
    src="https://avatars.githubusercontent.com/u/206151257?v=4"
    class="w-32 h-32 rounded-full mx-auto mb-4 border-4 border-transparent hover:border-green-400 transition-all duration-300 transform hover:scale-110"
  />
  <div class="text-xl font-bold">📝 Bhavnick Minhas</div>
  <a href="https://github.com/chonknick" target="_blank" class="text-sm opacity-75 hover:opacity-100">@chonknick</a>
</div>

<div
  v-motion
  :initial="{ y: 50, opacity: 0 }"
  :enter="{ y: 0, opacity: 1, transition: { delay: 600, duration: 600 } }"
  class="text-center"
>
  <img
    src="https://avatars.githubusercontent.com/u/224303370?v=4"
    class="w-32 h-32 rounded-full mx-auto mb-4 border-4 border-transparent hover:border-purple-400 transition-all duration-300 transform hover:scale-110"
  />
  <div class="text-xl font-bold">🧑‍💻 Hafedh Hichri (Lain)</div>
  <a href="https://github.com/chonk-lain" target="_blank" class="text-sm opacity-75 hover:opacity-100">@chonk-lain</a>
</div>

</div>

<div v-click class="text-center mt-12">
  Find us at <a href="https://chonkie.ai" target="_blank" class="font-bold text-blue-500 hover:underline">chonkie.ai</a>
</div>

<style>
h1 {
  background-color: #FFD700;
  background-image: linear-gradient(45deg, #FFD700 10%, #FFCC00 30%, #FFA500 60%, #FF8C00 90%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
  text-shadow: 0 0 20px rgba(255, 215, 0, 0.4), 0 0 40px rgba(255, 165, 0, 0.2);
  filter: drop-shadow(0 0 10px rgba(255, 215, 0, 0.5));
}

.slidev-layout {
  background: linear-gradient(135deg, #05070a 0%, #0d0f23 50%, #1a0a2d 100%);
}
</style>

---
transition: slide-up
level: 2
layout: two-cols
---

# chonkie

chonkie (not to be confused with Chonkie the company name) is an open-source library for building RAG pipelines easily.

<div class="mt-8">

## Why chonkie?

<v-clicks>

- 🚀 **Easy Integration**- Works seamlessly with popular vector databases
- 📦 **Simple API** - Minimal code to get started with RAG
- 🔌 **Built-in Connectors** - Native support for Qdrant, Pinecone, and more
- ⚡ **Fast Setup** - From zero to RAG in minutes

</v-clicks>

</div>

::right::

<div class="flex items-center justify-center h-full">
  <img src="/chonkie_ecosystem.png" alt="Chonkie Ecosystem" class="w-80 object-contain shadow-xl rounded-lg" v-motion :initial="{ x: 100, opacity: 0 }" :enter="{ x: 0, opacity: 1, transition: { duration: 800 } }"/>
</div>

<style>
h1 {
  background-color: #FFD700;
  background-image: linear-gradient(45deg, #FFD700 10%, #FFCC00 30%, #FFA500 60%, #FF8C00 90%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
  text-shadow: 0 0 20px rgba(255, 215, 0, 0.4), 0 0 40px rgba(255, 165, 0, 0.2);
  filter: drop-shadow(0 0 10px rgba(255, 215, 0, 0.5));
}

.slidev-layout {
  background: linear-gradient(135deg, #05070a 0%, #0d0f23 50%, #1a0a2d 100%);
}
</style>

---
transition: slide-left
layout: two-cols
layoutClass: 'gap-2'
---

# Try Chonkie!

Experience the simplicity of Chonkie in action.

```python
from chonkie import RecursiveChunker, Visualizer

# Initialize the chunker
chunker = RecursiveChunker(chunk_size=20)

# Chunk your text
text = """This is the first sentence. This is the second sentence.
And here's a third one with some additional context."""
chunks = chunker.chunk(text)

# Vizulize the results
viz = Visualizer()
viz(chunks)
```

::right::

<img src="/terminal_output.png" alt="Code 1" class="w-full h-full object-contain" />

<style>
h1 {
  background-color: #FFD700;
  background-image: linear-gradient(45deg, #FFD700 10%, #FFCC00 30%, #FFA500 60%, #FF8C00 90%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
  text-shadow: 0 0 20px rgba(255, 215, 0, 0.4), 0 0 40px rgba(255, 165, 0, 0.2);
  filter: drop-shadow(0 0 10px rgba(255, 215, 0, 0.5));
}

.slidev-layout {
  background: linear-gradient(135deg, #05070a 0%, #0d0f23 50%, #1a0a2d 100%);
}
</style>


---
transition: slide-left
layout: two-cols
layoutClass: 'gap-2'
---

# chonkie + Qdrant Integration

Integrating chonkie with Qdrant is as simple as one import:

```python
from chonkie import QdrantHandshake
```

<v-clicks>

<div
  v-motion
  :initial="{ scale: 0.8, opacity: 0 }"
  :enter="{ scale: 1, opacity: 1, transition: { duration: 600 } }"
  class="mt-8"
>

The `QdrantHandshake` handles all the complexity:

- ✅ Automatic collection management
- ✅ Seamless embedding and vectore store management
- ✅ Retrieval and storage made easy

</div>
</v-clicks>

::right::

<img src="/qdrant _code_snippet.png" alt="Code 1" class="w-full h-full object-contain" />

<style>
h1 {
  background-color: #FFD700;
  background-image: linear-gradient(45deg, #FFD700 10%, #FFCC00 30%, #FFA500 60%, #FF8C00 90%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
  text-shadow: 0 0 20px rgba(255, 215, 0, 0.4), 0 0 40px rgba(255, 165, 0, 0.2);
  filter: drop-shadow(0 0 10px rgba(255, 215, 0, 0.5));
}

.slidev-layout {
  background: linear-gradient(135deg, #05070a 0%, #0d0f23 50%, #1a0a2d 100%);
}
</style>

---
transition: slide-right
layout: two-cols
layoutClass: 'gap-16'
---

# We're Official! 🎉

Chonkie is now featured on the Qdrant Integrations page!

<div class="mt-4">
  <a href="https://qdrant.tech/documentation/data-management/chonkie/" target="_blank">
    <img
      src="https://qdrant.tech/img/hero-home-illustration-x2.webp"
      class="w-full border-2 border-gray-300 rounded-lg hover:opacity-90 transition-opacity cursor-pointer"
      alt="Qdrant Chonkie Integration"
      title="Click to visit Qdrant + Chonkie Documentation"
    />
  </a>
</div>

::right::

<div class="text-sm opacity-75">

Also checkout out these awesome resources:

<div class="mt-4 space-y-4">
  <div v-motion :initial="{ x: -50, opacity: 0 }" :enter="{ x: 0, opacity: 1, transition: { delay: 200 } }">
    <a href="https://cookbook.openai.com/examples/partners/temporal_agents_with_knowledge_graphs/temporal_agents" target="_blank" class="flex items-center gap-3 p-3 border border-gray-300 rounded-lg hover:bg-gray-100 hover:shadow-lg transition-all transform hover:scale-105">
      <img src="https://www.svgrepo.com/show/306500/openai.svg" alt="OpenAI" class="w-10 h-10" />
      <div>
        <div class="font-semibold text-blue-500">OpenAI Cookbook</div>
        <div class="text-xs opacity-60">Temporal Agents Example</div>
      </div>
    </a>
  </div>

  <div v-motion :initial="{ x: -50, opacity: 0 }" :enter="{ x: 0, opacity: 1, transition: { delay: 400 } }">
    <a href="https://docs.chonkie.ai/oss/handshakes/qdrant-handshake" target="_blank" class="flex items-center gap-3 p-3 border border-gray-300 rounded-lg hover:bg-gray-100 hover:shadow-lg transition-all transform hover:scale-105">
      <img src="https://www.chonkie.ai/chonkies/chonkie_icon.svg" alt="Chonkie" class="w-10 h-10" />
      <div>
        <div class="font-semibold text-blue-500">Chonkie Docs</div>
        <div class="text-xs opacity-60">Qdrant Handshake Guide</div>
      </div>
    </a>
  </div>
  <div v-motion :initial="{ x: -50, opacity: 0 }" :enter="{ x: 0, opacity: 1, transition: { delay: 600 } }">
    <a href="https://colab.research.google.com/drive/1uruoH1U72TJW1OXhmY7QxbPjFYajEO2z?usp=sharing " target="_blank" class="flex items-center gap-3 p-3 border border-gray-300 rounded-lg hover:bg-gray-100 hover:shadow-lg transition-all transform hover:scale-105">
      <img src="https://colab.research.google.com/img/colab_favicon_256px.png" alt="Colab" class="w-10 h-10" />
      <div>
        <div class="font-semibold text-blue-500">Google Colab</div>
        <div class="text-xs opacity-60">Chonkie + Qdrant Agentic Rag example</div>
      </div>
    </a>
  </div>
</div>

</div>

<style>
h1 {
  background-color: #FFD700;
  background-image: linear-gradient(45deg, #FFD700 10%, #FFCC00 30%, #FFA500 60%, #FF8C00 90%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
  text-shadow: 0 0 20px rgba(255, 215, 0, 0.4), 0 0 40px rgba(255, 165, 0, 0.2);
  filter: drop-shadow(0 0 10px rgba(255, 215, 0, 0.5));
}

.slidev-layout {
  background: linear-gradient(135deg, #05070a 0%, #0d0f23 50%, #1a0a2d 100%);
}
</style>

---
transition: slide-up
layout: two-cols
layoutClass: 'gap-16'
--- 

# Tables and Chunking

```python
from chonkie import TableChunker

table = """
| Name   | Age | City     |
|--------|-----|----------|
| Alice  | 30  | New York |
| Bob    | 25  | London   |
| Carol  | 28  | Paris    |
| Dave   | 35  | Berlin   |
"""

chunker = TableChunker(tokenizer="row", chunk_size=3)
chunks = chunker.chunk(table)
```


::right::

<img src="/chonkie_fixed.gif" class="w-full rounded-lg shadow-xl" />

<style>
h1 {
  background-color: #FFD700;
  background-image: linear-gradient(45deg, #FFD700 10%, #FFCC00 30%, #FFA500 60%, #FF8C00 90%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
  text-shadow: 0 0 20px rgba(255, 215, 0, 0.4), 0 0 40px rgba(255, 165, 0, 0.2);
  filter: drop-shadow(0 0 10px rgba(255, 215, 0, 0.5));
}

.slidev-layout {
  background: linear-gradient(135deg, #05070a 0%, #0d0f23 50%, #1a0a2d 100%);
}
</style>

---
transition: slide-up
layout: two-cols
layoutClass: 'gap-16'
---

# Our Growth Journey

Chonkie has seen incredible adoption since launch

## Community Highlights

- <span v-mark.underline.blue="2">3500+</span> GitHub stars
- ~300 Repositories Depend on chonkie
- 1.700.000+ PyPI downloads
- YC backed startup 🦛

<div v-click="3" class="mt-8">

### Join Our Community

<div class="flex gap-4 mt-4">
  <a
    href="https://github.com/chonkie-inc/chonkie"
    target="_blank"
    class="px-4 py-2 bg-blue-500 text-white rounded-lg hover:bg-blue-600 transition-colors"
  >
    Star on GitHub
  </a>
  <a
    href="https://discord.com/invite/Q6zkP8w6ur"
    target="_blank"
    class="px-4 py-2 border border-blue-500 text-blue-500 rounded-lg hover:bg-blue-50 transition-colors"
  >
    Join Discord
  </a>
</div>

</div>

::right::

<div v-click="1" v-motion :initial="{ x: 100, opacity: 0 }" :enter="{ x: 0, opacity: 1, transition: { duration: 800 } }">

<!-- <GithubStats /> -->
<div class="flex justify-center mb-4">
  <img alt="GitHub Repo stars" src="https://img.shields.io/github/stars/chonkie-inc/chonkie">
</div>

<StarHistory repo="chonkie-inc/chonkie" />

</div>

<style>
h1 {
  background-color: #FFD700;
  background-image: linear-gradient(45deg, #FFD700 10%, #FFCC00 30%, #FFA500 60%, #FF8C00 90%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
  text-shadow: 0 0 20px rgba(255, 215, 0, 0.4), 0 0 40px rgba(255, 165, 0, 0.2);
  filter: drop-shadow(0 0 10px rgba(255, 215, 0, 0.5));
}

.slidev-layout {
  background: linear-gradient(135deg, #05070a 0%, #0d0f23 50%, #1a0a2d 100%);
}
</style>

---
transition: slide-right
layout: two-cols
layoutClass: gap-0
---

# Catsu

One API for all embedding models. Switch between OpenAI, Cohere, Voyage, and more without changing your code.

<div class="mt-6 flex justify-center">
  <img
    v-motion
    :initial="{ scale: 0, rotate: -180 }"
    :enter="{ scale: 1, rotate: 0, transition: { type: 'spring', stiffness: 100, damping: 10 } }"
    src="https://github.com/chonkie-inc/catsu/blob/main/assets/catsu-icon.png?raw=true"
    alt="Catsu Icon"
    class="w-48"
  />
</div>


### Key Features

- 🔄 **Unified Implementation** - One library for all providers
- 💰 **Cost Tracking** - Built-in usage monitoring
- 🦀 **Multi-language** - Python and Rust clients



::right::

## Get Started in Seconds


```bash
pip install catsu
```


```python
# Switch providers instantly
from catsu import Client

client = Client()

# Just change the model name!
response = client.embed(
  "voyage-3",  # or "cohere:embed-english-v3.0"
  ["Build RAG apps faster", "with any embedding model"]
)

print(f"✓ {response.dimensions}D embeddings")
print(f"✓ {response.usage.tokens} tokens")
```

<style>
h1 {
  background-color: #FFD700;
  background-image: linear-gradient(45deg, #FFD700 10%, #FFCC00 30%, #FFA500 60%, #FF8C00 90%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
  text-shadow: 0 0 20px rgba(255, 215, 0, 0.4), 0 0 40px rgba(255, 165, 0, 0.2);
  filter: drop-shadow(0 0 10px rgba(255, 215, 0, 0.5));
}

.slidev-layout {
  background: linear-gradient(135deg, #05070a 0%, #0d0f23 50%, #1a0a2d 100%);
}
</style>

---
transition: slide-up
layout: two-cols
layoutClass: gap-16
---

# Memchunk

Memchunk is our latest and fastest chunking library, built for performance and scalability.

<div class="mt-4 text-[10px] opacity-90 border border-white/10 rounded-lg p-2 bg-white/5">

| library | throughput | vs memchunk |
| :--- | :--- | :--- |
| **memchunk** | **164 GB/s** | - |
| kiru | 4.5 GB/s | 36x slower |
| langchain | 0.35 GB/s | 469x slower |
| semchunk | 0.013 GB/s | 12,615x slower |
| llama-index | 0.0035 GB/s | 46,857x slower |
| text-splitter | 0.0017 GB/s | 96,471x slower |

</div>

::right::
## Get Started
```python
from chonkie import FastChunker

# Initialize the chunker
chunker = FastChunker(
    chunk_size=1024,
    delimiters="\n.?",
)

# Chunk your text
text = "Your long document text here..."
chunks = chunker.chunk(text)

# Print chunks count
print(f"Total chunks: {len(chunks)}")
```

<div
  v-motion
  :initial="{ x: 50, opacity: 0 }"
  :enter="{ x: 0, opacity: 1, transition: { delay: 400, duration: 800 } }"
  class="mt-6 flex justify-center"
>
  <img
    src="https://raw.githubusercontent.com/chonkie-inc/memchunk/main/assets/benchmark.png"
    alt="Memchunk Benchmark"
    class="max-w-xs rounded-lg shadow-lg"
  />
</div>

<style>
h1 {
  background-color: #FFD700;
  background-image: linear-gradient(45deg, #FFD700 10%, #FFCC00 30%, #FFA500 60%, #FF8C00 90%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
  text-shadow: 0 0 20px rgba(255, 215, 0, 0.4), 0 0 40px rgba(255, 165, 0, 0.2);
  filter: drop-shadow(0 0 10px rgba(255, 215, 0, 0.5));
}

.slidev-layout {
  background: linear-gradient(135deg, #05070a 0%, #0d0f23 50%, #1a0a2d 100%);
}
</style>

---
layout: center
class: text-center
---

<style scoped>
.slidev-layout {
  background-image: url(/orbit.png);
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
</style>

# Thank You!

<div class="mt-12 text-2xl opacity-90">
  Thanks for your attention!
</div>

<div class="mt-8 flex justify-center gap-8">
  <div class="flex flex-col items-center">
    <div class="text-sm opacity-60 mb-2">Documentation</div>
    <a href="https://docs.chonkie.ai/" target="_blank" class="font-bold text-emerald-400 hover:underline">docs.chonkie.ai</a>
  </div>
  <div class="flex flex-col items-center">
    <div class="text-sm opacity-60 mb-2">Website</div>
    <a href="https://chonkie.ai" target="_blank" class="font-bold text-blue-400 hover:underline">chonkie.ai</a>
  </div>
  <div class="flex flex-col items-center">
    <div class="text-sm opacity-60 mb-2">GitHub</div>
    <a href="https://github.com/chonkie-inc/chonkie" target="_blank" class="font-bold text-purple-400 hover:underline">chonkie-inc/chonkie</a>
  </div>
</div>

<style>
h1 {
  font-size: 5rem !important;
  background-color: #FFD700;
  background-image: linear-gradient(45deg, #FFD700 10%, #FFCC00 30%, #FFA500 60%, #FF8C00 90%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
  text-shadow: 0 0 30px rgba(255, 215, 0, 0.6);
  filter: drop-shadow(0 0 20px rgba(255, 215, 0, 0.4));
}
</style>
