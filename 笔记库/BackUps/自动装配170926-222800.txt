class w:
	dic={}
	def regist(self,x):
	      value=x.__dict__
	      for i in value.keys():
	      	if(i=="__dict__"):
	      		break
	      	elif(i=="__module__"):
	      		continue
	      	else:
	      	 self.dic[i]=value[i]
	      return x   #如果不返回x，就返回none。none调用x中的属性就是错的
	def auto(self,x):
		value=x.__dict__
		for i in value.keys():
			# print(i)
			if(i=="__dict__"):
				break
			elif(i=="__module__"):
				continue
			elif(i in (self.dic.keys())):
				setattr(x, i, self.dic[i])
		return x		
		

      	 



      
	



