# Aliyush

# Python 3 program to find the least frequent element in an array. 

  

  

 def leastFrequent(arr, n) : 

  

    # Sort the array 

    arr.sort() 

   

    # find the min frequency using 

    # linear traversal 

    min_count = n + 1

    res = -1

    curr_count = 1

    for i in range(1, n) : 

        if (arr[i] == arr[i - 1]) : 

            curr_count = curr_count + 1

        else : 

            if (curr_count < min_count) : 

                min_count = curr_count 

                res = arr[i - 1] 

              

            curr_count = 1

              

    

    # If last element is least frequent 

    if (curr_count < min_count) : 

        min_count = curr_count 

        res = arr[n - 1] 

      

    return res 

      

   

 arr = [1, 3, 2, 1, 2, 2, 3, 1] 

 n = len(arr) 

 print(leastFrequent(arr, n)) 
