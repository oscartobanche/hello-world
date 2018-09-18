#Oscar tobanche
#Prof. Diego Aguirre
# Lab 1 version C
#9/17/2018
import hashlib
from itertools import product
def hash_with_sha256(str):
    hash_object = hashlib.sha256(str.encode('utf-8'))
    hex_dig = hash_object.hexdigest()
    return hex_dig
def main():


    x=[]
    y=[]
    input = open("password_list", "r")
    i = 0
    for line in input:

        name,salt,hashed = line.split(",");
        salt.replace("","")
        x[i]
        hashed.replace("","")
        y[i]
        i = i + 1
# we call the method with the parameters that hold :length,
    hack(3, 0, '000', 1000, x, y)



def hack(length, position, password, maxVal ,x,y):
    for j in range(0,99):
        for i in range(0,maxVal):
        #this executes if we reach the max value}
            if i == maxVal:
                hack(length + 1, position, password +'0' , maxVal *10)
            #this happens if we have to verify
                s = password + x[position]
                hex_dig = hash_with_sha256('string')
                print(hex_dig)

        #if we found password
            if hex_dig == y[position]:
                return print("the password is:  " + password + " for user " + i+1)
            #if we dont
            print("we will try a different guess")
        #we have to perform casting from str to int and backwards, this is to change the password try ex, from 000 to 001
            int(password)
            password = password + 1
            str(password)
            i = i + 1
            # the position variable increments by 1 every time we go to the next user, this has an  array index counter purpose
        position = position + 1
        j = j + 1
