---
theme: seriph
background: /assets/AdobeStock_263911828.jpeg
title: Introduction to QGIS - Spring 2026
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
duration: 55min
---

# Introduction to QGIS

Open Source Geographic Information System\
<br>
Felipe Valdez\
felipe.valdez@temple.edu\
<br>
January 2026


<div class="abs-br m-6 text-xl">
  <a href="https://charlesstudy.temple.edu/calendar/workshops?&t=g&d=0000-00-00&cal%5B%5D=6197&ct%5B%5D=69157" title="More Workshops" target="_blank" class="slidev-icon-btn">
    <carbon:information />
  </a>
</div>


<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
layout: default
---

# Workshop contents

- 📝 **GIS basic concepts** - spatial data types, layers and overlay, attributes, coordinate systems
- 🎨 **QGIS interface** - panels, toolbars, data source manager
- 🧑‍💻 **Data Loading** - raster & vector
- 🤹 **Hands on exercise** - load data, attribute table, overlay, styling
- 💾 **Exporting a map** - print layout
- 🏁 **Wrap-up** - questions and upcoming workshops

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, rgb(146, 176, 35) 10%, rgb(90, 151, 50) 20%);
  background-size: 100%;
  background-clip: text;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: slide-up
layout: two-cols
---

# What is GIS?

is a computer system that analyzes and displays geographically referenced information. It uses data that is attached to a unique location. (USGS)
<br>
<br>
<br>
<br>

<div v-click>

- 💻 Hardware

</div>

<div v-click>

- 💾 Software

</div>

<div v-click>

- 📊 Data <span v-mark.red="6">*(Location)*</span>

</div>

<div v-click>

- ⚙️ Processes

</div>

<div v-click>

- 👥 <span v-mark.circle.orange="7">People</span>

</div>

::right::

<div class="h-full flex flex-col justify-center">
  <img src="/assets/gis_intro01.jpeg" />
</div>

---
layout: two-cols
layoutClass: gap-16
level: 2
transition: slide-up
---

# Types of data
<br>

<div class="space-y-6">
  <div class="transform hover:scale-105 transition-transform duration-200">
    <div class="text-2xl font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-blue-600 to-purple-600 mb-2">
      Vector Data
    </div>
    <div class="text-gray-700 ml-4">
      • Points, Lines, Polygons
    </div>
  </div>
  
  <div class="transform hover:scale-105 transition-transform duration-200">
    <div class="text-2xl font-extrabold text-transparent bg-clip-text bg-gradient-to-r from-green-600 to-teal-600 mb-2">
      Raster Data
    </div>
    <div class="text-gray-700 ml-4">
      • Pixel, cell
    </div>
  </div>
</div>

::right::
<div class="h-full flex items-center justify-center">
  <img src="https://bok-figures.s3.amazonaws.com/files/DM86_Fig1.png" class="max-w-full max-h-100 object-contain" />
</div>

---
layout: image-right
image: https://upload.wikimedia.org/wikipedia/commons/e/ee/Worlds_animate.gif
level: 2
---

# Coordinate Systems (CRS)
<br>

**Geographic Coordinate System**
- Latitude and Longitude
- Uses angles measured from the Earth's center

**Projected Coordinate System**
- Models the Earth as a plane
- Based on a *map projection*

<!-- Footer -->

[Learn more](https://gistbok-ltb.ucgis.org/page/34/concept/10535)

<!-- Inline style -->
<style>
.footnotes-sep {
  @apply mt-5 opacity-10;
}
.footnotes {
  @apply text-sm opacity-75;
}
.footnote-backref {
  display: none;
}
</style>

---
layout: image
image: https://upload.wikimedia.org/wikipedia/commons/thumb/c/c2/QGIS_logo%2C_2017.svg/2560px-QGIS_logo%2C_2017.svg.png?20170501030013
backgroundSize: contain
transition: slide-up
---

---
layout: image-right
image: /assets/qgis_intro02.png
backgroundSize: contain
---

# What is QGIS?
is a free, open-source desktop Geographic Information System (GIS) software used to create, edit, visualize, analyze, and publish geospatial data.
<br>
<br>
<br>
<br>
<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, rgb(146, 176, 35) 10%, rgb(90, 151, 50) 20%);
  background-size: 100%;
  background-clip: text;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>
<div v-click>
<div class="w-60 relative">
  <div class="relative w-60 h-60">
    <!-- Microsoft logo - top of triangle -->
    <img
      v-motion
      :initial="{ x: 800, y: -100, scale: 1, rotate: -50 }"
      :click-1="microsoftFinal"
      class="absolute w-16 h-16"
      src="https://upload.wikimedia.org/wikipedia/commons/4/44/Microsoft_logo.svg"
      alt=""
      />
    
  <img
      v-motion
      :initial="{ y: 500, x: -100, scale: 2 }"
      :click-1="appleFinal"
      class="absolute w-16 h-16"
      src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/fa/Apple_logo_black.svg/1024px-Apple_logo_black.svg.png"
      alt=""
  />
    
  <img
      v-motion
      :initial="{ x: 600, y: 400, scale: 2, rotate: 100 }"
      :click-1="linuxFinal"
      class="absolute w-16 h-16"
      src="https://upload.wikimedia.org/wikipedia/commons/d/d6/Linux_mascot_tux.png"
      alt=""
    />
  </div>

  <div
    class="text-5xl absolute top-14 left-40 text-[#7fa728] -z-1"
    v-motion
    :initial="{ x: 0, opacity: 0}"
    :click-1="{ x: 50, opacity: 1, transition: { delay: 2000, duration: 1000 } }">
    Multi platform
  </div>
</div>
</div>

<script setup lang="ts">
const microsoftFinal = {
  x: 80,  // center horizontally
  y: 0,   // top of triangle
  rotate: 0,
  scale: 1,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}

const appleFinal = {
  x: 20,   // left side
  y: 100,  // bottom of triangle
  rotate: 0,
  scale: 1,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}

const linuxFinal = {
  x: 140,  // right side
  y: 100,  // bottom of triangle
  rotate: 0,
  scale: 1,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
</script>

---
layout: section
transition: slide-up
---

# [Hands on](https://tuprd-my.sharepoint.com/:u:/g/personal/tuq76851_temple_edu/IQBfDC_j94lgSax1rWhFopYFAQlvp01WcDE7POio_fBUnPE?e=7JjHSm)

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, rgb(146, 176, 35) 10%, rgb(90, 151, 50) 20%);
  background-size: 100%;
  background-clip: text;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

--- 
layout: image-right
transition: slide-up
image: /assets/result.png
backgroundSize: contain
---

# Workflow

1. Open QGIS
2. Start a new project
3. Load data to the project (raster & vector)
4. Explore data attributes
5. Style layers
6. Export map
<br>
<br>
# Data sources:
- [OpenDataPhilly](https://opendataphilly.org/)
- [Temple Open Data](https://temple.maps.arcgis.com/home/index.html)

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, rgb(146, 176, 35) 10%, rgb(90, 151, 50) 20%);
  background-size: 100%;
  background-clip: text;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
layout: image
image: /assets/result.png
backgroundSize: contain
--- 

---
layout: image
transition: slide-up
image: /assets/workshoppromo.png
--- 

--- 
layout: end
---

Contact us at:\
felipe.valdez@temple.edu \
<br>
Visit our guides:\
https://guides.temple.edu/gis-mapping

<style>
.slidev-layout.end {
  background: linear-gradient(135deg, rgb(164, 30, 53) 0%, rgb(149, 56, 71) 100%);
}
</style>



