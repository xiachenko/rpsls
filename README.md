# rpsls game
#coding:gbk

import random

# 0 - 石头
# 1 - 史波克
# 2 - 纸
# 3 - 蜥蜴
# 4 - 剪刀

def name_to_number(name):
	if name=="石头":
		return 0
	elif name=="史波克":
		return 1
	elif name=="纸":
		return 2
	elif name=="蜥蜴":
		return 3
	elif name=="剪刀":
		return 4
	else:
		print("Error:No Correct Name")

def number_to_name(number):
	if number==0:
		return "石头"
	elif number==1:
		return "史波克"
	elif number==2:
		return "纸"
	elif number==3:
		return "蜥蜴"
	elif number==4:
		return "剪刀"

def rpsls(player_choice):
		print("您的选择为：",player_choice)
		player_choice_number=name_to_number(player_choice)
		comp_number=random.randrange(0,5)
		comp_choice=number_to_name(comp_number)
		print("计算机的选择为：",comp_choice)
		if comp_number==player_choice_number:
			print("您和计算机出的一样呢")
		elif player_choice_number-comp_number in range(-4,-2) or range(1,3):
			print("您赢了")
		else:
			print("计算机赢了")
	
print("欢迎使用RPSLS游戏")
print("----------------")
print("请输入您的选择:")
player_choice=input()
rpsls(player_choice)
