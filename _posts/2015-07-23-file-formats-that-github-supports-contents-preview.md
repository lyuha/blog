---
layout: post
title: "Github에서 미리보기 지원하는 파일 목록"
categories:
tags: 
---
github blog에서 [Improving map data on GitHub](https://github.com/blog/2041-improving-map-data-on-github)를 멍하니 보니 GeoJSON도 고칠 수 있었다. 중간에 PDF viewing에 관한 내용도 있었다. 그러면 "지원하는 파일이 얼마나 있을까?"라는 의문이 들었다. 그래서 [github blog new feature](https://github.com/blog/category/ship)의 글들을 대충 훑어보았다. 그리고 github에서 공식지원하는 문서들을 정리해보았다.

## Format List

* Markup language
  * Markdown
  * Texttile
  * RDoc
  * AsciiDoc
  * ReStructuredText
  * Org
  * Ceole
  * MediaWiki
  * Pod                                    
* SVG
* GeoJSON
* TopoJSON
* STL
* PDF
* CSV
* TSV
* ipynb
* PSD

* YAML Metadata

## Links

* Formatted Text
  * [Formatted Files](https://github.com/blog/115-formatted-files)
  * [Markdown'd, Textile'd Readmes](https://github.com/blog/19-markdown-d-textile-d-readmes)
* SVG
  * [SVG Viewing & Diffing](https://github.com/blog/1902-svg-viewing-diffing)

* Geo
  * [There's a map for that](https://github.com/blog/1528-there-s-a-map-for-that)
  * [View GeoJSON/TopoJSON Source](https://github.com/blog/1865-view-geojson-topojson-source)
  * [Diffable, more customizable maps](https://github.com/blog/1772-diffable-more-customizable-maps)
  * [GeoJSON Previewing](https://github.com/blog/1638-geojson-previewing)
  * [Gist meets GeoJSON](https://github.com/blog/1576-gist-meets-geojson)
  * [GeoJSON rendering improvements](https://github.com/blog/1541-geojson-rendering-improvements)
* STL
  * [STL File Viewing](https://github.com/blog/1465-stl-file-viewing)
  * [3D File Diffs](https://github.com/blog/1633-3d-file-diffs)
* PSD
  * [PSD Viewing & Diffing](https://github.com/blog/1845-psd-viewing-diffing)
* CSV/TSV
  * [See your CSVs](https://github.com/blog/1601-see-your-csvs)
* ipython notebook
  * [GitHub + Jupyter Notebooks = <3](https://github.com/blog/1995-github-jupyter-notebooks-3)
* YAML Metadata
  * [Viewing YAML Metadata in your Documents](https://github.com/blog/1647-viewing-yaml-metadata-in-your-documents)
* PDF
  * [PDF Viewing](https://github.com/blog/1974-pdf-viewing)
* ETC
  * [GitHub now supports Twitter Cards](https://github.com/blog/1388-github-now-supports-twitter-cards)

## Library

* PDF : [pdf.js](https://github.com/mozilla/pdf.js)
* GeoJson : [Leaflet.js](http://leafletjs.com/)
* STL : [Three.js](threejs.org)

## 삽질

반쯤 끝내고 나니 [Github Help:Working with non-code files](https://help.github.com/categories/working-with-non-code-files/) 카테고리가 있는 걸 알았다. OTL..
결국 삽질로 끝내기 싫어서 언급된 라이브러리도 정리했다. 결국 얻어낸 제일 큰 보상은 help 문서에 다 있었다는 깨달음.........