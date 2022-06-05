# KOSS_Task
#Task1
#Python script for giving a rough idea about co routine

#Co-routine Number 1

def search_text():
    import time
    test_str = "Hello This is my KOSS Task number - 1, about coroutines"
    time.sleep(3)
    #Adding a delay of 3 seconds in the first instance of usage

    while True:
        test = (yield)
        if test in test_str:
            print("The test string was found in test_str!")
        else:
            print("No!The test string was not found in test_str")



search = search_text()
next(search)
search.send("Hello")#This instance takes 3 seconds to be seen in the ouput
input("Now, Press any key !")
search.send("Hello This")#This instance almost instantly appears after previous operation
