7.2.2-6,

a,
 
TR Node Coverage = {1,2,3,4,5,6,7,8,9,10}
TR Edge Coverage = { (1,4), (1,5), (2,5), (3,6), (3,7), (4,8), (5,8), (5,9), (6,2), (6,10), (7,10), (9,6) }
TR Prime Path Coverage = { [1,4,8], [1,5,8], [1,5,9,6,2], [1,5,9,6,10], [2,5,9,6,2], [2,5,9,6,10], [3,6,2,5,8], [3,6,2,5,9], [3,6,10], [3,7,10], [5,9,6,2,5], [6,2,5,9,6], [9,6,2,5,8], [9,6,2,5,9] }

b,

T Node Coverage = {[1,4,8], [2,5,9,6,10], [3,7,10]}
Although T Node Coverage visits all nodes, T Node Coverage does not tour edges (1,5), (5,7), (6,1) and (3,6)

c,

T Edge Coverage = T Node Coverage U {[1,4,8], [3,6,2,5,8]}
Although T Edge Coverage tours all edges, T Edge Coverage does not tour prime paths [1,5,9,6,2], [2,5,9,6,2], [3,6,2,5,9], [2,6,10], [5,8,5,2,5], [5,1,6,9,6], [9,6,2,5,8], or [9,6,2,5,9]
