# n8n workflows for small businesses

Five free [n8n](https://n8n.io) workflows for the jobs small finance and operations teams still do by hand: chasing overdue invoices, keying in supplier bills, building the morning sales report, logging website enquiries and taking WhatsApp orders.

Each one was imported into n8n 2.40 and run against sample data before publishing. The step-by-step guide for each workflow (setup, what it checks, what it costs to run, and the test results) is on **[The Gantry](https://www.gantry.work)**.

| Workflow | What it does | File | Full guide |
|---|---|---|---|
| Xero overdue invoice reminders | Finds overdue Xero invoices, sends staged reminder emails based on how many days overdue each invoice is, and emails you a daily summary | [`xero-overdue-invoice-reminders.json`](workflows/xero-overdue-invoice-reminders.json) | [Xero invoice reminders](https://www.gantry.work/p/xero-invoice-reminders-automation) |
| Supplier invoice email → sheet | Reads PDF supplier bills arriving in Gmail, extracts the fields with AI, checks GST and totals, and logs each bill to a Google Sheet for review | [`supplier-invoice-email-to-sheet.json`](workflows/supplier-invoice-email-to-sheet.json) | [Automate invoice data entry](https://www.gantry.work/p/supplier-invoice-email-to-sheet) |
| Daily owner report from Xero | Emails six numbers at 8am: yesterday's sales, cash received, overdue by age and the top debtors | [`daily-owner-report-xero.json`](workflows/daily-owner-report-xero.json) | [Daily sales report from Xero](https://www.gantry.work/p/daily-owner-report-xero) |
| Enquiry form → Google Sheets | Logs website enquiries to a sheet, removes duplicates, assigns them round robin and sends an auto-reply | [`enquiry-form-to-google-sheets.json`](workflows/enquiry-form-to-google-sheets.json) | [Google Sheets lead automation](https://www.gantry.work/p/google-sheets-lead-automation) |
| WhatsApp order intake | Receives WhatsApp Cloud API messages, recognises orders, logs them to a sheet and confirms them to the customer | [`whatsapp-order-intake.json`](workflows/whatsapp-order-intake.json) | [n8n WhatsApp order automation](https://www.gantry.work/p/n8n-whatsapp-order-automation) |

## How to use

1. In n8n, open **Workflows → Import from file** and choose the `.json` file.
2. Connect your own credentials (Xero, Gmail, Google Sheets, WhatsApp Cloud API or an AI provider, depending on the workflow). None are included.
3. Replace the placeholders: `PASTE-YOUR-SHEET-ID` and the `@example.com` addresses.
4. Run it once by hand on test data before you switch on the schedule or webhook.

The guides list the exact credentials, the sheet columns each workflow expects and the edge cases it was tested against.

## More free tools

Calculators and templates for invoices, receipts, quotations, ERP cost, the EDGE grant and more: **[tools.gantry.work](https://tools.gantry.work)**.

## Licence

MIT. Use, change and share freely. If something breaks on a newer n8n version, open an issue.

---

Built and tested by Sayed, who writes [The Gantry](https://www.gantry.work): practical guides on business systems for Singapore and Southeast Asian SMEs.
