# CocktailRecipeNN

## The goal of this project is to make an RNN that will generate new cocktail recipes.

It's happened to every bartender out there. A guest wanting something "unique" and "off menu" while you're in the weeds and your coworkers are nowhere to be seen! Instead of wasting my time/ingredients trying to make something new, I wish I had an app I could pull up that generates a unique recipe every time!

## Data Collection

Unfortunately, I hit a snag very early on. Most major cocktail recipe websites forbid webscraping and a lot of restaurants want you to buy their cocktail recipe books. The only online resource I could locate was TheCocktailDB. Pulling their API(after subscribing to their Patreon), I then did my best to clean it. After some time spent with the DB, I realized hand-transcribing the recipes was the best bet for this project. I wrote the recipes into a txt file, one recipe per line.

## Building the Net

I tested a variety of models, but a single layer of LSTM proved to be the most effective due to how quickly it trains and how small our data set ended up being. Encoding by the individual letter as opposed to the full words allowed us a couple things:
- Unique results
- Funny results

## Example Outputs after 30-40 epochs

Sucambuec: 25 oz Gin, 0.5 oz Lemon
Suca Hot Ram: 1 oz Vodka, 1 oz Coffee, 6 oz Hon Cream, 1 oz Orange Juice
Logld Wines: 0.5 oz Gin, 4 oz Lemon Juice, 0.6 oz Simple Syrup

So our model was printing... at least legible results for the most part. But while this is the end of my work here at GA, I will continue to build this out. 
