---
theme: seriph
background: https://source.unsplash.com/collection/94734566/1920x1080
highlighter: shiki
lineNumbers: true
drawings:
    persist: false
    enabled: true
---

# Welcome to Slidev

Presentation slides for developers

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
layout: image-right
image: https://source.unsplash.com/collection/94734566/1920x1080
class: 'text-center'
---

# What is Slidev?

Slidev is a slides maker and presenter designed for developers, consist of the following features

-   📝 **Text-based** - focus on the content with Markdown, and then style them later
-   🎨 **Themable** - theme can be shared and used with npm packages
-   🧑‍💻 **Developer Friendly** - code highlighting, live coding with autocompletion
-   🤹 **Interactive** - embedding Vue components to enhance your expressions
-   🎥 **Recording** - built-in recording and camera view
-   📤 **Portable** - export into PDF, PNGs, or even a hostable SPA
-   🛠 **Hackable** - anything possible on a webpage
<Demo/>