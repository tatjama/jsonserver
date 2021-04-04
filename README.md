# Fake API for testing 

1. GET SINGLE PROJECT
http://localhost:3000/projects/1

2. GET ALL TASKS FROM PROJECT
http://localhost:3000/projects/1/tasks

3. FILTER PROJECTS BY NAME
http://localhost:3000/projects?name=Project2
http://localhost:3000/projects?name=Project2&name=Project3
http://localhost:3000/tasks?title=Task6&title=Task4

4. PAGINATION & LIMIT
http://localhost:3000/projects?_page=1&_limit=2
http://localhost:3000/tasks?_page=1&_limit=5

5. SORTING
http://localhost:3000/projects?_sort=name&_order=asc
http://localhost:3000/projects?_sort=name&_order=desc
http://localhost:3000/tasks?_sort=title&_order=

6. TASKS ESTIMATED HOURS
http://localhost:3000/tasks?estimate_gte=5
http://localhost:3000/tasks?estimate_gte=5&estimate_lte=10

7. FULL TEXT SEARCH 
http://localhost:3000/tasks?q=Zadatak




FULL DOCUMENTATION
https://github.com/typicode/json-server#install
Remote version is on the
https://jsonplaceholder.typicode.com/

# INSTRUCTION:

1. Create empty folder e.g. ("jsonserver")
2. cd jsonserver
3. npm init
4. mpn install --save json-server
5. jsonserver/package.json add in scripts

    "scripts": {
    "json:server": "json-server --watch db.json"
  },
6. create file db.json with data 
7. run server with
    npm run json:server
9. find it on 
    http://localhost:3000