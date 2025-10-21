---
# try also 'default' to start simple
theme: academic
layout: cover
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
class: text-white
coverAuthor: Sjoerd van de Wege
coverAuthorUrl: https://github.com/SvdWege
coverBackgroundUrl: /background.jpg
coverBackgroundSource: unsplash
coverBackgroundSourceUrl: https://unsplash.com/photos/black-typewriter-d34DtRp1bqo
#coverBackgroundSource: unsplash
#coverBackgroundSourceUrl: ./assets/background.jpg
coverDate: 2025-10-22
# some information about your slides (markdown enabled)
title: Terugkomdag 
info: |
  ## Terugkom dag 22 oktober 
# apply UnoCSS classes to the current slide
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
---
# Terugkomdag 
---
transition: fade-out
---

# Inhoud 

<Toc text-sm minDepth="1" maxDepth="2" />

<!--
-->

---
transition: fade-out
layout: figure-side
figureUrl: /intero_logo.jpg
---

# Het bedrijf


<v-click> Intero Integrity bv </v-click>
<br>
<br>
<v-click> R&D </v-click> 


<!--
[click] Intero integrity bv heeft het hoofd kantoor in Tricht aan de Steenoven 2b.
Intero maakt tools voor inspecties van leidingen in de petrochemische industrie.

[click] 
Ik loop mijn stage bij de R&D afdeling. Deze afdeling  bestaat uit 3 sub afdelingen onder de leiding van Hans(manager)
Deze 3 sub afdelingen zijn Mechanical(3) Electical (3) en embedde(2). Daarnaast lopen er nog 2 andere stagairs bij R&D 
-->

---
transition: fade-out
layout: figure-side
figureCaption: ZUBoard 1CG by AVNet
figureUrl: /zuboard.jpg
---

# De opdracht 
<div >
  <div
    v-click="1"
    border="2 solid orange-800" bg="orange-800/20"
    rounded-lg overflow-hidden
    transition duration-500 ease-in-out
    :class="$clicks < 1 ? 'opacity-0 translate-y-20' : 'opacity-100 translate-y-0'"
  >
    <div bg="orange-800/40" px-4 py-2 flex items-center>
      <div text-orange-400 text-xl mr-2 />
      <span font-bold>De opdracht</span>
    </div>
    <div px-5 py-3>
      <div
        v-for="(step, idx) in [ 'ZUBoard 1CG', 'onboard sensors', 'hardware en software link',  ]"
        :key="step"
        flex items-center gap-2 py-1
        :class="$clicks < 1 ? 'opacity-0' : 'opacity-100'"
        :style="{ transitionDelay: `${200 + idx * 200}ms`, transitionProperty: 'all', transitionDuration: '500ms' }"
      >
        <div i-carbon:dot-mark text-orange-400 />
        <span>{{step}}</span>
      </div>
    </div>
  </div>
</div>

<br>

<div >
  <div
    v-click="2"
    border="2 solid orange-800" bg="orange-800/20"
    rounded-lg overflow-hidden
    transition duration-500 ease-in-out
    :class="$clicks < 2 ? 'opacity-0 translate-y-20' : 'opacity-100 translate-y-0'"
  >
    <div bg="orange-800/40" px-4 py-2 flex items-center>
      <div text-orange-400 text-xl mr-2 />
      <span font-bold>De tools</span>
    </div>
    <div px-5 py-3>
      <div
        v-for="(step, idx) in [ 'Vivado', 'Vitis', 'git',  ]"
        :key="step"
        flex items-center gap-2 py-1
        :class="$clicks < 2 ? 'opacity-0' : 'opacity-100'"
        :style="{ transitionDelay: `${200 + idx * 200}ms`, transitionProperty: 'all', transitionDuration: '500ms' }"
      >
        <div i-carbon:dot-mark text-orange-400 />
        <span>{{step}}</span>
      </div>
    </div>
  </div>
</div>
<!--

[click] 
Voor mijn opdracht is mij gevraagt om een aantal testen uit te voeren op een nieuwe chip, de Zynq ultrascale+ MPSoC, zodat het bedrijf kan bepalen of ze in volgende versies van hun product deze chip willen gebruiken
De ZUBoard 1CG heeft 1 van deze Zynq chips
Deze CG series chips bevatten 2 Application cores, A53, 2 Real time processing units, R5F. en programmable logic.
andere series = EG met gpu en 4 cores || EV met videocodec

[click] 
Voor de ontwikkeling van de RTL voor deze chips word Vivado gebruikt, intel counterpart = quartus.
nadat de rtl gemaakt is wordt dat geexporteerd naar Vitis waar de software gebouwd kan worden.

Voor versie beheer wordt git gebruikt via de gitlab Instantie van het bedrijf.
-->


---
transition: fade-out
layout: center
---

# Zijn er nog vragen?

---
transition: fade-out
layout: end
---
