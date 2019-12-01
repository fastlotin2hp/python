# 1. list, tuples, set 

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
