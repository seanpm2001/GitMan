
***

# GitLabel

## Concept

### August 31st 2021

I have had this idea ever since I posted my first GitHub issue. I have always had an issue with GitHub issues, being that you can't export the issues with their associated label data. I aim to fix that.

GitLabel is a tool to apply issue labels to issues and discussions on Git repositories online and offline, and across various Git platforms. It is designed to keep the label data in a YAML file. As an example of how I currently store label data, here is an example for the default 9 GitHub issue labels:

```yaml
issuelabel_1: color1: "#ffffff" title1: "wontfix" description1: "This will not be worked on"
issueLabel_2: color2: "#d876e3" title2: "question" description2: "Further information is requested"
issueLabel_3: color3: "#e4e669" title3: "invalid" description3: "This doesn't seem right"
issueLabel_4: color4: "#008672" title4: "help wanted" description4: "Extra attention is needed"
issueLabel_5: color5: "#7057ff" title5: "good first issue" description5: "Good for newcomers"
issueLabel_6: color6: "#a2eeef" title6: "enhancement" description6: "New feature or request"
issueLabel_7: color7: "#cfd3d7" title7: "duplicate" description7: "This issue or pull request already exists"
issueLabel_8: color8: "#0075ca" title8: "documentation" description8: "Improvements or additions to documentation"
issueLabel_9: color9: "#d73a4a" title9: "bug" description9: "Something isn't working"
```

It is a bit broken, but you can see how complex this is. It should be a lot easier.

With GitLabels, you can define labels easily and just associate a few codes with each issue or discussion, like so:

```gitlabel
:1 :4 :5 :6 :8 :9
```

This will call the issues easily, and once installed on the proper Git platform, it will render properly. Although, a label data file is required, currently I propose for it to be something like this:

GitHub is being used as an example here:

```vim
:GitHubMode()
def label1()
find :(hex) :(numcode) # For color
find :title
find :description_box
find :usage
```

This format needs improvement, but I now have the general idea down.

**Concept defined on 2021 Tuesday August 31st** by [seanpm2001](https://github.com/seanm2001/)

***
