#Created By :- Pratyaksh Kumar
#Topic :- Leap and Non leap year
from datetime import datetime
startdate = input("Enter start date in dd/mm/yyyy format: ")
enddate = input("Enter end date dd/mm/yyyy format: ")
format='%d/%m/%Y'


start=datetime.strptime(startdate,format).year
end=datetime.strptime(enddate,format).year

if start < end:
    print()
    print()
    print ("Leaps years are between " + str(start) + " and " + str(end)  + ":")

for i in range(start,end+1):
    if i% 4 == 0 and i % 100 != 0:
        print(i,end=" ")
    if i % 100 == 0 and i% 400 == 0:
        print(i,end=" ")


if start < end:
    print()
    print()
    print("Non Leap Year are: ")


for j in range(start,end):
    if j %4!=0 and j %100==0:
        print(j, end=" ")

    if j %100!=0 and j %400!=0:
        print(j,end=" ")


if start >= end:
    print()
    print("Input is Wrong and please check your date and Format(dd/mm/yyyy)")
