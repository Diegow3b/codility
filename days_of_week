// Given S list of days in week and K days in advace, return the target day.

def answer(S, K):
    days = ["Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun"]
    
    week = int(K/len(days)) # Get the current Week
    cicles = week*len(days) # Check how many cicles
    step = K - cicles # Diference of days between current and target days
    
    count = 0
    subCount = 0
    result = ""
    doLoop = True
    isCurrentDay = False
    
    while doLoop:
        if days[count] == S: # Identify the current day
            isCurrentDay = True
            
        if isCurrentDay: # Start the count from current day to target day
            if subCount == step: # Find the target day
                doLoop=False
                result = days[count]
                
            subCount += 1
            
        if count == len(days)-1: # Resets the week
            count = 0
        else:
            count += 1    
        
    return result
