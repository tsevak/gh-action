# Build Application container image by github aciton


This Github action builds container image based on Dockerfile. While building Image it goes through triviy image scanner for security analaysis, if it founds critical non fixable issues,it stops building process and notify user on slack else it does produce build and push to container registry with slack notfication

Currently configured event triggers are push on main branch and manual worflow run

## Pre-requisites

* Configure secrets based repo
    * Slack webhook url for notifications
    * Container registry authentication access details
  

## Integration with Slack to get notifications
![gh-action-slack](gh-action-slack-notfication.png)
