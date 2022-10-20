# Beer Recommendor System

To understand if there are differences amongst the popular beer brand in terms of consumer's perceptions, I scraped ~6000 reviews from a beer review forum and performed the following analysis to develop a recommendor system to generate a list of beer brands that resonates with the constumer's preferences.

- Data Preprocessing: 
Cleaned the scraped reviews by remoing brands which had less than 50 reviews and removed stopwords

- Exploratory Data Analysis:
Generated word frequencies to understand which beer attributes are most talked about and combined similar attributes (replaced them in reviews). Performed LIFT analysis to get a sense of which beer brands are associated with which attributes and are there any noticable differences amongst the brands.

- Building Recommendor System:
I utilized two methods to build the recommendor system. One is a combination of VADER sentiment analysis and Bag of Words cosine similarity. Another is simply the cosine similarity using spacy word embeddings.


Below is the snapshot of the scraped data:

| product\_name | user\_rating | product\_review                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ------------- | ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Dinner        | 4.78         | been waiting over a decade to try this beer and even longer to visit the brewery finally did both had it on draft and took a few bottles home with a date of 26aug22 this absolutely meets the hype incredibly delicious and absurdly drinkable for the abv and style so fruity and so floral the smooth body and delicate mouthfeel are truly impressive this is the real deal                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Dinner        | 4.47         | pours a dirty darker straw color cloudy but see through white head that laces quite beautifully a dense film lingers and lingers  the aroma literally jumps out of the glass on this beer it has an essential oil like brightness to it incredibly vibrant a mix of fresh in season fruits nothing tropical to me just local summer fruits but with an extra citrus like bite to it a little bit of vegetal dank on the finish it cuts short of onion garlic territory for me  taste is much of the same but the beer becomes less fruity more citrus pithy with a pretty nice minor sweet malt presence slight resinsap aftertastes  this is a double ipa that is for sure it has a pretty hefty body higher end of medium a very clean drinking beer dry and biting bitterness on the finish prickly sappy tingling on the tongue also letting you know this is a double ipa is the slight alcohol presence on the finish no overbearing by any means but present  well it is easy to see why this beer has the reputation it does the aroma alone is intoxicating but the flavors and feel combine to make this a very good beer i love the bite and big hop presence on such an aromatic beer lovely beer |
| Dinner        | 4.14         | ive never come across this highly regarded beer so was pleasantly surprised to see it on tap when i was out to dinner last night the appearance was that ofbeer cloudy and medium yellow with almost no head the lack of head could certainly be chalked up to the fact that it had probably been a minute or two between the pour and its arrival at my table regardless while there was nothing wrong with the appearance nothing particularly stood out either  the nose was a different story im desensitized to ipa aromas at this point but this beer smelled amazing loads of citrus mango and other tropical notes simply an excellent smelling beer  the taste was very nice but not as tropical as the nose grapefruit was the only taste i could pick out but whatever else was there it was above average but didnt blow me away keeping in mind im not a big lover of ipas the feel however was amazing very full creamy and pillowy absolutely excellent  overall i though this was a very good beer led by the aroma and the feel i hope to be able to luck into some bottles sometime right around a nbs bif so i can share it with others                                                    |
| Dinner        | 4.36         | from a 169oz bottle dated 072922 served in a spiegelau ipa glass  pours a just barely hazed honeygold with twoplus fingers of pouffy shaving creamlike foam retention is excellent leaving a fat bubblysudsy cap and a tattered curtain of lacing  nose is sweet malty and layered with aromas of orange peel and pine needles  taste is as expected leaning into the sweet and malty end of balanced the earthywoody pine needle resinous character is prominent along with caramel sweetness oily orange peel and a squeeze of lemon  feel is clean just a little too brisk to pass as smooth entirely in a good way and no more than medium bodied with bright zesty carbonation theres a cheerful hop oily tingle on the tongue and a slight boozy warmth in the gullet  as always when rating mbc bottles overall score is marked down 025 in recognition of the stupid overpriced pintplus bottles because principles right replaces a 446 rating without a review from 110515 thank you dr j for the rare opportunity to have this one again                                                                                                                                                           |
| Dinner        | 4.79         | just an amazing step up from lunch another classic from maine beer co that really lets the tropical nature of the hops shine through where lunch is a mellow refined take on the style and very clean dinner is a punch in the mouth and in a good way                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



