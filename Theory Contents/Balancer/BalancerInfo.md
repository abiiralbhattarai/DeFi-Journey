# Balancer Pool

1. A Balancer Pool is an automated market maker with certain key properties that cause it to function as a selfbalancing weighted portfolio and price sensor.

2. #### Spot Price
   o  
    SP_{i}^o = (Bi/Wi)/ (Bo/Wo)
   i
   Where:
   Bi is the balance of token i, the token being sold by the trader which is going into the pool.
   Bo is the balance of token o, the token being bought by the trader which is going out of the pool.
   Wi is the weight of token i
   Wo is the weight of token o
   ***
   From this denition it is easy to see that if weights are held constant, the spot prices offered by Balancer
   Pools only change with changing token balances. If the pool owner does not add or remove tokens to/from
   the pool, token balances can only change through trades. The constant surface causes the price of tokens
   being bought by the trader (token ) to increase and price of tokens being sold by the trader (token ) to
   decrease. One can prove that whenever external market prices are different from those offered by a
   Balancer Pool, an arbitrageur will make the most prot by trading with that pool until its prices equal those
   on the external market. When this happens there is no more arbitrage opportunity. These arbitrage
   opportunities guarantee that, in a rational market, prices offered by any Balancer Pool move in lockstep with
   the rest of the market.
   ***
