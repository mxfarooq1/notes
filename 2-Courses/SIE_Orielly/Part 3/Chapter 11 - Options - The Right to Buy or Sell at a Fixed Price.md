IN THIS CHAPTER

![Bullet](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/check.png) **Understanding the specifics of options**

![Bullet](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/check.png) **Feeling comfortable with an options chart**

![Bullet](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/check.png) **Calculating the maximum loss, maximum gain, and break-even points**

![Bullet](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/check.png) **Discovering more about option rules**

Welcome to the wonderful world of options. I’m sure you’ve heard stories about the difficulty of options. Put your mind at ease — I’m here to make your life easier. Maybe I’m a little warped, but options are my favorite part of the SIE exam!

You don’t have to do a lot of calculations relating to options on the SIE, but the ones that you do have to do are relatively simple. More of the option questions on this exam are about understanding the terminology and rules. But, in this chapter I make facing any math questions you may encounter as simple as possible for you.

![Tip](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/tip.png) There are certainly many more complex options strategies such as straddles, spreads, combinations, and so on. However, you won’t need to calculate any of them on the SIE exam. However, if you're planning on taking the Series 7 exam after this one … be prepared.

## Brushing Up on Option Basics

Options are just another investment vehicle that (hopefully) more-savvy investors can use. An owner of an _option_ has the right, but not the obligation, to buy or sell an underlying security (stock, bond, and so on) at a fixed price; as derivatives, options draw their value from that underlying security. Investors may either _exercise_ the option (buy or sell the security at the fixed price) or trade the option in the market.

All option strategies (whether simple or sophisticated), when broken down, are made up of simple call and/or put options. After going over how to read an option, I explain a basic call option and help you figure out how to work with that before moving on to a put option. Next, I discuss options that are in-, at-, or out-of-the-money, and the cost of options. After you’ve sufficiently mastered the basics, the rest (the more difficult strategies later in this chapter) becomes easier.

### Reading an option

To answer SIE questions relating to options, you have to be able to read an option. The following example shows you how an option may appear on the SIE exam:

> Buy 1 XYZ Apr 60 call at 5

Here are the seven elements of the option order ticket and how they apply to the example:

1. **Whether the investor is buying or selling the option: Buy**
    
    When an investor buys (or _longs, holds,_ or _owns_) an option, she is in a position of power; that investor controls the option and decides whether and when to exercise the option. If an investor is selling (_shorting_ or _writing_) an option, she is obligated to live up to the terms of the contract and must either purchase or sell the underlying stock if the holder exercises the option.
    
2. **The contract size: 1**
    
    You can assume that one option contract is for _100 shares_ of the underlying stock. Although this idea isn’t as heavily tested on the SIE exam, an investor may buy or sell multiple options (for example, five) if she’s interested in having a position in more shares of stock. If an investor owns five option contracts, she’s interested in 500 shares of stock, which you will need to know in more detail when taking other exams such as the Series 7.
    
3. **The name of the stock: XYZ**
    
    In this case, XYZ is the underlying stock that the investor has a right to purchase at a fixed price.
    
4. **The expiration month for the options: Apr**
    
    All options are owned for a fixed period of time. The initial expiration for most options is _9 months_ from the issue date. In the preceding example, the option will expire in April. Options expire at 4 p.m. EST (3 p.m. CST) on the third Friday of the expiration month. Remembering the EST (Eastern Standard Time) is generally easier than recalling the CST (Central Standard Time) and is more often tested.
    
5. **The strike (exercise) price of the option: 60**
    
    When the holder (purchaser or owner) _exercises_ the option, she uses the option contract to make the seller of the option buy or sell the underlying stock at the strike price (see the next step for info on determining whether the seller is obligated to buy or sell). In this case, if the holder were to exercise the option, the holder of the option would be able to purchase 100 shares of XYZ at $60 per share.
    
6. **The type of option: call**
    
    An investor can buy or sell a call option or buy or sell a put option. Calls give holders the right to buy the underlying security at a set price; puts give holders the right to sell. So in the example scenario, the holder has the right to buy the underlying security at the price stated in the preceding step.
    
7. **The premium: 5**
    
    Of course, an option investor doesn’t get to have the option for nothing. An investor buys the option at the premium. In this case, the premium is 5, so a purchaser would have to pay $500 (5 × 100 shares per option).
    

### Looking at call options: The right to buy

![Remember](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/remember.png) A _call option_ gives the holder (owner) the right to buy 100 shares of a security at a fixed price and the seller the obligation to sell the stock at the fixed price. Owners of call options are bullish (picture a bull charging forward) because the investors want the price of the stock to increase. If the price of the stock increases above the strike price, holders can either exercise the option (buy the stock at a good price) or sell the option for a profit. By contrast, sellers of call options are bearish (imagine a bear hibernating for the winter) because they want the price of the stock to decrease.

