# construction-management using python
import pandas as pd

dt=pd.read_csv(r"C:\Users\vasud\Downloads\csv_file.csv")
print(dt)
C=dt.set_index('SID')
cost=int(input("enter cost"))
def range():
    B=C.loc[(C['COST_PER_FLAT']<cost)]
    print(B)

range()
C=dt.set_index('SID')

type=int(input("type of flat")) 
def flat_type(): 
    B=C.loc[(C['TYPE_OF_FLAT']==type)] 
    print(B)

flat_type()
import matplotlib.pyplot as plt

x1 = [1, 3, 4, 5, 6, 7, 9] 
y1 = [4, 7, 2, 4, 7, 8, 3]

x2 = [2, 4, 6, 8, 10]

y2 = [5,6,2,6,2]

plt.bar(x1, y1, label="TYPE_OF_FLAT(IN BHK)", color='pink') 
plt.bar(x2, y2, label="COST PER FLAT(IN LACK)", color='yellow')

plt.plot()

plt.xlabel("type(BHK)")

plt.ylabel("cost(LACK)")

plt.title("type vs cost")

plt.legend()

plt.show()
