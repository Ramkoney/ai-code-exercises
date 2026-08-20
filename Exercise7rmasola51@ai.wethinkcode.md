 The Critical section that I found in the code snipped is : 
 	1. for i in range(len(products)):
   		 for j in range(len(products)):

 	For 5,000 products, this performs:
	5,000 × 5,000 = 25,000,000 iterations

  	The i != j check removes only 5,000 self-comparisons, 
	so almost all of  those 25 million iterations still happen.

	The code checks both:
	Product A + Product B
	Product B + Product A
	even though they represent the same combination.
	So the algorithm is O(n²).

	2. The any() creates another bottleneck
		if not any(
    			r['product1']['id'] == product2['id'] and
    			r['product2']['id'] == product1['id']
   	      for r in results
		):

 Reflections Questions and Answers

1. How did optimization change my understanding of the algorithm?

	The optimization demonstrates that performance is strongly 	influenced by algorithm design. The original implementation works 	correctly, but it performs unnecessary comparisons. Changing the 	pair-generation logic removes duplicate work without changing the 	result.

2.What performance improvement did I achieve?

	Changing the nested loops to j = i + 1 reduces the number of pair 	comparisons from approximately 25 million to 12.5 million for 5,000 	products. Removing the any() search also eliminates an additional 	source of unnecessary work.

3. What did I learn about performance bottlenecks?

	I learned that a small section of code, 
	such as a nested loop, 
	can become a major bottleneck when the input dataset grows. 
	I also learned that inefficient data structures and repeated 	searches can compound the problem.

4. The biggest lesson from this exercise is:

Don't just make the code faster—reduce the amount of work the algorithm has to do.

5. How would I approach similar problems in the future?

	I would first measure the execution time, 
	profile the program, 
	identify the bottleneck, 
	analyze its Big-O complexity, 
	consider better algorithms or data structures,
        implement the optimization, 
	and then measure the result again.

6.What tools would I use?

	I would use 
	timeit for controlled timing, 
	cProfile to identify function-level bottlenecks, and 
	line_profiler when I need to identify expensive individual lines.

