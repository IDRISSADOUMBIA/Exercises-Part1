# Exercises-Part1

#-----------------------

def match_ends(my_list):
    
    count=0
    
    for words in my_list :
        size=len(words)
        if size >2 and words[0]== words[size-1]:
            count+=1    
    return count
    


my_words=["america", "Paris", "otto","volvo", "mooom"]  

print (match_ends(my_words))


#-----------------------


def front_x(my_list):
        
    sublist1=[]  # beginning with X
    sublist2=[]
    final=[]
    

    for wordss in my_list:
        if wordss[0]=="x": 
            if wordss==my_list[0]:                
                sublist1[0]= wordss
            else:
                sublist1.append(wordss) 
        else:
             sublist2.append(wordss) 
             
             
    sublist1.sort()
    sublist2.sort()
    
    final=sublist1+sublist2
    
    return final
    
         
test_words= ["mix", "xyz", "apple", "xanadu", "aardvark"]

print (front_x(test_words)) 


#--------------------

def takelast(elem):
    
    size_elem = len(elem)
    return elem[size_elem-1]



def sort_last(mtuples):
    
    result=[]

        
    mtuples.sort(key=takelast)
    
    result=mtuples     
        
    return result
   
        
my_tuples= [(1, 7), (1, 3), (3, 4, 5), (2, 2)]
print (sort_last(my_tuples)) 


#-------------------------------------

def remove_adjacent(nums):
    result = []
    for num in nums:
        if len(result) == 0 or num != result[-1]:
            result.append(num)
    return result
    
    
my_test= [1,2,2,3,4,2,5,6,7,8,8]
print (remove_adjacent(my_test)) 