For example, assume that Ms. Smith buys 1 DEF October 40 call option. Ms. Smith bought the right to purchase 100 shares of DEF at 40. If the price of DEF increases to over $40 per share, this option becomes very valuable to Ms. Smith, because she can purchase the stock at $40 per share and sell it at the market price or sell the option at a higher price.

If DEF never eclipses the 40 strike (exercise) price, then the option doesn’t work out for poor Ms. Smith and she doesn’t exercise the option. However, it does work out for the seller of the option, because the seller receives a premium for selling the option, and the seller gets to pocket that premium.

### Checking out put options: The right to sell

![Remember](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/remember.png) You can think of a put option as being the opposite of a call option (see the preceding section). The holder of a _put option_ has the right to sell 100 shares of a security at a fixed price, and the writer (seller) of a put option has the obligation to buy the stock if exercised. Owners of put options are bearish because the investors want the price of the stock to decrease (so they can buy the stock at market price and immediately sell it at the higher strike price or sell their option at a higher premium). However, sellers of put options are bullish (they want the price of the stock to increase), because that would keep the option from going in-the-money (see the next section) and allow them to keep the premiums they received.

For example, assume that Mr. Jones buys 1 ABC October 60 put option. Mr. Jones is buying the right to sell 100 shares of ABC at 60. If the price of ABC decreases to less than $60 per share, this option becomes very valuable to Mr. Jones. If you were in Mr. Jones’s shoes and ABC were to drop to $50 per share, you could purchase the stock in the market and exercise (use) the option to sell the stock at $60 per share, which would make you (the new Mr. Jones) very happy.

If ABC never drops below the 60 strike (exercise) price, then the option doesn’t work out for Mr. Jones and he doesn’t exercise the option. However, it does work out for the seller of the option, because the seller receives a premium for selling the option that she gets to keep.

### Getting your money back: Options in-, at-, or out-of-the-money

To determine whether an option is in- or out-of-the-money, you have to figure out whether the investor would be able to get at least some of his premium money back if the option were exercised.

![Remember](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/remember.png) You can figure out how much an option is in-the-money or out-of-the-money by finding the difference between the market value and the strike price. Here’s how you know wherein-the-money an option is:

- When an option is _in-the-money,_ exercising the option lets investors sell a security for more than its current market value or purchase it for less — a pretty good deal.
    
    The _intrinsic value_ of an option is the amount that the option is in-the-money; if an option is out-of-the-money or at-the-money, the intrinsic value is zero.
    
- When an option is _out-of-the-money,_ exercising the option means investors can’t get the best prices; they’d have to buy the security for more than its market value or sell it for less. Obviously, holders of options that are out-of-the-money don’t exercise them.
- When the strike price is the same as the market price, the option is _at-the-money;_ this is true whether the option is a call or a put.

Call options — the right to buy — go in-the-money when the price of the stock is above the strike price. Suppose, for instance, that an investor buys a DEF 60 call option and that DEF is trading at 62. In this case, the option would be in-the-money by two points (the option’s intrinsic value). If that same investor were to buy that DEF 60 call option when DEF was trading at 55, the option would be out-of-the-money by five points (with an intrinsic value of zero).

A put option — the right to sell — goes in-the-money when the price of the stock drops below the strike price. For example, a TUV 80 call option is in-the-money when the price of TUV drops below 80. The reverse holds as well: If a put option is in-the-money when the price of the stock is below the strike price, it must be out-of-the-money when the price of the stock is above the strike price.

![Warning](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/warning.png) Don’t take the cost of the option (the premium) into consideration when determining whether an option is in-the-money or out-of-the-money. Having an option that’s in-the-money is not the same as making a profit. (See the next section for info on premiums.)

![Tip](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/tip.png) Use the phrases _call up_ and _put down_ to recall when an option goes in-the-money. _Call up_ can help you remember that a _call_ option is in-the-money when the market price is _up,_ or above the strike price. _Put down_ can help you remember that a _put_ option is in-the-money when the market price is _down,_ or below the strike price.

The following question tests your knowledge of options being in- or out-of-the-money.

![example](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/example.png) Which TWO of the following options are in-the-money if ABC is trading at 62 and DEF is trading at 44?

1. An ABC Oct 60 call option
2. An ABC Oct 70 call option
3. A DEF May 40 put option
4. A DEF May 50 put option

**(A)** I and III

**(B)** I and IV

**(C)** II and III

**(D)** II and IV

The correct answer is Choice (B). Start with the strike (exercise) prices. You’re _calling up_ or _putting down_ from the strike prices, not from the market prices. Because call options go in-the-money when the market price is above the strike price, Statement I is the only one that works for ABC. An ABC 60 call option would be in-the-money when the price of ABC is above 60. ABC is currently trading at 62, so that 60 call option is in-the-money. For the ABC 70 call option to be in-the-money, ABC would have to be trading higher than 70. Next, use _put down_ for the DEF put options, because put options go in-the-money when the price of the stock goes below the strike price. Therefore, Statement IV makes sense because DEF is trading at 44, and that’s below the DEF 50 put strike price but not the 40 put strike price.

