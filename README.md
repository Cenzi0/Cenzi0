q1'''
    TLO: 112-SCRPY002, LSA 3,4
    Given the floatstr, which is a comma separated string of
    floats, return a list with each of the floats in the
    argument as elements in the list.
    '''
   
   def q1(floatstr):
      List = []
      for i in floatstr.split('.')
            List.append(float(i))
      return list

List comp 
    Return [float(i) for i in floatstr.split(‘,’)]

    

'''
    TLO: 112-SCRPY006, LSA 3
    TLO: 112-SCRPY007, LSA 4
    Given the variable length argument list, return the average
    of all the arguments as a float
    '''
    
    Return sum(args)/len(args)


'''
    TLO: 112-SCRPY004, LSA 3
    Given a list (lst) and a number of items (n), return a new
    list containing the last n entries in lst.
    '''
    
    return lst[-n:]

'''
    TLO: 112-SCRPY004, LSA 1,2
    TLO: 112-SCRPY006, LSA 3
    Given an input string, return a list containing the ordinal numbers of
    each character in the string in the order found in the input string.
    '''
   
   
   def q4(strng):
        dumb = []
        for i in strng:
                dumb.append(ord(strng))
        return dumb

List comp
    Return [ord(i) for i in strng]






'''
    TLO: 112-SCRPY002, LSA 1,3
    TLO: 112-SCRPY004, LSA 2
    Given an input string, return a tuple with each element in the tuple
    containing a single word from the input string in order.
    '''


Return tuple(strng.split())



Q6 '''
    TLO: 112-SCRPY007, LSA 2
    Given a dictionary (catalog) whose keys are product names and values are product
    prices per unit and a list of tuples (order) of product names and quantities,
    compute and return the total value of the order.

    Example catalog:
    {
        'AMD Ryzen 5 5600X': 289.99,
        'Intel Core i9-9900K': 363.50,
        'AMD Ryzen 9 5900X': 569.99
    }

    Example order:
    [
        ('AMD Ryzen 5 5600X', 5),
        ('Intel Core i9-9900K', 3)
    ]

    Example result:
    2540.45

    How the above result was computed:
    (289.99 * 5) + (363.50 * 3)
    '''


Total = 0
For product, quantity in order:
    Total += catalog[product] * quantity
Return total

*catalog is our dictionary, we are going to reference the product in said dictionary to get 




'''
    TLO: 112-SCRPY005, LSA 1
    Given a filename, open the file and return the length of the first line
    in the file excluding the line terminator.
    '''
    
    
    def q7(filename):
        Lines = []
        with open(filename, 'r') as fp:
                no = fp.readlines()
            return len(no[0]) -1




             '''
    TLO: 112-SCRPY003, LSA 1
    TLO: 112-SCRPY004, LSA 1,2
    TLO: 112-SCRPY005, LSA 1
    Given a filename and a list, write each entry from the list to the file
    on separate lines until a case-insensitive entry of "stop" is found in
    the list. If "stop" is not found in the list, write the entire list to
    the file on separate lines.
    '''



Def q8(filename,lst):
    With open(filename, ‘w’) as fp:
        For i in lst:
            If i.lower() == ‘stop’:
                Break
            fp.write(f’{i}\n’)



'''
    TLO: 112-SCRPY003, LSA 1
    Given the military time in the argument miltime, return a string
    containing the greeting of the day.
    0300-1159 "Good Morning"
    1200-1559 "Good Afternoon"
    1600-2059 "Good Evening"
    2100-0259 "Good Night"
    '''


def q9(miltime):
    if miltime >= 300 and miltime <= 1159:
            return "Good Morning"
    elif miltime >= 1200 and miltime <= 1559:
            return "Good Afternoon"
    elif miltime >= 1600 and miltime <= 2059:
            return "Good Evening"
    else:
            return "Good Night"


'''
    TLO: 112-SCRPY003, LSA 1
    TLO: 112-SCRPY004, LSA 1
    Given the argument numlist as a list of numbers, return True if all
    numbers in the list are NOT negative. If any numbers in the list are
    negative, return False.
    '''


def q10(numlist):
for i in numlist:
            if i < 0:
                    return False
        return True

OR

Return all(map(lambda x: x >= 0,numlist))
            

(Lambda ‘variable’: ‘action on variable’, ‘list we take it from’)

def q1(sentence):
    my = sentence.split(' ')
    almost = my[::-1]
    return ' '.join(almost)
    
    
    '''
    Given a string of multiple words separated by single spaces,
    return a new string with the sentence reversed. The words
    themselves should remain as they are. For example, given
    'it is accepted as a masterpiece on strategy', the returned
    string should be 'strategy on masterpiece a as accepted is it'.
    '''
    pass




def q2(n):
    if n > 0:
            return "{:,}".format(n)

    '''
    Given a positive integer, return its string representation with
    commas seperating groups of 3 digits. For example, given 65535
    the returned string should be '65,535'.
    '''
    pass




def q3(lst0, lst1):
    newL = []
    for i in lst0:
            newL.append(i)
    for i in lst1:
            newL.append(i)
    return sorted(newL, reverse=True)
   
OR
    Return sorted(lst0+lst1, reverse=True)
   
   
   '''
    Given two lists of integers, return a sorted list that contains
    all integers from both lists in descending order. For example,
    given [3,4,9] and [8,1,5] the returned list should be [9,8,5,4,3,1].
    The returned list may contain duplicates.
    '''
    pass



def q4(s1,s2,s3):
    sumting = (s1 + s2 + s3)/3
    if sumting > 50:
            return 'GO'
    else:
            return 'NOGO'
