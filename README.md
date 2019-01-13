# matrix_multiplication
def m_mul(a,b,c,d):
	if(b!=c):
		print "matrix multiplication is not possible"
	else:
		#A=[[0,0,0],[0,0,0]]
		#B=[[0,0],[0,0],[0,0]]
		ro1=[]
		co1=[]
		for i2 in range(0,a):
			ro1+=[0]
		for j2 in range (0,b):
			co1 += [0]
		for i2 in range(0,a):
			ro1[i2] = co1
		A=ro1
		print A
		ro2=[]
		co2=[]
		for i1 in range(0,c):
			ro2 += [0]
		for j1 in range (0,d):
			co2 += [0]
		for i1 in range(0,c):
			ro2[i1] = co2
		B=ro2
		print B
		for u in range(len(A)):
			for v in range(len(A[0])):
				A[u][v]=input("Enter elements for matrix1:")
		print A
		for i in range(len(B)):
			for j in range(len(B[0])):
				B[i][j]=input("Enter elements for matrix1:")
		print B
		ro3=[]
		co3=[]
		for t in range(0,a):
			ro3+=[0]
		for k in range (0,d):
			co3 += [0]
		for q in range(0,a):
			ro3[q] = co3
		z=ro3
		#print z#z=[[0,0],[0,0]]
		for x in range(0,len(A)):
			for y in range(len(B[0])):
				for w in range(len(A)):
					z[x][y] += A[x][w] * B[w][y]
					break;
		for r in z:
			print r

a=input("Enter number of rows for matrix1:");
b=input("Enter number of columns for matrix1:")
c=input("Enter number of rows for matrix2:");
d=input("Enter number of columns for matrix2:")
m_mul(a,b,c,d)
