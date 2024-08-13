# table-names
PO_HEADERS_ALL:
****************
-->This table stores PO header level data, each record in this table represents a purchase order, which is an order for goods or services from a single supplier. Each purchase order may have multiple lines (PO_LINES)

PO_LINES_ALL:
*************
--> This table stores PO line level data, each record in this table represents a purchase order line, which identifies the items and unit price for the goods ordered on a purchase order. Each purchase order line may have multiple shipments (PO_LINE_LOCATIONS).

PO_LINE_LOCATIONS_ALL:
**********************
-->This table stores PO line location level data, each record in this table represents a purchase order shipment, which identifies the quantity of an item shipped to a buyer location by the supplier. Each purchase order shipment may have multiple accounting distributions (PO_DISTRIBUTIONS).

PO_DISTRIBUTIONS_ALL:
*********************
-->This table stores PO distributions level data, each record in this table/view represents a purchase order distribution, which identifies the account charged for the items on a purchase order shipment.

PO_VENDORS_ALL:
***************
-->This table stores PO general information about the suppliers.

PO_VENDOR_SITES_ALL:
********************
-->This table stores PO related supplier site level information, each row includes the site address, supplier reference, purchasing, payment, bank, and general information.

PO_RELEASES_ALL: 
*****************
-->This table stores planned and blanket Purchase Order releases, each row includes the date, buyer, release status, and release number, each release must have at least one purchase order shipment.

PO_VENDOR_CONTACTS:
*******************
-->This table stores supplier contact details which are related to purchase order, each record includes contact name and supplier site.
MODULES
--------
AP(ACCOUNT PAYABLE):
********************
AP_INVOICES_ALL;
AP_INVOICES_LINES_ALL;
AP_INVOIECS_DISTRIBUTIONS_ALL;
AP_PAYMENT_SCHEDULES_ALL;
AP_INVOICE_PAYMENTS_ALL;
AP_CHECKS_ALL;
AP_BATCHES_ALL;
AP_ITEMS;
-----------------------
INVOICE TABLES:
-----------------------
SELECT * FROM AP_BATCHES_ALL;
SELECT * FROM AP_INVOICES_ALL;
SELECT * FROM AP_INVOICES_LINES_ALL;
SELECT * FROM AP_INVOICES_DISTRIBUTIONS_ALL;
SELECT * FROM AP_PAYMENT_SCHEDULES_ALL;
--------------------
PAYMENT TABLE:
--------------------
SELECT * FROM AP_CHECKS_ALL;
SELECT * FROM AP_INVOICE_PAYMENTS_ALL;
SELECT * FROM AP_PAYMEN_DISTRIBUTIONS_ALL;
SELECT * FROM AP_PAYMENT_HISTORY_ALL;
--------------------
TERMS TABLE:
--------------------
SELECT * FROM AP_ITEMS;
SELECT * FROM AP_ITEMS_TL;

PO REQUISITION TABLES:
**********************
PO_REQUISITION_HEADERS_ALL
PO_REQUISITION_LINES_ALL
PO_REQ_DISTRIBUTIONS_ALL

PO TABLES:
**********
PO_HEADERS_ALL
PO_LINES_ALL
PO_LINE_LOCATIONS_ALL
PO_DISTRIBUTIONS_ALL

RECEIPT TABLES:
***************
RCV_SHIPMENT_HEADERS
RCV_SHIPMENT_LINES
RCV_TRANSACTIONS

OTHER TABLES:
*************
PO_RELEASES_ALL
PO_LINE_TYPES
PO_ACTION_HISTORY

AR MODULE:
**********
RA_CUSTOMER_TRX_ALL;
RA_CUSTOMER_TRX_LINES_ALL;
RA_CUST_TRX_LINE_GL_DIST_ALL;
RA_CUST_TRX_TYPES_ALL;
AR_PAYMENT_SCHEDULES_ALL;
RA_BATCH_SOURCES_ALL;
AR_PERIOD_TYPES;
AR_VAT_TAX_ALL;
AR_PERIODS;
HZ_PARTIES;
HZ_PARTY_SITES;
HZ_CUST_ACCOUNTS_ALL;
HZ_CUST_ACCOUNTS_ALL;
HZ_CUST_ACCT_SITES_ALL;
HZ_CUST_SITE_USES_ALL;
HZ_CONTACT_POINTS;
HZ_CUSTOMER_PROFILES;
HZ_LOCATIONS;
HZ_ORGANIZATION_PROFILES;

RECEIPT TABLES:
****************
AR_CASH_RECEIPTS_ALL;
AR_CASH_RECEIPT_HISTORY_ALL;
AR_RECEIVABLE_APPLICATIONS_ALL;
