# Uniswap-AMM-Formula

```
x*y =k
/*
Here, dx =  Input amount
    dy = output amount
*/
(x+dx)*(y-dy) = k
dy= y-k/(x+dx)
dy= y-xy/(x+dx)   // x*y =k
dy = (xy+ydx-xy)/(x+dx)
dy = ydx/(x+dx)

// uniswap trading fee = 0.3%

dy = (y*0.997*dx)/(x+0.997*dx)
```

---

### output amount = (outToken*0.997 * Input amount)/(Input Token + 0.997 \* Input amount)

---
