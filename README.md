## Package Requirements

### Mac/Ubuntu Operating System
- Other OS-es have not been tested, and may cause unexpected errors.

## Creating A New Repository from the Template

To create a new project by using this template as skeleton, we need to manually "fork" this template. Extra precaution is also required as the python-template contains links to other repos (submodules).

Please replicate the steps below in Terminal to ensure success.

``` sh
# First: Create an empty repository in github via https://github.com/new

# Clone the newly created empty repo
git clone https://github.com/<username>/<new_repo_project_name>

# Define this clone as a fork of python-template
cd <new_repo_project_name> 
git remote add upstream https://github.com/lemuelkumarga/python-template.git

# Pull all the files from the template
git pull upstream master

# Initialize submodules
git submodule init
git submodule update

# When cloned, submodules are detached from the HEAD. We attempt to rectify this issue to prevent problems in git
cd shared
git checkout -b tmp
git checkout master
git merge tmp
git branch -d tmp
cd ..

# Push your changes to the cloud
git push -u origin master

# Return to original folder if desired
cd ..
```

## Cloning the Repository

Cloning the repository is not as straightforward due to the presence of git submodules.

Please replicate the steps below in Terminal to ensure success.

``` sh
# Clone the repo as usual
git clone https://github.com/lemuelkumarga/python-template

# Initialize submodule
cd python-template
git submodule init
git submodule update

# When cloned, submodules are detached from the HEAD. We attempt to rectify this issue to prevent problems in git
cd shared
git checkout -b tmp
git checkout master
git merge tmp
git branch -d tmp

# Return to original folder if desired
cd ../../
```


# Insert Title Here

### <i>Lemuel Kumarga</i>


## Problem Description

Insert Problem Description Here.



## Preliminaries

First load the necessary modules for this exercise.


```python
import sys
sys.path.append('shared/')
from defaults import *

# Load All Main Packages and SubPackages
load({"pd":"pandas",
      "np":"numpy",
      "py":"plotly",
      "sp":"scipy"},
     {"plot":"py.offline",
      "plot_g":"py.graph_objs"})

# Set Up Defaults
defaults()
```


<script>requirejs.config({paths: { 'plotly': ['https://cdn.plot.ly/plotly-latest.min']},});if(!window.Plotly) {{require(['plotly'],function(plotly) {window.Plotly=plotly;});}}</script>





<link href="shared/css/defaults.css" rel="stylesheet"><link href="../../shared/css/definitions.css" rel="stylesheet"><link href="../../shared/css/general.css" rel="stylesheet"><link href="shared/css/python.css" rel="stylesheet"><script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script><script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script><script src="shared/js/styles.js"></script><script src="shared/js/popover.js"></script>



## Lorem Ipsum

<a data-toggle="popover" title="Lorem Ipsum" data-content="Lorem Ipsum is simply dummy text of the printing and typesetting industry. Data obtained from https://www.lipsum.com/.">Lorem ipsum</a> dolor sit amet, consectetur adipiscing elit. Vivamus sit amet urna nunc. Ut bibendum sem nibh, lobortis tempor dolor scelerisque ut. Nunc elit lorem, accumsan in pharetra ac, sodales sit amet arcu. In hac habitasse platea dictumst. Sed accumsan fringilla purus. Aliquam tincidunt ultricies sapien, eu pellentesque quam porttitor dignissim. Cras convallis, ipsum feugiat porttitor tempus, tortor orci fringilla augue, vel ultrices magna massa varius nibh. Ut gravida posuere dolor, non tincidunt eros sollicitudin in. Curabitur quis odio condimentum lectus congue fermentum id eget odio. Proin sagittis, nisl ac imperdiet ornare, metus risus tempor velit, gravida laoreet lacus purus in metus. Sed sed cursus dolor. Aliquam lobortis purus eget iaculis interdum. Maecenas nec eros magna.

Curabitur at urna in urna scelerisque maximus non ut urna. Nulla pharetra ipsum neque, quis dapibus ex egestas a. Nunc condimentum lectus et sapien convallis molestie. Suspendisse vel massa fringilla, imperdiet diam ut, fringilla lacus. Aliquam molestie orci purus, a tristique lacus malesuada quis. Ut rutrum lacus non vulputate iaculis. Cras tincidunt risus nisl, lobortis pellentesque purus laoreet in. Ut malesuada erat eu massa efficitur, condimentum euismod ligula imperdiet. Nunc lorem tortor, placerat iaculis facilisis vitae, euismod id nisl. Duis venenatis pharetra arcu sed sagittis. Vivamus eu ex vitae odio eleifend congue. Proin iaculis imperdiet sapien, et lobortis libero efficitur in. In ac ex elementum, ornare elit id, lacinia erat.


```python
plot.iplot({
    "data": [plot_g.Scatter(x=[1, 2, 3, 4], y=[4, 3, 2, 1])],
    "layout": plot_g.Layout(title="hello world", autosize=True)
})
```


<div id="f83932e1-35ae-4d53-8e93-8056b93e626c" style="height: 525px; width: 100%;" class="plotly-graph-div"></div><script type="text/javascript">require(["plotly"], function(Plotly) { window.PLOTLYENV=window.PLOTLYENV || {};window.PLOTLYENV.BASE_URL="https://plot.ly";Plotly.newPlot("f83932e1-35ae-4d53-8e93-8056b93e626c", [{"type": "scatter", "x": [1, 2, 3, 4], "y": [4, 3, 2, 1]}], {"title": "hello world", "autosize": true}, {"showLink": true, "linkText": "Export to plot.ly"})});</script>

