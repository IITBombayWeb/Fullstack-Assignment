# Assignment for Fullstack Developer

1.  Create a simple full stack application for Farm management system
    1.  A farm has many plots
    2.  Each plot can grow a variety of trees or crops
    3.  The farmer wishes to keep track of the plantations she has made
2.  Create a github account (if you do not have one)
    1.  Create two **public** repositories
        1.  **Farm backend**
        2.  **Farm frontend**
    2.  Set up SSH key based access to the repositories from your local laptop.
    3.  For every major development in each of the above repositories:
        1.  Create a [new issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/creating-an-issue)
        2.  [Create a Branch](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue#manually-linking-a-pull-request-or-branch-to-an-issue-using-the-issue-sidebar) for this issue
        3.  git fetch and checkout to branch locally
        4.  Make changes, commit, and push to remote
        5.  Compare & pull request; Create pull request
        6.  Merge pull request
3.  **Farm backend: Spring-boot/Django backend service**
    1.  A Plot has information about the geographical aspects of the land
        1.  Identifying label (ID)
        2.  Area (in sq. m)
    2.  Tree has information about what is needed and what will be its annual yield
        1.  Name of tree
        2.  Plot area required for full grown tree (sq. m)
        3.  Annual Yield (in Rs)
    3.  Plantation has information on what was planted in a given plot
        1.  Plot ID
        2.  Name of tree
        3.  Number of trees planted
        4.  Date of plantation
    4.  Write  REST API endpoints that returns a JSON (where applicable):
        1.  /api/v1/plots, /api/v1/trees, /api/v1/plantations with standard http methods GET, POST, PUT, and DELETE
        2.  Implement as many APIs as possible.  Each API must be complete with sample data (see below).
        3.  Examples for plots (similar API must be developed for trees and plantations):
            1.  GET /api/v1/plots : returns a list of plots along with their properties
            2.  GET /api/v1/plots/\<id>: returns information about a single plot with ID=\<id>
            3.  POST /api/v1/plots: create a new plot with the necessary properties
            4.  PUT /api/v1/plots/\<id>: update the plot properties with ID=\<id>
            5.  DELETE /api/v1/plots/\<id>: delete plot with ID=\<id>
        4.  API response codes for each of the APIs
            1.  200: OK
            2.  201: Resource created
            3.  209: No content, resource deleted
            4.  400: Bad request
            5.  404: Resource not found
    5.  git commit your code after every new feature inclusion or bug fix
    6.  Add dummy data to all the entities.  Eg. using curl
        1.  Insert a new record:  
            curl -d ‘name=Manga&area=2&yield=60000’ [http://localhost:8081/api/v1/trees](http://localhost:8081/api/v1/trees)
        2.  Correct the typographical name error in the above request:   
            curl -X PUT ‘name=Mango&area=2&yield=60000’ [http://localhost:8081/api/v1/trees/1](http://localhost:8081/api/v1/trees/1)
    7.  Verify the response. Eg using curl
        1.  curl [http://localhost:8081/api/v1/trees](http://localhost:8081/api/v1/trees) 
        2.  curl [http://localhost:8081/api/v1/trees/2](http://localhost:8081/api/v1/trees/2) 
        3.  curl -X DELETE [http://localhost:8081/api/v1/trees/2](http://localhost:8081/api/v1/trees/2) 
        4.  curl [http://localhost:8081/api/v1/trees/2](http://localhost:8081/api/v1/trees/2)
4.  **Farm frontend: ReactJS/AngularJS frontend UI**
    1.  Develop a front end ReactJS framework for consuming the APIs developed in Farm backend
        1.  Use bootstrap and Material UI components
    2.  Frame 1: Dashboard should contain
        1.  Use any simple elegant design. 
        2.  Total crops: Count of number of types of crops (tree types)
        3.  Total Annual Yield in rupees from the farm
        4.  Buttons to manage the farm components (using the APIs developed)
    3.  Frame 2: Manage trees
        1.  Add a new tree type
        2.  Show list of trees
            1.  With Edit and Delete icons
    4.  Develop similar interfaces (Frames) for
        1.  Manage plots
        2.  Manage plantations        3.  

# Evaluation criteria for quality of code
1. Creation of repositories
2. At least four major issue (branches) in each repository
3. Each pull request must have at least about four commits, with meaningful commit messages
4. Code should follow standard best practices for naming, formatting, and inline documentation
5. Number of APIs implemented and equivalent Frontends
6. API implementation must be complete as specified in the problem statement
7. Frontend must be elegant and responsive



