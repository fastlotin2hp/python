# 1. list, tuples, set 
## list
  ```python
  courses =['machine_learning','statistics','algebra','computer_vision']
  print("length,first item,last item,item[1 and2]")
  print(len(courses),courses[0],courses[-1],courses[1:3])
  advanced_courses =['deep_learning','NLP']
  print(courses.extend(advanced_courses)
  print(courses.append(advanced_courses),courses.insert(0,'basic AI'))
  
  courses.remove('algebra')
  last_course_on_list=courses.pop()
  
  print(courses.reverse(),sorted(courses),courses.sort(reverse=True))
  
  # find course
  print('computer' in courses)
  print(courses.index('computer_vision'))
  
  # loop courses
  for index,course in enumerate(courses,start=1)
    print(index,course)
    
  # to one string 
  str=','.join(courses)
  list_str=str.split(',')
  print(str,list_str)
  ```
### slicing
  ```python
  a_list= [0,1,2,3,4,5]
  a_list[start:end:step]
  print(a_list[1:4:2],a_list[-2:1:-2])
  print("positve step go forward,negetive step go backward")
  ```
  
## tuple
### 1 mutable/ immutable
```python
#can /can not be modified after it is created

#string is immutable, so the a will be reassign,and the 
#charater inside the a can not be changed
a='item1'
print(a,'address of a is',id(a))

a='item2'
print(a,'address of a is',id(a))

a[1]='e' #get error

#list is mutable,
a=[1,2,3,4,5]
print(a,'address of a is',id(a))

a[0]=2
print(a,'address of a is',id(a))
```
### 2 immutable perfromance issue
```python
#create object in each iteration
courses =['machine_learning','statistics','algebra','computer_vision']
registered_courses='regeisted: '
for course in courses:
  registered_courses+=course
  print(id(registered_courses),registered_courses)

```

# 1. OOP
## 1 class
  
  ```python

  class Person(object):
    def __init__(self,name):
      self.name=name
      
    def show_identity(self):
      print("I am ",self.name)
      print("I am {}".format(self.name))
  
  class Occupation(Person):
    def __init__(self,name,occupation_title):
      super(Occupation,self).__init__(name)
      self.occupation_title=occupation_title
      
    def show_identity(self):
      super(OccupationTitle,self).show_identity()
      print("and my title is ",self.occupation_title)
      print("and my title is {}".format(self.occupation_title))
      
   #------------------------------
    me=Person('hp')
    me.show_identity()
    
    worker=Occupation('hp','engineer')
    worker.show_identity()
  ```
