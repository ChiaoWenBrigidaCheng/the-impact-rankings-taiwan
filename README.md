# Taiwan University Sustainability Rankings Dashboard

## Project Overview

This project provides an interactive website for visualizing Taiwan
universities' performance in:

-   **THE Impact Rankings**
-   **QS Sustainability Rankings**

The website is intended for internal use at **National Kaohsiung
University of Science and Technology (NKUST)** to support international
ranking analysis, benchmarking, and strategic planning.

------------------------------------------------------------------------

# Repository Structure

    /
    │
    ├── index.html              # Portal (landing page)
    │
    ├── the/
    │   ├── index.html
    │   ├── the_data.xlsm
    │   └── assets (optional)
    │
    ├── qs/
    │   ├── index.html
    │   ├── qs_data.xlsm
    │   └── assets (optional)
    │
    └── README.md

------------------------------------------------------------------------

# Website Architecture

## Portal

The portal is the landing page.

Responsibilities:

-   Navigation only
-   Links to THE and QS dashboards
-   Does not load ranking data

Navigation paths:

-   `./the/index.html`
-   `./qs/index.html`

------------------------------------------------------------------------

## THE Dashboard

Main functions

-   University selector
-   Base year selector
-   Comparison year selector
-   Overall trend
-   SDG performance
-   Taiwan Top 15 universities
-   Complete university table
-   SDG scoring methodology popup
-   Automatic Last Updated date

Data source

    the_data.xlsm

------------------------------------------------------------------------

## QS Dashboard

Main functions

-   University selector
-   Base year selector
-   Comparison year selector
-   Overall ESG comparison
-   Taiwan Top 15 universities
-   Complete university table
-   Automatic Last Updated date

Data source

    qs_data.xlsm

------------------------------------------------------------------------

# Data Update Workflow

Each year only replace:

THE

    the/the_data.xlsm

QS

    qs/qs_data.xlsm

Normally **no HTML modification** is required.

------------------------------------------------------------------------

# Annual Update Checklist

1.  Replace Excel data.
2.  Confirm all years are detected automatically.
3.  Check:
    -   University selector
    -   Trend chart
    -   Top 15 chart
    -   Data table
4.  Publish to GitHub.

------------------------------------------------------------------------

# Automatic Features

The dashboards automatically:

-   Detect available years
-   Update year range subtitle
-   Update "Last Updated"
-   Generate Top 15 using the selected/base year
-   Highlight NKUST
-   Freeze the University column
-   Adjust rankings for years with fewer than 15 Taiwan universities

------------------------------------------------------------------------

# Visual Design

Theme

-   Space / Galaxy
-   Purple (THE)
-   Gold (QS)

Shared elements

-   Nebula
-   Orbiting planets
-   Twinkling stars
-   Meteors
-   Animated background

THE

-   Purple charts

QS

-   Gold charts

------------------------------------------------------------------------

# Important Customizations

## THE

-   Top 15 follows **Base Year**
-   No separate Top Year selector
-   SDG methodology popup
-   Purple Top 15 bars

## QS

-   No metric selector
-   Top 15 uses Taiwan ranking
-   If fewer than 15 universities exist (e.g. 2023), display all
    available universities
-   Gold Top 15 bars

------------------------------------------------------------------------

# Known Critical Components

Do **not** remove without understanding their purpose:

-   `updateTop()`
-   `updateAutoRangeAndFooter()`
-   `averageScore()`
-   `chartOptions()`

These functions control most interactive behaviors.

------------------------------------------------------------------------

# Common Issues

## Top 15 tooltip misalignment

Solution:

-   Keep Chart.js interaction settings:

``` javascript
interaction:{
    mode:"nearest",
    axis:"y",
    intersect:false
}
```

Do not apply CSS transforms to the chart canvas.

------------------------------------------------------------------------

## Excel cannot be loaded

Check:

-   Correct file names
-   Relative paths
-   GitHub folder structure

------------------------------------------------------------------------

## NKUST highlight disappears

Check the table rendering function and NKUST highlighting CSS.

------------------------------------------------------------------------

# GitHub Pages

Recommended structure

    root/
        index.html

        the/
            index.html
            the_data.xlsm

        qs/
            index.html
            qs_data.xlsm

------------------------------------------------------------------------

# Future Improvements

Potential extensions:

-   ARWU
-   QS World University Rankings
-   THE World University Rankings
-   UI dark/light mode
-   Export charts
-   Download filtered data
-   SciVal integration
-   Responsive mobile optimization

------------------------------------------------------------------------

# Maintenance Notes

When modifying the dashboards:

1.  Back up the current HTML before editing.
2.  Test both dashboards locally.
3.  Verify Portal → THE → QS navigation.
4.  Verify all charts.
5.  Verify Excel loading.
6.  Commit changes with descriptive Git messages.

------------------------------------------------------------------------

Prepared for future maintainers of the NKUST Sustainability Rankings
Dashboard.
