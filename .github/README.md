# Liquid Collection Home
[heading__title]:
  #liquid-collection-home
  "&#x2B06; Top of ReadMe File"


Liquid layout that builds list of pages within named collection


## [![Byte size of collection-home.html][badge__master__collection_home__source_code]][collection_home__master__source_code] [![Open Issues][badge__issues__collection_home]][issues__collection_home] [![Open Pull Requests][badge__pull_requests__collection_home]][pull_requests__collection_home] [![Latest commits][badge__commits__collection_home__master]][commits__collection_home__master] [![Collection Home Demos][badge__demo__collection_home]][demo__collection_home]



------


#### Table of Contents


- [:arrow_up: Top of ReadMe File][heading__title]

- [:zap: Quick Start][heading__quick_start]

  - [:memo: Edit Your ReadMe File][heading__your_readme_file]
  - [&#x1F578; Utilize Collection Home][heading__utilize]
  - [:floppy_disk: Commit and Push][heading__commit_and_push]

- [&#x1F5D2; Notes][heading__notes]

- [&#x2696; License][heading__license]


------



## Quick Start
[heading__quick_start]:
  #quick-start
  "&#9889; Perhaps as easy as one, 2.0,..."


**Bash Variables**


```Bash
_module_name='collection-home'
_module_https_url="https://github.com/liquid-utilities/${_module_name}.git"
_module_relative_path="_layouts/modules/${_module_name}"
```


**Bash Submodule Commands**


```Bash
cd "<your-git-project-path>"

git checkout gh-pages
mkdir -vp "_layouts/modules"

git submodule add\
 -b master --name "${_module_name}"\
 "${_module_https_url}" "${_module_relative_path}"
```


### Your ReadMe File
[heading__your_readme_file]:
  #your-readme-file
  "&#x1F578; Suggested additions for your ReadMe.md file so everyone has a good time with submodules"


Suggested additions for your _`ReadMe.md`_ file so everyone has a good time with submodules


```MarkDown
Clone with the following to avoid incomplete downloads


    git clone --recurse-submodules <url-for-your-project>


Update/upgrade submodules via


    git submodule update --init --merge --recursive
```


### Utilize Collection Home
[heading__utilize]:
  #utilize-collection-home
  "&#x1F578; How to make use of this submodule within another project"


**`_your_collection/index.md`**

```YAML
---
layout: modules/collection-home/collection-home
title: Your Collection
collection_name: your_collection
list_title: Pages available within Your Collection
---

## Collection Home list content


> This text will be compiled and rendered
> prior to list of collection pages!
```


Additionally targeting by collection name enables...


**`your_collection.md`**


```YAML
---
layout: modules/collection-home/collection-home
title: Your Collection
collection_name: your_collection
list_title: Pages available within Your Collection
---
```


... meaning that collection homes may be placed anywhere!


Each collection page should contain the following FrontMatter...


**`_your_collection/something-collected.md`**


```YAML
## Layout maybe `post` or really any available layout
layout: page
title: Title for an individual post
date: 2019-07-21 11:42:11 -0300
description: Example collection page about something
```


### Commit and Push
[heading__commit_and_push]:
  #commit-and-push
  "&#x1F4BE; It may be just this easy..."


```Bash
git add .gitmodules
git add _layouts/modules/collection-home


## Add any changed files too


git commit -F- <<'EOF'
:heavy_plus_sign: Adds `liquid-utilities/collection-home#1` submodule



**Additions**


- `.gitmodules`, tracks submodules AKA Git within Git _fanciness_

- `README.md`, updates installation and updating guidance

- `_layouts/modules/collection-home`, builds list of pages for a named collection
EOF


git push origin gh-pages
```


**:tada: Excellent :tada:** your site is now ready to begin unitizing code from this repository!


___


## Notes
[heading__notes]:
  #notes
  "&#x1F5D2; Additional resources and things to keep in mind when developing"


This layout is written to operate without modifications **if** utilizing the Minima (default Jekyll) theme, otherwise edits are currently required icon lines...


```HTML
<use xlink:href="{{ '/assets/minima-social-icons.svg#rss' | relative_url }}"></use>
```


... In the future this theme may make an attempt to detect and auto link for themes available on GitHub Pages.


Permalinks and underscore (**`_`**) generally are _sluggified_ such that _`file_name.md`_ transmutes into something like _`file-name.html`_



------


Timezone offsets also require that `timezone` is set within the site `_config.yml` file; check [Wikipedia -- List of tz database time zones](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) for mapping hints, eg...


**`_config.yml`** snip...


```YAML
timezone: America/Los_Angeles
```


**`_your_collection/something-collected.md`** snip...


```YAML
date: 2019-07-21 11:42:11 -0800
```


... if `timezone` is not defined then built HTML documents will default to an offset of `0000` which will cause both the date (day) and time (hour) to be recalculated.


___


## License
[heading__license]:
  #license
  "&#x2696; Legal bits of Open Source software"


Legal bits of Open Source software


```
Collection Home ReadMe documenting how things like this could be utilized
Copyright (C) 2024  S0AndS0

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Affero General Public License as published
by the Free Software Foundation; version 3 of the License.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
```



[badge__commits__collection_home__master]:
  https://img.shields.io/github/last-commit/liquid-utilities/collection-home/master.svg

[commits__collection_home__master]:
  https://github.com/liquid-utilities/collection-home/commits/master
  "&#x1F4DD; History of changes on this branch"


[collection_home__community]:
  https://github.com/liquid-utilities/collection-home/community
  "&#x1F331; Dedicated to functioning code"


[collection_home__gh_pages]:
  https://github.com/liquid-utilities/collection-home/tree/gh-pages
  "Source code examples hosted thanks to GitHub Pages!"



[badge__demo__collection_home]:
  https://img.shields.io/website/https/liquid-utilities.github.io/collection-home/index.html.svg?down_color=darkorange&down_message=Offline&label=Demo&logo=Demo%20Site&up_color=success&up_message=Online

[demo__collection_home]:
  https://liquid-utilities.github.io/collection-home/index.html
  "&#x1F52C; Check the example collection tests"


[badge__issues__collection_home]:
  https://img.shields.io/github/issues/liquid-utilities/collection-home.svg

[issues__collection_home]:
  https://github.com/liquid-utilities/collection-home/issues
  "&#x2622; Search for and _bump_ existing issues or open new issues for project maintainer to address."


[badge__pull_requests__collection_home]:
  https://img.shields.io/github/issues-pr/liquid-utilities/collection-home.svg

[pull_requests__collection_home]:
  https://github.com/liquid-utilities/collection-home/pulls
  "&#x1F3D7; Pull Request friendly, though please check the Community guidelines"


[badge__master__collection_home__source_code]:
  https://img.shields.io/github/size/liquid-utilities/collection-home/collection-home.html.svg?label=collection-home.html

[collection_home__master__source_code]:
  https://github.com/liquid-utilities/collection-home/blob/master/collection-home.html
  "&#x2328; Project source, one Liquid file of actionable code!"
