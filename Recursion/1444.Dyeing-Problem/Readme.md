### 1444.Dyeing-Problem

此题考察的递归思想的构造.

对于第一个位置,有m种方法,之后的每一个位置,为了避免相邻重复,都是m-1种方法.总共m*(m-1)^(n-1).这其中包括了首尾相同颜色的情况,需要再额外排除.

对于这种情况,我们可以考虑把首尾并成一个色块.那样染色的可能性就等于f(n-1,m).

所以递推公式就是:```f(n,m) = m*(m-1)^(n-1) - f(n-1,m)```

边界条件是 n=2时, f(n,m) = m*(m-1)
