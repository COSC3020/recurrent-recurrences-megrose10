# Recurrent Recurrences

Give big $\Theta$ bounds for the following recurrence relations.

1.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

2.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

3.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$

1.T(n) = T(n/13) + 5
T(n/13) = T(n/13/13) + 5
T(n) = T(n/13^2) + 5 +5
T(n/13^2)  = T(n/13/13^2) + 5
T(n) = T(n/13^3) +5 +5+5
T(n) = T(n/13^i) + 5i, i = log(base 13)n
T(n) = T(1) + 5log(base13)n ∈ Θ(logn)

2. T(n) = 13T(n/13) + 5
T(n/13) = 13T(n/13/13) + 5
T(n) = 13*13T(n/13^2) + 5 +5
T(n/13^2)  = 13*13T(n/13/13^2) + 5
T(n) = 13*13*13T(n/13^3) +5 +5+5
T(n) = 13^iT(n/13^i) + 5i, i = log(base 13)n
T(n) = nT(1) + 5log(base13)n ∈ Θ(logn)

T(n) = 13T(n/13) + 2n 
T(n/13) = 13T(n/13/13) + 2n
T(n) = 13*13T(n/13^2) + 2n + 2n
T(n/13^2)  = 13*13T(n/13/13^2) + 4n
T(n) = 13*13*13T(n/13^3) + 4n + 2n
T(n) = 13^iT(n/13^i) + 2in, i = log(base 13)n
T(n) = nT(1) + 2log(base13)n * n ∈ Θ(nlogn)

