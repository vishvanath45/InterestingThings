# Mechanism Design 
## ...the rule of game matters
This 3 day course in mechanism design was an addition to Design and Analysis of Course(IT506) taught at my university.  
The instructor started this course by asking a simple question-  
```
Given a cake to be divided between 2 children such that there is no bias in dividing the cake, as the cake is still in
one piece and there is no unbiased identity in room to divide it. So how do you make the rules of cutting 
cake by either of child such that both children get satisfied from peice of cake they get.
```
One answer could be to use weight machine and then cut piece to match weight balance.  
Other could be children agree to one other over successfull division of cake pieces.  
but guess what these solution do not work in real world as the children here are *Strategic Agent* means they will go to any length to satisfy there goal(here getting bigger peice in cake).  
One solution to this problem could be asking one children to cut cake and giving choice to another child to pick first.  
Thus we have made rule of cutting cake such both participants are bound to cut cake in equal part to have maximum piece for themselves.  
Thus you must be getting some idea about this topic.  
__We design a system such that participants are bound to play fairly when we know they will try super hard to manipulate system for their benefit.In other words if participants plays unfairly then he is bound to loose.__  
Thus as writtern above the **__rule of game matters.__**  
Where can Mechanism Design me Applied  
- Auctions
- House Allocation Problem 
- Stable Marrige Problem 
- Internet Ads auction and several other places...


Let us dive into the course, we define utility as something like differance between what you had guessed the price of object and how much you have paid for it.  
Mathamatically we can represent utility as

<code>U<sub>i</sub> = V<sub>i</sub> - P<sub>i</sub></code>  
Where <code>V<sub>i</sub></code> is valuation of <code>i<sup>th</sup></code> object.  
<code>P<sub>i</sub></code> is price you paid of <code>i<sup>th</sup></code> object.  
<code>U<sub>i</sub></code> is utility you get after buying <code>i<sup>th</sup></code> object.  

To illustrate this, suppose in an auction there is a house for sell, you thought in your mind that house is worth $1k,
and you won the bid at price $800, so your gain(utility) is $200, but if you won the bid at $1200, then your loss(utility) is -$200,
that means you just bought a thing worth $1k(according to you) in $1.2k and that's not good business practice.   
Here, i am talking about most famous type of auction known as First Price auction, some features are
- bidders write down bids on pieces of paper
- auctioneer awards the good to the bidder with the highest bid
- that bidder pays the amount of his bid
  
<img src="https://github.com/vishvanath45/InterestingThings/blob/master/final.png" width=300 align="right" />
  
  
  
So we are certain of one thing that everyone tries to maximize his/her utility, right! then why study mechanism design
  
let auctioneer auction the object and highest bidder will get the object and seller will get maximum possible amount raised through
auction,profit isn't it ??????   
  
What's there to set up rules and make it complicated.


---
This is where actual fun begins :sunglasses:  

Think of it as this, You went to auction of a house for which your valuation was $1k and you won the bid at $800, you had an
gain(utility) of $200 but see from other side, the seller could have gotten $1k from you(and you would have paid) but instead he got $800,
he might be happy with that much amount of money but deep down you know he could have gotten more.  
This is what makes this subject interesting.  
We know that participants are going to cheat or try hard to gain more, so we set up rules such that if they do anything like 
that then will loose.  
For Ideal case we consider that each participant raises the price same at its valuation.  
so even if they win net Utility(gain/loss) is 0, and thus in that case both seller and buyer wins, but we can't enforce such things.  

To solve this there is another type of auction practised used by Google to sell ad space,  
The **Second Price Auction**  
let me write down 3 of its only rule-
- bidders write down bids on pieces of paper
- auctioneer awards the good to the bidder with the highest bid
- that bidder pays the amount bid by the *second-highest bidder*  


Now you must be thinking that this is total dumb, why highest bidder has to pay amount said by second highest bidder when seller
could have gotten amount bidded by Winner. Isn't this totally fucked up mechanism, Stop Stop!!, Do not close this Tab, i know
it already is kind of mind bending but just for a while be along with me and let me explain it to you why this is best mechanism.  
Best stratagy in this type of auction is telling Truth, Keeping Price value same as Valuation Guarentees maximum utility Gain.
Not going into much mathematics i will prove it by theory of contradiction-  
```
I need to show that best response for me will be to bid truthfully.
```
- Myself Bidding and winning(Max Bid value among all)


<img src="https://github.com/vishvanath45/InterestingThings/blob/master/1.png" width=200 align="center" />
here I have to pay what Second highest Bid value is. Profit!! :moneybag:  

---
- Myself Bidding somewhat higher that valuation and winning(Max Bid value among all)


<img src="https://github.com/vishvanath45/InterestingThings/blob/master/2.png" width=200 align="center" />
Still I have to pay what Second highest Bid value is, making higher bid then valuation doesn't help. :sweat:   

---
- Myself Bidding somewhat lower that my valuation and winning(Max Bid value among all)


<img src="https://github.com/vishvanath45/InterestingThings/blob/master/3.png" width=200 align="center" />
Still I have to pay what Second highest Bid value is, making lower bid then valuation doesn't help. :sweat:    

---
- Myself Bidding much lower than my valuation and loosing  


<img src="https://github.com/vishvanath45/InterestingThings/blob/master/4.png" width=200 align="center" />  
I loose but still my utility is zero, Nothing Bought so no loss.:dollar:     

---
- Myself Bidding Honestly and loosing  


<img src="https://github.com/vishvanath45/InterestingThings/blob/master/5.png" width=200 align="center" />  
I loose but still my utility is zero, I could not have afforded it.:dollar:     

---
- Myself Bidding Less than valuation and loosing  


<img src="https://github.com/vishvanath45/InterestingThings/blob/master/6.png" width=200 align="center" />  
I loose but still my utility is zero, same case as above :dollar:     

---
- Myself Bidding More than valuation and loosing  


<img src="https://github.com/vishvanath45/InterestingThings/blob/master/7.png" width=200 align="center" />  
I loose but still my utility is zero, same case as above :dollar:     

---
- Myself Bidding More than valuation and Winning Bid  


<img src="https://github.com/vishvanath45/InterestingThings/blob/master/8.png" width=200 align="center" />  
I Win the bid but i have to pay more than my Valuation, Seriously only a dumb person would do this.:dollar:     

---  
So i think uptill now you must be convinced that Second Price auction is somewhat successfull in making people only bid with there True Value.  
But think in this case where we have to sell only one object then you can guess which auction method would be best?  
... 
now places where this type of auction is used, Google used this auction to sell ad spaces for everytime you search on google, here they are selling neumorious ad spaces and the spaces are sold like that only winner pays amount equal to bid value of second winner, second winner pays bid value of third winner and so on.  
This type of sightly modified version of Second Price Auction is called **Generalized second-price auction**.    
Other places where this type of approch can be applied-
- Allocating Houses to Family in accordance to their Choice such that we maximise familes who get house according to choice.
- Stable Marriage Problem, Each Male and Female having their Choice of opp. Gender whom they would like to marry, and we have to design a syatem sucnh that their maximum Stable Marriages.
- Kidney Exchange Problem, What kind of Kidney will be best suited for person Whose Kidney needs to be transplanted.  

Now we will be looking into solving solving problem of house allocation.

