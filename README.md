
# Python program to convert time
# from 12 hour to 24 hour format

# Function to convert the date format
def convert24(strl):
    # checking if last two elements of time
    # is AM and first two elements are 12
    if strl[-2:] == "AM" and strl[:2] == "12":
        return "00" + strl[2:-2]

    # remove the AM
    elif strl[-2:] == "AM":
        return strl[:-2]

    # checking if last two elements of time
    # is PM and first two elements are 12
    elif strl[-2:] == "PM" and strl[:2] == "12":
        return strl[:-2]

    else:

        # add 12 to hours and remove PM
        return str(int(strl[:2]) + 12) + strl[2:8]


# Driver code
print(convert24("04:00:00 PM"))
