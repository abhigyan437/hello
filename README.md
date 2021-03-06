# hello
print("Helio")
def rough():
	r = input("Enter Roughly Paper : ")
	r=int(r)
	return r
def cost(total):
	cost=total*1.5
	print ("Cost Calculated :", cost)
	return cost

print("Welcome to Xerox Calculator")
a=1
while(a==1):
		i=2
		l=[]
		while(i==2):
			s=input("Enter number of SHEETS = ")
			s=int(s)
			c= input("Enter number of Copies = ")
			c=int(c)
			ind=c*s
			l.append(ind)
			print(s ,"*", c ,"=", ind)
			print(l)
			i=input(" For next Calculation Press 2\n To Calculate Total - Press 4 \n To Enter Roughly - Press 3\t")
			i=int(i)
		if i!=4 and i!=2 and i!=3 :
			print("Enter proper input only")
			i=input(" For next Calculation Press 2\n To Calculate Total - Press 4 \n To Enter Roughly - Press 3\t")
			i=int(i)
		if i!=4 and i!=2 and i!=3 :
			break
		r=0
		total = 0
		if i==3 :
			r=rough()
			for element in l :
				total=total+element
			total=total+r
			print("Total Calculated : ",total)
			i=input(" For New Calculation Press 1\n To Calculate Cost - Press 5\t")
			i=int(i)
		if i==4 :
			for element in l :
				total=total+element
			total=total+r
			print("Total Calculated : ",total)
			i=input(" For a new Calculation - Press 1\n To add up Roughly papers, Press 3\n To Calculate Cost - Press 5\t ")
			i=int(i)
			if i==3 :
				r=rough()
				for element in l :
					total=total+element
				total=total+r
				print("Total Calculated : ",total)
				i=input(" For New Calculation Press 1\n To Calculate Cost - Press 5\t")
			i=int(i)
		if i==5:
			cost=total*1.5
			print ("Cost Calculated :", cost)
			i=input(" To Exit Press 0\n For a new Calculation Press 1\t ")
			i=int(i)
		if i==0:
			break
print("Thanks for using Xerox Calculator")
