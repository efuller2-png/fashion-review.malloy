# What Makes Women Happy (With Their Clothes)?
### A Malloy Data Analysis of 23,000 Women's Fashion Reviews
I was curious whether all fashion categories are created equal — 
do women feel the same way about their dresses as their tops? 
Their jackets as their trend pieces? I used Malloy and DuckDB to 
dig into 23,000 reviews from a US women's e-commerce retailer to 
find out.

## The Dataset
This analysis uses the [Women's E-Commerce Clothing Reviews](https://www.kaggle.com/datasets/nicapotato/womens-ecommerce-clothing-reviews) 
dataset from Kaggle — 23,486 reviews across 6 departments: Tops, 
Dresses, Bottoms, Intimate, Jackets, and Trend. It is an unnamed US women's clothing store, which I found interesting because you can't have pre-conceived notions about the brand before working with the set. But, because we don't know the brand, we can't make generalized claims over the whole fashion industry.

Each review includes:
- **Age** of the reviewer
- **Rating** (1–5 stars)
- **Whether they recommended the item** (0 or 1)
- **Department and Class** of the clothing item
- **Written review text**

## Finding 1: Tops Dominate, But Trend Disappoints
![Department Ratings](department_ratings.png)

Tops account for nearly half of all reviews (10,468), making it 
the most-reviewed category by far. But the most surprising finding 
was the Trend department — it had both the lowest average rating 
(3.815) and the lowest recommendation rate (73.95%) of any 
department. Every other department cleared 80% recommendation rate. 

## Finding 2: Recommendation Rates Tell a Clearer Story
![Recommendation Rates](recommendation_rates.png)

When I converted the recommended flag into a percentage, the gap 
became even clearer. Bottoms and Intimates lead at ~85%, while 
Trend trails nearly 12 percentage points behind. For a retailer, 
this is a signal worth paying attention to — trend-driven inventory 
may be generating more returns and disappointment than staple pieces.

## Finding 3: Age Doesn't Predict Satisfaction
![Age vs Rating](age_ratings.png)

I assumed younger shoppers would be harder to please. I was wrong. 
Ratings stay remarkably consistent across all age groups, hovering 
between 4.1 and 4.5 stars from age 18 through the oldest reviewers. 
Satisfaction is not an age story — it's a category story.

## The Story Arc
I started by asking a simple question: which department makes 
customers happiest? The answer surprised me. It's not about 
which category is most popular — Tops wins that easily. It's 
about which category consistently delivers. Trend items 
generate excitement but underdeliver on expectations due to the fad. Staple 
categories like Bottoms and Intimates quietly lead in customer 
satisfaction. The data suggests that chasing trends may come at 
a real cost to customer loyalty.

## So What?
These findings matter to fashion buyers, merchandisers, and 
e-commerce managers. A retailer investing heavily in trend-driven 
inventory may be optimizing for initial clicks while quietly eroding 
customer trust. The recommendation rate gap between Trend (74%) and 
Bottoms (85%) represents exactly that. For anyone making inventory or 
assortment decisions, this data makes a case for balancing trend 
pieces with the reliable staples that customers consistently love.

## Files in This Repo
- `reviews.csv` — cleaned dataset
- `reviews.malloy` — all Malloy queries
- `reviews_story.malloynb` — narrative notebook