белые_фасоли = 75
черные_фасоли = 150
черные_на_столе = 0

while белые_фасоли + черные_фасоли > 1:
    if белые_фасоли >= 2:
        белые_фасоли -= 2
        черные_фасоли += 1
        черные_на_столе += 1
        if черные_на_столе > 0:
          черные_на_столе -= 1
        else:
            черные_фасоли -= 1
    elif белые_фасоли == 1 and черные_фасоли >= 1:
        белые_фасоли -= 1
        черные_на_столе +=1
    elif белые_фасоли == 0 and черные_фасоли >= 2:
      черные_фасоли -= 1
      черные_на_столе += 1 
    
    elif белые_фасоли == 1 and черные_фасоли == 0:
      break # Остался один белый горошек
    elif белые_фасоли == 0 and черные_фасоли == 1:
       break # Остался один черный горошек


if белые_фасоли == 1:
    print("белый горошек остался")
elif черные_фасоли == 1:
    print("черный горошек остался")
