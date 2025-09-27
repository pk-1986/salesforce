🔍 1. Lookup Relationship
Scenario: Imagine a company that tracks Customer Support Cases and wants to associate each case with the Customer who raised it.

Objects Involved:

Case (child)

Customer (parent)

How it works: Each Case record has a lookup field pointing to a Customer. This means:

You can link a case to a customer, but the relationship is not tightly bound.

If the customer record is deleted, the case remains (though the link breaks).

Useful for optional or loosely connected relationships.

Example: A support agent logs a case for "John Doe." They use the lookup field to find and link John's customer record. If John’s record is later deleted, the case still exists but loses its reference.

🧩 2. Master-Detail Relationship
Scenario: A company tracks Invoices and their associated Invoice Line Items.

Objects Involved:

Invoice (master)

Invoice Line Item (detail)

How it works:

Every line item must be linked to an invoice.

If the invoice is deleted, all its line items are deleted too.

Ownership and sharing settings of line items are inherited from the invoice.

You can create roll-up summaries on the invoice (e.g., total amount).

Example: An invoice for ₹10,000 has three line items: ₹4,000, ₹3,000, and ₹3,000. These line items are detail records. If the invoice is deleted, all three line items vanish. The invoice can also show a roll-up summary of the total.

🌐 3. External Lookup Relationship
Scenario: A company uses Salesforce to manage Orders, but the Product Catalog is stored in an external ERP system.

Objects Involved:

Order (Salesforce object)

Product (external object)

How it works:

The Order object has a field that links to a product stored outside Salesforce.

This allows referencing external data without importing it.

Example: A sales rep creates an order for a product called “SmartWatch X.” Instead of storing product details in Salesforce, the system uses an external lookup to fetch product data from the ERP system. This keeps Salesforce lean and synced with external systems.
