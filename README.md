To deploy our Angular website to Github pages using Github Actions, follow the below steps:-
1) create a file main.yaml in .github/workflows
2) Yaml file has event (on) , jobs , runner (run-on) , steps
3) We have chossen push on main braanch as event to trigger the workflow
4) Once you commit in main branch, it wil trigger a workflow which you can track in Actions Tab.
5) Here, we have used two steps :- checkout and custom step by Ayaz for github pages
  
  
  name: Angular Deploy gh-pages Actions
  on: 
    push:  (push event/ pull-request )
      branches:
      - main   (main bracnh)
  jobs:
   build:
    runs-on: Ubuntu-20.04
    steps:
    - uses: actions/checkout@v2
    - name: All things angular
      uses: AhsanAyaz/angular-deploy-gh-pages-actions@v1.3.1 ## replace by latest version without it you will see Expected format {org}/{repo}[/path]@ref. Actual 'AhsanAyaz/angular-deploy-
