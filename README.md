# Compliance Tests Flowchart Structure

## General Ledger Analytics
- **seldom_accounts**: Identifies rarely used GL accounts | Templates: [GeneralLedger]
- **seldom_user_accounts**: Detects inactive user accounts | Templates: [GeneralLedger]
- **repeating_numbers_journal**: Finds repeating digit patterns in amounts | Templates: [GeneralLedger]
- **recorded_approved_same_user**: Same user recorded+approved entries | Templates: [GeneralLedger]
- **record_no_approvals**: Unapproved journal entries | Templates: [GeneralLedger]
- **last_5_digits**: Analyzes last digits for anomalies | Templates: [GeneralLedger]
- **journals_with_keywords**: Detects suspicious keywords | Templates: [GeneralLedger]
- **no_username_journals**: System-generated entries detection | Templates: [GeneralLedger]
- **limited_character_entries**: Insufficient descriptions | Templates: [GeneralLedger]
- **entries_before_doc_date**: Backdated entries | Templates: [GeneralLedger]
- **holiday_entries**: Non-business day transactions | Templates: [GeneralLedger]
- **compound_journal_entries**: Complex multi-line entries | Templates: [GeneralLedger]

## Revenue Analytics
- **duplicate_invoices**: Exact duplicate invoices | Templates: [SalesRegister]
- **duplicate_invoices_same_date_different_customers**: Same invoice# + date, different customers | Templates: [SalesRegister]
- **duplicate_invoices_same_date_same_item**: Same invoice# + date + items | Templates: [SalesRegister]
- **missing_invoice_sequence**: Gaps in invoice numbering | Templates: [SalesRegister]
- **customer_price_difference**: Abnormal pricing variations | Templates: [SalesRegister]
- **period_end_sales**: End-of-period spikes | Templates: [SalesRegister]
- **sudden_price_spike**: Unusual price changes | Templates: [SalesRegister]
- **sudden_volume_spike**: Abnormal quantity changes | Templates: [SalesRegister]
- **unusual_product_discounts**: Irregular product discounts | Templates: [SalesRegister]
- **unusual_transaction_discounts**: Abnormal transaction discounts | Templates: [SalesRegister]

## Purchases Analytics
- **duplicate_period_invoices**: Same vendor duplicate invoices | Templates: [PurchaseRegister]
- **sudden_purchase_price_spike**: Abnormal purchase price changes | Templates: [PurchaseRegister]
- **sudden_purchase_volume_spike**: Unusual purchase quantities | Templates: [PurchaseRegister]
- **vendor_price_difference**: Vendor pricing anomalies | Templates: [PurchaseRegister]
- **purchase_order_quantity_mismatch**: PO vs received quantity mismatches | Templates: [PurchaseRegister]

## Payroll Analytics
- **duplicate_employee_code**: Duplicate employee IDs | Templates: [PayRegister]
- **duplicate_pan**: Duplicate PAN numbers | Templates: [PayRegister]
- **duplicate_uan**: Duplicate UAN numbers | Templates: [PayRegister]
- **duplicate_bank_account**: Duplicate bank accounts | Templates: [PayRegister]
- **payroll_cost_spike**: Abnormal payroll costs | Templates: [PayRegister]

## Receivables Analytics
- **customer_days_outstanding**: DSO calculation | Templates: [CustomerListing, SalesRegister]
- **long_outstanding_customers**: Aged receivables with sales | Templates: [CustomerListing]
- **negative_receivables**: Credit balances | Templates: [CustomerListing]

## Payables Analytics
- **supplier_days_outstanding**: DPO calculation | Templates: [Vendors, PurchaseRegister]
- **long_outstanding_payables**: Aged payables with purchases | Templates: [Vendors]
- **negative_payables**: Debit balances | Templates: [Vendors]

## Inventory Analytics
- **negative_inventory_quantity**: Negative stock | Templates: [InventoryRegister]
- **negative_inventory_rate**: Negative valuations | Templates: [InventoryRegister]
- **low_margin_items**: Low margin products | Templates: [InventoryRegister, SalesRegister]
- **no_sales_items**: Non-moving inventory | Templates: [InventoryRegister, SalesRegister]
- **no_movement_items**: Zero movement items | Templates: [InventoryRegister]
- **slow_moving_inventory**: Slow movers with purchases | Templates: [InventoryRegister, PurchaseRegister]

## Fixed Assets Analytics
- **capitalization_date_prior**: Early capitalization | Templates: [FixedAssetsRegister]
- **prior_year_capitalization**: FY mismatch in additions | Templates: [FixedAssetsRegister]
- **low_value_capitalization**: Small value assets | Templates: [FixedAssetsRegister]
- **negative_gross_block**: Negative asset values | Templates: [FixedAssetsRegister]
- **blank_narrations**: Missing descriptions | Templates: [FixedAssetsRegister]
- **keyword_narrations**: Suspicious descriptions | Templates: [FixedAssetsRegister]
- **existing_asset_additions**: Additions to existing assets | Templates: [FixedAssetsRegister]
- **deleted_assets_with_wdv**: Written-off assets with residual value | Templates: [FixedAssetsRegister]
- **different_useful_lives**: Inconsistent depreciation lives | Templates: [FixedAssetsRegister]
- **same_year_procurement_deletion**: Quick write-offs | Templates: [FixedAssetsRegister]
- **duplicate_asset_codes**: Duplicate asset IDs | Templates: [FixedAssetsRegister]
