title: Light Up Your Data with Streamlit
use_katex: False
class: title-slide

# Light Up Your Data with Streamlit!
<br>

![:scale 30%](images/streamlit-mark-color.png)

<br>
Thomas J. Fan<br>

@thomasjpfan<br>
<a href="https://www.github.com/thomasjpfan" target="_blank"><span class="icon icon-github icon-left"></span></a>
<a href="https://www.twitter.com/thomasjpfan" target="_blank"><span class="icon icon-twitter"></span></a>

![:scale 15%](images/labs.jpg)

<a class="this-talk-link title-page", href="https://github.com/thomasjpfan/scipy-2021-streamlit" target="_blank">
This talk on Github: thomasjpfan/scipy-2021-streamlit</a>

---

# What is Streamlit?

### Allows you to quickly build web applications and dashboards in `Python`

.center[
![:scale 80%](images/streamlit_dual_window.png)
]

---

class: chapter-slide

# Three Advantages of Streamlit 🚀
### (In my opinion)

---

# Regular Python Files

.center[
![:scale 90%](images/streamlit_dual_window.png)
]

---

# Compatible with Many Visualizations Libraries

.g[
.g-4[
## Matplotlib
![:scale 100%](images/matplotlib.png)
]
.g-4[
## Plotly
![:scale 100%](images/plotly-logomark.png)
]
.g-4[
## Altair
![:scale 100%](images/altair-logo-light.png)
]
]

---

# User interactions are simple to write

.g[
.g-7[
```python
import os
import streamlit as st

*penguin = st.radio(
    "Select a penguin",
    options=["adelie", "gentoo", "chinstrap"])

st.header(f"Here is a {penguin}!")

image_path = os.path.join("images",
                          f"{penguin}.jpeg")
st.image(image_path)
```
]
.g-5[
![:scale 100%](images/streamlit-interact.gif)
]
]

---

.g.g-center.g-middle[
.g-6[
# Streamlit's API 💻
### Text
### Media
### User Interactions
### Visualization
### Layout
]
.g-6[
![:scale 50%](images/streamlit-mark-color.png)
]
]

---

.g.g-middle[
.g-6.larger[
```python
import streamlit as st
```
]
.g-6.g-center[
![:scale 40%](images/streamlit-mark-color.png)
### Demo materials for this talk:
[github.com/thomasjpfan/scipy-2021-streamlit-demo](https://github.com/thomasjpfan/scipy-2021-streamlit-demo)
]
]

---

class: chapter-slide

# Text 🔠

---

# Text Demo 🔠

.g.g-middle[
.g-6[
- `st.title`
- `st.header`
- `st.subheader`
]
.g-6[
- `st.write`
    - Markdown
    - Math
    - DataFrames
]
]

---

class: chapter-slide

# Media 📸

---

# Media Demo  📸

- `st.image`
- `st.audio`
- `st.video`

---

class: chapter-slide

# User Interactions ☎️

---

# User Interactions ☎️

.g[
.g-8[
```python
import os
import streamlit as st

*penguin = st.radio(
    "Select a penguin",
    options=["adelie", "gentoo", "chinstrap"])

st.header(f"Here is a {penguin}!")

image_path = os.path.join("images",
                          f"{penguin}.jpeg")
st.image(image_path)
```
]
.g-4[
![:scale 100%](images/streamlit-interact.gif)
]
]

---

# User Interactions Demo ☎️

.g[
.g-6[
- `st.button`
- `st.checkbox`
- `st.radio`
- `st.selectbox`
- `st.multiselect`
- `st.slider`
- `st.select_slider`
]
.g-6[
- `st.text_input`
- `st.number_input`
- `st.text_area`
- `st.date_input`
- `st.time_input`
- `st.file_uploader`
- `st.color_picker`
]
]


---

class: chapter-slide

# Visualization 📊

---

# Visualization Demo 📊

.g[
.g-4[
## Matplotlib
![:scale 100%](images/matplotlib.png)
]
.g-4[
## Plotly
![:scale 100%](images/plotly-logomark.png)
]
.g-4[
## Altair
![:scale 100%](images/altair-logo-light.png)
]
]

---

# Matplotlib: use Object-oriented API 🚨

```python
import matplotlib.pyplot as plt

fig, ax = plt.subplots()
ax.plot([1, 2, 3, 4])
ax.set_ylabel('some numbers')

st.write(fig)
```

---

class: chapter-slide

# Layout 🗄

---

# Layout Demo 🗄

- `st.sidebar`
- `st.beta_columns`

---

# Performance 🚀

.g[
.g-6[
- `st.cache` to cache function return values
- Really useful for data loading
]
.g-6[
```python
@st.cache
def load_data():
    data = pd.read_csv(...)
    return data
```
]
]

---

# Building a Machine Learning Dashboard 💻

- [A Unified Approach to Interpreting Model Predictions](https://papers.nips.cc/paper/7062-a-unified-approach-to-interpreting-model-predictions)
- [Anchors: High-Precision Model-Agnostic Explanations](https://ojs.aaai.org/index.php/AAAI/article/view/11491)


```python
import streamlit.components.v1 as componenets
```

---

# Streamlit Components!

- Libraries with extensions built for Streamlit
- Gallery: [streamlit.io/gallery?type=components](https://streamlit.io/gallery?type=components)

.center[
![:scale 70%](images/components-gallery.png)
]

---

# Streamlit Components Demo!

- [Folium](https://python-visualization.github.io/folium/) & [streamlit-folium](https://github.com/randyzwitch/streamlit-folium)
- [HiPlot](https://facebookresearch.github.io/hiplot/index.html)

---

# Additional Streamlit API

.g[
.g-6[
- [Session State API](https://docs.streamlit.io/en/stable/add_state_app.html)
- [Forms](https://blog.streamlit.io/introducing-submit-button-and-forms/)
- [Custom Themes](https://docs.streamlit.io/en/stable/theme_options.html)
]
.g-6[
![:scale 80%](images/streamlit-mark-color.png)
]
]

---

![:scale 100%](images/sharing.png)

## [streamlit.io/sharing](https://streamlit.io/sharing)

---

.center[
![:scale 70%](images/app-gallery.png)
]

## [streamlit.io/gallery](https:/streamlit.io/gallery)

---

# Other Resources to get started!

- [github.com/streamlit/streamlit](https://github.com/streamlit/streamlit/)
- [discuss.streamlit.io](https://discuss.streamlit.io/)

.center[
![:scale 70%](images/discuss.png)
]

---

class: title-slide, left

.g.g-middle[
.g-7[
# Light Up Your Data with Streamlit!
.center[
![:scale 30%](images/streamlit-mark-color.png)
]
1. Regular Python files
2. Compatible with Many Visualizations Libraries
3. User interactions are simple to write
]
.g-5.center[
<br>
.larger[Thomas J. Fan]<br>
@thomasjpfan<br>
<a href="https://www.github.com/thomasjpfan" target="_blank"><span class="icon icon-github icon-left"></span></a>
<a href="https://www.twitter.com/thomasjpfan" target="_blank"><span class="icon icon-twitter"></span></a>

![:scale 40%](images/labs.jpg)

<a class="this-talk-link", href="https://github.com/thomasjpfan/scipy-2021-streamlit" target="_blank">
This talk on Github: github.com/thomasjpfan/scipy-2021-streamlit</a>
]
]
