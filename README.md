<h1>ExpNo 5 : Implement Simple Hill Climbing Algorithm</h1> 
<h3>Name:Balaji N            </h3>
<h3>Register Number:2305002002             </h3>
<H3>Aim:</H3>
<p>Implement Simple Hill Climbing Algorithm and Generate a String by Mutating a Single Character at each iteration </p>
<h2> Theory: </h2>
<p>Hill climbing is a variant of Generate and test in which feedback from test procedure is used to help the generator decide which direction to move in search space.
Feedback is provided in terms of heuristic function
</p>


## Algorithm:
```
1. Start


2. Input the target string from the user.


3. Generate a random string of the same length using printable characters.


4. Calculate the score (difference) between the random string and the target string.


5. Repeat until the score becomes 0:

Randomly change one character in the string.

Calculate the new score.

If the new score is better (smaller), accept the new string.



6. When score = 0, the string matches the target.


7. Print the final string.


8. Stop


```
## PROGRAM
```python
 import random, string

def hill_climb():
    target = input("Enter the target string: ")
    sol = [random.choice(string.printable) for _ in target]
    score = lambda s: sum(abs(ord(a)-ord(b)) for a,b in zip(s, target))
    best, best_score = sol, score(sol)

    while best_score:
        print(best_score, "".join(best))
        new = best.copy()
        new[random.randrange(len(new))] = random.choice(string.printable)
        new_score = score(new)
        if new_score < best_score:
            best, best_score = new, new_score

    print("Final:", "".join(best))

hill_climb()
```


## Input 
Enter the target string: Hi
## Output
```
60 K0
6 Kf
6 Kf
6 Kf
6 Kf
6 Kf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
4 Gf
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
2 Gj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
1 Hj
Final: Hi
```
## Result:
Thus, the program is executed sucessfully.
