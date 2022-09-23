# blind_auction
from replit import clear
from art import logo
print(logo)

name = input("What is your name: ")
price = int(input("What is your bid price:$"))
other_users = input("Type 'yes' if there are other users, otherwise type 'no'. ")

def find_highest_bid(bidding_record):
  highest_bid = 0
  winner = ""
  for bidder in bidding_record:
    bid_amount = bidding_record[bidder]
    if bid_amount > highest_bid:
      highest_bid = bid_amount
      winner = bidder
  print(f"The winner is {winner} with ${highest_bid} bid. ")    


blind_auction = {}
for user in name:
  blind_auction[name] = price
  if other_users == 'yes':
    clear()
    name = input("What is your name: ")
    price = int(input("What is your bid price:$"))
    other_users = input("Type 'yes' if there are other users, otherwise type 'no'. ")
  else:
    clear()
    find_highest_bid(blind_auction)
