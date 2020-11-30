# Given S=["A", "B"], X=[1,1] and Y=[1, -1] draw a circle with the minimal points inside ot it, tags cannot be repeated.

def get_distance(a,b):
    return (a**2 + b**2) ** 0.5

def solution(S, X, Y):
    arr_idx = []
    arr_keys = []
    arr_values = []
    distance_limit = 0
    for i in range(0, len(X)):
        distance = get_distance(X[i], Y[i])
        if S[i] in arr_keys:
            for x in range(0, len(arr_keys)):
                    
                if arr_keys[x] == S[i] and distance >= arr_values[x]:
                    distance_limit = distance
        else:
            arr_idx.append(i)
            arr_keys.append(S[i])
            arr_values.append(distance)
            
    if distance_limit:
        try:
            for _ in range(0, len(arr_values)):
                if arr_values[_] >= distance_limit:
                    arr_idx.pop(_)
                    arr_keys.pop(_)
                    arr_values[_] = -1
        except:
            return 0
    return len(arr_idx)
