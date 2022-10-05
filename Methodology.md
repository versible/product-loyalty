# Product Loyalty - Methodology

Assume you have the necessary source data: For a year snapshot, by product, count of distinct customers and count of distinct baskets belonging to those customers.

Make sure it is count of distinct baskets *belonging to identified customers*.  As in, exclude all baskets without a customer identifier from the analysis.


The calculcation is simply [count of distinct baskets belonging to those customers] divided by [count of distinct customers].

That's it!

---

If the methodology felt too easy, maybe spend some time understanding why the simple average is effective.

Pick a handful of products and plot the histogram of distinct basket count (x axis) again distinct customer count (y axis).  In virtually every example I have ever looked at, this has returned some form of decay relationship.  There will be exceptions, and it isn't always a perfectly smooth relationship, but across many products the pattern is consistent.

The arthmetic mean isn't a great way to summarise a decay curve.  Surely it is better to fit some form of decay equation and they quote something like the decay co-efficient.  Mathmetically, I agree.  Try doing it.  What I think you will find is a set of decay co-efficients will have high correlation to the arethmetic mean.  So you haven't gained any better insight by being more mathmetically rigourous.  In fact, I argue you have lost insight because a decay co-efficient is almost impossible for a business stakeholder to picture (other than as an abstract number of comparison).  Whereas an average purchase frequency is possible to picture - albeit picturing it might cause problems if a stakeholder mistakes it to mean *most* customers buy a product this many times.

---

© Versible 2022