OR
    Return ‘GO’ if (s1+s2+s3)/3 >50 else ‘NOGO’
    
    
    '''
    Given 3 scores in the range [0-100] inclusive, return 'GO' if
    the average score is greater than 50. Otherwise return 'NOGO'.
    '''
    pass



def q5(integer, limit):
    mylist = [0]
    dumb = integer
    while dumb < limit:
            dumb += integer
            if dumb % 2:
                pass
            else:
                mylist.append(dumb)
    return mylist
OR
    Multiples = []
For i in range(0, limit+1):
If (i%integer==0) and (i%2==0)
multiples.append(i)
Return multiples
OR
Return [for i in range(0,limit+1) if (i%integer==0) and (i%2 ==0)
 
    
    
    '''
    Given an integer and limit, return a list of even multiples of the
    integer up to and including the limit. For example, if integer==3 and
    limit==30, the returned list should be [0,6,12,18,24,30]. Note, 0 is
    a multiple of any integer except 0 itself.
    '''
    pass




def q6(f0, f1):
    diffs = []
    linenum = 0

    with open (f0) as fp0:
            with open(f1) as fp1:
                file0 = fp0.readlines()
                file1 = fp1.readlines()
    for i in file0:
            if i != file1[linenum]:
                diffs.append(linenum)
            linenum += 1

    return diffs



    '''
    Given two filenames, return a list whose elements consist of line numbers
    for which the two files differ. The first line is considered line 0.
    '''
    pass


def q7(lst):
    l1=[]
    for i in lst:
            if i not in l1:
                l1.append(i)
            else:
                   return i

   
   
   '''
    Return the first duplicate value in the given list.
    For example, if given [5,7,9,1,3,7,9,5], the returned value should
    be 7.
    '''
    pass



def q8(strng):
    return len(min(strng.split(), key=len))
OR
    smol=100
    For i in string.split():
        If len(i) < smol:
            Smol = len(i)
    Return smol
   
   
   '''
    Given a sentence as a string with words being separated by a single space,
    return the length of the shortest word.
    '''
    pass


def q9(strng):
    chars =[]
    for i in strng:
        if i.isnumeric()
            chars.append(i)

    return chr(int(''.join(chars)))
   
   
   
   '''
    Given an alphanumeric string, return the character whose ascii value
    is that of the integer represenation of all of the digits in the string
    concatenated in the order in which they appear. For example, given
    'hell9oworld7', the returned character should be 'a' which has
    the ascii value of 97.
    '''
    pass


def q10(arr):
   
    for i in range(0,len(arr)-1):
        if arr[i+1] - arr[i] != 1:
            return arr[+1]

   
   
   '''
    Given a list of positive integers sorted in ascending order, return
    the first non-consecutive value. If all values are consecutive, return
    None. For example, given [1,2,3,4,6,7], the returned value should be 6.
    '''
    pass




Take all unique letters from 2 strings and output a sorted string to the console

    def longest(a1, a2):
    Alpha = []
    for i in a1:
        if i not in Alpha:
            Alpha.append(i)
    for i in a2:
        if i not in Alpha:
            Alpha.append(i)
    return ''.join(sorted(Alpha))

***all join statements are what symbol/delimiter you are using to join the list with, followed by .join(your list)



TYPECASTING ITEMS IN A LIST

return [int(x) for x in list]

Find the shortest word
    def find_short(s):
    List = s.split()
    print(List)
    for i in List:
        if len(i) < len(List[-1]):
            List.append(i)
    return len(List[-1])



list(mylist[index]) == the


myIP = ‘192.168.28.50’
myIP.split(‘.’)
See if the fourth octet falls into a range
    If int (myIP.split(‘.’)[-1]) <= 62:
        print(‘this ip falls within that range’)



Mylist[start:stop:step]
    Reference a group of indices
Mylist[-1]
    Gives last value
Mylist[-2:]
    Starts at second to last and steps to the end


Mylist[::-1]
    Steps backwards (reversed
range(start:stop:step)
Mylist = list(range(0,10))
Mylist = [0,1,2,3,4,5,6,7,8,9]


First = ‘aaron’
Middle = ‘andrew’
Last = ‘anderson’
Domain = ‘cornetto’
SHORTHAND FORMAT
f’{first}.{middle[0]}.{last}@{domain}.com’


myDict = {}
myDict[‘Pvt’] = ‘E-1’
myDict[‘PFC’] =’E -2’
{‘pvt’: ‘E-1’, ‘PFC’: ‘E-2’}
For i in myDict:
    print(i)
    (prints the keys)
For i in myDict:
    Print(MyDict[i])



Myroster = [‘PFC’, LCpl, LCpl , Pvt, PFC, Pvt, Sgt’]
    For i in myRoster:
        If i in myDict:
            myDict[i] +=1
        Else :
            myDict[i] = 1


FILE IO
With open (‘myfile.txt’, ‘r’) as fp:
    print(fp.read()[:ammount of chars])
    print(fp.readlines()[:ammount of lines]

Infile = ‘myfile.txt’
Outfile = ‘outfile.txt’

With open(infile, ‘r’) as fp:
    lines0 = fp.readlines()

With open(outfile, ‘w’) as fp1:
    fp1.writelines(lines0)

With open (infile, ‘r’) as fp:
    With open(outfile, ‘w’) as fp1:
        fp1.writelines(fp.readlines())


***you can index reference read lines to only get the lines that you want

Email = (email)

Count = 0
    
    While count <10:
        Count += 1
        print(“ The count is: {}”.format(count))    
        If count == 5:
            print(“Count is 5”)
            break

myList = [‘dog’ , ‘cat’ , ‘bat’ , ‘SHARK’]
For c(index), i(digit) in enumerate(myList):
    myList[c] = i * 2

myList is now equal [‘dogdog’ , ‘catcat’ , ‘batbat’ , ‘SHARKSHARK’]



