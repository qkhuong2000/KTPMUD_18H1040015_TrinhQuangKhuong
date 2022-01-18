# KTPMUD_18H1040015_TrinhQuangKhuong
import math 

def is_prime(x):
    if x < 2: 
        return False

    if x == 2: 
        return True

    for i in range(2, int(math.sqrt(x))+1):
        if x % i == 0: return False

    return True

def check_array_1a(num_list):
    count = 0
    for x in num_list:
        if is_prime(x): 
            count += 1
    
    if count >= 2: 
        return True
    else:
        return False

    
def check_array_1b_1(num_list):
    for x in num_list:
        if is_prime(x): 
            return False
    return True

def check_array_1b_2(num_list):
    count = 0
    for x in num_list:
        if is_prime(x): 
            count += 1
    
    if count == 1: 
        return True
    else:
        return False

def check_array_1b_3(num_list):
    count = 0
    for x in num_list:
        if is_prime(x): 
            count += 1
    
    if count >= 1: 
        return True
    else:
        return False

a = [1,2,3,4,5,6]
print(check_array_1a(a))
print(check_array_1b_1(a))
print(check_array_1b_2(a))
print(check_array_1b_3(a))
