# Stat Count Cards — Finance & Commercial

> Pages এবং tabs যেগুলোতে `coaCashBankStatCard()` দিয়ে বানানো stat count cards আছে এবং এগুলো বাদ দিতে হবে।

---

## 🏦 Finance Menu

| Page / Tab                                       | Render Function                                     | Line (index.html) | Stat Cards                                                                                             |
| ------------------------------------------------ | --------------------------------------------------- | ----------------- | ------------------------------------------------------------------------------------------------------ |
| **Chart of Accounts** → Cash & Bank tab          | `renderChartOfAccounts` → `coaCashBankSummaryCards` | L:6008            | Total Cash-in-Hand · Total Bank Balance · Active Accounts · Total Accounts                             |
| **Voucher Management** → Accounts Payable tab    | `renderVoucherManagement` → `apArSummaryCards`      | L:6791            | Total Outstanding Payable · Overdue Amount · Due in Next 7 Days · Paid Total                           |
| **Voucher Management** → Accounts Receivable tab | `renderVoucherManagement` → `apArSummaryCards`      | L:6791            | Total Outstanding Receivable · Overdue Amount · Due in Next 7 Days · Paid Total                        |
| **VAT & Tax**                                    | `renderVatTax` → `vatSummaryCards`                  | L:7468            | Mushak 6.3 Issued · Total Taxable Value (BDT) · Output VAT Collected (BDT) · Total Invoice Value (BDT) |
| **Budget Management**                            | `renderBudgetManagement` → `budgetSummaryCards`     | L:7957            | Total Budgeted (BDT) · Total Actual Spend (BDT) · Remaining Balance (BDT) · Lines Over Budget          |
| **LC & Export Finance**                          | `renderLcExportFinance` → `lcSummaryCards`          | L:8242            | Total LC Value · Total Utilized · Available Balance · Expiring in 30 Days                              |
| **Audit**                                        | `renderFinanceAudit`                                | L:8432            | Total Findings Logged · Open / In Progress · Unresolved High Risk · Resolved / Closed                  |
| **Financial Statements** → Profit & Loss tab     | `renderFinancialStatements`                         | L:8840            | Total Revenue (BDT) · Total Expenses (BDT) · Net Profit / Net Loss (BDT)                               |
| **Financial Statements** → Balance Sheet tab     | `renderFinancialStatements`                         | L:8858            | Total Assets (BDT) · Total Liabilities (BDT) · Total Equity (BDT) · Assets = Liabilities + Equity      |

---

## 📦 Commercial Menu

| Page / Tab         | Function                  | Line (index.html) | Stat Cards                                                                 |
| ------------------ | ------------------------- | ----------------- | -------------------------------------------------------------------------- |
| **Export L/C** tab | `comLcTiles('export_lc')` | L:15513           | Total L/C Value · Total Utilized · Available Balance · Expiring in 30 Days |
| **BTB L/C** tab    | `comLcTiles('btb_lc')`    | L:15543           | Total L/C Value · Total Utilized · Available Balance · Expiring in 30 Days |
| **Local L/C** tab  | `comLcTiles('local_lc')`  | L:15549           | Total L/C Value · Total Utilized · Available Balance · Expiring in 30 Days |
| **Import L/C** tab | `comLcTiles('import_lc')` | L:15572           | Total L/C Value · Total Utilized · Available Balance · Expiring in 30 Days |

---

## Summary

- **Finance:** ৯টি page/tab এ stat cards আছে
- **Commercial:** ৪টি L/C tab এ stat cards আছে
- **Total:** ১৩টি জায়গা থেকে cards বাদ দিতে হবে

### Shared Helper Function

সব stat cards এই একটি function দিয়ে render হয়:

```js
// index.html — L:5995
function coaCashBankStatCard(iconHtml, value, label) { ... }
```
