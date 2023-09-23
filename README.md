[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=11730507&assignment_repo_type=AssignmentRepo)
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

Add your answers to this markdown file.

# Answers

- First, the asymptotic analysis of an algorithm could be misleading because it may have added constants that could greatly affect smaller data sets (Ex: $\theta$(n + 1000) is actually written as $\theta$(n)).  Second, there could also be constant multiples that are not shown (Ex: $\theta$(1000n) is written as $\theta$(n)).  Third, with big O notation, an algorithm can have a complexity in any set where the O(f(n)) grows at least as fast as the algorithm.  For example, the complexity T(n) = n could be an element of O(n), O($n^2$), and O($100^n$).

- The average time complexity of finding an element in a binary search tree is log(n).  If we take the complexity of the second set divided by the first set, it should give us the approximate factor by which the time increases: log(10000)/log(1000) = 4/3.  Therefore the time will be about 5 * 4/3 ≈ 6.67 seconds.

- First, the algorithm could have added constants of time that change the actual runtime for small sets although they don't affect it asymptotically.  Second, this difference could appear if the algorithm was run on a different computer with a slower processor or different hardware.  Third, it could even be this way on the same computer because of variances in background tasks, CPU limits for overheating, and dividing resources differently that would change the speed that the program runs.
