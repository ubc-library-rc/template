---
layout: default
title: Topics and workshop lists 
nav_order: 2 
---
# Topics and workshop lists 
The Research Commons uses GitHub *topics* to organize our repositories. We apply topics in a systematic way to:

- group repositories by team  
- generate online lists of workshops 

## Topics for teams
Each workshop repository should have at least one topic from the table below. Collaborative workshops may have more than on team topic.

| Topic | RC Team |
|-------|-------------|
| `citation` | Citation management |
| `data` | Data analysis and visualization |
| `digital-scholarship` | Digital Scholarship |
| `geospatial` | Geographic information systems and mapping |
| `research-data-management` | Research data management |
 
Team topics control how workshops are grouped in online lists
{: .note}


## Topics for online lists
Topics control how worskhops appear on two public-facing lists:

- <https://ubc-library-rc.github.io/all.html> - all workshops
- <https://ubc-library-rc.github.io/index.html> - featured workshops

To appear on the "all workshops" list, a repository must have at least one team topic in addition to the topic `workshop`.

To appear on the "featured workshops" page the repository must also have the `featured` topic.


When a repository is "archived" in GitHub settings it displays in italics on the "all workshops" list; archived workshops should not be `featured`. 
{: .note}


## _Optional:_ manual workshop lists
Teams may prefer to control their section of a workshop list manually instead of using the automatically generated list. For example: 

- The Research Data Managment team has several workshops in a single repository. To list each workshop separately they must edit manually, since the automatic process creates one list item per repository.

- Several Citation Management team workshops are not in GitHub. To include these non-repository workshops they must edit their list manually.

To change a manually edited list, edit the corresponding html file in the `ubc-library-rc.github.io` repository. 

- all workshop list: <https://github.com/ubc-library-rc/ubc-library-rc.github.io/blob/master/non_repo_workshops.html>
- featured workshop list: <https://github.com/ubc-library-rc/ubc-library-rc.github.io/blob/master/non_repo_featured_workshops.html>

For a group to switch between manual and automatic workshop lists, corresponding changes must be made to the the GitHub action script. 
{: .note}
