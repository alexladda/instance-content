# Architecture

*This document describes the high-level architecture of this project. If you want to get familiar with this site and what it is about, you are in just the right place!*

**The main purpose** of this project is for me to learn about all aspects of data science, data analysis and data management. This website is the last element in a modular chain of tools. This site is ever-evolving with a lot of things to be added along the way. [However there's already a lot to see!](/) In researching I am frequently confronted with diverging patterns. I'm interested in finding out about different approaches.

With a complete chain, I can immediately put this framework to use and dive into specific questions.

## birds eye view

**The idea** is to create an entire pipeline, that will cover all aspects from the acquisition of data to its representation. But isn't this an extremely broad and complex interdisciplinary field? Yes, absolutely. The point is not to dive deep into every aspect, but to first achieve a minimal viable project. And honestly, [I love complexity](/about%20me). Seems like when it comes to dealing with data, it means it helps to be thriving in multidimensional intricacies.

![Diagram of Pipeline with Modules](/static/data-pipeline.svg)

**API: Accessing (live) data:** First comes the acquisition of data. These tools will fetch data from APIs. Preferably live data, since that is what matters. Nobody really cares about [my survival discriminant](#).

**Extract, Transform, Load:** Next the data will need to be curated to the specific needs.

**Data Storage:** Intensely and systematically studying SQL has been first step into this project. Everything before this module and everything after is either transformed into SQL or from SQL. This growing familiarity to communicate with data is key to data literacy.

**Analysis:** Extract meaning and insights from the collected data. Having always been interested in mathematics, this is my chance to dive deep again. In the last 15 years I haven't had to use much beyond 11th Grade arithmetics.

**Representation:** The representational layer is what you see here on this Flask based site, specifically in [projects](/projects). Some projects harness the ease and accessibility of Tableau. Others dive into Python's Numpy, Pandas, Matplotlib & Seaborn, Plotly.

## Philosophy

1. Focus on Python, SQL, Tableau.

2. Utilise cloud resources and services (where ever possible / feasible) mainly on GCP and AWS.

3. Strike a balance in learning best practices and and getting things done. Keep an eye out for opportunities of learning in a broader context.
