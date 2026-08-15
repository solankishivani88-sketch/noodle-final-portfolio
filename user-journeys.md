\# User Journeys – Final Integration Testing



\---



\## Journey 1: New User Exploration



\### Journey: New User Explores Platform



\### Steps:

1\. Open homepage

2\. View overview statistics

3\. Click "Stablecoins" in navigation

4\. Browse stablecoins list

5\. Use search to find "USDT"

6\. Click on "Tether USDt"

7\. View Community Health Score

8\. View Market Metrics

9\. Interact with correlation chart (change time range)

10\. View Best Yields table



\### Expected Results:

\- All pages load within 3 seconds

\- No console errors

\- All data displays correctly

\- Charts are interactive

\- Navigation is smooth



\### Actual Results:



\- Stablecoins list loaded in 2.34s

\- Search returned “USDT” instantly

\- Detail page loaded in 2.10s

\- Community Health Score and Market Metrics displayed correctly

\- Correlation chart interactive in Chrome, Firefox, and Edge

\- Edge showed a minor layout spacing difference where the chart appeared slightly lower on the page compared to Chrome

\- No console errors in Chrome, Firefox, or Edge

\- Navigation smooth across all Windows browsers (Chrome, Firefox, Edge)



\### Issues Found:

\- Chart positioned lower than expected in Edge (Medium severity)

\- Detail page initial load slightly slow in Edge (3.2s)



\---



\## Journey 2: User Manages Watchlist



\### Journey: User Adds and Manages Watchlist



\### Steps:

1\. Login/authenticate

2\. Navigate to currency detail page

3\. Click "Add to Watchlist"

4\. Verify optimistic UI update

5\. Verify API call succeeds

6\. Check SQL Server for record

7\. Check MongoDB for activity log

8\. Navigate to watchlist page

9\. Verify currency appears

10\. Update holdings amount

11\. Verify SQL update

12\. Remove from watchlist

13\. Verify SQL deletion



\### Expected Results:

\- Optimistic update is instant

\- API calls succeed

\- SQL records created/updated/deleted

\- MongoDB logs all activities

\- No duplicates in database



\### Actual Results:

\- Login successful

\- “Add to Watchlist” triggered instant optimistic update

\- API call returned 200 OK

\- SQL Server showed new watchlist entry with correct user + currency ID

\- MongoDB logged “ADD\_WATCHLIST” activity with timestamp

\- Watchlist page displayed the added currency

\- Holdings update succeeded; SQL record updated correctly

\- MongoDB logged “UPDATE\_HOLDINGS”

\- Removal succeeded; SQL record deleted

\- MongoDB logged “REMOVE\_WATCHLIST”

\- No duplicate records found

\- All operations completed within expected response times



\### Issues Found:

\- MongoDB activity log entry contains an empty activity field for all watchlist operations (Medium severity)



\---



\## Journey 3: View Watchlist → Update Holdings → Remove from Watchlist



\### Steps

1\. Open Watchlist page  

2\. Select a currency  

3\. Update holdings amount  

4\. Save changes  

5\. Remove currency from watchlist  

6\. Verify SQL and MongoDB updates  



\### Expected Results

\- Watchlist loads correctly  

\- Holdings update instantly  

\- SQL Server record updated  

\- MongoDB activity log created  

\- Removal reflects in UI and DB  



\### Actual Results

\- Watchlist loaded correctly  

\- Holdings updated instantly  

\- SQL record updated  

\- MongoDB log created  

\- Removal successful  

\- No duplicates  



\### Issues Found

None  



\## Journey 4: View Homepage → Browse Stablecoins → View Details



\### Steps

1\. Open homepage  

2\. View overview statistics  

3\. Click "Stablecoins" in the navigation  

4\. Browse the stablecoins list  

5\. Use search to find "USDT"  

6\. Click on "Tether USDt"  

7\. View Community Health Score  

8\. View Market Metrics  

9\. Interact with correlation chart (change time range)  

10\. View Best Yields table  



\### Expected Results

\- Homepage and list pages load within 3 seconds  

\- No console errors  

\- Stablecoins list displays correct data  

\- Detail page loads with all sections visible  

\- Charts are interactive and responsive  

\- Navigation is smooth across browsers  



\### Actual Results

\- Homepage loaded in 1.32s  

\- Stablecoins list displayed correctly  

\- Search returned “USDT” instantly  

\- Detail page loaded in 2.9s  

\- Community Health Score and Market Metrics displayed correctly  

\- Correlation chart interactive  

\- No console errors  



\### Issues Found

None  



\---



\## Journey 5: View Watchlist → Update Holdings → Remove from Watchlist



\### Steps

1\. Open Watchlist page  

2\. Select a currency  

3\. Update holdings amount  

4\. Save changes  

5\. Verify SQL Server update  

6\. Verify MongoDB activity log  

7\. Remove currency from watchlist  

8\. Confirm removal in UI  

9\. Verify SQL deletion  

10\. Verify MongoDB removal log  



\### Expected Results

\- Watchlist loads correctly  

\- Holdings update instantly  

\- SQL Server record updated  

\- MongoDB activity log created  

\- Removal reflects in UI and database  

\- No duplicate entries  



\### Actual Results

\- Watchlist loaded correctly  

\- Holdings updated instantly  

\- SQL record updated successfully  

\- MongoDB log created  

\- Removal successful  

\- No duplicates found  



\### Issues Found

None  

