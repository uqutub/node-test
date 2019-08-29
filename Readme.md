# Test assignment:

This is a test assignment. We have developed a simple assignment to imitate real system situation. Test assignment should show the candidate ability to system thinking, coding style, and code versioning skills.

Test assignment described feature to implement.

### Pre-requirements

- NodeJS (ExpressJS / LoopBack)
- MochaJS as a testing framework
- Front-end level basic JavsScript experience
- Database (MySQL, MSSQL, PostgreSQL, MongoDB)

-----------------------------------------

# Feature: Invoice upload

As a customer, I would like to upload files and get converted them into Invoices with precalculation.

1. A customer prepares CSV file with invoices: the first column is internal invoice id, the second is invoice amount and "due on" date

```
1,100,2019-05-20
2,200.5,2019-05-10
B,300,2019-05-01
```

The real-life file includes five thousand rows and includes invalid rows.

2. Customer can upload invoice CSV to the system
3. System processes file so that every invoice gets the selling price according to the next logic:
> Invoice sell price depends on amount and days to the due date. The formula is `amount * coefficient`. The coefficient is 0.5 when the invoice uploaded more than 30 days before the due date and 0.3 when less or equal to 30 days.

3. Customer can check invoices uploaded to the system and check their selling price.
4. Customer can get upload report and understand errors related to CSV file row processing.