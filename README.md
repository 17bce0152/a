Abhinav kumar
17bce0152
Vellore institute of technology

Consider the following employee data in relational tables and write queries for questions below the data:

1) Write a query to print the number of employees per department in the organization
SELECT department AS 'Department', 
COUNT(*) AS 'No of Employees' 
FROM employees 
ON employee.employee_id = employee.department 
GROUP BY employee.employee_id, department 
ORDER BY department;
2) Write an SQL query to find the name of the top-level manager of each department
select DEPARTMENT,max(SALARY) MaxSalary from employee group by DEPARTMENT order by MaxSalary asc
3) Write a query to find the total incentive received by a given employee in a given month
select DEPARTMENT,(select IFNULL (max(INCENTIVE_AMOUNT),0) from INCENTIVES where EMPLOYEE_REF_ID=EMPLOYEE_ID) Max_incentive from EMPLOYEE
4) Write a query to find the month where employees got maximum incentive
select FIRST_NAME,INCENTIVE_AMOUNT,DENSE_RANK() OVER (PARTITION BY INCENTIVE_DATE ORDER BY  INCENTIVE_AMOUNT DESC) AS Rank from EMPLOYEE a, INCENTIVES b where a.EMPLOYEE_ID = b.EMPLOYEE_REF_ID

5)You have two sand timers, which can show 4 minutes and 7 minutes respectively. Use both the sand timers (at a time or one after other or any other combination) and measure a time of 9 minutes.
First of all start with  the 7 minute sand timer and the 4 minute sand timer.
Now when the 4 minute sand timer ends turn it upside down instantly.
We can calculate time Elapsed as : 4 minutes. At this moment, 3 minutes of sand is left in the 7 minute sand timer.
Now when the 7 minute sand timer ends turn it upside down instantly.
Time Elapsed: 7 minutes. At this moment, 1 minutes of sand is left in the 4 minute sand timer.
After the 4 minute sand timer ends, only 1 minute is elapsed in 7 minute sand timer, therefore for another minute turn the 7 minute sand timer upside down.
Time Elapsed: 8 minutes.
When the 7 minute sand timer ends, total time elapsed is 9 minutes.
Now, we can calculate the total time as  8 + 1 = 9.

6)John and Mary are a married couple. They have two kids, one of them is a girl. Assume safely that the probability of each gender is 1/2. What is the probability that the other kid is also a girl?

Ans)
We can observe that both the events are independent event

Now it is mentioned that one kid is girl,
So as independent event ,the probability of other kid as girl is ½

Therefore  probability of other kid as girl is 1/2 

7. The following appeared as part of a campaign to sell advertising time on a local radio station to local businesses. Ron’s Cafe began advertising on our local radio station this year and was delighted to see its business increase by 10 percent over last year's totals. Their success shows you how you can use radio advertising to make your business more profitable. 
Discuss how well reasoned you find this argument. In your discussion be sure to analyze the line of reasoning and the use of evidence in the argument. For example, you may need to consider what questionable assumptions underline the thinking and what alternative explanations or counterexamples might weaken the conclusion. You can also discuss what sort of evidence would strengthen or refute the argument, what changes in the argument would make it more logically sound and what, if anything, would help you better evaluate in conclusion.
Ans)
As mentioned in above statement that their sales increased by 10% over last year after they advertised in local radio station,it’s possible that due to advertisement their sales percent had increased but it’s not confirm statement because sales also gets increased due to different factors like some special occasion ,Improvement in quality of food because nowdays local radio station is not used much due to coming to television or social media people are generally getting engaged in socal life more than radio.
So , I refuse with the statement that radio advertising will be working better than television or social media because they need to pay for radio advertising also and output will not as effective as television or social media.
According to my opinion they should be much focused on advertising on social media because it is cheapest mode of advertising and had better result as compared to different mode of advertising. 
