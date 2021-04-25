# Architecture

*This document describes the high-level architecture of this project. If you want to get familiar with this site and what it is about, you are just in the right place!*

**The main purpose** of this project is for me to learn about all aspects of Data Science, Data Analysis and Data Management. This Website is the last element in a modular chain of tools. This site is ever involving with a lot of things being still added constanty. [However there's already a lot to see!](/)

With a complete chain, I can immediately put this framework to use and dive into on specific questions. Along the way I am frequently confronted with diverging patterns. This will make me find my way around other environments quickly.

## birds eye view

**The idea** is to create entire pipeline, that will cover all aspects from the aquisition of data to its representation. But isn't this an extremely broad and complex interdisciplinary field? Yes, absolutely. The point is not to dive deep into every aspect, but to first achieve a minimal viable project. And honestly, [I love complexity](/about%20me). Seems like when it comes to dealing with data, it means it helps to be thriving in multidimensional intricacies.

![Diagram of Pipeline with Modules](/static/data-pipeline.svg)

**API: Accessing (live) data:** First comes the acquisition of data. These tools will fetch data from APIs. Preferably live data, since that is what matters. Nobody really cares about [my survival discriminant](#).

**Extract, Transform, Load:** Next the data will need to be curated to the specific needs.

**Data Storage:** Intensely and systematically studying SQL has been first step into this project. Everything before this Module and everything after is either transformed into SQL or from SQL. This growing familiarity to communicate with data is key to data literacy.

**Analysis:** Extract meaning and insights from the collected data. This will have the steepest learning curve. Having always been interested in Mathematics, this is my chance to dive deep again. In the last 15 Years I haven't had to use much beyond 11th Grade arithmetics.

**Representation:** The representational layer is what you see here on this Flask based site, specifically in [projects](/projects). Some projects harness the ease and accessibility of Tableau. Others dive into Python's Numpy, Pandas, Matplotlib & Seaborn, Plotly.

## Philosophy

1. Focus on Python, SQL, Tableau.

2. Utilize cloud ressources and services (where ever possible / feasable) mainly on GCP and AWS.

3. Strike a balance in learning best practices and and getting things done. Keep an eye out for opportunities of learning for a broader context.
