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

- First, the asymptotic analysis of an algorithm could be misleading because the analysis could make it look like the algorithm is quick, but each action in the algorithm could take a lot of time if it is built that way.  Second, as we saw from the data in class, two algorithms with the same time complexity could actually have very different run times.  Third, although the asymptotic analysis could make us think an algorithm is fast or slow, it really just shows us how the runtime changes as the input size or some variable changes.

- The average time complexity of finding an element in a binary search tree is log(n).  If we take the complexity of the second set divided by the first set, it should give us the approximate factor by which the time increases: log(10000)/log(1000) = 4/3.  Therefore the time will be about 5 * 4/3 ≈ 6.67 seconds.

- First, the algorithm could have constant factors of time that change the actual runtime for small sets although they don't affect it asymptotically.  Second, this difference could appear if the algorithm was run on a different computer with a slower processor or different hardware.  Third, it could even be this way on the same computer because of variances in background tasks, CPU limits for overheating, and dividing resources differently that would change the speed that the program runs.