![Remember](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/remember.png) When people purchase an option, it is said that they are _long_ the option. An investor who is long an option is paid the premium for the option so he needs the option to go in-the-money (the price of the underlying security to go in the correct direction) enough for him to not only recoup his premium but also make a few bucks.

When someone is _short_ an option, it means that he sold the option. This person is on the opposite side of the transaction than the person who is long the option. In this case, the seller received a premium for selling the option. So, someone who is short an option is doing so for income and is hoping that the option expires out-of-the-money so that he gets to keep the premium.

### Paying the premium: The cost of an option

The _premium_ of an option is the amount that the purchaser pays for the option. The premium may increase or decrease depending on whether an option goes in- or out-of-the-money, gets closer to expiration, and so on. The premium is made up of many different factors, including

- Whether the option is in-the-money (see the preceding section)
- The amount of time the investor has to use the option
- The volatility of the underlying security
- Investor sentiment (for example, whether buying calls on ABC stock is the cool thing to do right now)

One of the simple options math questions you may run across on the SIE exam requires you to figure out the time value of an option premium. _Time value_ has to do with how long you have until an option expires. There’s no set standard for time value, such as every month until an option expires costs buyers an extra $100. However, you can assume that if two options have everything in common except for the expiration month, the one with the longer expiration will have a higher premium. Hopefully, the following equation can help keep you from getting a “pit” in your stomach:

![math](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/eq11001.png)

In this formula, _P_ is the premium or cost of the option, _I_ is the intrinsic value of the option (the amount the option is in-the-money), and _T_ is the time value of the option.

For example, here’s how you find the time value for a BIF Oct 50 call option if the premium is 6 and BIF is trading at 52: Call options (the right to buy) go in-the-money when the price of the stock goes above the strike price (_call up_ — see the preceding section). Because BIF is trading at 52 and the option is a 50 call option, it’s two points in-the-money; therefore, the intrinsic value is two. Because the premium is six and the intrinsic value is two, the premium must include four as a time value:

![math](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/eq11002.png)

![math](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/eq11003.png)

![math](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/eq11004.png)

The following question tests your knowledge of using the formula _P_ = _I_ + _T_.

![example](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/example.png) Use the following chart to answer the next question.

![Chart presenting the price of the stock trading in the market, the strike prices for the options, and the premiums for the calls and puts and the expiration months.](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/9781119545002-un1101.png)

What is the time value of an LMN Oct 30 call?

**(A)** 2.5

**(B)** 4

**(C)** 6.25

**(D)** 9.5

The answer you’re looking for is Choice (B). I threw you a curveball by giving you a chart similar to what you may see on the SIE exam. I hope you’re able to find the premium that you need to answer the question. Most of the exhibits you get on the SIE are simple, and solving the problem is just a matter of locating the information you need.

Using the chart, the first column shows the price of the stock trading in the market, the second column shows the strike prices for the options, and the rest of the chart shows the premiums for the calls and puts and the expiration months. Scan the chart under the October calls, which is in the fourth column; then look for the 30 strike price, which is in the first row of data. The column and row intersect at a premium of 14.5.

Now you need to find the intrinsic value (how much the option is in-the-money). Remember that call options go in-the-money when the price of the stock is above the strike price (call up). This is a 30 call option and the price of the stock is 40.50, which is 10.5 above the strike price. Plug in the numbers, and you find that the premium includes a time value of 4:

![math](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/eq11005.png)

![math](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/eq11006.png)

![math](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/eq11007.png)

## Incorporating Standard Option Math

I’m here to make your life easier. Prep courses use several different types of charts and formulas to figure out things such as gains or losses, break-even points, maximum gain or loss, and so on. I believe that the easiest way is to use the options chart that follows. It’s a simple _Money Out, Money In_ chart you can use to plug in numbers. What’s great about this chart is that you don’t even necessarily have to understand what the heck is going on to determine the answers to most options questions. As this chapter progresses, I show you how incredibly useful the options chart can be.

![Chart depicting the Basic Options chart with the Money Out Money In columns to understand the money spent and received.](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/9781119545002-un1102.png)

If it looks basic, it is — and that’s the idea. Any time an investor spends money, you place that value in the Money Out side of the options chart, and any time an investor receives money, you place the number in the Money In side of the chart.

### Calls same: Buying or selling call options

The most basic options calculations involve buying or selling call or put options. Although using the options chart may not be totally necessary for the more basic calculations (such as the one that follows in the next section), working with the chart now can help you get used to the tool so you’ll be ready when the SIE exam tests your sanity with more-complex calculations.

