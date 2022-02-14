---
title: Syracuse University Wagtail Migration
description: A complete migration to Wagtail CMS from WordPress.
date: 2021-08-12
tags: ['Python', 'Django', 'Wagtail']
layout: layouts/project.njk
image: /img/screens/su-wagtial-1.jpg
image_alt: A screenshot of the homepage.
site_link: https://www.syracuse.edu
---
The team was tasked with migrating the site to Wagtail. One of the things I worked on early on was modifying the WordPress API to output all of the data in our custom WordPress blocks. I assisted with python scripts to migrate data from the WordPress API and recreated in Wagtail all the blocks we had in WordPress. We've since added more custom blocks and with them added much more content to the <a href="{{ site_link | url }}">homepage</a>.
