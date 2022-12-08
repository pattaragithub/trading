import pandas as pd

#Set the price range and grid width
price_range = (20000, 200000)
grid_width = 0.32

#Calculate the number of grids
num_grids = (price_range[1] - price_range[0]) / (price_range[1] * grid_width)

#Create a list of grid prices
grid_prices = [price_range[0] + (price_range[1] * grid_width) * i for i in range(num_grids)]

#Set the investment size
investment_size = 10000

#Create a DataFrame to store the grid orders
df = pd.DataFrame(columns=['price', 'quantity'])

#Loop through the grid prices and create a buy and sell order for each price
for price in grid_prices:
df = df.append({'price': price, 'quantity': investment_size}, ignore_index=True)
df = df.append({'price': price, 'quantity': -investment_size}, ignore_index=True)

#Print the grid orders
print(df)