As you work with options charts, you may notice a pattern when determining maximum losses and gains. [Table 11-1](https://learning.oreilly.com/library/view/securities-industry-essentials/9781119545002/c11.xhtml#c11-tbl-0001) gives you a quick reference concerning the maximum gain or maximum loss an investor faces when buying or selling call options. Notice that the buyer’s loss is equal to the seller’s gain (and vice versa).

[TABLE 11-1](https://learning.oreilly.com/library/view/securities-industry-essentials/9781119545002/c11.xhtml#rc11-tbl-0001) Maximum Gains and Losses for Call Options

|**Buying or Selling**|**Maximum Loss**|**Maximum Gain**|
|---|---|---|
|Buying a call|Premium|Unlimited|
|Selling a call|Unlimited|Premium|

![Tip](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/tip.png) The key phrase to remember when working with call options is _calls same,_ which means that the premium and the strike price go on the same side of the options chart.

#### Buying call options

The following steps show you how to calculate the maximum loss and gain for holders of call options (which give the holder the right to buy). I also show you how to find the break-even point. Here’s the order ticket for the example calculations:

> Buy 1 XYZ Oct 40 call at 5

1. **Find the maximum loss.**
    
    The holder of an option doesn’t have to exercise it, so the most she can lose is the premium. The premium is five, so this investor purchased the option for $500 (5 × 100 shares per option); therefore, you enter that value in the Money Out side of the options chart (think “money out of the investor’s pocket”). According to the chart, the maximum loss (the most this investor can lose) is $500.
    
    ![Illustration of the Basic Options chart with a spend of 500 dollars entered in the Money Out column.](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/9781119545002-un1103.png)
    
2. **Determine the maximum gain.**
    
    To calculate the maximum gain, you have to exercise the option at the strike price. The strike price is 40, so you enter $4,000 (40 strike price × 100 shares per option) under its premium (which you added to the chart when calculating maximum loss); exercising the call means buying the stock, so that’s Money Out. When exercising call options, always put the multiplied strike price under its premium. (Remember _calls same:_ The premium and the strike price go on the same side of the options chart.)
    
    ![Illustration of the Basic Options chart with a spend of 500 and 4,000 dollars entered in the Money Out column.](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/9781119545002-un1104.png)
    
    Because you’ve already determined the maximum loss, look at the Money In portion of the options chart. The Money In is empty, so the maximum gain (the most money the investor can make) is unlimited.
    

When you see a question about the break-even point, the SIE examiners are asking, “At what point does this investor not have a gain or loss?” The simplest way to figure out this point for a call option is to use _call up_ (remember that call options go in-the-money when the price of the stock goes above the strike price — see the section “[Getting your money back: Options in-, at-, or out-of-the-money](https://learning.oreilly.com/library/view/securities-industry-essentials/9781119545002/c11.xhtml#c11-sec-0006)”). When using _call up,_ you add the strike price to the premium:

![math](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/eq11008.png)

For this investor, the break-even point is 45. This number makes sense because the investor paid $5 for the option, so the option has to go $5 in-the-money for the investor to recoup the amount she paid. _**Note:**_ The break-even point is always the same for the buyer and the seller.

#### Selling call options

Here, I show you how to find the maximum gain and loss, as well as the break-even point, for sellers of call options. Here’s the order ticket for the example calculations:

> Sell 1 ZYX Oct 60 call at 2

1. **Determine the maximum gain.**
    
    The seller makes money only if the holder fails to exercise the option or exercises it when the option is in-the-money by less than the premium received. This investor sold the option for $200 (2 × 100 shares per option); therefore, you enter that amount in the Money In side of the options chart. According to the chart, the maximum gain (the most that this investor can make) is the $200 premium received. _**Note:**_ The exercised strike price of $6,000 (60 × 100 shares) doesn’t come into play when determining the maximum gain in this example because the holder of the option would exercise the option only if it were in-the-money.
    
    ![Illustration of the Basic Options chart with a received amount of 200 dollars entered in the Money In column.](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/9781119545002-un1105.png)
    
2. **Find the maximum loss.**
    
    To calculate the maximum loss, you need to exercise the option at the strike price. The strike price is 60, so you enter $6,000 (60 strike price × 100 shares per option) under its premium. The $6,000 goes in the Money In side of the options chart because this investor had to sell the stock to the holder at the strike price (60 × 100 shares). When exercising call options, always enter the multiplied strike price under its premium. (Remember _calls same:_ The premium and the strike price go on the same side of the options chart.)
    
    ![Illustration of the Basic Options chart with a received amount of 200 and 6,000 dollars entered in the Money In column.](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/9781119545002-un1106.png)
    
    You’ve already determined the maximum gain; now look at the Money Out portion of the options chart. The Money Out is empty, so the maximum loss (the most money the investor can lose) is unlimited.
    

When you see a question about the break-even point, the examiners are asking you, “At what point does this investor not have a gain or loss?” The simplest way to figure this out for a call option is to use _call up._ When using _call up,_ you add the strike price to the premium:

![math](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/eq11009.png)

For this investor, the break-even point is 62. This makes sense because the investor received $2 for the option, so the option has to go $2 in-the-money for this investor to lose the amount that she received for selling the option. Call options go in-the-money when the price of the stock goes above the strike price.

### Puts switch: Buying or selling put options

Fortunately, when you’re calculating the buying or selling of put options (which give the holder the right to sell), you use the options chart in the same way but with a slight change (see the preceding section for info on call options). Instead of using _calls same_ as you do with call options, you use _puts switch_ — in other words, you place the premium and the strike price on opposite sides of the options chart.

[Table 11-2](https://learning.oreilly.com/library/view/securities-industry-essentials/9781119545002/c11.xhtml#c11-tbl-0002) serves as a quick reference regarding the maximum gain or maximum loss an investor faces when buying or selling put options.

[TABLE 11-2](https://learning.oreilly.com/library/view/securities-industry-essentials/9781119545002/c11.xhtml#rc11-tbl-0002) Maximum Gains and Losses for Put Options

|**Buying or Selling**|**Maximum Loss**|**Maximum Gain**|
|---|---|---|
|Buying a put|Premium|(strike – premium) × 100 shares|
|Selling a put|(strike – premium) × 100 shares|Premium|

#### Buying put options

This section explains how to find the maximum loss, maximum gain, and the break-even point for buyers (holders) of put options. Here’s the ticket order for the calculations:

> Buy 1 TUV Oct 55 put at 6

1. **Find the maximum loss.**
    
    Exercising an option is, well, optional for the holder, so buyers of put options can’t lose more than the premium. Because this investor purchased the option for $600 (6 × 100 shares per option), you enter that value in the Money Out side of the options chart. The maximum loss (the most that this investor can lose) is the $600 premium paid.
    
    ![Illustration of the Basic Options chart with a spend of 600 dollars entered in the Money Out column.](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/9781119545002-un1107.png)
    
2. **Determine the maximum gain.**
    
    To find the maximum gain, you have to exercise the option at the strike price. The strike price is 55, so you enter $5,500 (55 strike price × 100 shares per option) on the opposite side of the options chart. (Remember _puts switch:_ The premium and the strike price go on opposite sides of the options chart.) Exercising the option means selling the underlying stock, so that $5,500 is Money In.
    
    ![Illustration of the Basic Options chart with a spend of 600 dollars entered in the Money Out column and a received amount of 5,500 dollars entered in the Money In column.](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/9781119545002-un1108.png)
    
    You’ve already determined the maximum loss; now look at the Money In portion of the options chart. Because you find $4,900 more Money In than Money Out ($5,500 – $600), the maximum gain is $4,900.
    

The break-even point is the security price where the investor doesn’t have a gain or loss. The simplest way to figure this point out for a put option is to use _put down_ (put options go in-the-money when the price of the stock goes below the strike price). When using _put down,_ you subtract the premium from the strike price:

![math](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/eq11010.png)

For this investor, the break-even point is 49. The investor paid $6 for the option, so the option has to go $6 in-the-money in order for this investor to recoup the amount that she paid. As with call options, the break-even point is always the same for the buyer and the seller.

#### Selling put options

The following steps show you how to calculate the maximum gain and loss for the seller of a put option. I also demonstrate calculations for the break-even point. Here’s the ticket order for the example:

> Sell 1 TUV Sep 30 put at 8

1. **Determine the maximum gain.**
    
    The seller makes money only if the holder of the option fails to exercise it. This investor sold the option for $800 (8 × 100 shares per option); you put that number in the Money In side of the options chart. The maximum gain (the most this investor can make) is $800.
    
    ![Illustration of the Basic Options chart with a received amount of 800 dollars entered in the Money In column.](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/9781119545002-un1109.png)
    
2. **Find the maximum loss.**
    
    To calculate the maximum loss, you have to exercise the option at the strike price. The strike price is 30, so you place $3,000 (30 strike price × 100 shares per option) on the opposite side of the options chart. (Remember _puts switch:_ The premium and strike price go on opposite sides of the options chart.)
    
    ![Illustration of the Basic Options chart with a spend of 3,000 dollars entered in the Money Out column and a received amount of 800 dollars entered in the Money In column.](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/9781119545002-un1110.png)
    
    You’ve already determined the maximum gain; now look at the Money Out portion of the options chart and compare it to the Money In. The maximum potential loss for this investor is the $2,200 difference between the Money Out and the Money In.
    

You calculate the break-even point for buying or selling puts the same way: You use _put down_ (the strike price minus the premium) to figure out the break-even point:

![math](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/eq11011.png)

For this investor, the break-even point is 22. Because this investor received $8 for the option, the option has to go $8 in-the-money for this investor to lose the amount she received for selling the option. Put options go in-the-money when the price of the stock goes below the strike price (put down).

### Trading options: Opening and closing transactions

Although some investors hold onto their options long enough to actually exercise them, a lot of investors trade options the way that they trade other investments. On the SIE exam, not only do you need to know the difference between opening and closing transactions, but you also have to be able to calculate the profit or loss for an investor trading options. This process is actually pretty easy when you break it down.

#### Putting things back where you found them: Doing opposite transactions

When distinguishing between opening and closing transactions, your key is to know whether this transaction is the first time or the second time the investor is buying or selling an option: The first time is an _opening,_ and the second time is a _closing._

Here are your opening transactions:

- **Opening purchase:** An opening purchase occurs when an investor first buys a call or a put.
- **Opening sale:** An opening sale is when an investor first sells a call or a put.

If an investor already has an option position, the investor has to close that position by doing the opposite — through a closing transaction. If the investor originally purchased the option, she has to sell to close it. By contrast, if she originally sold the option, she has to purchase to close. Here are the two types of closing transactions:

- **Closing purchase:** A closing purchase occurs when an investor buys herself out of a previous option position that she sold. For example, if an investor sold an XYZ Oct 40 call (opening sale), she would have to buy an XYZ Oct 40 call to close out the position. The second transaction is a closing purchase.
- **Closing sale:** A closing sale occurs when an investor sells herself out of a previous option position that she purchased. For example, if an investor bought an ABC Sep 60 put (opening purchase), she would have to sell an ABC Sep 60 put to close out the position. The second transaction is a closing sale.

![Remember](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/remember.png) When determining opening or closing transactions, whether the transactions are both calls or both puts doesn’t matter.

The following question tests your knowledge of opening and closing transactions.

![example](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/example.png) Mr. Dimpledell previously bought 1 XYZ Oct 65 call at 8 when the market price of XYZ was 64. XYZ is currently trading at 69, and Mr. Dimpledell decides that now would be a good time to sell the option that he previously purchased. The second option order ticket would be marked

**(A)** opening sale

**(B)** opening purchase

**(C)** closing sale

**(D)** closing purchase

The right answer is Choice (C). This is the second time that Mr. Dimpledell does something with the option that he owns; therefore, the move has to be a closing transaction, and you can immediately eliminate Choices (A) and (B). Mr. Dimpledell has to sell himself out of the position because he owns the option. The second order ticket would have to be marked _closing sale._

#### Tricks of the options trade: Calculating gains and losses

In addition to knowing how to mark the order ticket, you have to be able to figure out an investor’s gain or loss when trading options. This task isn’t difficult after you master the options chart. The key thing to remember is that when an investor closes, she does the opposite of what she did before.

The following question tests your mastery of options trades.

![example](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/example.png) Mrs. Cleveland purchased 100 shares of DPY stock at $50 per share. Two weeks later, Mrs. Cleveland sold 1 DPY Oct 55 call at 6. Mrs. Cleveland held that position for three months before selling the DPY stock at $52 per share and closing the DPY Oct 55 call at 4. What is Mrs. Cleveland’s gain or loss on the transactions?

**(A)** $400 gain

**(B)** $400 loss

**(C)** $600 gain

**(D)** no gain or loss

The correct answer is Choice (A). This question introduces stock trades as well as options transactions, but that’s no problem. The options chart works for questions involving actual stocks and options or just options.

When you approach the transactions one at a time, the problem-solving process is actually pretty straightforward. Mrs. Cleveland purchased 100 shares of DPY stock at $50 per share for a total of $5,000; therefore, you enter $5,000 in the Money Out side of the options chart. Next, she sold the DPY 55 call for a premium of 6, so you need to enter $600 (6 × 100 shares per option) on the Money In side of the chart because she received money for selling that option.

Three months later, Mrs. Cleveland sold the stock for $5,200 ($52 per share × 100 shares) and received money for selling the stock. Place the $5,200 in the Money In side of the options chart. When closing the option, the customer has to do the opposite of what she did before. Originally, Mrs. Cleveland sold the option, so to close, she has to buy the option (make a closing purchase). She purchased the option for $400 (4 × 100 shares per option), so enter $400 in the Money Out side of the options chart. All that’s left for you to do is total up the two sides. Mrs. Cleveland has $5,800 in and $5,400 out for a gain of $400.

![Illustration of the Basic Options chart with a total spend of 5,400 dollars entered in the Money Out column and a received amount of 5,800 dollars entered in the Money In column.](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/9781119545002-un1111.png)

## Gaining Additional Option Info

To help you get a deeper understanding of options, you need to know a few additional things that you will most certainly see on the real-deal SIE exam. Some of these items include who issues the options, what an ROP is, what a risk disclosure document is, and so on.

### Clearing through the OCC

The Options Clearing Corporation (OCC) is the issuer and guarantor of all listed options. The OCC decides which options will trade and their strike prices. In addition, when an investor decides to exercise her option, it’s the OCC that randomly decides which firm on the other end will be responsible for fulfilling the terms of the option.

![Remember](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/remember.png) The OCC does not determine the premium for options; the premium is determined by investors based on supply and demand, the options intrinsic value (how much it’s in the money — or away from the money), and the amount of time until the option expires.

### That’s ODD: Options risk disclosure document

Because options have a risk that is greater than almost any other investment, all investors must receive an options risk disclosure document (ODD) prior to their first options transaction. This ODD explains to investors the risk involved in investing in options, such as the chance of losing all money invested or, if selling call options, facing an unlimited maximum loss potential.

### Getting the go-ahead: Registered options principal

Because of the extra risk of investing in options, all new accounts and option order tickets must be approved and signed by a registered options principal (ROP), which is a manager with a Series 4 license. The registered options principal determines the amount of risk that each investor can take. Certainly, sophisticated investors with a lot of money are able to handle more risk than new option investors with a limited supply of funds.

### Options account agreement

Within 15 days after approval of the account by an ROP, the customer must sign and return an options account agreement (OAA). Basically, the OAA just states that the customer has read the ODD, understands the risk associated with trading options, and will abide by the rules and regulations regarding options trading. Should anything change (such as the customers, investment objectives, financial situation, and so on), the customer agrees to notify the firm. In the event that the OAA is not received within 15 days after approval of the account, the customer cannot open any new options positions.

### Order ticket

You can find out more about what is required on an order ticket in [Chapter 16](https://learning.oreilly.com/library/view/securities-industry-essentials/9781119545002/c16.xhtml). However, a few things are required on an order ticket that are unique to options. Besides the option that is being bought or sold, you have to write down whether the customer is establishing a long position (if he’s buying) or a short position (if he's selling). In addition, for option sellers, you need to put down whether the seller is covered or uncovered (naked). The seller of a call option is considered covered if he owns the underlying security or owns an option on the same security with the same or longer expiration that will be in-the-money first. And, of course an uncovered (naked) position is when the seller owns neither the underlying stock nor an option on the same security that will be in-the-money first with an equal or longer expiration date.

### Last trade, last exercise, and expiration of an option

Unlike stock certificates, options do expire after a certain period of time. In addition, investors are limited as to when they can trade and exercise an option. Here’s the timeline to keep in mind:

- **Last trade:** The last time an investor can trade an option is 4:00 p.m. EST on the business day of expiration.
- **Last exercise:** The last time an investor can exercise an option is 5:30 p.m. EST on the business day of expiration. If an option is in-the-money by at least 1 point at expiration, it will be automatically exercised. A vast majority of options can be exercised any time up till expiration — this is known as _American style_. However there are also _European-style_ options that can only be exercised on the expiration date. European-style options include capped index options and some foreign currency options.
- **Option expiration:** Options expire at 11:59 p.m. EST on the third Friday of the expiration month.

### Exercise and assignment

When taking the SIE exam, you will be expected to have a basic understanding of how options are exercised and assigned. Options are cleared through the OCC. Here’s how an option is _exercised:_

When a client wants to exercise an option she owns, she contacts her broker-dealer. The broker-dealer contacts the OCC. The trade settles in two business days after the OCC is notified because when the investor is exercising an option, she is actually trading stock (the right to buy or sell stock). Stock trades settle in two business days, so exercises of options settle in two business days (trades of options settle in one business day).

The steps involved look like this:

1. **Client #1 tells her broker-dealer (Broker A) to exercise the option.**
2. **Broker A notifies the Options Clearing Corporation.**
3. **The Options Clearing Corporation chooses the contra broker (the broker-dealer on the other side of the transaction — Broker B) randomly.**
4. **Broker B assigns (chooses the client — Client #2) either randomly, first-in-first-out (FIFO), orby any other method which is fair and reasonable. However, Broker B cannot choose the assignment based on size (the one with the most options, the one with the least options, and so on).**
5. **Client #2 sends the proceeds (stock or cash) to Broker B.**
6. **Broker B sends the proceeds directly to Broker A (the OCC doesn’t handle stock or cash).**

So, if you were to look at a flow chart, it would look something like this:

![Flow chart depicting that Client #1 sends the proceeds to Broker A and Client #2 sends the stock or cash to Broker B.](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/9781119545002-un1112.png)

![Tip](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781119545002/files/images/tip.png) Although most exercises of options are settled by the delivery of the underlying security, there are some that are settled by the delivery of _cash_. Specifically, _index_ (options on an index of securities) and _foreign currency options_ are always settled in cash. This just makes sense because investors can’t be expected to deliver an entire index for index options nor be expected to deliver the underlying foreign currency for foreign currency options.

### Additional definitions

For some reason, the SIE exam writers decided you need to know some additional option-specific definitions. I cover several of them earlier in this chapter, but there are several more that you need to be aware of. I will try to make this as painless as possible.

- **Aggregate exercise price:** The exercise (strike) price of an option multiplied by the number of units (usually shares) of the underlying security covered by the option contract (usually 100 shares).
- **Class of options:** All option contracts of the same type (puts or calls) covering the same underlying security or index.
- **Clearing member:** A FINRA member that has been admitted to membership in the OCC (Options Clearing Corporation).
- **Closing sale transaction:** An option transaction in which the seller wants to reduce or eliminate a long position. So, for argument’s sake, say an investor is long (owns) 1 ABC Oct 40 call. To close that position, the investor would short (write or sell) the 1 ABC Oct 40 call.
- **Conventional index option:** An option that overlies a basket (nine or more equity securities) or index of securities providing that no one security comprises more than 30 percent of the basket or index.
- **Conventional option:** (A) Any option contract not issued or subject to issuance by the OCC, or (B) an OCC-cleared OTC option.
- **Delta neutral:** An equity options position that has been fully hedged. For example, owning 100 shares of ABC stock and owning an at-the-money put on ABC stock. Basically, offsetting long and short positions.
- **Net delta:** The number of shares that must be maintained (either long or short) to offset the risk the investor is facing having an equity option position.
- **Opening writing (opening sale) transaction:** The initial sale of an option in which the seller receives the premium paid.
- **Outstanding:** An option contract that has been neither closed (closing sale) nor exercised, and has not reached the expiration date.
- **Series of options:** All option contracts that are of the same class, same expiration date, and same exercise price, and cover the same number of units of the underlying security or index.
- **Type of option:** Either a call or a put.

### Some additional option rules

Yes, I know … even more? Don’t blame me; I didn’t design the test. Anyway, as with the preceding section, I think a quick perusal of the following items will give you enough of a general understanding of some of the additional rules that you should be able to pick them out of any multiple-choice questions posed on the exam.

- **Position limits:** A number placed on the amount of option contracts that a person can hold or write on the same side of the market (bullish or bearish) on the same security. This will be covered more in depth if you are taking the Series 7.
- **Exercise limits:** A number placed on the amount of option contracts that a person can exercise on the same side of the market (bullish or bearish) within five consecutive business days. This will be covered in more detail if you are taking the Series 7 exam.
- **Limit on uncovered short positions:** FINRA may decide to limit the amount of uncovered short positions on option contracts of a given class if deemed necessary for the protection of investors.
- **Restrictions on option transactions and exercises:** As with the limit on uncovered short positions, FINRA may also place restrictions on option transactions or the exercise of option contracts in one or more series of options of any class when deemed necessary to help maintain a fair and orderly market.
- **Open order on the “ex-date” (ex-dividend date):** Since the underlying stock price will be lowered due to a dividend, the OCC will adjust option contracts accordingly unless otherwise instructed by the customer.
- **Confirmations:** Members are responsible for providing a written confirmation of each option transaction for each customer’s account. The confirmation must include the type of option (call or put); the underlying security or index; the expiration month; the exercise (strike) price; the number of option contracts; the premium, trade, and settlement dates; whether it was a purchase or sale (long or short); opening or closing transaction; whether it was done on a principal or agency basis; the amount of commission; and so on. There’s more on confirmations in [Chapter 16](https://learning.oreilly.com/library/view/securities-industry-essentials/9781119545002/c16.xhtml) — yippee!
- **Statements of account (account statements):** All clients must receive account statements at least monthly if there has been any trading in the account for the previous month and at least quarterly (once every three months) when there has been no trading in the previous month. The account statements must show the security and money positions, entries, interest charges, and any other charges assessed against the account. Account statements are covered in more detail in [Chapter 16](https://learning.oreilly.com/library/view/securities-industry-essentials/9781119545002/c16.xhtml).
- **Opening of accounts:** In order to open an options account for a client, the client must receive an ODD, and you must exercise due diligence by getting the customer’s investment objectives, employment status, estimated annual income, estimated net worth, estimated liquid net worth, marital status, number of dependents, age, investment experience and knowledge, and so on. In addition, the account and all transactions must be approved by a registered options principal (ROP), branch office manager, or limited principal-general securities sales supervisor. All options accounts must be approved or disapproved within ten business days. Please note that all option accounts may not be approved for all transactions — depending on the client, he may be approved for buying covered writing, uncovered writing, spreading, discretionary transactions, and so on.
- **Options account agreement (OAA):** Within 15 days after approval of the account, a member must obtain from the customer a written account agreement, which states that the customer understands that he is aware of and agrees to be bound by FINRA rules regarding option trading.
- **Uncovered short option contracts:** Since uncovered short option contracts are the riskiest of all option contracts, member firms must create standard rules for evaluating the suitability of customers who plan on writing uncovered options.
- **Maintenance of records:** Each member must keep a current log, index, or other file for options-related complaints. Each complaint should be easily identified and easy to retrieve if necessary. Each complaint file (hopefully there aren’t many) must contain the identification of the complaint, the date the complaint was received, the name of the registered rep handling the account, a description of the complaint, any action taken (if any), and so on.
- **Discretionary account:** As with any discretionary account in which the client gives you the right to trade his account without pre-approval, it must be approved by a principal (manager). Options discretionary accounts must be approved in writing by a registered options principal (ROP) or limited principal-general securities sales supervisor, and written approval must be received from the client. In addition, discretionary accounts must be reviewed frequently by an ROP.
- **Suitability:** You may not recommend any option transaction(s) to a customer unless you believe that the transaction is suitable for the customer. Remember that you should already know the customer’s investment objectives, financial information, and so on. In other words, you should not be recommending a risky option transaction for someone you deem incapable of handling the risk.
- **Supervision of accounts:** Members conducting an options business must have a written supervisory system in place to adequately address the public customer’s option business. In addition, each branch office must have either a registered options principal or a limited principal-general securities sales supervisor in order to conduct options business.