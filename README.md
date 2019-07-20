# RateMyProfessorPy


*RateMyProfessor API for py(no auth required)*

* [2019/07/20] - Added a function to allow users to specify ```schoolId```, if ```schoolId``` is not specified, ASU will be the default school for the search result.
* [2019/07/19] - Added a function to get tags of a specific professor from RMP
* [2019/07/18] - Project Launched

install the package using the following command:

```
py -m pip install RateMyProfessorPyAPI
```

if update is needed, use following code:
```
py -m pip install RateMyProfessorPyAPI --upgrade
```

Use following code to start the api in python:
```py
aapi = RMPClass.RateMyProfAPI(schoolId="xxx", teacher="xxx")
aapi.retrieveRMPInfo()
```

* `schoolId`, string type, **optional, but recommended**. Can be found when searching on the RMP wesbite. I will consider to add a function to get the `schoolId` in the future, a sample input will be `schoolId="45"`
* `teacher`, string type, **required**. Must be the full name! A sample input will be: `teacher="Yinong Chen"`

Use following code to check specific professor's rating out of 5.0:
```
aapi.getRMPInfo()            #string
```

Use following code to check specific professor's tags:
```
aapi.getTags()              #string
```

Use following code to check specific professor's hottest tag:
```
aapi.getFirstTag()         #string
```

Use following code to check the percentage that students would take again:
```
aapi.getWouldTakeAgain()   #string
```

When result is not found, methods will return `INFO_NOT_AVAILABLE`, in that case, you can customize the msg that you want to return in the package.
