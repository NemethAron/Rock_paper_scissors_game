rock = '''
    _______
---'   ____)
      (_____)
      (_____)
      (____)
---.__(___)
'''

paper = '''
    _______
---'   ____)____
          ______)
          _______)
         _______)
---.__________)
'''

scissors = '''
    _______
---'   ____)____
          ______)
       __________)
      (____)
---.__(___)
'''

#Write your code below this line 👇
import random
your_item = input("Choose one:\n Rock = 0\n Paper = 1\n Scissors = 2\n Your Choice: ")

list = [rock, paper, scissors]
your_item_number = int(your_item)

print(list[your_item_number]) 

num_items = len(list)

random_choice = random.randint(0, num_items - 1)
random_item = list[random_choice]
print(f"Computer choise:\n {random_item}")

if random_choice == 0 and your_item_number == 0 or random_choice == 1 and your_item_number == 1 or random_choice == 2 and your_item_number == 2:
  print("Draw.")
elif random_choice == 0 and your_item_number == 1 or random_choice == 1 and your_item_number == 2 or random_choice == 2 and your_item_number == 0:
  print("You Win!!!")
elif your_item_number >= 3:
  print("NOT VALID")
else:
  print("You LOSE")
