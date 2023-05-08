Download Link: https://assignmentchef.com/product/solved-stat823-homework-3-data-cleaning-and-management
<br>
<ol>

 <li>(a) Clean up the workspace using the rm() function. Use the data() function to display the built-in datasets you can access. Use the R help to learn more about the ‘longley’ dataset: ?longley.

  <ul>

   <li>Print only the records in the ‘longley’ dataset that are from the years 1947-1950: longley[longley$Year==1947:1950,]. attach(longley).</li>

   <li></li>

  </ul></li>

</ol>

<ul>

 <li>You track your commute times for two weeks and record the following (in minutes):17plot(Unemployed <em>∼ </em>Year).</li>

 <li>Change the type of plot to a line: plot(Unemployed <em>∼ </em>Year, type =”l”)</li>

</ul>

16 20 24 22 15 21 15 17 22.

<ul>

 <li>Enter these numbers into R and find the 5-number summary.</li>

 <li>You find a data entry error, the number 24 should have been 18. Using R, replace the incorrect value without reentering the entire set of data and find the new 5-number summary.</li>

 <li>Use R to count the number of times your commute was at least 20 minutes.</li>

 <li>Use R to calculate the percent of your commutes that were less than 17 minutes.</li>

</ul>

<ol start="3">

 <li>Using the maltreat.dta dataset, explore the variable ethnic using tab1(ethnic). There are spelling mistakes that need to be corrected. Correct mis-spelt names, and create a numeric, categorical variable ethncity. The “Jola” cleaning code for part (i) has been provided. Finish the remaining part of the code and produce the final (clean) bar chart.

  <ul>

   <li>Replace ethnic = “Jola” if ethnic value starts with a “J”.</li>

   <li>Replace ethnic = “Mandinka” if ethnic value starts with an “M”</li>

   <li>Replace ethnic = “Serahule” if ethnic value starts with an “S”</li>

  </ul></li>

</ol>

<ul>

 <li>Replace ethnic = “Wollof” if ethnic value starts with a “W”</li>

</ul>

<table width="632">

 <tbody>

  <tr>

   <td width="632"><strong>library</strong>(“readstata13”)maltreat &lt;- <strong>read.dta13</strong>(“data/maltreat.dta”) <em># Original ethnic (string) variable </em><strong>tab1</strong>(maltreat<strong>$</strong>ethnic, col = “grey”)<em># convert it to a new factor variable ethnicity </em>maltreat<strong>$</strong>ethnicity &lt;- <strong>as.factor</strong>(maltreat<strong>$</strong>ethnic)<em># explore the levels (unclean) </em><strong>levels</strong>(maltreat<strong>$</strong>ethnicity)<em># clean up for Jola</em><strong>levels</strong>(maltreat<strong>$</strong>ethnicity)[<strong>startsWith</strong>(<strong>levels</strong>(maltreat<strong>$</strong>ethnicity),“J”)] &lt;- “Jola”</td>

  </tr>

 </tbody>

</table>

<strong>Distribution of maltreat$ethnic</strong>

Frequency