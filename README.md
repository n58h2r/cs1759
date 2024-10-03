java c
Hiking I
This is a regular task. You must submit a PDF, which can be produced using the LATEX template on Moodle, exported from a word processor, hand-written or any other method.
There are n people that you need to guide through a difficult mountain pass. Each person has a time in days that it will take to guide them through the pass. You will guide people in groups of up to k people, but you can only move as fast as the slowest person in each group.
For example, if we have 7 people with travel times 3, 6, 4, 2, 1, 8 and 6, with k = 3, we may choose to put them into groups [3, 1], [2, 8] and [6, 4, 6]. The first group will take 3 days, the second will take 8 days and the third will take 6 days, for a total of 17 days. Note that this is not the optimal grouping.

We want to form. groups to guide everyone through the pass in the fewest possible number of days.
(a) Describe how the groups should be formed in the general case (not for the given example), and explain your intuition for why this is optimal.
Hint: Who should be grouped with the slowest person? Think carefully about the case where n is not a multiple of k.
We will now justify the correctness of this algorithm using an exchange argument. We need to show that we can make any grouping better (or at least, not worse) by making it closer to our grouping. We will consider the grouping created by our greedy method, which we’ll call G for greedy. We’re going to compare this to some other grouping, which we’ll call O for other.
Our first step is to ignore any groups that are the same in both G and O. We want to transform. O into G, and there isn’t anything we need to do for these groups. Now, in each grouping, we’ll consider the slowest remaining group, which we’ll call Oslow and Gslow. In the above example, we would have slow = [2, 8] and Gslow = [6, 6, 8].
If Gslow is not a full group, then it follows that there is no way to beat it using two or more g代 写Hiking ISQL
代做程序编程语言roups (why?), so the only interesting cases are when Gslow has k people (and Oslow could have exactly k or fewer than k). The next parts of the task will guide you through the process of constructing a new grouping O′from O in which Oslow is replaced by Gslow, and the argument that O′is the same or better than O in terms of days hiked.
(b) Suppose that Oslow has fewer than k people. How can we move one person into Oslow (from some other group of O), without making any group in O slower?
(c) Now suppose instead that Oslow has exactly k people. Identical groups between G and O were already ignored, and since these two groups are of equal size, there must be a person Alice who is in Gslow but not in Oslow, as well as a person Bob who is in Oslow but not in Gslow. If we make the new grouping O′ by swapping Alice and Bob’s positions in O, what happens to the travel times of their respective groups?

Hint. Is Alice among the k slowest people remaining? How about Bob?
By applying these modifications repeatedly (which address all differences between G and O), we can transform. any grouping into our greedy grouping without making it worse, so by the exchange argument, our greedy algorithm must be correct.
◦ This task is continued on Moodle.
Rubric.
(a) Describe a way to form. groups of up to k people that allows all n people to be guided through the path in as few days as possible and give a short informal reason for why this grouping should be optimal.
Expected length: 3 or 4 sentences.
(b) Describe how you can choose a person to move into Oslow without making any group slower. Briefly justify how this does not make any group slower.
Expected length: two or three sentences.
(c) Identify what happens to the travel times of Alice and Bob’s groups if they are swapped in O. Briefly explain why this is the case.
Expected length: two or three sentences.





         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
