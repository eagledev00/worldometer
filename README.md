<h1 align="center">
    <img src="https://raw.githubusercontent.com/matheusfelipeog/worldometer/master/.github/assets/images/worldometer.png" alt="Logo Worldometer - Scraping & API" width="550px" />
</h1>


<p align="center">
    <a href="https://pypi.org/project/worldometer/">
        <img alt="PyPI - Status" src="https://img.shields.io/pypi/status/worldometer?style=for-the-badge" />
    </a>
    <a href="https://pypi.org/project/worldometer/">
        <img alt="PyPI" src="https://img.shields.io/pypi/v/worldometer?style=for-the-badge" />
    </a>
    <a href="https://github.com/matheusfelipeog/worldometer/releases">
        <img alt="GitHub release (latest by date)" src="https://img.shields.io/github/v/release/matheusfelipeog/worldometer?style=for-the-badge" />
    </a>
    <a href="https://github.com/matheusfelipeog/worldometer/blob/master/LICENSE">
        <img src="https://img.shields.io/github/license/matheusfelipeog/worldometer?style=for-the-badge" alt="License MIT" />
    </a>
</p>


# Index

- [About](#about)
   - [worldometers.info](#worldometersinfo)
   - [How it works?](#how-it-works)
- [Install](#install)
- [Demo](#demo)
- [Contributions](#contributions)
- [License](#license)


# About

[Worldometer](https://github.com/matheusfelipeog/worldometer) is a python module that collects data from [worldometers.info](https://www.worldometers.info/) and provides a simple and self-explanatory interface for using the data.

## worldometers.info

> Worldometer is run by an international team of developers, researchers, and volunteers with the goal of making world statistics available in a thought-provoking and time relevant format to a wide audience around the world. It is published by a small and independent digital media company based in the United States. We have no political, governmental, or corporate affiliation. Furthermore, we have no investors, donors, grants, or backers of any type. We are completely independent and self-financed through automated programmatic advertising sold in real time on multiple ad exchanges.

More info: [worldometers.info/about](https://www.worldometers.info/about/)

## How it works?

> **[Adapted]:** For the data, is elaborate instead a real-time estimate through a proprietary algorithm which processes the latest data and projections provided by the most reputable organizations and statistical offices in the world.

More info about data source: [worldometers.info/sources](https://www.worldometers.info/sources/)


# Install

First, create a directory and enter it:

```bash
$ mkdir my_project && cd my_project
```

Create a virtual environment to avoid breaking dependence on other projects.

This project uses [`pipenv`](https://pipenv.pypa.io/en/latest/), it already does it alone ;)

```bash
$ pipenv install worldometer
```

But you can use `virtualenv` + `pip` if you prefer:

```bash
$ virtualenv venv && source venv/Scripts/activate
```

Now install:

```bash
$ pip install worldometer
```


# Demo

*The first time you run any function/method or class, it will download Chromium to its home directory (for example, `~/.pyppeteer/`). It only happens once.*

*After, it will only open the chromium to render the contents of worldometers.*

**Simple API usage:**

```python
>>> import worldometer

>>> worldometer.current_world_population()
7845085923

>>> worldometer.tweets_sent_today()
4539558

>>> worldometer.get_metric_of(label='computers_produced_this_year')
27760858
```

**Or complete use with Worldometer Class:**

```python
>>> from worldometer import Worldometer
>>> w = Worldometer()

>>> w.what_is_here()
{'categories': 8, 'labels': 63, 'metrics': 63}

>>> w.categories()
[   
    'world_population',
    'government_and_economics',
    'society_and_media',
    ...  # compressed
]

>>> w.metrics_labels()
[   
    'current_world_population',
    'births_this_year',
    'births_today',
    'deaths_this_year',
    'deaths_today',
    'net_population_growth_this_year',
    ...  # compressed
]

>>> w.metrics()
[   
    7845087963,
    15741371,
    5676,
    6608605,
    2383,
    9132766,
    ...  # compressed
]

>>> w.metrics_with_labels()
{   
    'abortions_this_year': 4785492,
    'bicycles_produced_this_year': 17070566,
    'births_this_year': 15741371,
    'births_today': 5676,
    'blog_posts_written_today': 110171,
    'cars_produced_this_year': 8999185,
    'cellular_phones_sold_today': 98846,
    ...: ...  # compressed
}
```


# Contributions

All contributions are welcome!

Found a problem, want to give a tip? open an issue.

Do you have a solution to the problem? Send me a PR.

Did you like this project? [Click on the star](https://github.com/matheusfelipeog/worldometer/stargazers) ⭐


# License

This project is using the MIT license, see in [MIT LICENSE](https://github.com/matheusfelipeog/worldometer/blob/master/LICENSE).
