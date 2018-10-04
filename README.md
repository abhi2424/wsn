# database-modification
d={'name':['a','b','c','d','e'],'m':[41,75,30,60,65],'e':[40,75,35,62,53],'h':[59,72,21,89,46]}
passed=[]
failstd=[]
add=[]
c=0
for i in range(5):
    add=add+[d['m'][i]+d['h'][i]+d['e'][i]]
    print(add)
    if(d['m'][i]>40 and d['h'][i]>40 and d['e'][1]>40  and (add[i]/3)>60):
        passed=passed+[d['name'][i]]
    else:
        failstd=failstd+[d['name'][i]]


print(passed)
print(failstd)


max1=add[0]
for i in range(len(add)):
    if(max1<add[i]):
        max1=add[i]
        p=i;
topper=d['name'][p]
print(topper)
data={'passed':passed,'failstd':failstd,'topper':topper}
print(data)

          
