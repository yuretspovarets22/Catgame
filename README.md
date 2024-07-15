# Catgame
import random

def play_cat_game():
  """Plays a simple cat game where the user guesses the cat's location."""

  cats = ["under the bed", "behind the sofa", "in the cupboard", "on the windowsill", 
          "in the bathtub", "on the table", "in the laundry basket"]
  
  cat_location = random.choice(cats)
  guesses = 0

  print("The cat is hiding somewhere in the house. Can you find it?")
  print("You have 5 guesses.")

  while guesses < 5:
    guess = input("Where is the cat? ")
    guesses += 1

    if guess == cat_location:
      print("You found the cat! You win!")
      return

    print("That's not right. Try again.")

  print("You ran out of guesses. The cat was hiding", cat_location)

play_cat_game()
