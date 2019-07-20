# RateMyProfessorPy


*RateMyProfessor API for py(no auth required)

* [2019/07/20] - Added a function to allow users to specify ```schoolId```, if ```schoolId``` is not specified, ASU will be the default school for the search result.
* [2019/07/19] - Added a function to get tags of a specific professor from RMP
* [2019/07/18] - Project Launched

installing the package using the following command:

```
py -m pip install RateMyProfessorPyAPI
```

if update is needed, use following code:
```
pip -m pip install RateMyProfessorPyAPI --upgrade
```

Use following code to start the api in python:
```py
aapi = RMPClass.RateMyProfAPI(schoolId=45, teacher="xxx")
aapi.retrieveRMPInfo()
```

Use following code to check specific professor's rating out of 5.0:
```py
aapi.getRMPInfo()            #string
```

Use following code to check specific professor's tags:
```py
aapi.getTags()              #string
```

Use following code to check specific professor's hottest tag:
```py
aapi..getFirstTag()         #string
```

Use following code to check the percentage that students would take again:
```py
aapi.getWouldTakeAgain()   #string
```
