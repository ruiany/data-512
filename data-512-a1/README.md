# DATA512 - A1: Data Curation

## Goal of the project
For this assignment, the combined data about Wikipedia page traffic from two different Wikimedia REST API endpoints were used to perform data processing and analysis

The goal of this assignment is to construct, analyze, and publish a dataset of monthly traffic on English Wikipedia from January 1 2008 through August 30 2020. All analysis should be performed in a single Jupyter notebook and all data, documentation, and code should be published in a single GitHub repository.

## Source data
In order to measure Wikipedia traffic from 2008-2020, two different API endpoints, the Legacy Pagecounts API and the Pageviews API.

The Legacy Pagecounts API ([documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts#Pagecounts), [endpoint](https://wikimedia.org/api/rest_v1/#/Pagecounts_data_(legacy)/get_metrics_legacy_pagecounts_aggregate_project_access_site_granularity_start_end)) provides access to desktop and mobile traffic data from December 2007 through July 2016.

The Pageviews API ([documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews#Monthly_counts), [endpoint](https://wikimedia.org/api/rest_v1/#/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end)) provides access to desktop, mobile web, and mobile app traffic data from July 2015 through last month.

At minimum, you README file should:

Describe the goal of the project.
List the license of the source data and a link to the Wikimedia Foundation REST API terms of use: https://www.mediawiki.org/wiki/REST_API#Terms_and_conditions (Links to an external site.)
Link to all relevant API documentation
Describe the values of all fields in your final data file.
List any known issues or special considerations with the data that would be useful for another researcher to know. For example, you should describe that data from the Pageview API excludes spiders/crawlers, while data from the Pagecounts API does not.
