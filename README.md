# Product Loyalty

## Overview
This project aims to allow like-minded companies and individuals to co-operate in using and developing a basic measurement model for how loyally a product is purchased.  This metric can be interpretted and used several different ways to help inform a variety of business decisions.  For example, level of repeat purchase and importance of product to customer's buying it.  The setting is exemplified by grocery retail, but can no doubt be applied to other settings which share similar product purchasing characteristics.


## Definition: What is a Product Loyalty?
Product Loyalty is a number reflecting how important that product is to the customers that buy it.  Put increasingly mathematically, it is the average purchase frequency, which is the number of distinct baskets containing the product divided by the number of distinct customers buying the product.

Although a product loyalty number has a direct interpretation (average purchase frequency during some time period), the direct interpretation is avoided.  We are calling the metric "product loyalty" rather than "average purchase frequency" after all.  This is because the number is best used in comparison, or as the basis of a classification, rather than to gain insight from absolute numbers.


## Ethos

Until there is source code associated with this project, the question of licensing is probably mute.

The intention is to provide this knowledge on a Copyleft (GPLv3) basis.  If you don't know what a Copyleft license is, please educate yourself before cloning / copying this repository.

The intention is to make this project free for anyone to use to measure product loyalty within their own organisation.  "Anyone" could be an employee of a retailer, a researcher or a student.

The intention is to discourage companies or individuals from re-selling this work and gaining payment, partly or wholly, as a consequence.  At least, not without seeking explicit permission first.  In principle, permission will be granted, but in exchange for suitable contribution to the project (financial or otherwise - dependent on scale of commercial gain).

The technical methodology outlined here is not complex and probably too generic to even consider questions of authorship and ownership.  The intention for making this methodology openly available is to enable collaborative improvements between individuals and companies that are otherwise unwilling to collaborate due to perceived or real conflicts of interest.  

By making a methodology openly available we also hope to faciliate some side-effects:
* To make it harder for software and consulting vendors to hide behind a mask of having a "complex proprietory algorithm" which turns out to be inferior to the one presented here. 
* To equipe inhouse Data / Analytics / Insight / Science teams to deliver externally credible models themselves.
* If a company wants Versible to help implement, we are of course happy to be engaged ;-).


## Data Sources
Source data is one year's worth of basket product level sales where a known customer identifier is present.
* If your data only has a known customer identifier for 60% of baskets, only use that 60% of baskets.
* The customer identifier is simply a number to link baskets together.  No other information about a customer is required.
* You don't need the actual sales, just a record that the basket, belonging to a customer, contained a product.  For interest, this is called a [factless fact table](https://www.kimballgroup.com/data-warehouse-business-intelligence-resources/kimball-techniques/dimensional-modeling-techniques/factless-fact-table/) in dimensional modelling theory.


## Methodology

The methodology is a simple count of distinct baskets divided by count of distinct customers. 

Details are given in the separate `Methodology.md` file in this repository. 

## Code

Until we are aware of a suitably licensed openly available data set, we are not providing the source code of an implementation of this methodology.  While at first sight the lack of source code might disappoint, anyone fully engaging in this topic will realise it is the methodological description that is far more important.  Specific technical implementations should be straight-forward for any Analyst with suitable skills, data access and compute resource.

## Caveats about this Approach

This methodology leads to a simple metric which cannot in itself really ever by wrong.  The complexity is all about how the metric is interpreted and applied to business issues.

A classic pitfall is the average purchase frequency interpretation.  Say bananas has a value of 10.  10 is a very high product loyalty score, meaning customers that buy bananas buy them repeatedly, making bananas an important product for those customers and therefore the store.  The trap is to picture the typical customer buying bananas 10 times a year.  This implies purchase frequency distribution is like a Normal distribution centred around 10.  Purchase frequency distribution for all products is always a decay curve.  More people will buy bananas once and once only, than twice and twice only, then thrice, etc.  All the value of 10 means is that if there are X customers buying bananas across the year, all those customer combined put bananas in 10X baskets.

   

---

© Versible 2022