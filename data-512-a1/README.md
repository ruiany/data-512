# DATA512 - A1: Data Curation

## Goal of the project
For this assignment, the combined data about Wikipedia page traffic from two different Wikimedia REST API endpoints were used to perform data processing and analysis

The goal of this assignment is to construct, analyze, and publish a dataset of monthly traffic on English Wikipedia from January 1 2008 through August 30 2020. This GitHub repo includes the [Jupyter notebook](https://github.com/ruiany/data-512/blob/main/data-512-a1/a1-data-curation.ipynb) used for gathering and analyzing the data as well as all data and result.

## Source data
The Wikipedia data was gathered from the [Wikimedia REST API](https://wikimedia.org/api/rest_v1/#/Pagecounts_data_(legacy)/get_metrics_legacy_pagecounts_aggregate_project_access_site_granularity_start_end), which is licensed under the [CC-BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/) and [GFDL](https://www.gnu.org/licenses/fdl-1.3.html) licenses.

In order to measure Wikipedia traffic from 2008-2020, two different API endpoints, the Legacy Pagecounts API and the Pageviews API:

The Legacy Pagecounts API ([documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts#Pagecounts), [endpoint](https://wikimedia.org/api/rest_v1/#/Pagecounts_data_(legacy)/get_metrics_legacy_pagecounts_aggregate_project_access_site_granularity_start_end)) provides access to desktop and mobile traffic data from December 2007 through July 2016.

The Pageviews API ([documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews#Monthly_counts), [endpoint](https://wikimedia.org/api/rest_v1/#/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end)) provides access to desktop, mobile web, and mobile app traffic data from July 2015 through September 2020.

Wikimedia Foundation REST API [terms of use](https://www.mediawiki.org/wiki/REST_API#Terms_and_conditions)

## Final data
The final [csv](https://github.com/ruiany/data-512/blob/main/data-512-a1/csv/en-wikipedia_traffic_200712-202009.csv) was created by combing the information from the Legacy Pagecounts API and the Pageviews API.

| Column | Description |
|--------|-------------|
| `year`   | The year of the view counts |
| `month`  | The month of the view counts |
| `pageview_mobile_views` | Page views by mobile web and mobile app |
| `pageview_desktop_views` | Page views by desktop |
| `pageview_all_views` | Page views by desktop, mobile web, and mobile app |
| `pagecount_mobile_views` | Page counts by mobile |
| `pagecount_desktop_views` | Page counts by desktop|
| `pagecount_all_views` | Page counts by mobile and desktop|

## Misc
The Legacy Pagecounts API doesn't provide any mobile visit data till October 2014.
