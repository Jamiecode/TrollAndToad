What is this?

This is a program designed to take TrollAndToad's buylists,which are available for download as CSV files from https://www.trollandtoad.com/buylist and query them for relevant information.

What is the goal?

The endgame is being able to query any of TrollandToad's buylists for relevant information and generate buylists to send back to them.  The goal for the current iteration of this project (Version 1.0) is to be able to parse TrollAndToad's Yugioh buylist.  In future versions, functionality for other buylists as well as the ability to generate a buylist to turn into TrollAndToad will be added.

Why do we care about this?

If you are into trading card or collectables arbitrage, this program should make selling to one of the largest collectbibles retailers in the US an easier and more lucrative process.  When their buylist's data is stored in an easily queryable way, you can analyze the data in an attempt to see market trends or spot lucrative outliers to take advantage of.

What are the biggest issues?

The biggest issue by far is parsing through TrollAndToad's CSV files.  Currently, the files offer information in a less than optimal way, often with much more information than we truly care about. Another issue is a lack of consistency between the information provided in each row.  Take this example row from TrollAndToad's Yugioh buylist CSV.
The format for the CSV is as follows:
Product Id,Set,Edition,Condition,Buy Price,Buy Qty,Sell Qty (Note: The Sell Qty is left blank as this is used if you were to re-upload their buylist in order to sell to them.)

Let us analyze this example.
"1663216","Invasion of Chaos IOC","Black Luster Soldier - Envoy of the Beginning - IOC-025 - Ultra Rare","Near Mint 1st Edition English Yugioh Card","29.25","9",""

For our purposes the product ID isn't important, it's only important on their end.  The product ID is important however when we want to create our own buylist to send to TrollAndToad however, so we cannot discard this information.

The set is important, but real information that we care about,the set number(IOC-025) is given to us in the "Edition" category.

The Edition category doesn't have the actual edition of the card(1st edition or unlimited) in this example, but in other rows of the CSV the edition of the card is present. This also gives us the rarity of the card which we care about in cases of seperating valuable collectibles from "Bulk" purchases.

The condition is more or less irrellevent because those experienced in arbitrage know that collectibles are overwhelmingly bought and sold at "Near Mint" condition but when dealing with older products this category becomes relevent because there's a large difference between a Near Mint 20 year old collectible and a Heavily Damaged one.

The buy price and buy quantity are obviously the most important things we care about considering the intented use of this program.

That's all for now.  More information to come as I think of it or if the scope of this project changes.