# Balancer Pool

1.  A Balancer Pool is an automated market maker with certain key properties that cause it to function as a selfbalancing weighted portfolio and price sensor.

2.  Balancer Pools with high token counts are similar to traditional index funds, allowing users to have broad exposure to the crypto market.

3.  ### Spot Price

    ## $SP^o_i$ = ${B_i \over W_i} \over {B_o \over W_o}$

    Where:

    - Bi is the balance of token i, the token being sold by the trader which is going into the pool.

    - Bo is the balance of token o, the token being bought
      by the trader which is going out of the pool.

    - Wi is the weight of token i

    - Wo is the weight of token o

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

4.  ### Spot Price with Swap Fees

    When we consider swap fees, we do exactly the same calculations as without fees, but using instead of . This strategy is referred to as charging fees "on the way in." With the swap fee, the spot price increases. It then becomes:

    ## $SP^o_i$ = ${B_i \over W_i} \over {B_o \over W_o}$ \* ${1 \over (1-swapFee) }$

5.  ### In- Given-Out (Amount of tokens in)

    Formula for the amount of tokens in - $A_i$ - a trader needs to swap to get a desired amount - $A_o$ - of tokens out in return, considering a Balancer pool without any swap fees:

    ## $A_i$ = $B_i * {(({B_o \over B_o - A_o})^{W_o \over W_i} -1)}$

    ***

    ### With Swapping Fee

    ## $A_i$ = $B_i * {(({B_o \over B_o - A_o})^{W_o \over W_i} -1)}$ \* ${1 \over (1-swapFee)}$

    ***

6.  ### Out-Given-In (Amount of Tokens Out)

    Formula for the amount of tokens out - $A_o$ - a trader gets in return for a given amount of tokens in - $A_i$ -, considering a Balancer pool without any swap fees:

    ## $A_o$ = $B_o * {(1-({B_i \over B_i + A_i})^{W_i \over W_o})}$

    ***

    ### With Swapping Fee

    ## $A_o$ = $B_o * {(1-({B_i \over B_i + A_i})^{W_i \over W_o})}$ \* ${1 \over (1-swapFee)}$

    ***

7.  ### All-Asset Deposit/Withdrawal

    Anyone can be issued Balancer pool tokens (provided the pool is finalized) by depositing proportional amounts of each of the assets contained in the pool. So, for each token k in the pool, the amounts of token k –
    $D_k$ -
    that need to be deposited for someone to get pool tokens are:

    ### $D_k$ = $({P_{supply} + P_{issued} \over P_{supply}} -1)$

    ***

    Conversely, if a user wants to redeem their pool tokens to get their proportional share of each of the underlying tokens in the pool, the amounts of token k – $A_k$– a user gets for redeeming pool tokens will be:

    ### $A_k$ = $(1-{P_{supply} - P_{issued} \over P_{supply}} ) . B_k$

    ***

8.  ### Single Asset Deposit/ Withdrawl

    ### Single Asset Deposit:

    Formula for the amount of pool tokens – $P_{issued}$ – a liquidity provider gets in return for depositing an amount of a single token t present in the pool:

    - Without Swap Fee

      ### $P_{issued}$ = $P_{supply}$. ($(1+ {A_t \over B_t}-1)$)

    - With Swap Fee

      ### $P_{issued}$ = $P_{supply}$. ${({(1+ {{(A_t - A_t.(1-W_t).swapFee) }\over B_t}})^{W_t}}-1)$



    ### Single Asset Deposit:

    - Without Swap Fee

        ### $A_t$ = $B_t$. $(1- (1-{P_{redeemed} \over P_{supply}})^{1 \over W_t})$


    - With Swap Fee

      ### $A_t$ = $B_t$. $(1- (1-{P_{redeemed} \over P_{supply}})^{1 \over W_t}).(1-(1-W_t).swapFee)$

        If there were an exit fee, it would be taken from the amount of tokens redeemed
    
