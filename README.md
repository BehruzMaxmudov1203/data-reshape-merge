<!-- Banner Typing Animation with Gradient Colors -->
<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=30&pause=800&color=FF5733,33FF57,3357FF&center=true&vCenter=true&width=900&lines=📊+Data+Harmonization;🔗+Merging+%26+Reshaping;💻+Python+Pandas;📔+Jupyter+Notebooks" alt="Typing SVG" />
</p>

---

# 🚀 Data Harmonization, Merging & Reshaping

This module covers **working with hierarchical data, reshaping, merging, and concatenating datasets** in Python using Pandas.  
It includes hands-on exercises in **Jupyter Notebooks**.

---

## 🧩 Module Structure

| Topic | Description |
|-------|-------------|
| 🗂 Hierarchical Indexed Dataset | Introduction to hierarchical indexing |
| 🔄 `.stack()` & `.unstack()` | Reshaping DataFrames by stacking/unstacking |
| 🏷 Hierarchical indexing on dataset | Working with multi-level indexes |
| 🗄 Hierarchical column dataset | Managing columns with hierarchical indices |
| 🔀 `.swaplevel()` & `sort_index()` | Swapping index levels and sorting hierarchical data |
| 📔 Jupyter Notebook – 1 | Practical exercises with hierarchical data |
| 🔗 Merging datasets (.merge() & .join()) | SQL-style merging of datasets |
| 💡 Merge example | Hands-on merging example |
| ➕ Concatenating datasets (.concat()) | Combining datasets vertically or horizontally |
| 🔄 Long to wide dataset | Pivoting long data to wide format |
| 📔 Jupyter Notebook – 2 | Practical reshaping exercises |
| 🔗 Practical Exercise | Final harmonization & merging project |

---

## 🛠 Technologies Used

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)

---

## 📊 GitHub Stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=BehruzMaxmudov1203&show_icons=true&theme=tokyonight" alt="GitHub Stats" /> 
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=BehruzMaxmudov1203&theme=tokyonight" alt="GitHub Streak" /> 
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=BehruzMaxmudov1203&theme=react-dark" alt="GitHub Activity Graph" /> 
</p>

---

## 📌 Example: Hierarchical Indexing & Merging

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=24&pause=800&color=FF6F61,61FF6F,6161FF&center=true&vCenter=true&width=900&lines=Hierarchical+Indexing;Merge+%26+Join;Stack+%26+Unstack;Reshape+DataFrames" alt="Typing SVG" />
</p>

<p align="center"> <img src="https://media.giphy.com/media/3o7aD2saalBwwftBIY/giphy.gif" width="450" alt="Merging & Reshaping Animation"> </p>

```python
import pandas as pd

# Sample hierarchical DataFrame
arrays = [['A','A','B','B'], ['one','two','one','two']]
index = pd.MultiIndex.from_arrays(arrays, names=('letter','number'))
df = pd.DataFrame({'value':[10,20,30,40]}, index=index)

# Stack & Unstack
df_stacked = df.stack()
df_unstacked = df_stacked.unstack()

# Swap levels
df_swapped = df.swaplevel().sort_index()

# Merging datasets
df1 = pd.DataFrame({'key':[1,2,3],'val1':[10,20,30]})
df2 = pd.DataFrame({'key':[1,2,4],'val2':[100,200,400]})
df_merged = pd.merge(df1, df2, on='key', how='outer')

# Concatenating datasets
df_concat = pd.concat([df1, df2], ignore_index=True)
