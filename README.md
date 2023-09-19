---
description: https://timberid.gitbook.io/timberid/
cover: .gitbook/assets/ddf-logo-trimmed-green.png
coverY: 0
layout:
  cover:
    visible: true
    size: full
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# 🌳 Welcome to TimberID

**TimberID** is a web application plus API used by researchers, auditors and enforcement professionals to manage, analyze and share information on timber samples collected from the Brazilian rainforest.

The analysis TimberID provides helps to understand the true nature of seized timber, such as the actual location it was harvested. This information is crucial to preventing deforestation and degradation of protected areas of the Amazon. This protects a vital resource for Brazil and helps safeguard the environment.

The API allows researchers to easily access reference information and analysis through Earth Engine. TimberID uses this API itself to run machine learning on reference data to build timber based isoscapes (isotopic maps) of the Brazilian rain-forest.

Finally, TimberID introduces innovative approach to building isoscapes (isotopic maps) of the amazon using a [machine learning variational model](architecture-of-timberid/detailed-design/variational-inference-colabs/isoscape-generation.md).

### Who can use TimberID?

TimberID is _currently_ optimized for researchers, auditors and enforcement professionals. Users register in TimberID to be part of a new or existing _organization_. In TimberID, all timber data is private within an organization, and is not visible to other organizations.&#x20;

Researchers can use the Web UI to input and manage their timber samples. They record aspects about each of their reference samples, such as isotopic measurements or species. After entering reference sample data, they may use the provided Earth Engine API to access this data to perform additional geospatial research.

Auditors and enforcement can use TimberID to perform an analysis on seized timber. When users enter data on seized timber, analysis such as an isotopic t test is performed. This test gives a statistical probability that the given timber sample actually came from the location it's owner claimed.  This analysis also includes nearby Mapbiomas Alerta deforestation alerts, vegetation and water cover maps. The goal is for TimberID to centralize the numerous signals that may be relevant to a piece of seized timber.

TimberID is open source and easy to extend. We invite researchers to add further analysis both on the timber sample and the claimed or actual locations the tree was obtained.

<img src=".gitbook/assets/file.excalidraw (4).svg" alt="" class="gitbook-drawing">



