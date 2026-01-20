

# Day 1
## 1.1 What is CRM?

### Definition

CRM stands for **Customer Relationship Management**. It is both a strategy and a technology system that businesses use to manage all interactions and relationships with current and potential customers.

### The Business Problem CRM Solves

Without a CRM system, businesses typically face these challenges:

| Challenge | Impact |
|-----------|--------|
| Customer information scattered across spreadsheets, emails, and paper notes | Difficult to get a complete view of customer history |
| No standardized process for handling leads and sales | Inconsistent customer experience |
| Manual tracking of follow-ups and tasks | Missed opportunities and forgotten commitments |
| Limited visibility into sales pipeline | Poor forecasting and resource allocation |
| No centralized communication history | Team members unaware of past interactions |

### How CRM Addresses These Challenges

A CRM system provides:

1. **Centralized Database**: All customer information in one place, accessible to authorized team members

2. **Process Standardization**: Defined workflows ensure consistent handling of leads, deals, and support cases

3. **Automation**: Routine tasks like follow-up reminders, email notifications, and data updates happen automatically

4. **Visibility**: Dashboards and reports provide real-time insights into business performance

5. **Collaboration**: Team members can share information and work together on customer accounts

### Further Reading

- [What is CRM? | A guide to CRM software by Zoho CRM](https://www.youtube.com/watch?v=hnEQq7kNFWo)
- [Introduction to Zoho CRM - Online Help](https://help.zoho.com/portal/en/kb/crm/getting-started)


## 1.2 Setup CRM Account 
- Please Setup a zoho crm account. Use the below link
- [ How to Use Zoho CRM Free](https://www.youtube.com/watch?v=7i826PTnSqo)
- Go through the below links
- [Zoho CRM Home Page Overview](https://help.zoho.com/portal/en/kb/crm/getting-started/articles/home-page)
- [Understanding the CRM Interface](https://help.zoho.com/portal/en/kb/crm/getting-started/articles/understand-crm-account#Key_CRM_Terminologies)





### Initial Setup and Navigation
- Objective: Familiarize yourself with the Enterprise interface and personal settings.
- Access the System: Log in to your Zoho CRM Enterprise account.
- Locate Setup: Identify the "Setup" icon in the top-right corner. This menu is the command center for all administrative tasks discussed in this course.
- Personalize: Navigate to Setup > General > Personal Settings. Configure your locale, time zone, and language. This is critical as automation rules often rely on the system time zone.3
- Explore Modules: Click through the standard tabs (Leads, Contacts, Accounts) to observe the default list views.


## 1.3 Setup Sandbox for Development
- Zoho CRM Sandbox is a secure, isolated testing environment that enables administrators and developers to test customizations, workflows, and configurations without risking production data.

### What Sandbox does and why it matters

Sandbox creates a parallel version of your CRM where teams can safely experiment with configurations. Think of it as a laboratory for your CRM—changes made here affect only the test environment until you explicitly deploy them to production.

**The core problems Sandbox addresses:**

- **Risk mitigation**: Untested changes can break workflows, corrupt data, or disrupt sales operations. Sandbox eliminates this risk entirely.
- **Developer collaboration**: Third-party developers can build and test customizations without ever accessing live customer data.
- **Quality assurance**: Teams can thoroughly validate complex automations before they touch production records.
- **Change management**: A unified deployment log tracks every modification pushed to production, creating a complete audit trail.

Zoho offers **two sandbox types**. Configuration-only sandboxes copy your CRM setup without data—ideal for testing layout changes and workflow logic. Configuration-and-data sandboxes include actual records, either **10 sample records per module** or a user-specified subset of production data for realistic testing scenarios.

### Step-by-step sandbox creation process

Creating a sandbox requires Administrator profile permissions. The process takes just a few minutes but involves several important decisions.

**To create your first sandbox:**

Please go through this link - [Zoho CRM Sandbox Tutorial](https://www.youtube.com/watch?v=FfMFLTHRvWs)

1. Navigate to **Setup** (gear icon) → **Data Administration** → **Sandbox**
2. Click **Create Sandbox** or **Create New Sandbox**
3. Enter a descriptive name (e.g., "Q1 Workflow Testing" or "API Integration Dev")
4. Add an optional description identifying the sandbox purpose
5. Select sandbox type: **Configuration** or **Configuration and Data**
6. If choosing Configuration and Data, select either Sample Data (10 records/module) or Partial Data (specify record count)
7. In the **Items Availability in Sandbox** window, choose **All** to copy everything or **Selected** to import only specific feature configurations
8. Assign CRM users who need sandbox access
9. Click **Create** to provision the environment

The system generates a custom URL automatically based on your sandbox name. Access follows the format `https://crmsandbox.zoho.com/crm/{sandbox_name}`. A prominent **gold "Sandbox" ribbon** appears at the top of the interface whenever you're working in a test environment, preventing accidental confusion with production.

- From now onwards , Use the sandbox to make changes to your crm account 


## Module 2: Core Data Components


## Overview

The Core Data Components form the foundation of your CRM. Before you can automate processes or build reports, you need to establish how data is structured and stored. This module covers seven essential components:

| Component | Purpose |
|-----------|---------|
| **Modules** | Define what types of entities you track |
| **Layouts** | Organize how fields appear on screen |
| **Fields** | Store individual pieces of information |
| **Forms (Webforms)** | Capture data from external sources |
| **Wizards** | Guide users through complex data entry |
| **Validation Rules** | Ensure data integrity |
| **Views** | Filter and display records |

---
## 2.1 Modules

### What Are Modules?

Modules are the fundamental building blocks of Zoho CRM. Each module represents a distinct business entity or concept.

Think of modules as:
- **Database analogy**: Tables in a relational database
- **Business analogy**: Categories of information you need to track
- **Filing analogy**: Filing cabinets, each dedicated to a type of document

### Types of Modules

- Standard Modules: These come pre-installed and support standard business processes. Key modules include Leads (prospecting), Accounts (business entities), Contacts (people), Deals (sales pipeline), Activities (tasks/calls), and Reports.8
- Custom Modules: Enterprise accounts allow for the creation of Custom Modules to track unique business entities not covered by standard options. For example, a Real Estate firm might create a "Properties" module, or an Education firm might create "Courses" and "Students".12
Creating a Custom Module effectively creates a new table in the database, complete with API endpoints, allowing for specialized relationship mapping.

#### Standard Modules (Pre-built by Zoho)

| Module | Purpose | Typical Records |
|--------|---------|-----------------|
| **Leads** | Unqualified prospects | Initial inquiries, marketing responses |
| **Contacts** | Individual people | Customers, decision-makers |
| **Accounts** | Organizations | Companies you do business with |
| **Deals** | Sales opportunities | Revenue tracking, pipeline |
| **Tasks** | To-do items | Action items for users |
| **Events** | Calendar entries | Meetings, appointments |
| **Calls** | Phone interactions | Call logging |
| **Products** | Items you sell | Product catalog |
| **Cases** | Support tickets | Customer issues |

#### Custom Modules (Created by you)

Custom modules allow you to track business-specific entities that standard modules do not cover.

**Examples of Custom Modules**:
- **Vehicles** (for auto dealers or repair shops)
- **Properties** (for real estate)
- **Projects** (for service businesses)
- **Equipment** (for maintenance tracking)
- **Training Sessions** (for education providers)

- [What is a module in Zoho CRM](https://help.zoho.com/portal/en/kb/crm/faqs/customization/articles/faqs-modules#What_is_a_module_in_Zoho_CRM)

### Module Relationships (Lookups)

Modules connect to each other through **Lookup Fields**. These create relationships between records in different modules.

**Common Relationships**:

```
CONTACTS -----(belongs to)-----> ACCOUNTS
    |
    +------(associated with)---> DEALS
    |
    +------(has)---------------> TASKS, EVENTS, CALLS
```

**Relationship Types**:

| Type | Description | Example |
|------|-------------|---------|
| **One-to-Many** | One parent record has multiple child records | One Account has many Contacts |
| **Many-to-One** | Multiple records link to one parent | Many Deals link to one Account |
| **Many-to-Many** | Multiple records on both sides | Contacts can be on multiple Deals |

### How to Work with Modules

#### Accessing Module Settings

1. Go to **Setup** (gear icon)
2. Navigate to **Customization** > **Modules and Fields**
3. Select the module you want to configure

#### Module Configuration Options

For each module, you can configure:

- **Module Name**: Singular and plural forms
- **Layouts**: Field arrangement and sections
- **Fields**: Data elements within the module
- **Validation Rules**: Data integrity checks
- **Related Lists**: Child records display
- **Module Permissions**: Who can access this module




### Further Reading


- [Modules Overview](https://help.zoho.com/portal/en/kb/crm/modules)
- [Creating Custom Modules](https://help.zoho.com/portal/en/kb/crm/customization/modules/articles/create-custom-module)
- [Mastering Module Relationships in Zoho CRM: From One-to-Many to Many-to-Many](https://www.youtube.com/watch?v=CPwu-szIiuA)
- [Look up field](https://zenatta.com/lookup-fields-tutorial-for-zoho-crm/)
- [Customizing Modules](https://help.zoho.com/portal/en/kb/crm/customize-crm-account/customizing-modules)

# Day 2
## 2.2 Fields

### What Are Fields?

Fields are the atomic units of data storage. Every piece of information in Zoho CRM is stored in a field.

Think of fields as:
- **Database analogy**: Columns in a table
- **Form analogy**: Individual input boxes
- **Spreadsheet analogy**: Column headers

### Field Types Reference

| Type | Use Case | Example |
|------|----------|---------|
| **Single Line** | Short text (< 255 chars) | Name, Email, VIN |
| **Multi-Line** | Long text (up to 32000 chars) | Description, Notes |
| **Email** | Email addresses with validation | customer@email.com |
| **Phone** | Phone numbers | +1-555-123-4567 |
| **Picklist** | Single selection from options | Status, Priority |
| **Multi-Select Picklist** | Multiple selections | Services Requested |
| **Number** | Integers | Quantity, Mileage |
| **Decimal** | Numbers with decimals | Rating (4.5) |
| **Currency** | Money values | Amount, Price |
| **Percent** | Percentage values | Discount %, Tax % |
| **Date** | Date only | Service Date |
| **Date/Time** | Date and time | Appointment Time |
| **Checkbox** | Boolean (Yes/No) | Is Active, Approved |
| **Lookup** | Relationship to another module | Customer, Vehicle |
| **Multi-Select Lookup** | Multiple relationships | Assigned Team Members |
| **User** | Reference to CRM user | Assigned To |
| **Auto Number** | System-generated sequence | JOB-0001 |
| **Formula** | Calculated from other fields | Total = Parts + Labor |
| **Rollup Summary** | Aggregation from child records | Total Orders Count |
| **Image** | Image upload | Product Photo |
| **File Upload** | Document attachment | Contract PDF |

### Field Properties

Every field has configurable properties:

| Property | Description |
|----------|-------------|
| **Field Label** | Display name shown to users |
| **API Name** | System name for integrations (no spaces) |
| **Required** | Must have a value to save |
| **Unique** | No duplicate values allowed |
| **Read Only** | Cannot be edited by users |
| **Default Value** | Pre-filled value for new records |
| **Tooltip** | Help text shown on hover |

### Formula Fields

Formula fields calculate values based on other fields. They are read-only and update automatically.

**Basic Syntax**:
```
// Arithmetic
field1 + field2
field1 * 0.18

// Text concatenation
concat(First_Name, " ", Last_Name)

// Conditional
if(Amount > 10000, "High Value", "Standard")

// Date calculations
datecomp(Closing_Date, Created_Time, 'd')

// Null handling
if(isnull(Discount), 0, Discount)
```

**Example Formula Fields**:

```
Field: Full Name
Formula: concat(First_Name, " ", Last_Name)

Field: Age in Days
Formula: datecomp(now(), Created_Time, 'd')

Field: Total with Tax
Formula: Amount + (Amount * Tax_Percent / 100)

Field: Priority Score
Formula: if(Priority == "High", 3, if(Priority == "Medium", 2, 1))
```

### Rollup Summary Fields

Rollup summaries aggregate data from child records (related records linked via lookup).

**Available Functions**:
- **COUNT**: Number of related records
- **SUM**: Total of a number/currency field
- **AVERAGE**: Average of a number/currency field
- **MAX**: Maximum value
- **MIN**: Minimum value

**Example**:
```
On ACCOUNTS module:

Field: Total Deals
- Related Module: Deals
- Function: COUNT
- Filter: Stage = "Closed Won"

Field: Total Revenue
- Related Module: Deals
- Function: SUM
- Summary Field: Amount
- Filter: Stage = "Closed Won"
```

### Creating Custom Fields

1. Go to **Setup** > **Customization** > **Modules and Fields**
2. Select the module
3. Click on the layout
4. In the left panel, click **Create New Field**
5. Select field type
6. Configure properties:
   - Field Label
   - Field API Name (set it yourself for clarity)
   - Required, Unique, etc.
7. Drag field to desired position in layout
8. Save

### Common Mistakes to Avoid

| Mistake | Why It's Bad | Better Approach |
|---------|--------------|-----------------|
| Using Text for numbers | Cannot calculate or sort properly | Use Number/Currency/Decimal |
| Not setting API names | Auto-generated names are cryptic | Set readable API names |
| Making everything required | Users frustrated, create workarounds | Only truly essential fields |
| Picklist with too many values | Unusable dropdown | If >15 options, use lookup |
| Circular formula references | Error, won't save | Plan formula dependencies |

-  [Working with Fields](https://help.zoho.com/portal/en/kb/crm/customize-crm-account/customizing-fields)
- [Customizing Fields](https://help.zoho.com/portal/en/kb/crm/customize-crm-account/customizing-fields)
- [How To Add Custom Fields To Zoho CRM](https://www.youtube.com/watch?v=IibYnrSKXSw)
- [How to Use Formula Fields in Zoho CRM | Step-by-Step Guide
](https://www.youtube.com/watch?v=pUfX_aN0Ndg)


# Day 3
## Module 3: Interface Design & User Experience (UX)

## 3.1 Layouts

### What Are Layouts?

Layouts define **how fields are arranged and which fields appear** for a module. A single module can have multiple layouts, allowing different field configurations for different scenarios or user types.


### Why Multiple Layouts?

Different users or scenarios may require different information:

| Scenario | Layout Approach |
|----------|-----------------|
| Different products/services | Each product type has specific fields |
| Different user roles | Sales sees different fields than Support |
| Different processes | Insurance claims need different fields than regular sales |
| Regional differences | Different countries may have different requirements |

Please go through the below links to understand how to create and work with layouts

- [Conditional Layouts - Concept and Benefits](https://help.zoho.com/portal/en/kb/crm/customize-crm-account/customizing-page-layouts/articles/conditional-layouts-concept-and-benefits)
- [Working with Page Layouts](https://help.zoho.com/portal/en/kb/crm/customize-crm-account/customizing-page-layouts/articles/create-page-layouts)

### Layout Components

A layout consists of:

1. **Sections**: Groups of related fields
2. **Fields**: Individual data elements
3. **Section Properties**: Column layout, collapsibility
4. **Layout Rules**: Dynamic field behavior

```
+------------------------------------------+
|  LAYOUT: Standard Deal Layout            |
+------------------------------------------+
|  SECTION: Deal Information               |
|  +----------------+  +----------------+  |
|  | Deal Name      |  | Stage          |  |
|  +----------------+  +----------------+  |
|  +----------------+  +----------------+  |
|  | Amount         |  | Close Date     |  |
|  +----------------+  +----------------+  |
+------------------------------------------+
|  SECTION: Contact Information            |
|  +----------------+  +----------------+  |
|  | Contact Name   |  | Account Name   |  |
|  +----------------+  +----------------+  |
+------------------------------------------+
|  SECTION: Additional Details [Collapsed] |
|  (Click to expand)                       |
+------------------------------------------+
```

### Section Types

| Section Type | Use Case |
|--------------|----------|
| **Two-Column** | Most common, efficient use of space |
| **Single-Column** | For large text fields or emphasis |
| **Collapsible** | For optional or less-used fields |

### Layout Rules (Dynamic Behavior)

Layout rules add dynamic behavior without coding. They allow you to:

- Show or hide fields based on other field values
- Show or hide sections based on conditions
- Make fields required or optional based on context

**Example Layout Rule**:
```
CONDITION: If "Service Type" equals "Insurance Claim"
ACTIONS:
  - Show field: "Claim Number"
  - Show field: "Insurance Company"
  - Make required: "Claim Number"
  - Show section: "Insurance Details"
```

### Creating and Editing Layouts

1. Go to **Setup** > **Customization** > **Modules and Fields**
2. Select the module
3. Click on the **Layouts** tab (or the layout name)
4. Use the layout editor:
   - Drag fields from left panel to layout
   - Create new sections using "Add Section"
   - Configure section properties (columns, collapsibility)
   - Remove fields by dragging back to left panel

### Assigning Layouts to Users

Layouts can be assigned to specific profiles, so different users see different layouts:

1. In layout settings, find "Layout Assignment"
2. Map profiles to layouts
3. Each profile can only use assigned layouts

### Common Mistakes to Avoid

| Mistake | Why It's Bad | Better Approach |
|---------|--------------|-----------------|
| Creating too many layouts | Maintenance nightmare | Use layout rules for dynamic behavior |
| Hiding critical fields in some layouts | Data inconsistency | Keep key fields across all layouts |
| Not testing layout rules | Unexpected behavior | Test all condition combinations |
| Forgetting to assign layouts | Users see wrong layout | Always complete profile assignment |


### Understanding Records, Layouts, and Modules

#### Overview

It is important to understand how records, layouts, and modules relate to each other in Zoho CRM.

---

#### Records, Modules, and Layouts

A **record** is a single data entry that belongs to exactly one **module**. A contact record lives in the Contacts module, a deal record lives in the Deals module. This relationship is permanent and one-to-one—a record cannot belong to multiple modules.

A **layout** is the form template used when a record is created. The key insight: **a record is associated with exactly one layout at any given time**. It cannot belong to multiple layouts simultaneously.

---

#### How Layout Assignment Works

When a record is created, it gets stamped with the layout that was used during creation. This layout assignment is stored as a system field (visible in record details or list views).

However, **the layout assignment can be changed**. A record can be moved from one layout to another:

- Manually by a user (if they have permission)
- Automatically through workflow rules

At any given moment, a record is associated with only one layout.

---

#### Practical Example: Car Repair CRM

Consider two layouts in a Deals module: "Quick Service" and "Major Repair."

1. A customer comes in for an oil change. You create a deal using the **Quick Service** layout with minimal fields.

2. During inspection, the technician discovers transmission problems. This is now a major job.

3. You change the record's layout to **Major Repair**—either manually or via a workflow triggered by updating the service type.

4. The record now displays the Major Repair layout with additional fields for diagnostics, parts ordering, and extended timeline tracking.

The record didn't duplicate or exist in both layouts. It migrated from one to the other.

---

#### What Happens to Data During Layout Changes?

When you switch a record's layout:

| Scenario | Behavior |
|----------|----------|
| Fields common to both layouts | Retain their values |
| Fields only in the old layout | Data retained in database but hidden from UI |
| Fields unique to the new layout | Appear empty, ready to be filled |

The data isn't deleted when you change layouts—it's just not visible if the new layout doesn't include those fields. If you switch back, the old values reappear.

---

#### Why This Matters

This design means layouts are about *presentation and process*, not data partitioning.

**Key implications:**

- All records in a module share the same underlying database table regardless of layout
- You can run reports across all records in a module without worrying about which layout they use
- You can create views and build automations that span all layouts
- Different teams still get tailored interfaces for data entry and viewing

---

#### Related Component Relationships

##### Layouts and Fields

Fields live inside layouts. Custom fields are added to specific layouts and won't automatically appear in other layouts of the same module. Standard fields exist across layouts, but visibility and mandatory settings are controlled per-layout.

### Layouts and Profiles

Profiles determine which layouts a user can access. Multiple layouts can be assigned to a profile, with one designated as default. Users see their default layout when creating new records.

### Layouts and Wizards

A wizard is built on top of a specific layout, redistributing fields across sequential screens with conditional branching. One layout can have multiple wizards or none at all.

### Layouts and Validation Rules

Validation rules are defined at the layout level. Different layouts can enforce different validation logic.

### Layouts and Workflow Rules / Blueprints

Workflow rules and blueprints can be scoped to specific layouts, allowing different automations to trigger based on which layout was used.

---

## Summary

| Component | Relationship |
|-----------|--------------|
| Record → Module | One-to-one, permanent |
| Record → Layout | One-to-one at any given time, but can be changed |
| Module → Layouts | One-to-many (a module can have multiple layouts) |
| Layout → Fields | One-to-many (a layout contains multiple fields) |
| Layout → Profiles | Many-to-many (profiles can access multiple layouts) |

---

# Day 4
## 3.2 Webforms

### What Are Webforms?

Webforms are HTML forms generated by Zoho CRM that can be embedded on websites. When someone submits a webform, a record is automatically created in the CRM.

### Why Use Webforms?

| Without Webform | With Webform |
|-----------------|--------------|
| Manual data entry from emails | Automatic record creation |
| Risk of data entry errors | Direct capture from source |
| Delayed data availability | Immediate record in CRM |
| No tracking of source | Automatic source tracking |

### Webform Components

**Form Configuration**:
- Module (which module receives the data)
- Layout (which layout's fields are available)
- Fields (selected subset of layout fields)
- Notifications (who gets notified on submission)
- Return URL (where to redirect after submit)

**Form Elements**:
- Standard fields from module
- Required field marking
- Custom field labels (can differ from CRM labels)
- Captcha (spam prevention)
- File upload fields (limited)
- Submit button

### Creating a Webform

1. Go to **Setup** > **Developer Space** > **Webforms**
2. Click **+ New Form**
3. Select module (e.g., Leads)
4. Design the form:
   - Drag fields from left panel to form
   - Set field labels and required status
   - Configure form title and submit button
5. Configure settings:
   - Enable/disable captcha
   - Set notification recipients
   - Set return URL
   - Configure duplicate handling
6. Save and generate embed code

### Webform Settings

| Setting | Purpose |
|---------|---------|
| **Auto-Response** | Send automatic email to form submitter |
| **Notify Users** | Alert CRM users about new submission |
| **Record Assignment** | Automatically assign to users/round robin |
| **Return URL** | Redirect page after submission |
| **Duplicate Check** | How to handle duplicate submissions |
| **Captcha** | Prevent spam submissions |


### Troubleshooting Tips

**Problem**: Form submissions not creating records
- Check if webform is active (not draft)
- Verify all required CRM fields have defaults or are on form
- Check webform submission logs for errors

**Problem**: Duplicate records being created
- Enable duplicate checking in form settings
- Verify duplicate check field is correctly mapped

### Further Reading

- [Web Forms](https://help.zoho.com/portal/en/kb/crm/generate-leads-and-manage-customers/web-forms)
- [Creating Web Forms](https://help.zoho.com/portal/en/kb/crm/generate-leads-and-manage-customers/web-forms/articles/creating-web-forms)
- [Web Form Analytics](https://help.zoho.com/portal/en/kb/crm/generate-leads-and-manage-customers/web-forms/articles/web-form-analytics)

## 3.3 Wizards

### What Are Wizards?

Wizards provide a guided, multi-step form experience for creating or editing records. Unlike standard forms where all fields appear at once, wizards present fields in logical sequences.

**Note**: Wizards are available in Professional edition and above. Free edition users cannot create wizards.

### When to Use Wizards

| Scenario | Standard Form | Wizard |
|----------|---------------|--------|
| Quick data entry | Better | Overkill |
| Complex records with many fields | Overwhelming | Digestible steps |
| Conditional field capture | Limited | Dynamic paths |
| New user training | Easy to miss fields | Guided process |
| Compliance requirements | No confirmation | Built-in validation per step |

### Wizard Components

```
WIZARD FLOW

Form 1 (Step 1): Basic Information
  - Fields: Name, Contact, Source
  - Navigation: Next only
        |
        v
Form 2 (Step 2): Details
  - Fields: Product, Amount, Priority
  - Conditional: If Amount > $10000, show "Executive Approval"
  - Navigation: Back, Next
        |
        v (conditional branch)
Form 3a (High Value Path):     Form 3b (Standard Path):
  - Additional approvals    OR   - Standard fields
        |                              |
        +----------+-------------------+
                   v
Form 4 (Final Step): Review
  - Summary of all data
  - Button: Create Record
```

### Wizard Features

| Feature | Description |
|---------|-------------|
| **Multi-Step Navigation** | Back/Next buttons between forms |
| **Conditional Forms** | Different paths based on data entered |
| **Per-Step Required Fields** | Different requirements at each step |
| **Messages** | Instructions and guidance per step |
| **Confirmation Screen** | Review before final submission |

### Designing Effective Wizards

**Best Practices**:
- Keep to 3-5 steps maximum
- Group related fields together
- Always allow back navigation
- Provide clear instructions
- Keep conditional logic simple

**Step Design Guidelines**:

| Step | Content | Example |
|------|---------|---------|
| Step 1 | Most critical identification fields | Who, What |
| Step 2 | Details and specifications | Product, Amount, Date |
| Step 3 | Optional or conditional fields | Approvals, Special Requirements |
| Final | Review and confirmation | Summary, Submit |

### Common Mistakes to Avoid

| Mistake | Why It's Bad | Better Approach |
|---------|--------------|-----------------|
| Too many steps | User fatigue | 3-5 steps maximum |
| Too few fields per step | Unnecessary clicking | Group related fields |
| No back navigation | Users feel trapped | Always allow back |
| Missing validation messages | Users confused | Clear error messages |
| Complex conditional logic | Hard to test | Keep branching simple |

### Further Reading

- [Wizards Overview](https://help.zoho.com/portal/en/kb/crm/customize-crm-account/wizards/articles/wizards)
---

## 3.4 Validation Rules

### What Are Validation Rules?

Validation rules are conditions that records must satisfy before they can be saved. They enforce data integrity at the database level, regardless of how data is entered.

### Why Validation Rules?

| Without Validation | With Validation |
|-------------------|-----------------|
| Discount > Sale Amount possible | Blocked with message |
| Future birth dates allowed | Prevented |
| Inconsistent data | System-enforced consistency |
| Relies on user knowledge | Automatic enforcement |

### Validation Rule Logic

The condition should evaluate to **TRUE when data is INVALID**.

```
IF [Condition is TRUE] THEN [Show Error / Block Save]

Example:
IF (Discount > Grand_Total) = TRUE
THEN Show error: "Discount cannot exceed total amount"
```

### Criteria Functions

Common functions for validation criteria:

```
// Comparison
${Field} == value       // Equals
${Field} != value       // Not equals
${Field} > value        // Greater than
${Field} < value        // Less than

// Text functions
contains(${Field}, "text")
startswith(${Field}, "prefix")
len(${Field})

// Null checks
isnull(${Field})        // Is empty
!isnull(${Field})       // Is not empty

// Date functions
${Date_Field} < today() // Before today
${Date_Field} > now()   // After current time

// Logical operators
(condition1) && (condition2)   // AND
(condition1) || (condition2)   // OR
!(condition)                   // NOT
```

### Example Validation Rules

**Rule 1: Prevent Discount Exceeding Amount**
```
Name: Maximum Discount Check
Criteria: (${Discount} > ${Amount})
Error Message: "Discount cannot exceed the deal amount."
```

**Rule 2: Require Phone or Email**
```
Name: Contact Info Required
Criteria: (isnull(${Phone})) && (isnull(${Email}))
Error Message: "Please provide either a phone number or email address."
```

**Rule 3: Future Date Validation**
```
Name: Valid Close Date
Criteria: (!isnull(${Close_Date})) && (${Close_Date} < today())
Error Message: "Close Date must be today or in the future."
```

**Rule 4: Email Format Validation**
```
Name: Valid Email Format
Criteria: (!isnull(${Email})) && (!contains(${Email}, "@"))
Error Message: "Please enter a valid email address."
```

### Creating Validation Rules

1. Go to **Setup** > **Customization** > **Modules and Fields**
2. Select the module
3. Click **Validation Rules** tab
4. Click **+ Create New Rule**
5. Configure:
   - Rule Name
   - Layout(s) to apply
   - Criteria (condition that identifies INVALID data)
   - Error Message
6. Save

### Validation Rule Execution Flow

```
User Attempts to Save Record
        |
        v
Check Required Fields (built-in)
        |
        v
Check Field-Level Validation (format, range)
        |
        v
Execute Validation Rules (custom rules)
        |
        v
If any fail: Show Error, Block Save
If all pass: Save Record
```

### Common Mistakes to Avoid

| Mistake | Why It's Bad | Better Approach |
|---------|--------------|-----------------|
| Overly complex criteria | Hard to debug | Break into multiple rules |
| Unclear error messages | Users confused | Specific, actionable messages |
| Not handling null values | Unexpected failures | Always check for null |
| Conflicting rules | Impossible to save | Review all rules together |

### Troubleshooting Tips

**Problem**: Validation firing when it should not
- Check if logic is correct (TRUE = invalid)
- Verify null handling
- Add debug info to message temporarily

**Problem**: Validation not firing when it should
- Check if rule is active
- Verify correct layout is selected
- Check "Execute On" settings (Create vs Edit)

### Further Reading

- [Validation Rules](https://help.zoho.com/portal/en/kb/crm/customize-crm-account/validation-rules)
- [Creating Validation Rules](https://www.youtube.com/watch?v=-BgHI_xUdNM)

---

## 3.5 Views

### What Are Views?

Views are saved filter configurations that display a subset of records based on criteria you define. They don't change data—they're lenses through which you look at records.

### Why Use Views?

| Without Views | With Views |
|---------------|------------|
| Search/filter each time | One-click access |
| See all records at once | Focused on relevant data |
| Manual sorting | Pre-sorted by priority |
| Same view for everyone | Role-specific displays |

### Types of Views

**List Views**: Traditional tabular display
- Spreadsheet-like format
- Columns and rows
- Easy sorting and bulk actions

**Canvas Views**: Customizable card-based layouts
- Visual card representation
- Grouping and color coding
- Good for Kanban-style workflows

### View Components

| Component | Description |
|-----------|-------------|
| **Filter Criteria** | Conditions that records must match |
| **Columns** | Which fields are displayed |
| **Sort Order** | How records are arranged |
| **Grouping** | How records are categorized (Canvas) |
| **Access Control** | Who can see this view |

### Filter Criteria Options

```
Simple Conditions:
- Field equals/not equals value
- Field is empty/not empty
- Field contains/does not contain

Date Conditions:
- Today, Yesterday, Tomorrow
- This Week, Last Week, Next Week
- This Month, Last Month
- Custom date range

User-Based:
- My Records (owner is current user)
- My Team's Records
- All Records

Combined Conditions:
- Multiple criteria with AND/OR logic
```

### Creating Views

1. Go to the module (e.g., Leads)
2. Click the view dropdown (usually shows "All Leads")
3. Click **+ Create View** or **New Custom View**
4. Configure:
   - View Name
   - Filter Criteria
   - Select Columns
   - Sort Order
   - Visibility (Only Me, All Users, Selected Profiles)
5. Save

### Example Views

**View: My Open Deals**
```
Criteria:
- Owner = ${Current User}
- Stage NOT IN ("Closed Won", "Closed Lost")

Columns: Deal Name, Amount, Stage, Close Date, Account

Sort: Close Date (Ascending)

Access: All Users
```

**View: High Priority Tasks**
```
Criteria:
- Priority = "High"
- Status != "Completed"

Columns: Task Name, Due Date, Related To, Owner

Sort: Due Date (Ascending)

Access: All Users
```

**View: This Month's Closed Deals**
```
Criteria:
- Stage = "Closed Won"
- Close Date = This Month

Columns: Deal Name, Amount, Account, Close Date

Sort: Amount (Descending)

Access: Managers only
```

### View Best Practices

| Do | Don't |
|----|-------|
| Name views descriptively | Use vague names like "My View 1" |
| Create views users need | Create too many views |
| Set appropriate access | Make all views public |
| Review and clean up periodically | Let obsolete views accumulate |

### Common Mistakes to Avoid

| Mistake | Why It's Bad | Better Approach |
|---------|--------------|-----------------|
| Too many views | Hard to find right one | 5-10 views per module |
| Unclear names | Users confused | Descriptive, action-oriented |
| Complex filters | Confusing, possibly slow | Simple filters, multiple views |
| No access control | Everyone sees everything | Restrict to relevant roles |

### Troubleshooting Tips

**Problem**: View showing no records
- Check filter criteria (too restrictive?)
- Verify user's role can see matching records
- Check date filters (relative vs. specific)

**Problem**: View slow to load
- Reduce number of columns
- Avoid complex formula fields in columns
- Use indexed fields for filtering

### Further Reading

- [Custom List Views](https://help.zoho.com/portal/en/kb/crm-nextgen/customize-crm-account/managing-module-views/articles/nextgen-list-view)
- [Canvas Views](https://help.zoho.com/portal/en/kb/crm/customize-crm-account/canvas)


---
# Day 5
## Module 4: Security & Governance

Access control in Zoho CRM answers two fundamental questions:

1. **What data can a user see?** (Roles and Data Sharing)
2. **What can a user do with that data?** (Profiles)

This module covers five components that work together to secure your CRM:

| Component | Primary Purpose |
|-----------|-----------------|
| **Users** | Individual people with login credentials |
| **Roles** | Determine data visibility hierarchy |
| **Profiles** | Determine action permissions |
| **Data Sharing Rules** | Create exceptions to role visibility |
| **Record Locking Rules** | Prevent editing of specific records |


## 4.1 Users
Users are the individuals with login credentials to the CRM. Access is governed by licensing.

Users are individual people who access Zoho CRM with their own credentials. Each user has:
- Unique login email address
- Assigned Role (determines data visibility)
- Assigned Profile (determines permissions)
- Personal settings and preferences

### User Properties

| Property | Description |
|----------|-------------|
| **Email** | Login credential (unique identifier) |
| **First/Last Name** | Display name |
| **Role** | Position in data visibility hierarchy |
| **Profile** | Permission set assigned |
| **Status** | Active, Inactive, or Not Confirmed |
| **Language/Timezone** | Personal locale settings |


### Further Reading

- [Managing Users](https://help.zoho.com/portal/en/kb/crm/users-and-control/users)
- [Adding Users](https://help.zoho.com/portal/en/kb/crm/users-and-control/users/articles/adding-users)
- [User Licenses](https://help.zoho.com/portal/en/kb/crm/users-and-control/users/articles/user-licenses)



## 4.2 Roles
Roles define the Data Visibility Hierarchy. They answer the question: "Who reports to whom?". The role of a user determines "Which records can this user see?"
- Hierarchy Logic: A user can see their own data and the data of users below them in the hierarchy. They cannot see data owned by users at the same level (peers) or above them, assuming the organization default is set to Private.25
- Example: The "VP of Sales" Role can view data from "Regional Managers," who can in turn view data from "Sales Reps."

### The Role Hierarchy Concept

Roles are arranged in a tree structure. Users in higher roles can see data owned by users in lower roles.

```
                    CEO
                     |
          +----------+----------+
          |                     |
    Sales Director        Service Director
          |                     |
    +-----+-----+         +-----+-----+
    |           |         |           |
Sales Manager  Sales Manager  Service Manager
    |           |               |
Sales Rep    Sales Rep    Service Rep
```

### How Role Visibility Works

| User Role | Can See Records Owned By |
|-----------|-------------------------|
| CEO | Everyone in organization |
| Sales Director | Sales Managers, Sales Reps |
| Sales Manager | Sales Reps under them |
| Sales Rep | Only their own records |

**Key Principle**: You can always see:
- Records you own
- Records owned by users below you in the role hierarchy

### Role vs Organizational Hierarchy

**Important**: The CRM role hierarchy does not have to match your organizational chart.

- **Role hierarchy** = CRM data visibility
- **Reporting Manager** = HR/organizational reporting

You can configure these independently based on data access needs.

### Creating the Role Hierarchy

1. Go to **Setup** > **Users and Control** > **Security Control** > **Roles**
2. You will see the default "CEO" role at the top
3. To add roles:
   - Click **+ New Role**
   - Enter role name
   - Select "Reports To" (parent role)
   - Configure "Share Data with Peers" setting
4. Arrange roles in hierarchy from top to bottom

### Share Data with Peers

This setting controls whether users at the same role level can see each other's records:

| Setting | Behavior | When to Use |
|---------|----------|-------------|
| **Enabled** | All users in this role see each other's records | Collaborative teams |
| **Disabled** | Each user sees only their own records | Competitive teams, privacy |

**Example**:
- Enable for Support Team (collaboration needed)
- Disable for Sales Reps (individual territories)

### Designing an Effective Role Hierarchy

**Step 1**: Identify data visibility requirements
- Who needs to see all data?
- Who should only see their own data?
- Who needs to see their team's data?

**Step 2**: Map to organizational structure
- Start with top executives (full visibility)
- Add management layers
- Add individual contributors at bottom

**Step 3**: Determine peer sharing needs
- Should peers collaborate or compete?
- Are there regional or product boundaries?

**Step 4**: Keep it simple
- 3-4 levels is usually sufficient
- Don't create roles for individual users

### Example Role Hierarchy

```
General Manager (sees all)
    |
    +-- Sales Manager (sees sales team)
    |       |
    |       +-- Sales Reps [Peer sharing: OFF]
    |
    +-- Service Manager (sees service team)
            |
            +-- Service Advisors [Peer sharing: ON]
            |
            +-- Technicians [Peer sharing: OFF]
```

### Common Mistakes to Avoid

| Mistake | Why It's Bad | Better Approach |
|---------|--------------|-----------------|
| Flat hierarchy | No data segregation | Design proper levels |
| Too deep hierarchy | Complex, hard to manage | Keep to 3-4 levels |
| Confusing role with profile | Wrong access control | Role = visibility, Profile = permissions |
| Role for each person | Over-engineering | Roles represent job functions |

### Troubleshooting Tips

**Problem**: User can see records they shouldn't
- Check their role position
- Check data sharing rules
- Check peer sharing setting

**Problem**: User can't see records they need
- Check record owner's role
- May need data sharing rule
- Consider role hierarchy adjustment

### Further Reading

- [Organization Roles](https://help.zoho.com/portal/en/kb/crm/users-and-control/security-control/articles/roles)
- [Setting Up Role Hierarchy](https://help.zoho.com/portal/en/kb/crm/users-and-control/security-control/articles/creating-roles)

----------------------------------------------------------------

## 4.3 Profiles

### What Are Profiles?

Profiles define **what actions users can perform**. They answer: "What is this user allowed to do?"
- Permissions: Controls access to modules (Can they see Reports?), actions (Can they Export data? Delete records?), and Setup features (Can they add new fields?)


### The Critical Distinction: Role vs Profile

| Aspect | Role | Profile |
|--------|------|---------|
| **Controls** | Which records user sees | What user can do with records |
| **Structure** | Hierarchical tree | Flat (no inheritance) |
| **Analogy** | Which filing cabinets you can open | What you can do with files inside |


### Standard Profiles

Zoho CRM comes with pre-built profiles:

| Profile | Description |
|---------|-------------|
| **Administrator** | Full access to everything |
| **Standard** | Typical user permissions |
| **Custom profiles** | You create based on needs |

### Creating Custom Profiles

1. Go to **Setup** > **Users and Control** > **Security Control** > **Profiles**
2. Click **+ New Profile**
3. Choose starting point:
   - Clone existing profile, OR
   - Start from scratch
4. Configure permissions:
   - Set module permissions
   - Set field permissions
   - Set feature permissions
5. Save the profile


## 4.4 Data Sharing Rules
Data sharing rules create **exceptions** to the default role-based visibility. They allow you to share records beyond the normal hierarchy.

### Why Need Sharing Rules?

Role hierarchy works for standard reporting structures, but organizations have complex needs:

| Scenario | Role Hierarchy Alone | With Sharing Rules |
|----------|---------------------|-------------------|
| Cross-functional teams | Cannot see each other's data | Share specific records |
| Manager covering for colleague | Cannot see peer's data | Share temporarily |
| Executive oversight | May not be in hierarchy | Share all records |
| Special projects | Team spans roles | Share project records |

- Scenario: The "Sales Team A" role cannot see "Sales Team B" data. However, both teams need to see any Account marked "Key Account."
- Configuration: A Sharing Rule is set up to share records where "Type = Key Account" with a group containing both teams.30
- Levels: Access can be granted as Read Only or Read/Write.

## Default Module Sharing Settings

Before creating sharing rules, understand module defaults:

| Default | Meaning |
|---------|---------|
| **Private** | Users see only own records + hierarchy |
| **Public Read Only** | Everyone can view, owner + hierarchy can edit |
| **Public Read/Write** | Everyone can view and edit |

### Types of Sharing Rules

#### Owner-Based Sharing

Share records owned by specific users or roles with others.

```
Share records owned by [Role A] with [Role B]
```

**Example**: Share all records owned by "Sales Reps" with "Support Team"

#### Criteria-Based Sharing

Share records matching specific criteria with users or roles.

```
Share records where [Condition] with [Users/Roles]
```

**Example**: Share all Deals where Amount > $50,000 with "Executive Team"

### Creating Data Sharing Rules

1. Go to **Setup** > **Users and Control** > **Security Control** > **Data Sharing Settings**
2. Set default sharing for each module
3. Click **New Sharing Rule** for a module
4. Configure:
   - Rule Name
   - Sharing Type (Owner-based or Criteria-based)
   - Who to share with
   - Permission level (Read Only or Read/Write)
5. Save

### Example Sharing Rules

**Rule 1: Manager Sees All Open Deals**
```
Type: Criteria-Based
Module: Deals
Criteria: Stage NOT IN ("Closed Won", "Closed Lost")
Share With: Role: Sales Manager
Permission: Read/Write
```

**Rule 2: High-Value Deals to Executive**
```
Type: Criteria-Based
Module: Deals
Criteria: Amount > 100000
Share With: Role: CEO
Permission: Read Only
```

**Rule 3: Support Sees Customer Contacts**
```
Type: Owner-Based
Module: Contacts
Owned By: Role: Sales Reps
Share With: Role: Support Team
Permission: Read Only
```

### Groups for Sharing

Groups are collections of users for sharing purposes:

1. Go to **Setup** > **Users and Control** > **Security Control** > **Groups**
2. Create group with selected users, roles, or other groups
3. Use group as target in sharing rules

### Common Mistakes to Avoid

| Mistake | Why It's Bad | Better Approach |
|---------|--------------|-----------------|
| Too many sharing rules | Complex, performance impact | Use role hierarchy first |
| Sharing everything | Defeats security purpose | Share only what's needed |
| Not testing | Unexpected access gaps | Test from each role's view |
| Forgetting groups | Individual user updates tedious | Create and use groups |

### Troubleshooting Tips

**Problem**: Sharing rule not working
- Check if rule is active
- Verify record matches criteria exactly
- Confirm user's role/group membership

**Problem**: User sees too many records
- Multiple sharing rules may compound
- Check default module settings

### Further Reading
- [Manage Users, Roles, and Permissions](https://help.zoho.com/portal/en/kb/crm/security-control/data-security-types/articles/get-started-manage-user)
- [How to understand the difference between Users, Profiles, Roles and Groups in Zoho CRM](https://www.youtube.com/watch?v=ttZldoXaQUk)
- [How to manage Roles and Groups within Zoho CRM](https://www.youtube.com/watch?v=sGS-mO5PPLw)
- [Data Sharing Rules](https://help.zoho.com/portal/en/kb/crm/users-and-control/security-control/articles/data-sharing-settings)
- [Creating Sharing Rules](https://help.zoho.com/portal/en/kb/crm/users-and-control/security-control/articles/creating-data-sharing-rules)

## 4.5 Record Locking Rules
Record locking rules prevent editing of records based on criteria you define. They enforce "this record is finalized."

**Note**: Record locking is available in Enterprise edition and above.

### Why Lock Records?

| Scenario | Without Locking | With Locking |
|----------|-----------------|--------------|
| Closed deals | Can be reopened/modified | Protected |
| Approved quotes | Changes after approval | Requires new approval |
| Compliance records | Historical data altered | Immutable audit trail |
| Finalized invoices | Amounts changed | Locked for accounting |

### Types of Record Locking

| Type | Description |
|------|-------------|
| **Full Record Lock** | No fields can be edited |
| **Field-Level Lock** | Only specified fields locked |

### Creating Record Locking Rules

1. Go to **Setup** > **Customization** > **Modules and Fields**
2. Select the module
3. Click **Record Locking Configuration**
4. Click **+ New Rule**
5. Configure:
   - Rule Name
   - Criteria (which records to lock)
   - Lock Type (full or field-level)
   - Exceptions (who can still edit)
   - Custom Message
6. Save

### Example Locking Rules

**Rule 1: Lock Closed Deals**
```
Name: Lock Closed Deals
Criteria: Stage IN ("Closed Won", "Closed Lost")
Lock Type: Full Record
Exceptions: Administrator profile
Message: "This deal has been closed and cannot be edited."
```

**Rule 2: Lock Financial Fields After Approval**
```
Name: Lock Approved Amounts
Criteria: Approval_Status = "Approved"
Lock Type: Field-Level
Locked Fields: Amount, Discount, Tax
Exceptions: Finance Manager role
Message: "Financial fields are locked after approval."
```

### Best Practices

| Do | Don't |
|----|-------|
| Always allow admin override | Lock without exceptions |
| Provide clear lock messages | Leave users confused |
| Lock only necessary fields | Lock entire record unnecessarily |
| Test thoroughly | Deploy without testing |

---

## Security Design Framework

### Step-by-Step Security Design

When designing security for your CRM, follow this framework:

**Step 1: Identify User Groups**
- List all types of users who need access
- Group by job function, not individual

**Step 2: Define Data Visibility Needs**
- What data does each group need to see?
- Who should see only their own records?
- Who needs to see team or all records?

**Step 3: Design Role Hierarchy**
- Create hierarchy based on visibility needs
- Higher roles see more data
- Decide peer sharing settings

**Step 4: Define Action Permissions**
- What can each group do? (Create, Edit, Delete)
- What features do they need? (Import, Export)
- What fields should be hidden?

**Step 5: Create Profiles**
- Build profiles for each user group
- Start restrictive, add permissions as needed

**Step 6: Identify Exceptions**
- Are there cross-functional needs?
- Do some records need broader visibility?
- Create data sharing rules for exceptions

**Step 7: Determine Locking Requirements**
- Which records should become immutable?
- What conditions trigger locking?
- Create record locking rules

**Step 8: Document and Test**
- Document all configurations
- Test from each user type's perspective
- Verify edge cases

---

## Exercises

### Exercise 4.1: Conceptual Questions

1. Explain the difference between Roles and Profiles in your own words.

2. A user can see a record but cannot edit it. Which security component(s) could be responsible? List all possibilities.

4. When would you use a Data Sharing Rule instead of adjusting the Role hierarchy?

## Summary

In this module, you learned about the five components of access control:

- **Users**: Individual accounts with credentials, role, and profile assignments

- **Roles**: Hierarchical structure that determines data visibility; users see their own records plus records of users below them

- **Profiles**: Permission sets that define what actions users can take and what fields they can see

- **Data Sharing Rules**: Exceptions to role-based visibility for cross-functional needs (Enterprise+)

- **Record Locking Rules**: Prevent editing of records based on criteria (Enterprise+)

**Key Principle**: Design security by combining Roles (what you see) with Profiles (what you can do).


## Additional Resources

- [Security Control Overview](https://help.zoho.com/portal/en/kb/crm/users-and-control/security-control)
- [Access Control Best Practices](https://help.zoho.com/portal/en/kb/crm/users-and-control)
- [GDPR and Data Security in Zoho CRM](https://www.zoho.com/crm/gdpr.html)

# Day 6
## Module 5: Process Automation

## Learning Objectives

By the end of this module, you will be able to:

- Design and implement Blueprints for process enforcement
- Create Workflows for event-driven automation
- Set up Schedules for time-based batch operations
- Configure Assignment Rules for automatic record routing
- Implement Case Escalation Rules for SLA management
- Build Approval Processes for sign-off workflows
- Use Scoring Rules for lead/contact prioritization
- Understand CommandCenter for cross-module orchestration

---

## Overview

Process Automation is the heart of a productive CRM. It ensures consistency, reduces manual work, and enforces business rules. This module covers eight automation components:

| Component | Purpose | Edition Required |
|-----------|---------|------------------|
| **Blueprints** | Enforce sequential stage-based processes | Professional+ |
| **Workflows** | React to record events with automatic actions | Standard+ |
| **Schedules** | Execute time-based batch operations | Professional+ |
| **Assignment Rules** | Route records to appropriate users | Standard+ |
| **Case Escalation** | Escalate unresolved cases over time | Enterprise+ |
| **Approval Processes** | Require sign-off before proceeding | Standard+ |
| **Scoring Rules** | Calculate priority scores for records | Standard+ |
| **CommandCenter** | Orchestrate cross-module journeys | Enterprise+ |

**Note**: Many automation features require paid editions. Free edition users should understand the concepts for future use.

---

## 5.1 Blueprints

### What Are Blueprints?

Blueprints enforce **sequential processes** by controlling how records move through stages. They ensure that specific conditions are met and data is captured before a record can progress.

Think of Blueprints as:
- A state machine controlling stage transitions
- A gatekeeper ensuring process compliance


### Why Use Blueprints?

| Without Blueprint | With Blueprint |
|-------------------|----------------|
| Users can skip stages | Stages enforced in order |
| Critical data may be missing | Mandatory fields per transition |
| No approval gates | Built-in approval requirements |
| Inconsistent process | Standardized workflow |
| Manual tracking | Automatic progression |

### Blueprint Components

A Blueprint consists of:

#### States (Stages)
- **Entry State**: Starting point
- **Intermediate States**: Process steps
- **Exit States**: Ending points

#### Transitions (Movements between states)
- **From State**: Where the transition starts
- **To State**: Where the transition goes
- **Who Can Execute**: Roles/Profiles allowed
- **Before Requirements**: What must be done first
- **After Actions**: What happens automatically

### Blueprint Example: Sales Process

```
[Qualification] --> [Proposal] --> [Negotiation] --> [Closed Won]
                                        |
                                        +--> [Closed Lost]
```

**Transition: Qualification to Proposal**
- Required Fields: Budget, Decision Maker, Timeline
- Checklist: Needs analysis completed
- Who Can Execute: Sales Reps, Sales Managers

**Transition: Proposal to Negotiation**
- Required Fields: Proposal Sent Date, Proposal Document
- After Action: Create follow-up task for 3 days

**Transition: Negotiation to Closed Won**
- Required Fields: Contract Signed, Payment Terms
- Approval: Manager approval if deal > $50,000
- After Action: Send congratulations email

### Creating a Blueprint

1. Go to **Setup** > **Process Management** > **Blueprint**
2. Click **+ Create Blueprint**
3. Configure basics:
   - Blueprint Name
   - Module (e.g., Deals)
   - Layout
   - Field (the stage field to control)
4. Add States (drag from stage picklist values)
5. Create Transitions (draw arrows between states)
6. Configure each transition:
   - Before Tab: Required fields, checklists
   - During Tab: Approvals
   - After Tab: Field updates, emails, tasks
7. Set transition permissions
8. **Publish** the Blueprint

### Transition Configuration Details

#### Before Tab (Requirements to transition)
| Option | Purpose |
|--------|---------|
| **Mandatory Fields** | Fields that must have values |
| **Checklists** | Items user must confirm |
| **Messages** | Instructions displayed to user |

#### During Tab (Actions during transition)
| Option | Purpose |
|--------|---------|
| **Approvals** | Require sign-off from approvers |
| **Webhooks** | Call external systems |

#### After Tab (Automatic actions post-transition)
| Option | Purpose |
|--------|---------|
| **Field Updates** | Change field values |
| **Email Notifications** | Send emails |
| **Tasks** | Create tasks |
| **Webhooks** | Call external systems |
| **Custom Functions** | Execute Deluge scripts |

### Blueprint Best Practices

| Do | Don't |
|----|-------|
| Keep states to 5-10 maximum | Create too many stages |
| Include exception paths | Force linear-only progression |
| Keep mandatory fields reasonable | Require too much data at once |
| Test all transitions thoroughly | Deploy without testing |
| Document the process | Assume it's self-explanatory |

### Common Mistakes to Avoid

| Mistake | Why It's Bad | Better Approach |
|---------|--------------|-----------------|
| Too many mandatory fields | Users frustrated | Only essential fields |
| No backward transitions | Records get stuck | Allow rework paths |
| Long checklists | Users check without reading | 3-5 items maximum |
| Complex approval chains | Delays progress | Simple approval structure |

### Troubleshooting Tips

**Problem**: Transition not available to user
- Check role/profile permissions for transition
- Verify mandatory fields are visible in their layout
- Check if there's an unmet condition

**Problem**: After-transition action not firing
- Check email configuration
- Verify field update formula
- Check webhook endpoint

### Further Reading

- [Blueprint Overview](https://help.zoho.com/portal/en/kb/crm/process-management/blueprint)
- [Zoho Blueprint Explained For Managers and Business Owners](https://www.youtube.com/watch?v=lCwHpT-7fq0)

-----------------------------

# Day 7 and 8
## 5.2 Workflows

### What Are Workflows?

Workflows are **event-triggered automations** that execute actions when specific conditions are met. Unlike Blueprints (which control stage progression), Workflows react to record events.

Think of Workflows as:
- "When this happens, do that" rules
- Automatic response to changes
- Background automation engine

**Edition Required**: Standard and above (limited workflows in Free)

### Workflow Triggers

| Trigger Type | When It Fires |
|--------------|---------------|
| **On Create** | When record is first saved |
| **On Create or Edit** | Any save operation |
| **On Edit** | Only when existing record modified |
| **On Field Update** | When specific field changes |
| **On Date/Time** | Relative to a date field value |
| **On Delete** | When record is removed |

### Workflow Components

```
WORKFLOW STRUCTURE

1. TRIGGER: What event starts the workflow
   Example: "When a Deal is created"

2. CONDITION: Which records should be affected
   Example: "Where Amount > $10,000"

3. ACTIONS: What happens when triggered
   Example: "Send email to Sales Manager"

4. SCHEDULED ACTIONS: What happens later
   Example: "After 3 days, create follow-up task"
```

### Workflow Execution Flow

```
Record Event Occurs
        |
        v
Workflow Trigger Matched?
        |
   +----+----+
   |         |
   No        Yes
   |         |
 Stop        v
        Conditions Met?
             |
        +----+----+
        |         |
        No        Yes
        |         |
      Stop        v
             Execute Immediate Actions
                  |
                  v
             Schedule Time-Based Actions
```

### Workflow Actions

| Action Type | Description |
|-------------|-------------|
| **Email Notification** | Send templated email |
| **Task** | Create task for a user |
| **Field Update** | Change field value(s) |
| **Tag** | Add or remove tags |
| **Webhook** | Call external URL |
| **Custom Function** | Execute Deluge script |
| **Create Record** | Create record in related module |
| **Convert Lead** | Convert lead to contact/account/deal |

### Example Workflows

**Workflow 1: Welcome Email for New Leads**
```
Trigger: On Lead Create
Condition: Lead Source = "Website"
Immediate Actions:
  - Email: Send "Welcome" template to Lead Email
  - Task: Create "Initial Call" for Lead Owner, due in 1 day
```

**Workflow 2: High-Value Deal Alert**
```
Trigger: On Deal Create or Edit
Condition: Amount > $50,000
Immediate Actions:
  - Email: Notify Sales Manager
  - Field Update: Set Priority = "High"
```

**Workflow 3: Stale Lead Follow-up**
```
Trigger: On Lead Create
Condition: None (all leads)
Scheduled Actions:
  - After 7 days (if Status = "New"):
    - Task: Create "Follow up on inactive lead"
  - After 30 days (if Status = "New"):
    - Field Update: Set Status = "Stale"
```

**Workflow 4: Deal Stage Change Notification**
```
Trigger: On Field Update (Stage)
Condition: Stage = "Proposal Sent"
Immediate Actions:
  - Email: Notify Account Manager
  - Task: Create "Follow up on proposal" due in 5 days
```

### Creating a Workflow

1. Go to **Setup** > **Automation** > **Workflow Rules**
2. Click **+ Create Rule**
3. Select module
4. Configure trigger:
   - When to execute (Create, Edit, Field Update, etc.)
   - On which records (All or conditions)
5. Set conditions (if applicable)
6. Add Instant Actions
7. Add Scheduled Actions (if needed)
8. Save and activate

### Instant vs Scheduled Actions

| Instant Actions | Scheduled Actions |
|-----------------|-------------------|
| Execute immediately | Execute at specified time |
| No delay | Relative to trigger or date field |
| Cannot be cancelled | Can be cancelled if conditions change |
| Use for: notifications, updates | Use for: follow-ups, reminders |

### The "Execute Once" Setting

This important setting controls repeat execution:

| Setting | Behavior |
|---------|----------|
| **Execute Once** | Fires only once per record, ever |
| **Execute Every Time** | Fires each time conditions are met |

**Use Execute Once for**:
- Welcome emails (send only on creation)
- One-time setup tasks
- Initial notifications

**Use Execute Every Time for**:
- Status change notifications
- Field update automations
- Repeated triggers on same record

### Common Mistakes to Avoid

| Mistake | Why It's Bad | Better Approach |
|---------|--------------|-----------------|
| Workflow loops | A triggers B triggers A... | Check for circular dependencies |
| Too many emails | Recipients overwhelmed | Consolidate notifications |
| Not using "Execute Once" | Duplicate actions | Set appropriately |
| Missing null checks | Errors on empty fields | Add "is not empty" conditions |
| No testing | Broken in production | Test with sample records |

### Troubleshooting Tips

**Problem**: Workflow not triggering
- Check if rule is active
- Verify record meets ALL conditions
- Check trigger type (Create vs Edit)
- Check "Execute Once" setting

**Problem**: Email not sending
- Check recipient field has value
- Verify email address is valid
- Check daily email limits
- Verify template exists

**Problem**: Scheduled action not executing
- Check if date field has value
- Verify date hasn't passed already
- Check time zone settings

### Further Reading

- [Workflow Rules](https://help.zoho.com/portal/en/kb/crm/automate-business-processes/workflow-management)
- [Workflow Rules & Automation](https://www.youtube.com/watch?v=yg_ECYi4sRg)

---


## 5.3 Schedules

### What Are Schedules?

Schedules are **time-based automations** that run at fixed intervals, independent of record events. They are for batch operations and periodic tasks.

**Edition Required**: Professional and above

### Schedules vs Workflows

| Aspect | Workflow | Schedule |
|--------|----------|----------|
| **Trigger** | Record event | Clock/Calendar |
| **Scope** | Single record | Multiple records |
| **Timing** | Immediate or relative | Fixed schedule |
| **Use Case** | React to changes | Periodic operations |

### Schedule Types

| Frequency | Description |
|-----------|-------------|
| **Daily** | Runs at specified time each day |
| **Weekly** | Runs on specified days at set time |
| **Monthly** | Runs on specified date at set time |
| **Yearly** | Runs on specified date annually |

### What Schedules Can Do

Schedules execute Custom Functions (Deluge scripts) that can:
- Query multiple records
- Send batch emails
- Generate reports
- Update records in bulk
- Call external APIs
- Perform data cleanup

### Example Schedule Use Cases

**Daily: Send Pending Approvals Summary**
```
Frequency: Daily at 8:00 AM
Logic:
  - Query deals pending approval > 2 days
  - Build summary report
  - Email to Sales Manager
```

**Weekly: Performance Report**
```
Frequency: Monday at 7:00 AM
Logic:
  - Query closed deals from last week
  - Calculate metrics (total, average, by rep)
  - Send report to executives
```

**Monthly: Data Cleanup**
```
Frequency: 1st of month at 2:00 AM
Logic:
  - Find leads with no activity > 90 days
  - Update status to "Inactive"
  - Notify marketing team
```

### Creating a Schedule

1. Go to **Setup** > **Automation** > **Schedules**
2. Click **+ Create Schedule**
3. Configure:
   - Schedule Name
   - Frequency (Daily, Weekly, Monthly)
   - Time
   - Timezone
4. Create or select Custom Function
5. Save and activate

### Best Practices

| Do | Don't |
|----|-------|
| Run during off-hours | Schedule at peak times |
| Handle errors gracefully | Let errors go unnoticed |
| Batch operations | Process records one at a time |
| Test functions first | Deploy untested code |
| Monitor execution | Assume it's working |

### Further Reading

- [Creating Schedules in Automation](https://help.zoho.com/portal/en/kb/crm/automate-business-processes/schedules/articles/custom-schedules)

---

## 5.4 Assignment Rules

### What Are Assignment Rules?

Assignment Rules automatically set record ownership based on criteria. They route leads, deals, or other records to the right person automatically.

**Edition Required**: Standard and above

### Why Use Assignment Rules?

| Without Assignment Rules | With Assignment Rules |
|-------------------------|----------------------|
| Manual assignment | Automatic routing |
| Delayed response | Immediate assignment |
| Uneven distribution | Balanced workload |
| Missed leads | Every lead handled |

### Assignment Methods

| Method | Description |
|--------|-------------|
| **Specific User** | Always assign to one person |
| **Round Robin** | Rotate among users evenly |
| **Load Balanced** | Consider current workload |

### Creating Assignment Rules

1. Go to **Setup** > **Automation** > **Assignment Rules**
2. Select module
3. Click **+ New Rule**
4. Configure rule entries (in priority order):
   - Condition
   - Assign To (user or round robin)
5. Save

### Assignment Rule Structure

```
RULE 1: Enterprise Leads
  Condition: Annual Revenue > $1M
  Assign To: Senior Sales Rep

RULE 2: West Region
  Condition: State IN (CA, OR, WA)
  Assign To: Round Robin - West Team

RULE 3: East Region
  Condition: State IN (NY, NJ, MA)
  Assign To: Round Robin - East Team

RULE 4: Default
  Condition: All others
  Assign To: Round Robin - General Pool
```

### Assignment Thresholds

Prevent overwhelming users with a maximum record limit:

```
Threshold Configuration:
  Maximum Records: 10
  Count Records Where: Status = "Open"
  
When user reaches threshold:
  - Skip to next user in round robin
  - If all users at threshold: Goes to queue
```

### Common Mistakes to Avoid

| Mistake | Why It's Bad | Better Approach |
|---------|--------------|-----------------|
| No default rule | Some records unassigned | Always have catch-all |
| Wrong rule order | Wrong rule matches first | Most specific rules first |
| Inactive users in list | Assignment failures | Audit user lists regularly |
| No threshold | Users overwhelmed | Set reasonable limits |

### Further Reading

- [Assignment Rules](https://help.zoho.com/portal/en/kb/crm/automate-business-processes/assignment-rules/articles/set-assignment-rules)


---

## 5.5 Case Escalation Rules

### What Are Case Escalation Rules?

Case Escalation Rules automatically escalate records based on time conditions. If a record is not handled within defined timeframes, it gets escalated.

**Edition Required**: Enterprise and above

### Why Use Escalation Rules?

Escalation rules help ensure SLA compliance:

| Without Escalation | With Escalation |
|-------------------|-----------------|
| Cases forgotten | Automatic reminders |
| SLAs breached silently | Alerts before breach |
| No accountability | Clear escalation path |
| Customer frustration | Timely response |

### Escalation Rule Components

```
ESCALATION RULE STRUCTURE

Apply To: Records matching criteria
Business Hours: Define working hours

Escalation Levels:
  Level 1: After X hours
    - Actions: Email, Task, Field Update
  
  Level 2: After Y hours
    - Actions: Email Manager, Reassign
  
  Level 3: After Z hours
    - Actions: Email Executive, High Priority
```

### Example Escalation Rule

**Rule: Support Case Escalation**
```
Apply To: Cases where Status != "Resolved"
Business Hours: Mon-Fri, 9 AM - 6 PM

Level 1 (4 business hours):
  - Email: Alert assigned agent
  - Task: "Urgent - Case needs attention"

Level 2 (8 business hours):
  - Email: Alert Support Manager
  - Field Update: Priority = "High"

Level 3 (24 business hours):
  - Email: Alert Director of Support
  - Task: "Critical escalation - immediate action required"
```

### Creating Escalation Rules

1. Go to **Setup** > **Automation** > **Case Escalation Rules**
2. Click **+ New Rule**
3. Define criteria (which records to escalate)
4. Set business hours
5. Configure escalation levels:
   - Time threshold
   - Actions at each level
6. Save and activate

### Business Hours Configuration

Escalation timers can count:
- **Calendar Hours**: 24/7 counting
- **Business Hours**: Only during defined work hours

Configure business hours in Setup to match your actual support availability.

### Further Reading

- [Case Escalation Rules](https://help.zoho.com/portal/en/kb/crm/automate-business-processes/case-escalation-rules/articles/set-case-escalation-rules)

---

## 5.6 Approval Processes

### What Are Approval Processes?

Approval Processes require designated approvers to review and approve records before certain actions can proceed.

**Edition Required**: Standard and above

### Why Use Approval Processes?

| Scenario | Why Approval Needed |
|----------|---------------------|
| Discounts over threshold | Financial control |
| High-value deals | Executive oversight |
| Contract modifications | Legal review |
| Expense submissions | Budget approval |

### Approval Process Components

```
APPROVAL PROCESS STRUCTURE

Entry Criteria: When to trigger approval
  Example: Discount > 20%

Approvers: Who must approve
  - Specific user
  - Manager of record owner
  - Role-based (Sales Manager)

Actions:
  - On Approval: What happens if approved
  - On Rejection: What happens if rejected
  - On Delegation: Allow reassigning approval
```

### Example Approval Process

**Process: High Discount Approval**
```
Entry Criteria:
  - Module: Deals
  - Condition: Discount Percent > 15%

Approval Path:
  1. Direct Manager of Deal Owner
  2. If Discount > 25%: Also requires Sales Director

On Approval:
  - Field Update: Discount_Approved = true
  - Email: Notify Sales Rep

On Rejection:
  - Field Update: Discount = 0
  - Email: Rejection notice with reason
```

### Creating an Approval Process

1. Go to **Setup** > **Automation** > **Approval Processes**
2. Click **+ Create Process**
3. Select module
4. Set entry criteria
5. Configure approval path:
   - Approver(s)
   - Approval/Rejection actions
   - Delegation settings
6. Save and activate

### Approval Actions

| Action Type | Options |
|-------------|---------|
| **On Approval** | Field update, email, task, webhook |
| **On Rejection** | Field update, email, task |
| **On Delegation** | Email new approver |

### Best Practices

| Do | Don't |
|----|-------|
| Keep approval chains short | Create complex multi-level approvals |
| Set clear criteria | Make criteria too broad |
| Notify on completion | Leave submitter wondering |
| Allow delegation | Require single person always |

### Further Reading

- [Approval Processes](https://help.zoho.com/portal/en/kb/crm/automation/approval-processes)
- [Creating Approval Processes](https://help.zoho.com/portal/en/kb/crm/automation/approval-processes/articles/creating-approval-processes)

---

## 5.7 Scoring Rules

### What Are Scoring Rules?

Scoring Rules automatically calculate a score for records based on field values, behaviors, and engagement. This helps prioritize which records deserve attention.

**Edition Required**: Standard and above

### Why Use Scoring?

| Without Scoring | With Scoring |
|-----------------|--------------|
| All leads treated equally | Focus on hot leads |
| Manual prioritization | Automatic ranking |
| Subjective assessment | Data-driven evaluation |
| Missed opportunities | Best leads identified |

### Scoring Components

```
SCORING RULE STRUCTURE

Positive Criteria (add points):
  - Field conditions that indicate quality
  - Engagement signals
  
Negative Criteria (subtract points):
  - Warning signs
  - Disqualifying factors
  
Score Field: Where score is stored
Score Ranges: Categories based on score
```

### Example Lead Scoring

**Positive Criteria**:
| Criteria | Points |
|----------|--------|
| Industry = "Technology" | +15 |
| Company Size > 100 employees | +10 |
| Job Title contains "Director" | +10 |
| Downloaded whitepaper | +20 |
| Visited pricing page | +25 |
| Attended webinar | +15 |

**Negative Criteria**:
| Criteria | Points |
|----------|--------|
| Email bounced | -20 |
| Competitor domain | -50 |
| No activity in 30 days | -10 |
| Unsubscribed from emails | -15 |

**Score Ranges**:
| Range | Category |
|-------|----------|
| 0-25 | Cold |
| 26-50 | Warm |
| 51-75 | Hot |
| 76+ | Very Hot |

### Creating Scoring Rules

1. Go to **Setup** > **Automation** > **Scoring Rules**
2. Click **+ Create Rule**
3. Select module
4. Add positive criteria with point values
5. Add negative criteria with point values
6. Save and activate

### Using Scores

Once scoring is active:
- Create Views filtered by score
- Build dashboards showing score distribution
- Set Workflows triggered by score thresholds
- Prioritize follow-up based on score

### Best Practices

| Do | Don't |
|----|-------|
| Start simple, refine over time | Create complex scoring immediately |
| Validate with sales team | Assume you know what matters |
| Review and adjust regularly | Set and forget |
| Consider negative indicators | Only score positively |

### Further Reading

- [Scoring Rules](https://help.zoho.com/portal/en/kb/crm/automation/scoring-rules)
- [Creating Scoring Rules](https://help.zoho.com/portal/en/kb/crm/automation/scoring-rules/articles/creating-scoring-rules)

---

## 5.8 CommandCenter

### What Is CommandCenter?

CommandCenter orchestrates **complex, multi-module processes** that span across different stages and modules. While Blueprint handles single-module progression, CommandCenter handles interconnected journeys.

**Edition Required**: Enterprise and above

### When to Use CommandCenter

| Scenario | Blueprint | CommandCenter |
|----------|-----------|---------------|
| Single record, multiple stages | Yes | Overkill |
| Multiple modules involved | No | Yes |
| Customer journey across touchpoints | No | Yes |
| Complex branching across systems | No | Yes |

### CommandCenter Components

```
COMMANDCENTER STRUCTURE

Journey: The overall process
  |
  +-- States: Major phases of the journey
  |     |
  |     +-- Entry Criteria: How records enter this state
  |     +-- Actions: What happens in this state
  |     +-- Exit Criteria: How records leave this state
  |
  +-- Transitions: Movement between states
  |
  +-- Signals: Events that trigger transitions
```

### Example Customer Journey

```
[Welcome] --> [Onboarding] --> [Active] --> [Renewal]
                                   |
                                   +--> [At Risk] --> [Churned]
                                           |
                                           +--> [Recovered] --> [Active]
```

**Welcome State**:
- Entry: New contact created
- Actions: Send welcome email, create onboarding task
- Wait: 7 days
- Exit: Move to Onboarding

**At Risk State**:
- Entry: No activity for 30 days
- Actions: Alert Customer Success, send re-engagement email
- Monitor: Activity or response
- Exit: If activity, move to Recovered; if none after 14 days, move to Churned

### Creating a CommandCenter Journey

1. Go to **Setup** > **Process Management** > **CommandCenter**
2. Click **+ Create Journey**
3. Define journey basics
4. Add states and configure:
   - Entry criteria
   - Actions
   - Wait conditions
   - Exit criteria
5. Connect states with transitions
6. Configure signals for transitions
7. Publish

### CommandCenter vs Blueprint Summary

| Feature | Blueprint | CommandCenter |
|---------|-----------|---------------|
| Scope | Single module | Multiple modules |
| Complexity | Stage progression | Full customer journey |
| Transitions | User-initiated | System or user |
| Wait logic | None | Built-in |
| Ideal for | Sales process | Customer lifecycle |



## Automation Decision Framework

Use this framework to choose the right automation:

```
DECISION TREE: WHICH AUTOMATION TO USE?

Q: Do you need to enforce a sequence of stages?
  - Yes: Use BLUEPRINT
  - No: Continue...

Q: Should actions happen based on a record event?
  - Yes: Use WORKFLOW
  - No: Continue...

Q: Should actions happen at a scheduled time?
  - Yes: Use SCHEDULE
  - No: Continue...

Q: Do you need records automatically routed?
  - Yes: Use ASSIGNMENT RULES
  - No: Continue...

Q: Do you need time-based escalation?
  - Yes: Use ESCALATION RULES
  - No: Continue...

Q: Do you need sign-off before proceeding?
  - Yes: Use APPROVAL PROCESS
  - No: Continue...

Q: Do you need to prioritize records by criteria?
  - Yes: Use SCORING RULES
  - No: Continue...

Q: Is this a complex multi-module journey?
  - Yes: Use COMMANDCENTER
  - No: May not need automation
```

---

## Exercises

### Exercise 5.1: Conceptual Questions

1. What is the key difference between a Blueprint and a Workflow?

2. When would you use a Schedule instead of a Workflow?

3. Explain the difference between "Execute Once" and "Execute Every Time" in Workflows.

4. Why would you use Case Escalation Rules instead of just creating workflows with time-based actions?

5. What type of automation would you use to automatically assign leads based on their geographic region?

### Exercise 5.2: Workflow Design

Design workflows for these scenarios:

**Scenario A**: When a new lead is created from the website (Lead Source = "Website"), send a welcome email and create a task for the lead owner to call within 24 hours.

Document:
- Trigger
- Conditions
- Instant Actions
- Scheduled Actions (if any)

**Scenario B**: When a deal stage changes to "Negotiation," notify the sales manager and update a custom field "Negotiation Start Date" to today's date.

Document:
- Trigger
- Conditions
- Instant Actions

**Scenario C**: If a lead has status "New" for more than 7 days, update their status to "Stale" and send an alert to the lead owner.

Document:
- Trigger
- Conditions
- Scheduled Actions

### Exercise 5.3: Blueprint Design

Design a Blueprint for a deal process with these requirements:

**Stages**:
1. Qualification
2. Needs Analysis
3. Proposal
4. Negotiation
5. Closed Won
6. Closed Lost

**Requirements**:
- From Qualification to Needs Analysis: Require Budget field
- From Needs Analysis to Proposal: Require Decision Maker field
- From Proposal to Negotiation: Require Proposal Sent Date field
- From Negotiation to Closed Won: Require Contract Date, require manager approval if Amount > $50,000
- Can go from any stage to Closed Lost (requires Loss Reason)

Document:
- All transitions
- Required fields for each transition
- Any approvals needed
- After-transition actions

### Exercise 5.4: Scoring Rule Design

Design a lead scoring system for a B2B software company:

1. Identify 5 positive criteria (field values or behaviors that indicate a good lead)
2. Assign point values to each
3. Identify 3 negative criteria (warning signs)
4. Assign negative point values
5. Define score ranges and what they mean

### Exercise 5.5: Hands-On - Create a Workflow (Free Edition)

**Note**: Free edition has limited workflow capabilities. Try creating a basic workflow:

1. Go to **Setup** > **Automation** > **Workflow Rules**
2. Create a new workflow for the Leads module
3. Configure:
   - Trigger: On Lead Create
   - Condition: Lead Source = "Web" (or any value you choose)
   - Action: Create Task "Follow up on new lead" for Lead Owner
4. Save and test by creating a lead that matches the condition

### Exercise 5.6: Scenario Planning

For each scenario, identify which automation component(s) you would use:

1. Every Monday, send a report of all open deals to the sales team
2. When a contact's email bounces, mark them as "Bad Email"
3. Route support cases to different teams based on product type
4. Ensure deals cannot be marked as won without a signed contract
5. Alert management if a support case is open for more than 48 hours
6. Calculate a priority score for leads based on company size and industry
7. Require VP approval for any discount over 30%
8. Track a customer's journey from first contact through renewal

---

## Knowledge Check

Before moving to the next module, ensure you can answer:

1. What is the difference between event-driven and state-driven automation?

2. What are the three types of actions available in workflows?

3. When would you use a Schedule instead of a workflow with scheduled actions?

4. How do Assignment Rules determine who receives a record?

5. What is the purpose of Scoring Rules?

---

## Summary

In this module, you learned about eight process automation components:

- **Blueprints**: Enforce sequential stage-based processes with validation and required data
- **Workflows**: React to record events with automatic actions
- **Schedules**: Execute batch operations at scheduled times
- **Assignment Rules**: Automatically route records to appropriate users
- **Case Escalation**: Escalate records that aren't addressed in time
- **Approval Processes**: Require sign-off before proceeding
- **Scoring Rules**: Calculate priority scores for records
- **CommandCenter**: Orchestrate complex multi-module journeys

**Key Principle**: Choose the right automation for the job. Blueprints enforce process, Workflows react to events, Schedules handle batch operations.

---

## Next Steps

Now that you understand process automation, the next module covers Actions - the execution layer that makes automation work.

<!-- Proceed to [Module 6: Actions - The Execution Layer](./06-Actions.md) -->

---

## Additional Resources

- [Automation Overview](https://help.zoho.com/portal/en/kb/crm/automation)
- [Workflow Best Practices](https://help.zoho.com/portal/en/kb/crm/automation/workflow-rules/articles/workflow-best-practices)
- [Blueprint Best Practices](https://help.zoho.com/portal/en/kb/crm/automation/blueprint/articles/blueprint-best-practices)

# Day 9
## Module 6: Actions - The Execution Layer

## Learning Objectives

By the end of this module, you will be able to:

- Understand the different types of actions available in Zoho CRM
- Configure email notifications with templates and merge fields
- Create tasks and events automatically
- Use field updates for data manipulation
- Implement webhooks for external integration
- Write basic custom functions

---

## Overview

Actions are the "verbs" of Zoho CRM automation. When a workflow triggers, a blueprint transition completes, or a schedule runs, it is the **Actions** that actually do the work.

This module covers the execution layer - what happens when automation fires.

---

## 6.1 Understanding Actions

### What Are Actions?

Actions are the operations that execute when automations run. They are the practical outcomes of your automation rules.

### Types of Actions

| Action Type | Description | Available In |
|-------------|-------------|--------------|
| **Email Notification** | Send templated email | Workflows, Blueprints |
| **Task** | Create task for user | Workflows, Blueprints |
| **Field Update** | Change field values | Workflows, Blueprints |
| **Tag** | Add/remove tags | Workflows |
| **Webhook** | Call external URL | Workflows, Blueprints |
| **Custom Function** | Execute Deluge script | Workflows, Blueprints, Schedules |
| **Create Record** | Create related record | Workflows |
| **Convert** | Convert lead | Workflows (Leads only) |
| **Send Notification** | In-app notification | Workflows |

### Action Execution Order

When multiple actions are configured, they execute in this order:

```
1. Field Updates (instant)
2. Email Notifications
3. Tasks
4. Webhooks
5. Custom Functions
6. Other actions
```

---

## 6.2 Email Notifications

### What Are Email Notifications?

Email notifications send automated emails when triggered. They use templates with merge fields to personalize content.

### Email Notification Components

| Component | Description |
|-----------|-------------|
| **Template** | Pre-defined email content |
| **From** | Sender address |
| **To** | Recipient(s) |
| **Subject** | Email subject line |
| **Message** | Email body |
| **Merge Fields** | Dynamic placeholders |

### Creating Email Templates

1. Go to **Setup** > **Customization** > **Templates** > **Email Templates**
2. Click **+ New Template**
3. Select module
4. Design template:
   - Enter subject line with merge fields
   - Compose message body
   - Insert merge fields
   - Format with HTML editor
5. Save

### Merge Fields

Merge fields pull data from records into emails:

```
Dear ${Leads.First Name},

Thank you for your interest in ${Products.Product Name}.

Your dedicated representative is ${Leads.Owner.First Name}.

Best regards,
The Sales Team
```

**Common Merge Fields**:
- `${Module.Field Name}` - Field from triggering record
- `${Module.Owner.First Name}` - Related user fields
- `${Module.Lookup.Field}` - Fields from related records
- `${User.First Name}` - Current user info
- `${Organization.Company Name}` - Organization info

### Email Notification Settings

When adding email action to workflow:

| Setting | Options |
|---------|---------|
| **From** | Current user, Record owner, Specific email |
| **To** | Record field, Specific email, User, Multiple |
| **Template** | Select from created templates |
| **Attachments** | Include file field attachments |

### Example Email Notifications

**Welcome Email for New Leads**:
```
Subject: Welcome to ${Organization.Company Name}

Body:
Dear ${Leads.First Name},

Thank you for reaching out to us. We're excited to learn more 
about your needs.

A member of our team will contact you within 24 hours at 
${Leads.Phone}.

Best regards,
${Leads.Owner.First Name} ${Leads.Owner.Last Name}
```

**Deal Stage Update**:
```
Subject: Deal "${Deals.Deal Name}" moved to ${Deals.Stage}

Body:
Hi ${Deals.Owner.First Name},

The deal "${Deals.Deal Name}" has been updated:
- Account: ${Deals.Account Name.Account Name}
- Amount: ${Deals.Amount}
- New Stage: ${Deals.Stage}
- Close Date: ${Deals.Closing Date}

Please take appropriate action.
```

### Best Practices for Emails

| Do | Don't |
|----|-------|
| Keep subject lines clear | Use vague subjects |
| Use merge fields for personalization | Send generic messages |
| Test templates before activating | Deploy without testing |
| Include unsubscribe option (marketing) | Ignore compliance |
| Keep messages concise | Write long emails |

### Troubleshooting Email Issues

**Problem**: Email not sending
- Check recipient field has valid email
- Verify daily email limit not reached
- Check spam filters on recipient side

**Problem**: Merge fields showing blank
- Verify field API name is correct
- Check if field has data

**Problem**: Formatting looks wrong
- Test in multiple email clients
- Use simple HTML formatting

### Further Reading

- [Customizing Templates](https://help.zoho.com/portal/en/kb/crm/customize-crm-account/customizing-templates)


---

## 6.3 Tasks

### What Are Task Actions?

Task actions automatically create tasks for users when automations trigger. Tasks appear in the user's task list and can have due dates, priorities, and associations.

### Task Action Configuration

| Setting | Description |
|---------|-------------|
| **Task Name** | What the task is called |
| **Due Date** | When the task is due |
| **Assign To** | Who should complete it |
| **Priority** | High, Medium, Low |
| **Status** | Initial status |
| **Description** | Task details |
| **Associate With** | Link to triggering record |

### Due Date Options

| Option | Example |
|--------|---------|
| **After X days** | Due 3 days from trigger |
| **After X hours** | Due 4 hours from trigger |
| **Specific date field** | Due on Close Date |
| **Specific date** | Due on specific calendar date |

### Example Task Configurations

**Follow-up Task on New Lead**:
```
Task Name: Follow up with new lead - ${Leads.First Name}
Due Date: After 1 day
Assign To: Record Owner
Priority: High
Status: Not Started
Description: Call ${Leads.First Name} at ${Leads.Phone} 
             to qualify the lead.
Associate With: Lead Record
```

**Proposal Follow-up**:
```
Task Name: Follow up on proposal - ${Deals.Deal Name}
Due Date: After 5 days
Assign To: Deal Owner
Priority: Medium
Description: Check if customer has reviewed proposal.
             Deal Amount: ${Deals.Amount}
             Contact: ${Deals.Contact Name.Full Name}
```

### Best Practices

| Do | Don't |
|----|-------|
| Set realistic due dates | Create tasks due immediately |
| Include useful context | Create vague tasks |
| Assign to specific user | Leave unassigned |
| Use merge fields in description | Write generic descriptions |

---

## 6.4 Field Updates

### What Are Field Updates?

Field Update actions automatically change field values when triggered. They can set fixed values, calculate values, or copy from other fields.

### Field Update Options

| Option | Description | Example |
|--------|-------------|---------|
| **Fixed Value** | Set to specific value | Status = "Contacted" |
| **Empty** | Clear the field | Clear Follow_Up_Date |
| **Current Date** | Today's date | Set Modified_Date |
| **Current Time** | Current timestamp | Set Last_Activity |
| **Current User** | Logged-in user | Set Processed_By |
| **Formula** | Calculate value | Set Tax = Amount * 0.1 |
| **Field Value** | Copy another field | Set Backup = Primary |

### Example Field Updates

**Set Status on Create**:
```
Field: Status
Value: "New"
```

**Record Contact Timestamp**:
```
Field: Last_Contacted
Value: Current Date/Time
```

**Calculate Tax**:
```
Field: Tax_Amount
Formula: ${Amount} * 0.18
```

**Copy Email from Contact**:
```
Field: Backup_Email
Value: ${Contact_Name.Email}
```

**Set SLA Deadline**:
```
Field: SLA_Deadline
Formula: ${Created_Time} + 48 hours
```

### Field Update Best Practices

| Do | Don't |
|----|-------|
| Document what triggers updates | Create unexplained changes |
| Test formulas thoroughly | Use complex untested formulas |
| Consider impact on other automations | Ignore cascade effects |
| Use for calculated fields | Overuse for user-editable fields |

### Common Use Cases

| Use Case | Field Update |
|----------|--------------|
| Timestamp changes | Set Last_Modified = Current Time |
| Default values | Set Priority = "Medium" |
| Calculated totals | Set Total = Subtotal + Tax |
| Status progression | Set Stage = "Completed" |
| Copy related data | Set Account_Email = Account.Email |

### Troubleshooting

**Problem**: Field not updating
- Check workflow conditions
- Verify field is not locked
- Check formula syntax

**Problem**: Wrong value calculated
- Test formula in formula field first
- Check field API names
- Handle null values


---

## 6.5 Tags

### What Are Tag Actions?

Tag actions add or remove tags from records. Tags are labels for flexible categorization.

### Tag Action Types

| Action | Description |
|--------|-------------|
| **Add Tag** | Attach specified tag to record |
| **Remove Tag** | Remove specified tag from record |

### Example Tag Configurations

**Tag High-Value Leads**:
```
Trigger: Lead Created
Condition: Annual Revenue > $1M
Action: Add Tag "High Value"
```

**Tag Inactive Contacts**:
```
Trigger: 30 days after Last Activity
Condition: No recent activity
Action: Add Tag "Inactive"
```

**Remove Tag on Activity**:
```
Trigger: Activity logged
Action: Remove Tag "Inactive"
```

### Using Tags Effectively

| Use Case | Tag |
|----------|-----|
| Priority marking | "VIP", "Hot Lead", "Urgent" |
| Status tracking | "Needs Review", "Follow Up" |
| Segmentation | "Enterprise", "SMB", "Startup" |
| Process flags | "Onboarding", "Renewal Due" |

### Best Practices

| Do | Don't |
|----|-------|
| Use consistent naming | Create variations |
| Limit total tags | Create hundreds |
| Document tag meanings | Assume everyone knows |
| Review and clean up | Let tags accumulate |


---

# Day 10 and 11
## 6.6 Webhooks

### What Are Webhooks?

Webhooks call external URLs when triggered, allowing Zoho CRM to communicate with other systems.

### How Webhooks Work

```
Workflow Triggers
      |
      v
Webhook Action
      |
      v
HTTP Request to External URL
      |
      v
External System Receives Data
      |
      v
(Optional) Response Handled
```

### Webhook Configuration

| Setting | Description |
|---------|-------------|
| **URL** | External endpoint to call |
| **Method** | GET or POST |
| **Parameters** | Data to send |
| **Headers** | HTTP headers (auth, content-type) |

### Webhook Parameters

You can include record data in webhooks:

```
URL: https://api.example.com/crm-webhook

Parameters:
- lead_id = ${Leads.Lead Id}
- name = ${Leads.Full Name}
- email = ${Leads.Email}
- source = ${Leads.Lead Source}
```

### Example Webhook Use Cases

| Use Case | External System |
|----------|-----------------|
| Send SMS on deal won | SMS gateway |
| Create ticket in support system | Help desk API |
| Update inventory on sale | ERP system |
| Notify Slack channel | Slack webhook |
| Log event in analytics | Analytics platform |

### Example Webhook Configuration

**Notify Slack on High-Value Deal**:
```
URL: https://hooks.slack.com/services/xxx/yyy/zzz
Method: POST
Content-Type: application/json

Body:
{
  "text": "New high-value deal created!",
  "attachments": [{
    "fields": [
      {"title": "Deal", "value": "${Deals.Deal Name}"},
      {"title": "Amount", "value": "${Deals.Amount}"},
      {"title": "Account", "value": "${Deals.Account Name}"}
    ]
  }]
}
```

### Best Practices

| Do | Don't |
|----|-------|
| Test endpoints first | Point to untested URLs |
| Handle errors gracefully | Ignore failures |
| Use HTTPS | Send sensitive data over HTTP |
| Document integrations | Create undocumented webhooks |
| Consider rate limits | Overwhelm external systems |

### Troubleshooting

**Problem**: Webhook not firing
- Check workflow conditions
- Verify URL is accessible
- Check for timeout

**Problem**: External system not receiving data
- Verify URL is correct
- Check parameters are mapped
- Review external system logs

### Further Reading

- [Webhooks](https://help.zoho.com/portal/en/kb/crm/automate-business-processes/actions/articles/webhooks-workflow)
- [Creating Webhooks ](https://help.zoho.com/portal/en/kb/crm/help-videos/articles/actions-webhooks#Creating_Webhooks)

---



## 6.8 Other Actions

### Create Record

Automatically create records in related modules:

```
Trigger: Deal Closed Won
Action: Create Record in "Invoices"
  - Customer = ${Deals.Account Name}
  - Amount = ${Deals.Amount}
  - Due Date = Today + 30 days
```

### Convert Lead

Available only for Leads module:

```
Trigger: Lead Score > 80
Action: Convert Lead
  - Create Contact: Yes
  - Create Account: Yes
  - Create Deal: Optional
```

### Send Notification

In-app and mobile notifications:

```
Action: Send Notification
  - To: Record Owner
  - Message: "New high-priority lead assigned to you"
```

---

## Action Limits and Best Practices

### Limits to Consider

| Limit | Value |
|-------|-------|
| Emails per day | Varies by edition |
| Webhook timeout | 10 seconds |
| Custom function timeout | 60 seconds |
| Workflow actions per rule | 5 instant, 5 scheduled |

### General Best Practices

| Area | Recommendation |
|------|----------------|
| **Testing** | Always test in sandbox or with test data |
| **Documentation** | Document what each action does and why |
| **Monitoring** | Review automation logs regularly |
| **Error Handling** | Plan for failures |
| **Performance** | Keep actions efficient |

---

## Exercises

### Exercise 6.1: Conceptual Questions

1. What is the difference between a Field Update action and a Custom Function?

2. When would you use a Webhook instead of a Custom Function?

3. What are merge fields and how are they used in email templates?

4. List three scenarios where you would use Tag actions.

### Exercise 6.2: Email Template Design

Create an email template specification for a "Deal Won Congratulations" email:

1. Subject line (include merge fields)
2. Body content (include at least 3 merge fields)
3. Identify what module this template is for
4. What workflow would trigger this email?

### Exercise 6.3: Field Update Planning

For each scenario, specify the field update configuration:

1. When a lead is created, set Status to "New"
2. When a deal moves to "Closed Won", set Closed_Date to today
3. When amount is updated, recalculate Tax as Amount * 0.18
4. When a contact is created, copy the email to Backup_Email field

### Exercise 6.4: Webhook Design

Design a webhook configuration for this scenario:

A company wants to send an SMS when a deal is closed won. They use an SMS gateway with this API:
- URL: https://api.smsgateway.com/send
- Method: POST
- Required parameters: phone_number, message

Specify:
- Workflow trigger and conditions
- Webhook URL
- HTTP Method
- Parameters and their source

### Exercise 6.5: Hands-On - Create Email Template

In your Zoho CRM account:

1. Go to Setup > Customization > Templates > Email Templates
2. Create a new template for the Leads module
3. Add:
   - Subject: "Thank you for your interest, ${Leads.First Name}"
   - Body with personalized greeting and company info
   - At least 3 merge fields
4. Save and preview the template

### Exercise 6.6: Action Selection

For each requirement, identify the appropriate action type:

1. Send an email to the deal owner when a deal is created
2. Mark a lead as "Contacted" when an email is sent
3. Create a task for follow-up 7 days after a meeting
4. Notify an external inventory system when a product is sold
5. Calculate and store a customer's lifetime value
6. Add a "VIP" label to high-value customers
7. Alert the sales manager via mobile notification

---

## Knowledge Check

Before moving to the next module, ensure you can answer:

1. What are the main types of actions available in Zoho CRM automation?

2. How do merge fields work in email templates?

3. What is the difference between instant actions and scheduled actions?

4. When would you need to use a Custom Function instead of standard actions?

5. How do webhooks enable integration with external systems?

---

## Summary

In this module, you learned about the execution layer of Zoho CRM:

- **Email Notifications**: Send templated, personalized emails with merge fields
- **Tasks**: Create automatic follow-up tasks with due dates and assignments
- **Field Updates**: Change field values automatically based on triggers
- **Tags**: Add or remove labels for categorization
- **Webhooks**: Call external systems via HTTP requests
- **Custom Functions**: Execute Deluge scripts for complex logic
- **Other Actions**: Create records, convert leads, send notifications

**Key Principle**: Actions are the outcomes of automation. Choose the right action type for each need, and test thoroughly before deployment.

---

## Next Steps

Now that you understand actions, the next module covers Advanced Features - special capabilities that extend Zoho CRM functionality.

Proceed to [Module 7: Advanced Features](./07-Advanced-Features.md)

---

# Day 12 and 13
## Module 7: Advanced Features

## Learning Objectives

By the end of this module, you will be able to:

- Create and use Subforms for line-item data
- Apply Tags for flexible record categorization
- Build Macros for one-click multi-action execution
- Configure Signals for real-time notifications
- Design advanced Webforms with conditional logic
- Set up Customer Portal for external user access

---

## Overview

Beyond the core functionality, Zoho CRM offers advanced features that extend its capabilities for specialized use cases. This module covers six advanced features:

| Feature | Purpose | Edition Required |
|---------|---------|------------------|
| **Subforms** | Capture multiple related items within a record | Professional+ |
| **Tags** | Flexible labels for categorization | All editions |
| **Macros** | One-click execution of multiple actions | Standard+ |
| **Signals** | Real-time engagement notifications | Professional+ |
| **Webforms (Advanced)** | Conditional fields, file uploads | All editions |
| **Customer Portal** | External user access to CRM data | Enterprise+ |

---

## 7.1 Subforms

### What Are Subforms?

Subforms are embedded tables within a record that capture multiple related items. Think of them as line items in an invoice or order.

**Edition Required**: Professional and above

### When to Use Subforms

| Use Case | Example |
|----------|---------|
| Line items | Products in an order |
| Multiple entries | Attendees at an event |
| Repeating data | Work history entries |
| Related items | Parts used in a repair |

### Subform Components

```
SUBFORM STRUCTURE

Parent Record: Deal
  |
  +-- Subform: "Products Ordered"
        |
        +-- Row 1: Product A, Qty: 2, Price: $100
        +-- Row 2: Product B, Qty: 1, Price: $250
        +-- Row 3: Product C, Qty: 3, Price: $75
        |
        +-- Aggregate: Total = $675
```

### Subform Fields

Subforms can contain various field types:

| Field Type | Use Case |
|------------|----------|
| **Lookup** | Link to Products module |
| **Number** | Quantity |
| **Currency** | Unit price, line total |
| **Picklist** | Status, category |
| **Text** | Notes, description |
| **Formula** | Calculated values |

### Creating a Subform

1. Go to **Setup** > **Customization** > **Modules and Fields**
2. Select the parent module
3. Open the layout editor
4. Drag **Subform** element from left panel
5. Configure subform:
   - Subform name
   - Fields to include
   - Field properties
6. Set up aggregations (if needed)
7. Save layout

### Subform Aggregations

Aggregate functions calculate totals from subform rows:

| Function | Description |
|----------|-------------|
| **SUM** | Total of a number field |
| **COUNT** | Number of rows |
| **AVERAGE** | Average of values |
| **MAX** | Maximum value |
| **MIN** | Minimum value |

**Example**:
```
Subform: Order Items
  - Product (Lookup)
  - Quantity (Number)
  - Unit_Price (Currency)
  - Line_Total (Formula: Quantity * Unit_Price)

Parent Fields (Aggregations):
  - Total_Items = COUNT(Order Items)
  - Order_Total = SUM(Order Items.Line_Total)
```

### Subform Best Practices

| Do | Don't |
|----|-------|
| Use for true line items | Use for simple lists |
| Keep fields minimal (5-7) | Add too many columns |
| Set up aggregations | Manually calculate totals |
| Filter lookups | Show irrelevant options |

### Common Mistakes to Avoid

| Mistake | Why It's Bad | Better Approach |
|---------|--------------|-----------------|
| Too many subform fields | Cluttered, slow | Keep to essential fields |
| No default values | Extra clicks | Set sensible defaults |
| Missing lookup filters | Irrelevant options | Filter to relevant records |
| Forgetting aggregates | Manual calculations | Always set up rollups |

### Troubleshooting

**Problem**: Subform data not saving
- Check required fields in subform
- Verify validation rules

**Problem**: Aggregate not calculating
- Check formula syntax
- Verify data types match

### Further Reading

- [Subforms Overview](https://help.zoho.com/portal/en/kb/crm/customization/subforms)
- [Creating Subforms](https://help.zoho.com/portal/en/kb/crm/customization/subforms/articles/creating-subforms)
- [Subform Aggregations](https://help.zoho.com/portal/en/kb/crm/customization/subforms/articles/aggregate-functions)

---

## 7.2 Tags

### What Are Tags?

Tags are labels you can add to records for flexible categorization that does not fit into fixed picklists. They provide an informal way to group and identify records.

**Edition Required**: All editions

### Tags vs Picklists

| Aspect | Tags | Picklists |
|--------|------|-----------|
| Structure | Freeform | Predefined values |
| Multiple values | Yes | Only with multi-select |
| User-created | Yes | Admin-defined |
| Searchable | Yes | Yes |
| Reportable | Limited | Full |

### Tag Use Cases

| Category | Example Tags |
|----------|--------------|
| **Priority** | "VIP", "Hot Lead", "Urgent" |
| **Status** | "Needs Review", "Follow Up", "On Hold" |
| **Segment** | "Enterprise", "SMB", "Startup" |
| **Process** | "Onboarding", "Renewal Due", "At Risk" |
| **Source** | "Referral", "Conference", "Partner" |

### Managing Tags

#### Adding Tags Manually
1. Open a record
2. Click the tag icon
3. Type tag name
4. Press Enter

#### Adding Tags via Workflow
```
Trigger: Lead Score > 80
Action: Add Tag "Hot Lead"
```

#### Removing Tags via Workflow
```
Trigger: Status changed to "Inactive"
Action: Remove Tag "Active Customer"
```

### Tag Colors

Tags can be color-coded for visual identification:

| Color | Suggested Use |
|-------|---------------|
| Red | Urgent, critical |
| Orange | Warning, needs attention |
| Yellow | Pending, in progress |
| Green | Positive, complete |
| Blue | Informational |
| Purple | Special category |

### Using Tags in Views

Create views filtered by tags:

```
View: VIP Customers
Criteria: Tags contains "VIP"
```

### Tag Best Practices

| Do | Don't |
|----|-------|
| Use consistent naming | Create variations (VIP, V.I.P., vip) |
| Limit total tags (10-15) | Create hundreds of tags |
| Document tag meanings | Assume everyone knows |
| Review periodically | Let tags accumulate |
| Use for informal grouping | Replace structured fields |

### Further Reading

- [Tags in Zoho CRM](https://help.zoho.com/portal/en/kb/crm/customization/articles/tags)
- [Working with Tags](https://help.zoho.com/portal/en/kb/crm/customization/articles/working-with-tags)

---

## 7.3 Macros

### What Are Macros?

Macros are user-executable quick actions that perform multiple operations with one click. They serve as shortcuts for common multi-step tasks.

**Edition Required**: Standard and above

### When to Use Macros

| Scenario | Without Macro | With Macro |
|----------|---------------|------------|
| Close a deal with all updates | Multiple clicks, easy to miss steps | One-click completion |
| Escalate an issue | Several field updates, notifications | Single button |
| Standard follow-up | Create task, update field, send email | One action |

### Macro Components

A macro can include:

| Action | Description |
|--------|-------------|
| **Field Update** | Change field values |
| **Task** | Create task for user |
| **Email** | Send email notification |
| **Tag** | Add or remove tags |
| **Webhook** | Call external URL |

### Example Macros

**Quick Close - Won**:
```
Name: Close Deal - Won
Actions:
  - Field Update: Stage = "Closed Won"
  - Field Update: Closing Date = Today
  - Email: Send "Congratulations" template
  - Task: Create "Send invoice" due in 3 days
  - Tag: Add "Closed This Quarter"
```

**Escalate to Manager**:
```
Name: Escalate Case
Actions:
  - Field Update: Priority = "High"
  - Field Update: Escalated = true
  - Task: Create "Review escalation" for Manager
  - Email: Notify Manager
  - Tag: Add "Escalated"
```

**Schedule Follow-up**:
```
Name: Schedule Follow-up
Actions:
  - Task: Create "Follow up call" due in 7 days
  - Field Update: Next_Contact_Date = Today + 7
  - Tag: Add "Pending Follow-up"
```

### Creating Macros

1. Go to **Setup** > **Automation** > **Macros**
2. Click **+ New Macro**
3. Configure:
   - Macro Name
   - Module
   - Actions (add multiple)
4. Set availability:
   - Which profiles can use it
5. Save

### Running Macros

Users can run macros from:
- Record detail page (Actions dropdown)
- List view (bulk selection)

### Macro Best Practices

| Do | Don't |
|----|-------|
| Name clearly by action | Use vague names |
| Combine related actions | Create too many small macros |
| Test thoroughly | Deploy without testing |
| Limit to relevant profiles | Give everyone all macros |
| Document what each does | Assume it's self-explanatory |

### Further Reading

- [Macros Overview](htthttps://help.zoho.com/portal/en/kb/crm/collaborate-and-increase-team-productivity/macros/articles/using-macros)


---

## 7.4 Signals

### What Are Signals?

Signals are real-time notifications that appear in CRM when specific events occur - email opens, website visits, social mentions, and more.

**Edition Required**: Professional and above

### Signal Types

| Signal | Trigger |
|--------|---------|
| **Email Open** | Recipient opened email |
| **Email Click** | Recipient clicked link |
| **Email Bounce** | Email delivery failed |
| **Webform Submit** | Form submitted |
| **Missed Call** | Call not answered |
| **Survey Response** | Survey completed |

### How Signals Work

```
EVENT OCCURS (email opened)
        |
        v
SIGNAL GENERATED
        |
        v
NOTIFICATION APPEARS
  - In CRM interface
  - Mobile app
  - Browser notification
        |
        v
USER TAKES ACTION
  - Click to view record
  - Follow up immediately
```

### Configuring Signals

1. Go to **Setup** > **Channels** > **Signals**
2. Enable desired signals:
   - Email signals
   - Telephony signals
   - Webform signals
3. Configure notification preferences:
   - Desktop notification
   - Mobile notification
   - In-app notification

### Signal Use Cases

| Signal | Recommended Action |
|--------|-------------------|
| Email opened | Call while engaged |
| Link clicked | Follow up on interest |
| Email bounced | Update contact info |
| Form submitted | Immediate response |
| Missed call | Return call promptly |

### Signals Best Practices

| Do | Don't |
|----|-------|
| Enable relevant signals only | Enable all and get overwhelmed |
| Act on signals promptly | Ignore signals |
| Use for sales engagement | Rely solely on signals |
| Train team on response | Assume everyone knows |

### Further Reading

- [Signals Overview](https://www.zoho.com/crm/developer/docs/signals/)

---

## 7.5 Advanced Webforms

### Beyond Basic Webforms

We  covered basic webforms. Advanced features extend functionality for complex scenarios.

### Advanced Webform Features

| Feature | Description | Edition |
|---------|-------------|---------|
| **Conditional Fields** | Show/hide based on selections | Standard+ |
| **File Uploads** | Allow document attachment | All |
| **Pre-fill** | Pass values via URL | All |
| **Double Opt-in** | Email confirmation required | Standard+ |
| **A/B Testing** | Test different form versions | Professional+ |
| **Analytics** | Track form performance | All |

### Conditional Fields

Show or hide fields based on user selections:

```
CONDITIONAL LOGIC EXAMPLE

Field: Interest (Picklist)
  - Sales
  - Support
  - Partnership

IF Interest = "Sales":
  - Show: Budget field
  - Show: Timeline field
  
IF Interest = "Support":
  - Show: Product field
  - Show: Issue Description field
  
IF Interest = "Partnership":
  - Show: Company Size field
  - Show: Partnership Type field
```

### Configuring Conditional Fields

1. In webform editor, select a field
2. Click "Conditional Rules"
3. Set condition:
   - IF [Field] [Operator] [Value]
   - THEN [Show/Hide] [Target Field]
4. Add multiple rules as needed
5. Test the form

### File Uploads

Enable visitors to upload files:

```
Configuration:
  - Field Type: File Upload
  - Allowed Types: PDF, DOC, JPG
  - Max Size: 5 MB
  - Required: Optional
```

### Pre-fill via URL Parameters

Pass values to pre-populate fields:

```
Base URL: https://crm.zoho.com/crm/WebFormServeServlet?...

With parameters:
?First_Name=John&Email=john@example.com&Source=Campaign123

Result: Form loads with fields pre-filled
```

### Double Opt-in

Require email confirmation before creating record:

```
Flow:
1. Visitor submits form
2. Confirmation email sent
3. Visitor clicks confirmation link
4. Record created in CRM
```

### Webform Analytics

Track form performance:

| Metric | Description |
|--------|-------------|
| Submissions | Total form completions |
| Conversion Rate | Submissions / Views |
| Drop-off Points | Where visitors abandon |
| Source Tracking | Where visitors came from |
| Time to Complete | Average fill time |



---

## 7.6 Customer Portal

### What Is the Customer Portal?

Customer Portal gives external users (customers, partners) limited access to view and interact with their data in your CRM.

**Edition Required**: Enterprise and above

### Why Use Customer Portal?

| Without Portal | With Portal |
|----------------|-------------|
| Customers call for status | Self-service access |
| Manual status updates | Real-time visibility |
| Staff time on inquiries | Automated transparency |
| Delayed communication | Instant access |

### Portal Components

```
PORTAL STRUCTURE

Portal URL: portal.yourcompany.com

Modules Available:
  - My Contacts (their info)
  - My Deals (their purchases)
  - My Cases (their support tickets)
  - My Invoices (their billing)

Permissions:
  - View their records
  - Create new requests
  - Update certain fields
  - Upload documents
```

### Portal User Types

| Type | Description |
|------|-------------|
| **Contact-based** | Linked to Contact records |
| **Partner-based** | For channel partners |
| **Vendor-based** | For supplier access |

### Portal Configuration

#### Step 1: Enable Portal
1. Go to **Setup** > **Channels** > **Portals**
2. Click **Create Portal**
3. Configure portal basics:
   - Portal name
   - Portal URL
   - Contact module

#### Step 2: Configure Modules
For each module available in portal:
1. Select module
2. Set permissions (View, Create, Edit)
3. Configure field visibility
4. Set filter criteria (what records they see)

#### Step 3: Customize Appearance
- Upload logo
- Set colors
- Configure welcome message
- Customize navigation

#### Step 4: Invite Users
- From Contact record, click "Enable Portal Access"
- User receives invitation email
- User sets password and logs in

### Portal Layout Configuration

Control what portal users see:

```
PORTAL LAYOUT: Deals (Customer View)

Visible Fields:
  - Deal Name (Read Only)
  - Stage (Read Only)
  - Amount (Read Only)
  - Expected Close Date

Hidden Fields:
  - Internal Notes
  - Commission
  - Competitor Info
  - Sales Rep Notes
```

### Portal Actions

Enable customers to take actions:

| Action | Example |
|--------|---------|
| **Request Update** | Creates task for staff |
| **Approve Quote** | Updates approval field |
| **Upload Document** | Attaches file to record |
| **Submit Feedback** | Creates feedback record |

### Portal Best Practices

| Do | Don't |
|----|-------|
| Limit visible fields | Expose internal data |
| Filter to their records only | Show other customers' data |
| Keep navigation simple | Create complex menus |
| Enable useful actions | Make it view-only |
| Test as portal user | Deploy without testing |

### Common Mistakes to Avoid

| Mistake | Why It's Bad | Better Approach |
|---------|--------------|-----------------|
| Exposing internal fields | Confusion, security | Carefully select fields |
| No data filtering | Others' data visible | Always filter by user |
| Complex navigation | Poor experience | 3-4 tabs maximum |
| No status updates | Customers still call | Enable real-time status |

### Troubleshooting

**Problem**: Portal user cannot see records
- Check data sharing rules
- Verify contact linkage
- Check filter criteria

**Problem**: Portal user sees too much
- Review field permissions
- Check hidden sections

### Further Reading

- [Customer Portal Overview](https://help.zoho.com/portal/en/kb/crm/users-and-control/portal)
- [Setting Up Portal](https://help.zoho.com/portal/en/kb/crm/users-and-control/portal/articles/setting-up-portal)
- [Portal Customization](https://help.zoho.com/portal/en/kb/crm/users-and-control/portal/articles/customizing-portal)

---

## Exercises

### Exercise 7.1: Conceptual Questions

1. What is the difference between a Subform and a Related List?

2. When would you use Tags instead of a Picklist field?

3. What are Signals and how can they improve sales response times?

4. List three scenarios where a Customer Portal would benefit a business.

5. What is the advantage of using Macros for repetitive tasks?

### Exercise 7.2: Subform Design

Design a subform for an "Order" module that tracks line items:

1. List the fields needed (minimum 5)
2. Specify field types for each
3. Identify which fields should be calculated (formulas)
4. What aggregations would you need on the parent record?

### Exercise 7.3: Tag Strategy

Create a tagging strategy for a sales team:

1. Define 5-8 tags for lead/contact categorization
2. Specify the color for each tag
3. Document what each tag means
4. Identify which tags should be added automatically via workflow

### Exercise 7.4: Macro Design

Design macros for these scenarios:

**Scenario A**: Sales rep wants to quickly mark a deal as lost and log the reason.
- List the actions needed
- What information should be captured?

**Scenario B**: Support agent wants to escalate a case to senior support.
- List the actions needed
- Who should be notified?

### Exercise 7.5: Hands-On - Working with Tags

In your Zoho CRM account:

1. **Create Tags**:
   - Open any Lead or Contact record
   - Add a new tag called "High Priority"
   - Add another tag called "Needs Follow-up"

2. **Create a Tagged View**:
   - Go to the Leads module
   - Create a new view called "High Priority Leads"
   - Set filter: Tags contains "High Priority"

3. **Test the View**:
   - Verify only tagged records appear

### Exercise 7.6: Portal Planning

Design a customer portal for a software company:

1. Which modules should be available to customers?
2. For each module, what fields should be:
   - Visible
   - Hidden
   - Editable
3. What actions should customers be able to take?
4. How would you handle customer feedback or requests?

### Exercise 7.7: Conditional Webform Design

Design a webform with conditional logic:

**Scenario**: A multi-purpose inquiry form where:
- If inquiry type is "Sales", show: Budget, Timeline, Company Size
- If inquiry type is "Support", show: Product, Issue Description, Urgency
- If inquiry type is "Billing", show: Invoice Number, Amount Disputed

Document:
1. All fields on the form
2. Which fields are always visible
3. Conditional rules for each scenario
4. Required fields for each path

---

## Knowledge Check

Before moving to the next module, ensure you can answer:

1. What are Subforms and when should you use them?

2. How do Tags differ from regular fields?

3. What actions can be included in a Macro?

4. What do Signals notify you about?

5. What is the purpose of a Customer Portal?

---

## Summary

In this module, you learned about six advanced features:

- **Subforms**: Capture multiple related items within a single record (line items)
- **Tags**: Flexible labels for informal categorization
- **Macros**: One-click execution of multiple actions
- **Signals**: Real-time notifications of engagement events
- **Advanced Webforms**: Conditional fields, file uploads, analytics
- **Customer Portal**: External user access for self-service

**Key Principle**: These advanced features extend CRM capabilities for specialized needs. Use them when standard features are insufficient.

---

## Next Steps

The final module covers Custom Functions and Deluge Scripting - unlocking unlimited customization possibilities.

Proceed to [Module 8: Custom Functions and Deluge Scripting](./08-Custom-Functions-Deluge.md)

---
# Day 14 and 15
## Module 8: Custom Functions and Deluge Scripting

## Learning Objectives

By the end of this module, you will be able to:

- Understand what Deluge is and when to use it
- Write basic Deluge scripts with variables, conditions, and loops
- Work with CRM data (get, create, update, delete records)
- Use collections (Lists and Maps) effectively
- Manipulate strings and dates
- Handle errors gracefully
- Send emails and make HTTP requests
- Create custom functions for workflows, blueprints, and buttons
- Follow best practices for maintainable code

---

## Overview

Custom Functions powered by Deluge scripting unlock unlimited customization possibilities in Zoho CRM. When standard automation actions are not sufficient, Deluge allows you to write code that can do virtually anything.

**Edition Required**: Professional and above for custom functions

**What You Can Do With Deluge**:
- Complex calculations and data manipulation
- Cross-module operations
- External API integrations
- Custom notifications and reports
- Data validation and transformation
- Automated record management

---

## 8.1 Introduction to Deluge

### What is Deluge?

Deluge stands for **Data Enriched Language for the Universal Grid Environment**. It is Zoho's proprietary scripting language used across all Zoho products.

### Characteristics of Deluge

| Characteristic | Description |
|----------------|-------------|
| **Online IDE** | Write and test code in browser |
| **No Setup** | No installation or configuration needed |
| **Pre-built Functions** | Rich library for CRM operations |
| **Error Handling** | Built-in try-catch mechanism |
| **Debugging** | Info statements for logging |

### When to Use Deluge

| Scenario | Standard Actions | Deluge Needed |
|----------|------------------|---------------|
| Send email on record create | Yes | No |
| Update a field value | Yes | No |
| Complex calculation across records | No | Yes |
| Call external API | Limited (webhook) | Yes |
| Create multiple related records | No | Yes |
| Custom validation logic | Limited | Yes |
| Generate custom reports | No | Yes |
| Data transformation | No | Yes |

### Where Deluge is Used in Zoho CRM

| Location | Purpose |
|----------|---------|
| **Workflow Custom Functions** | Execute on record events |
| **Blueprint Custom Functions** | Execute on stage transitions |
| **Schedule Functions** | Execute at scheduled times |
| **Custom Buttons** | Execute on user click |
| **Validation Rules** | Custom validation logic |
| **Standalone Functions** | Reusable code modules |

### Further Reading

- [Deluge Overview](https://www.zoho.com/deluge/help/)
- [Deluge in Zoho CRM](https://help.zoho.com/portal/en/kb/crm/automation/actions/articles/custom-functions)

---

## 8.2 Deluge Basics

### The Deluge Editor

Access the Deluge editor:
1. Go to **Setup** > **Automation** > **Actions** > **Custom Functions**
2. Click **+ New Function**
3. The editor opens with syntax highlighting and auto-complete

### Variables and Data Types

Variables store data. Deluge is dynamically typed - you do not declare types explicitly.

```deluge
// String
name = "John Smith";
company = 'Acme Corp';  // Single or double quotes

// Number (Integer)
count = 42;
quantity = -10;

// Decimal
price = 99.99;
rate = 0.18;

// Boolean
isActive = true;
isComplete = false;

// Null
emptyValue = null;

// Date
today = zoho.currentdate;

// DateTime
now = zoho.currenttime;
```

### Variable Naming Rules

| Rule | Example |
|------|---------|
| Start with letter or underscore | `name`, `_count` |
| Can contain letters, numbers, underscores | `total_amount`, `item1` |
| Case-sensitive | `Name` and `name` are different |
| Cannot use reserved words | Avoid `if`, `for`, `true`, etc. |

### Comments

```deluge
// This is a single-line comment

/* 
   This is a 
   multi-line comment 
*/

// Use comments to explain complex logic
// Calculate tax based on region
taxRate = 0.18;  // 18% GST
```

### Operators

#### Arithmetic Operators

```deluge
sum = 10 + 5;      // Addition: 15
diff = 10 - 5;     // Subtraction: 5
product = 10 * 5;  // Multiplication: 50
quotient = 10 / 5; // Division: 2
remainder = 10 % 3; // Modulo: 1
```

#### Comparison Operators

```deluge
a == b    // Equal to
a != b    // Not equal to
a > b     // Greater than
a < b     // Less than
a >= b    // Greater than or equal
a <= b    // Less than or equal
```

#### Logical Operators

```deluge
a && b    // AND - both must be true
a || b    // OR - at least one must be true
!a        // NOT - inverts boolean
```

#### String Concatenation

```deluge
firstName = "John";
lastName = "Smith";
fullName = firstName + " " + lastName;  // "John Smith"
```

### The info Statement

Use `info` for debugging - it logs output to the execution log:

```deluge
name = "John";
amount = 1500;

info "Processing record for: " + name;
info "Amount: " + amount;
info "Calculation: " + (amount * 1.18);
```

### Further Reading

- [Deluge Data Types](https://www.zoho.com/deluge/help/data-types.html)
- [Deluge Operators](https://www.zoho.com/deluge/help/operators.html)

---

## 8.3 Control Structures

### Conditional Statements (if/else)

Execute different code based on conditions:

```deluge
// Simple if
if(amount > 1000)
{
    discount = 10;
}

// if-else
if(amount > 1000)
{
    discount = 10;
}
else
{
    discount = 0;
}

// if-else if-else
if(amount > 10000)
{
    discount = 20;
}
else if(amount > 5000)
{
    discount = 15;
}
else if(amount > 1000)
{
    discount = 10;
}
else
{
    discount = 0;
}
```

### Nested Conditions

```deluge
if(customerType == "Premium")
{
    if(amount > 5000)
    {
        discount = 25;
    }
    else
    {
        discount = 15;
    }
}
else
{
    if(amount > 5000)
    {
        discount = 10;
    }
    else
    {
        discount = 5;
    }
}
```

### Compound Conditions

```deluge
// AND condition
if(amount > 1000 && customerType == "Premium")
{
    discount = 20;
}

// OR condition
if(source == "Website" || source == "Referral")
{
    priority = "High";
}

// Complex conditions
if((amount > 5000 && customerType == "Premium") || isVIP == true)
{
    discount = 25;
}
```

### Loops

#### For Each Loop (iterate over collections)

```deluge
// Iterate over a list
fruits = {"Apple", "Banana", "Orange"};
for each fruit in fruits
{
    info fruit;
}

// Iterate over records
leads = zoho.crm.getRecords("Leads");
for each lead in leads
{
    info lead.get("Last_Name");
}
```

#### For Loop (iterate with counter)

```deluge
// Count from 0 to 9
for i = 0 to 9
{
    info "Iteration: " + i;
}

// Count from 1 to 10
for i = 1 to 10
{
    info "Number: " + i;
}
```

### Loop Control

```deluge
// Break - exit loop early
for each item in items
{
    if(item == "stop")
    {
        break;
    }
    info item;
}

// Continue - skip to next iteration
for each item in items
{
    if(item == "skip")
    {
        continue;
    }
    info item;
}
```

### Practical Examples

**Example 1: Determine Lead Grade**
```deluge
score = 75;

if(score >= 80)
{
    grade = "A";
}
else if(score >= 60)
{
    grade = "B";
}
else if(score >= 40)
{
    grade = "C";
}
else
{
    grade = "D";
}

info "Lead Grade: " + grade;
```

**Example 2: Calculate Tiered Discount**
```deluge
amount = 7500;
customerYears = 3;

// Base discount by amount
if(amount > 10000)
{
    baseDiscount = 15;
}
else if(amount > 5000)
{
    baseDiscount = 10;
}
else
{
    baseDiscount = 5;
}

// Loyalty bonus
if(customerYears > 5)
{
    loyaltyBonus = 5;
}
else if(customerYears > 2)
{
    loyaltyBonus = 2;
}
else
{
    loyaltyBonus = 0;
}

totalDiscount = baseDiscount + loyaltyBonus;
info "Total Discount: " + totalDiscount + "%";
```

### Further Reading

- [Conditional Statements](https://www.zoho.com/deluge/help/conditional-statements.html)
- [Loops](https://www.zoho.com/deluge/help/loop-statements.html)

---

## 8.4 Collections: Lists and Maps

### Lists

Lists are ordered collections of items:

```deluge
// Create a list
fruits = List();
fruits.add("Apple");
fruits.add("Banana");
fruits.add("Orange");

// Create with initial values
colors = {"Red", "Green", "Blue"};

// Access elements (0-indexed)
firstFruit = fruits.get(0);  // "Apple"

// Get list size
count = fruits.size();  // 3

// Check if empty
isEmpty = fruits.isEmpty();  // false

// Check if contains
hasApple = fruits.contains("Apple");  // true

// Remove element
fruits.remove("Banana");

// Clear all
fruits.clear();
```

### List Operations

```deluge
numbers = {1, 2, 3, 4, 5};

// Add at specific index
numbers.add(2, 10);  // Insert 10 at index 2

// Get index of element
index = numbers.indexOf(3);

// Sort list
numbers.sort(true);   // Ascending
numbers.sort(false);  // Descending

// Convert to string
str = numbers.toString();
```

### Maps

Maps store key-value pairs:

```deluge
// Create a map
person = Map();
person.put("name", "John");
person.put("age", 30);
person.put("city", "New York");

// Access values
name = person.get("name");  // "John"

// Check if key exists
hasName = person.containsKey("name");  // true

// Get all keys
keys = person.keys();

// Get all values
values = person.values();

// Get size
size = person.size();  // 3

// Remove key
person.remove("city");

// Clear all
person.clear();
```

### Nested Collections

```deluge
// List of Maps
employees = List();

emp1 = Map();
emp1.put("name", "John");
emp1.put("department", "Sales");
employees.add(emp1);

emp2 = Map();
emp2.put("name", "Jane");
emp2.put("department", "Marketing");
employees.add(emp2);

// Access nested data
for each emp in employees
{
    info emp.get("name") + " works in " + emp.get("department");
}

// Map with List values
departments = Map();
departments.put("Sales", {"John", "Mike", "Sarah"});
departments.put("Marketing", {"Jane", "Tom"});

salesTeam = departments.get("Sales");
for each member in salesTeam
{
    info member;
}
```

### Practical Examples

**Example: Build Summary from Records**
```deluge
// Get all deals
deals = zoho.crm.getRecords("Deals");

// Initialize counters
totalAmount = 0;
dealCount = 0;
stageCount = Map();

// Process each deal
for each deal in deals
{
    amount = deal.get("Amount");
    stage = deal.get("Stage");
    
    // Sum amounts
    if(amount != null)
    {
        totalAmount = totalAmount + amount;
    }
    
    // Count deals
    dealCount = dealCount + 1;
    
    // Count by stage
    if(stageCount.containsKey(stage))
    {
        currentCount = stageCount.get(stage);
        stageCount.put(stage, currentCount + 1);
    }
    else
    {
        stageCount.put(stage, 1);
    }
}

info "Total Deals: " + dealCount;
info "Total Amount: " + totalAmount;
info "By Stage: " + stageCount;
```

### Further Reading

- [Lists](https://www.zoho.com/deluge/help/list.html)
- [Maps](https://www.zoho.com/deluge/help/map.html)

---

## 8.5 Working with CRM Data

### Getting Records

#### Get Record by ID

```deluge
// Get a single record by its ID
dealId = "1234567890";
deal = zoho.crm.getRecordById("Deals", dealId);

// Access field values
dealName = deal.get("Deal_Name");
amount = deal.get("Amount");
stage = deal.get("Stage");
ownerId = deal.get("Owner").get("id");

info "Deal: " + dealName + ", Amount: " + amount;
```

#### Get Multiple Records

```deluge
// Get first page of records (default: 200 records)
leads = zoho.crm.getRecords("Leads");

// Get with pagination
page = 1;
perPage = 100;
leads = zoho.crm.getRecords("Leads", page, perPage);

// Process records
for each lead in leads
{
    info lead.get("Last_Name");
}
```

#### Search Records

```deluge
// Search with criteria
criteria = "(Email:equals:john@example.com)";
contacts = zoho.crm.searchRecords("Contacts", criteria);

// Multiple criteria with AND
criteria = "((Lead_Status:equals:Hot) and (Lead_Source:equals:Website))";
leads = zoho.crm.searchRecords("Leads", criteria);

// Multiple criteria with OR
criteria = "((Stage:equals:Closed Won) or (Stage:equals:Closed Lost))";
deals = zoho.crm.searchRecords("Deals", criteria);

// Search with comparison
criteria = "(Amount:greater_than:10000)";
deals = zoho.crm.searchRecords("Deals", criteria);

// Process results
for each contact in contacts
{
    info contact.get("Full_Name");
}
```

#### Search Criteria Operators

| Operator | Syntax | Example |
|----------|--------|---------|
| Equals | `equals` | `(Status:equals:Active)` |
| Not Equals | `not_equals` | `(Status:not_equals:Closed)` |
| Contains | `contains` | `(Email:contains:@gmail.com)` |
| Starts With | `starts_with` | `(Name:starts_with:John)` |
| Greater Than | `greater_than` | `(Amount:greater_than:1000)` |
| Less Than | `less_than` | `(Amount:less_than:5000)` |
| Between | `between` | `(Amount:between:1000,5000)` |

### Creating Records

```deluge
// Build record data as Map
newLead = Map();
newLead.put("First_Name", "John");
newLead.put("Last_Name", "Smith");
newLead.put("Company", "Acme Corp");
newLead.put("Email", "john.smith@acme.com");
newLead.put("Phone", "555-1234");
newLead.put("Lead_Source", "Website");
newLead.put("Lead_Status", "New");

// Create the record
response = zoho.crm.createRecord("Leads", newLead);

// Get the new record ID
newId = response.get("id");
info "Created Lead with ID: " + newId;
```

### Updating Records

```deluge
// Build update data
updateData = Map();
updateData.put("Stage", "Closed Won");
updateData.put("Closing_Date", zoho.currentdate);
updateData.put("Amount", 15000);

// Update the record
dealId = "1234567890";
response = zoho.crm.updateRecord("Deals", dealId, updateData);

info "Updated Deal: " + response;
```

### Deleting Records

```deluge
// Delete a single record
recordId = "1234567890";
response = zoho.crm.deleteRecord("Leads", recordId);

info "Delete response: " + response;
```

### Working with Related Records

```deluge
// Get related records (e.g., Contacts related to an Account)
accountId = "1234567890";
relatedContacts = zoho.crm.getRelatedRecords("Contacts", "Accounts", accountId);

for each contact in relatedContacts
{
    info contact.get("Full_Name");
}
```

### Working with Lookup Fields

```deluge
// Get a deal and its related account
deal = zoho.crm.getRecordById("Deals", dealId);

// Lookup field returns a map with id and name
accountLookup = deal.get("Account_Name");
if(accountLookup != null)
{
    accountId = accountLookup.get("id");
    accountName = accountLookup.get("name");
    
    // Get full account record if needed
    account = zoho.crm.getRecordById("Accounts", accountId);
    info account.get("Website");
}

// Setting a lookup field
newDeal = Map();
newDeal.put("Deal_Name", "New Opportunity");
newDeal.put("Account_Name", accountId);  // Just pass the ID
newDeal.put("Stage", "Qualification");
```

### Practical Examples

**Example 1: Update Related Records**
```deluge
// When an Account is updated, update all related Contacts
accountId = "1234567890";
account = zoho.crm.getRecordById("Accounts", accountId);
newAddress = account.get("Billing_Street");

// Get all contacts for this account
contacts = zoho.crm.getRelatedRecords("Contacts", "Accounts", accountId);

// Update each contact
for each contact in contacts
{
    contactId = contact.get("id");
    updateMap = Map();
    updateMap.put("Mailing_Street", newAddress);
    zoho.crm.updateRecord("Contacts", contactId, updateMap);
}

info "Updated " + contacts.size() + " contacts";
```

**Example 2: Create Related Records**
```deluge
// When a Deal is won, create a Project record
dealId = "1234567890";
deal = zoho.crm.getRecordById("Deals", dealId);

// Only proceed if deal is won
if(deal.get("Stage") == "Closed Won")
{
    // Create project
    project = Map();
    project.put("Project_Name", "Project - " + deal.get("Deal_Name"));
    project.put("Account", deal.get("Account_Name").get("id"));
    project.put("Start_Date", zoho.currentdate);
    project.put("Budget", deal.get("Amount"));
    project.put("Status", "Planning");
    
    response = zoho.crm.createRecord("Projects", project);
    info "Created Project: " + response.get("id");
}
```

### Further Reading

- [CRM Deluge Tasks](https://www.zoho.com/deluge/help/crm/)
- [Get Records](https://www.zoho.com/deluge/help/crm/get-records.html)
- [Search Records](https://www.zoho.com/deluge/help/crm/search-records.html)
- [Create Records](https://www.zoho.com/deluge/help/crm/create-record.html)

---

## 8.6 String Operations

### Basic String Functions

```deluge
text = "  Hello World  ";

// Length
len = text.len();  // 15

// Trim whitespace
trimmed = text.trim();  // "Hello World"

// Case conversion
upper = text.toUpperCase();  // "  HELLO WORLD  "
lower = text.toLowerCase();  // "  hello world  "

// Substring
sub = text.subString(2, 7);  // "Hello"

// Index of
index = text.indexOf("World");  // 8
lastIndex = text.lastIndexOf("o");  // 9

// Contains
hasWorld = text.contains("World");  // true

// Starts/Ends with
startsH = text.startsWith("  H");  // true
endsD = text.endsWith("d  ");  // true
```

### String Manipulation

```deluge
text = "John,Jane,Mike,Sarah";

// Split into list
names = text.toList(",");  // {"John", "Jane", "Mike", "Sarah"}

// Replace
newText = text.replaceAll(",", " | ");  // "John | Jane | Mike | Sarah"

// Replace first occurrence only
newText = text.replaceFirst(",", " and ");  // "John and Jane,Mike,Sarah"

// Remove characters
cleaned = text.remove(",");  // "JohnJaneMikeSarah"
```

### String Formatting

```deluge
// Concatenation
firstName = "John";
lastName = "Smith";
fullName = firstName + " " + lastName;

// Number to string
amount = 1500.50;
amountStr = amount.toString();

// Padding
code = "42";
padded = code.leftPad("0", 5);  // "00042"
padded = code.rightPad("0", 5);  // "42000"

// Format numbers
amount = 1234567.89;
formatted = amount.round(2);  // 1234567.89
```

### Regular Expressions

```deluge
// Match pattern
email = "john@example.com";
isValidEmail = email.matches("^[A-Za-z0-9+_.-]+@(.+)$");  // true

// Extract with regex
text = "Order #12345 confirmed";
orderNum = text.getMatches("\\d+");  // Returns list: {"12345"}
```

### Practical Examples

**Example 1: Format Phone Number**
```deluge
phone = "5551234567";

// Format as (555) 123-4567
if(phone.len() == 10)
{
    formattedPhone = "(" + phone.subString(0, 3) + ") " + 
                     phone.subString(3, 6) + "-" + 
                     phone.subString(6, 10);
    info formattedPhone;  // (555) 123-4567
}
```

**Example 2: Clean and Validate Email**
```deluge
email = "  John.Smith@Example.COM  ";

// Clean
email = email.trim().toLowerCase();  // "john.smith@example.com"

// Validate
if(email.contains("@") && email.contains("."))
{
    isValid = true;
}
else
{
    isValid = false;
}
```

**Example 3: Generate Unique Code**
```deluge
// Generate a unique reference code
prefix = "ORD";
timestamp = zoho.currenttime.toString("yyyyMMddHHmmss");
random = ((zoho.currenttime.toLong() % 10000) + "").leftPad("0", 4);

uniqueCode = prefix + "-" + timestamp + "-" + random;
info uniqueCode;  // Example: ORD-20240115143022-7834
```

### Further Reading

- [String Functions](https://www.zoho.com/deluge/help/text-functions.html)

---

## 8.7 Date and Time Operations

### Getting Current Date/Time

```deluge
// Current date (date only, no time)
today = zoho.currentdate;

// Current date and time
now = zoho.currenttime;

info "Today: " + today;
info "Now: " + now;
```

### Creating Dates

```deluge
// From string
dateStr = "2024-01-15";
myDate = dateStr.toDate();

// From components
myDate = "15-Jan-2024".toDate("dd-MMM-yyyy");

// DateTime from string
dateTimeStr = "2024-01-15 14:30:00";
myDateTime = dateTimeStr.toDateTime();
```

### Date Arithmetic

```deluge
today = zoho.currentdate;

// Add/subtract days
tomorrow = today.addDay(1);
yesterday = today.addDay(-1);
nextWeek = today.addDay(7);
lastMonth = today.addMonth(-1);

// Add other units
nextMonth = today.addMonth(1);
nextYear = today.addYear(1);
nextHour = zoho.currenttime.addHour(1);
nextMinute = zoho.currenttime.addMinutes(30);
```

### Date Extraction

```deluge
myDate = zoho.currentdate;

// Get components
year = myDate.getYear();      // 2024
month = myDate.getMonth();    // 1 (January)
day = myDate.getDay();        // 15
dayOfWeek = myDate.getDayOfWeek();  // 1=Sunday, 2=Monday, etc.

// For DateTime
myTime = zoho.currenttime;
hour = myTime.getHour();      // 14
minute = myTime.getMinutes(); // 30
second = myTime.getSeconds(); // 45
```

### Date Formatting

```deluge
myDate = zoho.currentdate;

// Format to string
formatted = myDate.toString("dd-MMM-yyyy");     // "15-Jan-2024"
formatted = myDate.toString("MM/dd/yyyy");      // "01/15/2024"
formatted = myDate.toString("MMMM d, yyyy");    // "January 15, 2024"
formatted = myDate.toString("yyyy-MM-dd");      // "2024-01-15"

// DateTime formatting
myTime = zoho.currenttime;
formatted = myTime.toString("yyyy-MM-dd HH:mm:ss");  // "2024-01-15 14:30:45"
formatted = myTime.toString("hh:mm a");              // "02:30 PM"
```

### Date Comparison

```deluge
date1 = "2024-01-15".toDate();
date2 = "2024-01-20".toDate();

// Compare
if(date1 < date2)
{
    info "date1 is before date2";
}

if(date1 > date2)
{
    info "date1 is after date2";
}

if(date1 == date2)
{
    info "dates are equal";
}

// Days between dates
daysDiff = date2.daysBetween(date1);  // 5
```

### Practical Examples

**Example 1: Calculate Due Date**
```deluge
// Set due date based on priority
priority = "High";
createdDate = zoho.currentdate;

if(priority == "High")
{
    dueDate = createdDate.addDay(1);
}
else if(priority == "Medium")
{
    dueDate = createdDate.addDay(3);
}
else
{
    dueDate = createdDate.addDay(7);
}

info "Due Date: " + dueDate.toString("dd-MMM-yyyy");
```

**Example 2: Check SLA Breach**
```deluge
createdTime = record.get("Created_Time");
now = zoho.currenttime;

// Calculate hours elapsed
hoursElapsed = now.hoursBetween(createdTime);

slaHours = 24;

if(hoursElapsed > slaHours)
{
    info "SLA BREACHED! Hours elapsed: " + hoursElapsed;
    isBreached = true;
}
else
{
    remaining = slaHours - hoursElapsed;
    info "SLA OK. Hours remaining: " + remaining;
    isBreached = false;
}
```

**Example 3: Business Days Calculation**
```deluge
// Add business days (skip weekends)
startDate = zoho.currentdate;
businessDaysToAdd = 5;

resultDate = startDate;
daysAdded = 0;

while(daysAdded < businessDaysToAdd)
{
    resultDate = resultDate.addDay(1);
    dayOfWeek = resultDate.getDayOfWeek();
    
    // Skip Saturday (7) and Sunday (1)
    if(dayOfWeek != 1 && dayOfWeek != 7)
    {
        daysAdded = daysAdded + 1;
    }
}

info "Due Date (5 business days): " + resultDate.toString("dd-MMM-yyyy");
```

### Further Reading

- [Date Functions](https://www.zoho.com/deluge/help/date-functions.html)
- [DateTime Functions](https://www.zoho.com/deluge/help/datetime-functions.html)

---

## 8.8 Error Handling

### The try-catch Block

Always wrap risky operations in try-catch to handle errors gracefully:

```deluge
try
{
    // Code that might fail
    record = zoho.crm.getRecordById("Deals", dealId);
    amount = record.get("Amount");
    result = 1000 / amount;  // Could fail if amount is 0
}
catch(e)
{
    // Handle the error
    info "Error occurred: " + e;
    result = 0;
}
```

### Common Error Scenarios

```deluge
// 1. Null value access
try
{
    record = zoho.crm.getRecordById("Leads", leadId);
    email = record.get("Email");
    
    // email might be null
    if(email != null)
    {
        domain = email.subString(email.indexOf("@") + 1);
    }
}
catch(e)
{
    info "Error: " + e;
}

// 2. Division by zero
try
{
    total = 1000;
    count = 0;
    average = total / count;  // Error!
}
catch(e)
{
    info "Cannot divide by zero";
    average = 0;
}

// 3. Invalid record ID
try
{
    record = zoho.crm.getRecordById("Deals", "invalid_id");
}
catch(e)
{
    info "Record not found";
}

// 4. API call failure
try
{
    response = invokeurl
    [
        url: "https://api.example.com/data"
        type: GET
    ];
}
catch(e)
{
    info "API call failed: " + e;
}
```

### The ifnull Function

Use `ifnull` to provide default values for null:

```deluge
// Without ifnull - may cause errors
amount = record.get("Amount");
total = amount * 1.18;  // Error if amount is null

// With ifnull - safe
amount = ifnull(record.get("Amount"), 0);
total = amount * 1.18;  // Works even if Amount was null

// Other examples
name = ifnull(record.get("Name"), "Unknown");
date = ifnull(record.get("Due_Date"), zoho.currentdate);
```

### Null Checking Best Practices

```deluge
// Check before using
email = record.get("Email");
if(email != null && email != "")
{
    // Safe to use email
    sendEmail(email);
}

// Check lookup fields
account = record.get("Account_Name");
if(account != null)
{
    accountId = account.get("id");
    accountName = account.get("name");
}

// Check list before iterating
records = zoho.crm.searchRecords("Leads", criteria);
if(records != null && records.size() > 0)
{
    for each record in records
    {
        // Process record
    }
}
else
{
    info "No records found";
}
```

### Logging for Debugging

```deluge
// Add strategic logging
info "=== Function Start ===";
info "Input dealId: " + dealId;

try
{
    deal = zoho.crm.getRecordById("Deals", dealId);
    info "Deal retrieved: " + deal.get("Deal_Name");
    
    amount = ifnull(deal.get("Amount"), 0);
    info "Amount: " + amount;
    
    // Processing logic
    tax = amount * 0.18;
    info "Calculated tax: " + tax;
    
    // Update record
    updateMap = Map();
    updateMap.put("Tax", tax);
    response = zoho.crm.updateRecord("Deals", dealId, updateMap);
    info "Update response: " + response;
    
    info "=== Function Complete ===";
}
catch(e)
{
    info "!!! ERROR: " + e;
}
```

### Further Reading

- [Error Handling](https://www.zoho.com/deluge/help/error-handling.html)
- [Debugging Tips](https://www.zoho.com/deluge/help/debugging.html)

---

## 8.9 Sending Emails

### Basic Email Sending

```deluge
sendmail
[
    from: zoho.adminuserid
    to: "recipient@example.com"
    subject: "Test Email"
    message: "This is a test email from Zoho CRM."
];
```

### Email with HTML Content

```deluge
htmlContent = "<html><body>";
htmlContent = htmlContent + "<h1>Welcome!</h1>";
htmlContent = htmlContent + "<p>Thank you for your interest.</p>";
htmlContent = htmlContent + "<p>We will contact you shortly.</p>";
htmlContent = htmlContent + "</body></html>";

sendmail
[
    from: zoho.adminuserid
    to: "customer@example.com"
    subject: "Welcome to Our Service"
    message: htmlContent
];
```

### Email with Dynamic Content

```deluge
// Get record data
deal = zoho.crm.getRecordById("Deals", dealId);
contactId = deal.get("Contact_Name").get("id");
contact = zoho.crm.getRecordById("Contacts", contactId);

// Build personalized email
recipientEmail = contact.get("Email");
recipientName = contact.get("First_Name");
dealName = deal.get("Deal_Name");
amount = deal.get("Amount");

subject = "Your Order Confirmation - " + dealName;

message = "<html><body>";
message = message + "<p>Dear " + recipientName + ",</p>";
message = message + "<p>Thank you for your order!</p>";
message = message + "<p><strong>Order Details:</strong></p>";
message = message + "<ul>";
message = message + "<li>Order: " + dealName + "</li>";
message = message + "<li>Amount: $" + amount + "</li>";
message = message + "</ul>";
message = message + "<p>Best regards,<br>The Sales Team</p>";
message = message + "</body></html>";

sendmail
[
    from: zoho.adminuserid
    to: recipientEmail
    subject: subject
    message: message
];

info "Email sent to: " + recipientEmail;
```

### Email with CC and BCC

```deluge
sendmail
[
    from: zoho.adminuserid
    to: "primary@example.com"
    cc: "manager@example.com,supervisor@example.com"
    bcc: "archive@example.com"
    subject: "Important Update"
    message: "This is the message content."
];
```

### Email with Reply-To

```deluge
sendmail
[
    from: zoho.adminuserid
    to: "customer@example.com"
    reply-to: "support@yourcompany.com"
    subject: "Support Request Received"
    message: "We have received your request."
];
```

### Further Reading

- [Send Mail](https://www.zoho.com/deluge/help/send-mail.html)

---

## 8.10 HTTP Requests (invokeurl)

### Making API Calls

Use `invokeurl` to call external APIs or services:

### GET Request

```deluge
response = invokeurl
[
    url: "https://api.example.com/users/123"
    type: GET
];

info response;
```

### POST Request

```deluge
// Prepare data
payload = Map();
payload.put("name", "John Smith");
payload.put("email", "john@example.com");

// Make request
response = invokeurl
[
    url: "https://api.example.com/users"
    type: POST
    parameters: payload.toString()
    headers: {"Content-Type": "application/json"}
];

info response;
```

### Request with Headers

```deluge
// Set authentication and content type
headers = Map();
headers.put("Authorization", "Bearer your_api_token");
headers.put("Content-Type", "application/json");

response = invokeurl
[
    url: "https://api.example.com/data"
    type: GET
    headers: headers
];
```

### Handling JSON Response

```deluge
// Make API call
response = invokeurl
[
    url: "https://api.example.com/users/123"
    type: GET
];

// Parse response (if JSON)
userData = response.toMap();
userName = userData.get("name");
userEmail = userData.get("email");

info "User: " + userName + " (" + userEmail + ")";
```

### Practical Examples

**Example 1: Send SMS via API**
```deluge
// Get contact info
contact = zoho.crm.getRecordById("Contacts", contactId);
phone = contact.get("Phone");
message = "Your order has been shipped!";

// Build request
smsPayload = Map();
smsPayload.put("to", phone);
smsPayload.put("message", message);

headers = Map();
headers.put("Authorization", "Bearer SMS_API_KEY");
headers.put("Content-Type", "application/json");

try
{
    response = invokeurl
    [
        url: "https://api.smsgateway.com/send"
        type: POST
        parameters: smsPayload.toString()
        headers: headers
    ];
    
    info "SMS sent: " + response;
}
catch(e)
{
    info "SMS failed: " + e;
}
```

**Example 2: Fetch Data from External System**
```deluge
// Get customer info from external ERP
customerId = "CUST-12345";

headers = Map();
headers.put("Authorization", "Bearer ERP_API_KEY");

try
{
    response = invokeurl
    [
        url: "https://erp.company.com/api/customers/" + customerId
        type: GET
        headers: headers
    ];
    
    // Parse and use data
    customerData = response.toMap();
    creditLimit = customerData.get("credit_limit");
    outstandingBalance = customerData.get("outstanding");
    
    // Update CRM record
    updateMap = Map();
    updateMap.put("Credit_Limit", creditLimit);
    updateMap.put("Outstanding_Balance", outstandingBalance);
    zoho.crm.updateRecord("Accounts", accountId, updateMap);
}
catch(e)
{
    info "Failed to fetch customer data: " + e;
}
```

**Example 3: Post to Slack**
```deluge
// Send notification to Slack channel
dealName = "Big Sale Corp";
amount = 50000;
stage = "Closed Won";

slackMessage = Map();
slackMessage.put("text", "Deal Won! " + dealName + " for $" + amount);

response = invokeurl
[
    url: "https://hooks.slack.com/services/YOUR/SLACK/WEBHOOK"
    type: POST
    parameters: slackMessage.toString()
    headers: {"Content-Type": "application/json"}
];
```

### Further Reading

- [Invoke URL](https://www.zoho.com/deluge/help/invoke-url.html)
- [Integration Examples](https://www.zoho.com/deluge/help/integration.html)

---

## 8.11 Creating Custom Functions

### Function Types and Locations

| Type | Location | Trigger |
|------|----------|---------|
| **Workflow Function** | Workflow Action | Record event |
| **Blueprint Function** | Blueprint Transition | Stage change |
| **Schedule Function** | Schedule | Time-based |
| **Button Function** | Custom Button | User click |
| **Standalone Function** | Actions | Called by other functions |

### Creating a Workflow Function

1. Go to **Setup** > **Automation** > **Actions** > **Custom Functions**
2. Click **+ New Function**
3. Configure:
   - Function Name: `calculateDealMetrics`
   - Module: Deals
   - Description: Calculate and update deal metrics
4. Write the code:

```deluge
// Function receives dealId as argument
deal = zoho.crm.getRecordById("Deals", dealId);

// Get values
amount = ifnull(deal.get("Amount"), 0);
discount = ifnull(deal.get("Discount_Percent"), 0);

// Calculate
discountAmount = amount * (discount / 100);
netAmount = amount - discountAmount;
tax = netAmount * 0.18;
grandTotal = netAmount + tax;

// Update record
updateMap = Map();
updateMap.put("Discount_Amount", discountAmount);
updateMap.put("Net_Amount", netAmount);
updateMap.put("Tax_Amount", tax);
updateMap.put("Grand_Total", grandTotal);

zoho.crm.updateRecord("Deals", dealId, updateMap);
info "Metrics calculated for deal: " + deal.get("Deal_Name");
```

5. Save the function
6. Associate with a Workflow:
   - Create workflow for Deals
   - Add action: Custom Function
   - Select your function

### Creating a Button Function

1. Create the function (as above)
2. Go to **Setup** > **Customization** > **Modules and Fields**
3. Select module (e.g., Deals)
4. Click **Links and Buttons**
5. Click **+ New Button**
6. Configure:
   - Button Name: "Calculate Metrics"
   - Position: Detail Page
   - Action: Custom Function
   - Select your function

### Creating a Schedule Function

1. Create a standalone function:

```deluge
// Daily summary report function
today = zoho.currentdate;
todayStr = today.toString("yyyy-MM-dd");

// Get today's closed deals
criteria = "((Stage:equals:Closed Won) and (Closing_Date:equals:" + todayStr + "))";
deals = zoho.crm.searchRecords("Deals", criteria);

// Calculate totals
totalAmount = 0;
dealCount = deals.size();

for each deal in deals
{
    amount = ifnull(deal.get("Amount"), 0);
    totalAmount = totalAmount + amount;
}

// Send summary email
subject = "Daily Sales Summary - " + today.toString("dd-MMM-yyyy");

message = "<h2>Daily Sales Summary</h2>";
message = message + "<p><strong>Date:</strong> " + today.toString("dd-MMM-yyyy") + "</p>";
message = message + "<p><strong>Deals Closed:</strong> " + dealCount + "</p>";
message = message + "<p><strong>Total Revenue:</strong> $" + totalAmount + "</p>";

if(dealCount > 0)
{
    message = message + "<h3>Deal Details:</h3><ul>";
    for each deal in deals
    {
        message = message + "<li>" + deal.get("Deal_Name") + " - $" + deal.get("Amount") + "</li>";
    }
    message = message + "</ul>";
}

sendmail
[
    from: zoho.adminuserid
    to: "manager@company.com"
    subject: subject
    message: message
];

info "Daily summary sent. Deals: " + dealCount + ", Total: $" + totalAmount;
```

2. Go to **Setup** > **Automation** > **Schedules**
3. Click **+ Create Schedule**
4. Configure:
   - Name: "Daily Sales Summary"
   - Frequency: Daily at 6:00 PM
   - Function: Select your function
5. Activate

### Function Arguments

When functions are triggered, they receive arguments:

| Context | Available Arguments |
|---------|---------------------|
| **Workflow** | Record ID of triggering record |
| **Blueprint** | Record ID, Transition info |
| **Button** | Record ID, User info |
| **Schedule** | None (standalone) |

```deluge
// Workflow function - dealId is automatically passed
// Function signature: dealId (Long)

deal = zoho.crm.getRecordById("Deals", dealId);
```

### Further Reading

- [Custom Functions](https://help.zoho.com/portal/en/kb/crm/automation/actions/articles/custom-functions)
- [Creating Functions](https://help.zoho.com/portal/en/kb/crm/automation/actions/articles/creating-custom-functions)

---

## 8.12 Best Practices

### Code Organization

```deluge
// ========================================
// Function: calculateDealMetrics
// Purpose: Calculate all financial metrics for a deal
// Trigger: Workflow on Deal Create/Edit
// Author: Your Name
// Date: 2024-01-15
// ========================================

// --- CONFIGURATION ---
TAX_RATE = 0.18;
MAX_DISCOUNT = 0.30;

// --- GET RECORD ---
deal = zoho.crm.getRecordById("Deals", dealId);
info "Processing deal: " + deal.get("Deal_Name");

// --- VALIDATE ---
amount = ifnull(deal.get("Amount"), 0);
if(amount <= 0)
{
    info "Invalid amount. Exiting.";
    return;
}

// --- CALCULATE ---
// Calculate discount
discountPercent = ifnull(deal.get("Discount_Percent"), 0) / 100;
if(discountPercent > MAX_DISCOUNT)
{
    discountPercent = MAX_DISCOUNT;
    info "Discount capped at " + (MAX_DISCOUNT * 100) + "%";
}

discountAmount = amount * discountPercent;
netAmount = amount - discountAmount;
taxAmount = netAmount * TAX_RATE;
grandTotal = netAmount + taxAmount;

// --- UPDATE ---
updateMap = Map();
updateMap.put("Discount_Amount", discountAmount);
updateMap.put("Net_Amount", netAmount);
updateMap.put("Tax_Amount", taxAmount);
updateMap.put("Grand_Total", grandTotal);

try
{
    response = zoho.crm.updateRecord("Deals", dealId, updateMap);
    info "Update successful: " + response;
}
catch(e)
{
    info "Update failed: " + e;
}

info "=== Function Complete ===";
```

### Naming Conventions

| Element | Convention | Example |
|---------|------------|---------|
| Functions | camelCase, verb-noun | `calculateTax`, `sendWelcomeEmail` |
| Variables | camelCase, descriptive | `totalAmount`, `customerEmail` |
| Constants | UPPER_SNAKE_CASE | `TAX_RATE`, `MAX_DISCOUNT` |
| Maps | Descriptive name | `updateMap`, `customerData` |

### Performance Tips

| Tip | Description |
|-----|-------------|
| **Minimize API calls** | Batch operations where possible |
| **Use search instead of getRecords** | More efficient for filtered data |
| **Avoid loops within loops** | Can cause timeouts |
| **Cache repeated lookups** | Store in variables |
| **Keep functions focused** | One function, one purpose |

### Security Considerations

```deluge
// DO NOT hardcode sensitive data
// BAD:
apiKey = "sk_live_12345abcde";

// GOOD: Use Zoho connections or store in secure location
// Set up connection in Setup > Developer Space > Connections

// Validate user inputs
userInput = input.get("email");
if(userInput != null && userInput.matches("^[A-Za-z0-9+_.-]+@(.+)$"))
{
    // Safe to use
}
else
{
    info "Invalid email input";
    return;
}
```

### Testing Checklist

Before deploying a custom function:

1. Test with valid data
2. Test with null/empty values
3. Test with edge cases (zero, negative, very large numbers)
4. Test with invalid record IDs
5. Check error handling works
6. Review logs for unexpected behavior
7. Test in sandbox if available

### Further Reading

- [Best Practices](https://www.zoho.com/deluge/help/best-practices.html)
- [Performance Tips](https://www.zoho.com/deluge/help/performance.html)

---

## 8.13 Troubleshooting

### Common Errors and Solutions

#### "Variable not defined"
```deluge
// ERROR: Using variable before defining
total = amount * 1.18;  // 'amount' not defined

// FIX: Define variable first
amount = 1000;
total = amount * 1.18;
```

#### "Cannot invoke method on null"
```deluge
// ERROR: Calling method on null value
email = record.get("Email");
domain = email.subString(email.indexOf("@") + 1);  // Fails if email is null

// FIX: Check for null first
email = record.get("Email");
if(email != null)
{
    domain = email.subString(email.indexOf("@") + 1);
}
```

#### "Record not found"
```deluge
// ERROR: Invalid record ID
record = zoho.crm.getRecordById("Deals", "invalid");

// FIX: Use try-catch
try
{
    record = zoho.crm.getRecordById("Deals", dealId);
}
catch(e)
{
    info "Record not found: " + dealId;
}
```

#### "API limit exceeded"
```deluge
// ERROR: Too many API calls in loop
for each id in recordIds
{
    record = zoho.crm.getRecordById("Deals", id);  // Each is an API call
}

// FIX: Use batch operations or search
criteria = "(id:in:" + recordIds.toString(",") + ")";
records = zoho.crm.searchRecords("Deals", criteria);  // Single API call
```

#### "Function timeout"
```deluge
// ERROR: Function takes too long (>60 seconds)

// FIX: Optimize code
// - Reduce API calls
// - Avoid nested loops
// - Process in batches
// - Move to scheduled function for large operations
```

### Debugging Techniques

```deluge
// 1. Use info liberally during development
info "=== DEBUG START ===";
info "Input ID: " + dealId;
info "Type: " + dealId.getClass();

// 2. Log at each major step
info "Step 1: Getting record...";
record = zoho.crm.getRecordById("Deals", dealId);
info "Step 1 complete. Record: " + record;

// 3. Log variable values
info "Amount: " + amount;
info "Discount: " + discount;
info "Calculated tax: " + tax;

// 4. Log before and after updates
info "Before update: " + record.get("Status");
zoho.crm.updateRecord("Deals", dealId, updateMap);
info "After update: Status should be 'Complete'";

// 5. Catch and log errors
try
{
    // risky operation
}
catch(e)
{
    info "!!! ERROR at step X: " + e;
    info "dealId was: " + dealId;
    info "amount was: " + amount;
}
```

### Viewing Execution Logs

1. Go to **Setup** > **Automation** > **Actions** > **Custom Functions**
2. Click on your function
3. Click **View Logs** or **Execution Logs**
4. Review the output from `info` statements

### Further Reading

- [Troubleshooting Guide](https://www.zoho.com/deluge/help/troubleshooting.html)
- [Error Messages](https://www.zoho.com/deluge/help/error-messages.html)

---

## Exercises

### Exercise 8.1: Conceptual Questions

1. What is Deluge and why is it used in Zoho CRM?

2. What is the difference between a List and a Map in Deluge?

3. Why is error handling important in custom functions?

4. When would you use `ifnull()` function?

5. What are the different contexts where custom functions can be used?

### Exercise 8.2: Basic Syntax Practice

Write Deluge code for each scenario:

1. Create variables for: name (text), age (number), salary (decimal), isActive (boolean)

2. Write an if-else statement that assigns a grade based on score:
   - 90+: A
   - 80-89: B
   - 70-79: C
   - Below 70: D

3. Create a list of fruits and iterate through it, printing each fruit

4. Create a map with keys: name, email, phone, and values of your choice. Print each key-value pair.

### Exercise 8.3: CRM Data Operations

Write Deluge code for each scenario:

1. Get a Deal record by ID and print the Deal Name and Amount

2. Search for all Leads where Lead Source is "Website"

3. Create a new Contact with First Name, Last Name, Email, and Phone

4. Update a Deal's Stage to "Closed Won" and Closing Date to today

### Exercise 8.4: String and Date Operations

Write Deluge code for each scenario:

1. Given an email "john.smith@example.com", extract just the domain name

2. Given a phone number "5551234567", format it as "(555) 123-4567"

3. Calculate the number of days between today and a given date

4. Generate a unique reference code with format: "REF-YYYYMMDD-XXXX" where XXXX is random

### Exercise 8.5: Complete Function

Write a complete custom function for this scenario:

**High-Value Deal Notification**

When a Deal amount exceeds $50,000:
1. Get the Deal and its associated Contact
2. Calculate 18% tax and total with tax
3. Update the Deal with calculated values
4. Send an email to the sales manager with deal details
5. Log all steps for debugging

Include:
- Proper null handling
- Error handling with try-catch
- Informative logging
- Well-organized code with comments

### Exercise 8.6: Schedule Function

Design a schedule function that runs weekly and:

1. Finds all Deals with Close Date in the past that are still open
2. Counts how many days overdue each deal is
3. Updates a custom field "Days Overdue" on each deal
4. Sends a summary email listing all overdue deals

Write the pseudo-code or actual Deluge code.

### Exercise 8.7: API Integration

Write Deluge code to:

1. Call an external API (use a sample URL like https://jsonplaceholder.typicode.com/users/1)
2. Parse the JSON response
3. Extract specific fields from the response
4. Handle potential errors

---

## Knowledge Check

Before completing this module, ensure you can answer:

1. What are the basic data types in Deluge?

2. How do you iterate over a list of records?

3. What is the difference between `zoho.crm.getRecords()` and `zoho.crm.searchRecords()`?

4. How do you handle null values safely?

5. What does `invokeurl` do and when would you use it?

6. How do you create and update CRM records using Deluge?

7. What is the purpose of the `try-catch` block?

8. How do you debug a custom function?

---

## Summary

In this module, you learned:

- **Deluge Basics**: Variables, data types, operators, and the info statement for debugging

- **Control Structures**: Conditional statements (if/else) and loops (for each, for)

- **Collections**: Lists for ordered data and Maps for key-value pairs

- **CRM Operations**: Getting, searching, creating, updating, and deleting records

- **String Operations**: Manipulation, formatting, and validation of text data

- **Date Operations**: Working with dates, calculations, and formatting

- **Error Handling**: Using try-catch and ifnull for robust code

- **Email and HTTP**: Sending emails and making API calls to external services

- **Custom Functions**: Creating and deploying functions in workflows, blueprints, schedules, and buttons

- **Best Practices**: Code organization, naming conventions, performance, and security

**Key Principle**: Custom functions unlock unlimited possibilities in Zoho CRM. Start simple, test thoroughly, handle errors gracefully, and always document your code.

---

## Next Steps

Congratulations on completing the Zoho CRM course modules! You now have a comprehensive understanding of:

- CRM concepts and Zoho CRM architecture
- Data components: modules, layouts, fields, forms, views
- Security: users, roles, profiles, data sharing
- Automation: blueprints, workflows, schedules, and more
- Actions and custom functions with Deluge

**Recommended Next Steps**:

1. **Practice**: Build a complete implementation in your Zoho CRM account
2. **Capstone Project**: Apply all concepts to the TurboFix Auto Care project
3. **Certification**: Consider Zoho CRM certification
4. **Community**: Join Zoho Community forums for support and learning

---

## Additional Resources

### Official Documentation

- [Deluge Script Reference](https://www.zoho.com/deluge/help/)
- [CRM Deluge Tasks](https://www.zoho.com/deluge/help/crm/)
- [Custom Functions in CRM](https://help.zoho.com/portal/en/kb/crm/automation/actions/articles/custom-functions)

### Learning Resources

- [Zoho Developer Documentation](https://www.zoho.com/developer-hub/)
- [Zoho CRM API Documentation](https://www.zoho.com/crm/developer/docs/api/v8/)
- [Zoho Community](https://help.zoho.com/portal/community/zoho-crm)

### Practice Environments

- [Zoho CRM Sandbox](https://help.zoho.com/portal/en/kb/crm/settings/data-administration/articles/sandbox) (Enterprise+)
- [Zoho Creator](https://www.zoho.com/creator/) - Practice Deluge in a low-code environment

---

## Quick Reference Card

### Common CRM Operations

```deluge
// Get record by ID
record = zoho.crm.getRecordById("Module", recordId);

// Search records
records = zoho.crm.searchRecords("Module", "(Field:equals:Value)");

// Get multiple records
records = zoho.crm.getRecords("Module", page, perPage);

// Create record
newRecord = Map();
newRecord.put("Field1", "Value1");
response = zoho.crm.createRecord("Module", newRecord);

// Update record
updateMap = Map();
updateMap.put("Field1", "NewValue");
response = zoho.crm.updateRecord("Module", recordId, updateMap);

// Delete record
response = zoho.crm.deleteRecord("Module", recordId);
```

### Common Utilities

```deluge
// Current date/time
today = zoho.currentdate;
now = zoho.currenttime;

// Null handling
value = ifnull(field, defaultValue);

// Error handling
try { /* code */ } catch(e) { info e; }

// Send email
sendmail [ from: zoho.adminuserid  to: "email"  subject: "Sub"  message: "Body" ];

// HTTP request
response = invokeurl [ url: "https://..."  type: GET/POST ];
```

### Data Types Quick Reference

```deluge
// String
text = "Hello";

// Number
count = 42;

// Decimal
price = 99.99;

// Boolean
flag = true;

// List
items = {"a", "b", "c"};
items.add("d");
item = items.get(0);

// Map
data = Map();
data.put("key", "value");
value = data.get("key");
```
## 6.7 Custom Functions

### What Are Custom Functions?

Custom Functions are Deluge scripts that execute when triggered. They provide unlimited automation possibilities beyond standard actions.


### When to Use Custom Functions

Use custom functions when:
- Standard actions are not sufficient
- Complex logic is required
- Cross-module operations needed
- External API calls required
- Data manipulation needed


### Example Custom Functions

**Auto-Calculate Total**:
```deluge
// Get deal record
deal = zoho.crm.getRecordById("Deals", dealId);

// Get values
subtotal = ifnull(deal.get("Subtotal"), 0);
discount = ifnull(deal.get("Discount"), 0);
taxRate = 0.18;

// Calculate
discountedAmount = subtotal - discount;
tax = discountedAmount * taxRate;
total = discountedAmount + tax;

// Update record
updateMap = Map();
updateMap.put("Tax_Amount", tax);
updateMap.put("Grand_Total", total);
zoho.crm.updateRecord("Deals", dealId, updateMap);
```

**Create Follow-up Record**:
```deluge
// Get original deal
deal = zoho.crm.getRecordById("Deals", dealId);

// Create follow-up task
taskMap = Map();
taskMap.put("Subject", "Follow up on " + deal.get("Deal_Name"));
taskMap.put("Due_Date", zoho.currentdate.addDay(7));
taskMap.put("Status", "Not Started");
taskMap.put("Priority", "High");
taskMap.put("Owner", deal.get("Owner").get("id"));
taskMap.put("What_Id", dealId);

zoho.crm.createRecord("Tasks", taskMap);
```

**Send Custom Notification**:
```deluge
// Get record details
deal = zoho.crm.getRecordById("Deals", dealId);
owner = zoho.crm.getRecordById("Users", deal.get("Owner").get("id"));

// Build message
subject = "Deal Alert: " + deal.get("Deal_Name");
message = "<h2>Deal Update</h2>";
message = message + "<p>Deal: " + deal.get("Deal_Name") + "</p>";
message = message + "<p>Amount: $" + deal.get("Amount") + "</p>";
message = message + "<p>Stage: " + deal.get("Stage") + "</p>";

// Send email
sendmail
[
    from: zoho.adminuserid
    to: owner.get("email")
    subject: subject
    message: message
];
```

### Creating Custom Functions

1. Go to **Setup** > **Automation** > **Actions** > **Custom Functions**
2. Click **+ New Function**
3. Configure:
   - Function Name
   - Module (if record-specific)
   - Arguments
4. Write Deluge code
5. Test with sample data
6. Save
7. Use in Workflow or Button

### Best Practices

| Do | Don't |
|----|-------|
| Handle errors with try-catch | Let errors fail silently |
| Check for null values | Assume fields have data |
| Use meaningful variable names | Use cryptic names |
| Add comments | Write uncommented code |
| Test thoroughly | Deploy untested code |

### Further Reading

- [Custom Functions](https://help.zoho.com/portal/en/kb/flow/user-guide/create-a-flow/articles/using-custom-functions)
- [Deluge Reference](https://www.zoho.com/deluge/)
- [CRM Deluge Tasks](https://www.zoho.com/deluge/help/crm/)

# Day 16 17 and 18
## Module 9: Connecting Zoho CRM to External APIs

## Learning Objectives

By the end of this module, you will be able to:

- Understand the Zoho CRM REST API architecture
- Implement OAuth 2.0 authentication for API access
- Register applications in the Zoho Developer Console
- Generate and manage access and refresh tokens
- Configure appropriate API scopes for your integration
- Perform CRUD operations using the API
- Set up webhooks for real-time external integrations
- Manage API rate limits and credits effectively

---

## 9.1 Introduction to Zoho CRM API

### What is the Zoho CRM API?

The Zoho CRM API is a RESTful interface that allows external applications to interact with your CRM data programmatically. It enables you to build integrations, automate workflows, and connect Zoho CRM with virtually any third-party application.

### API Versions

Zoho CRM currently supports API version 8 (v8), which offers enhanced features and improved performance over previous versions.

| API Version | Status | Base URL |
|-------------|--------|----------|
| V8 | Current | `https://www.zohoapis.com/crm/v8/` |
| V7 | Supported | `https://www.zohoapis.com/crm/v7/` |
| V6 | Legacy | `https://www.zohoapis.com/crm/v6/` |

### API Categories

The Zoho CRM API is organized into several categories:

| Category | Purpose |
|----------|---------|
| **Metadata APIs** | Fetch metadata of modules, fields, layouts, custom views, and related lists |
| **Core APIs** | Perform CRUD operations on CRM module entities |
| **Composite API** | Combine up to five API calls in a single request |
| **Bulk APIs** | Push and retrieve data in bulk using asynchronous APIs |
| **Notification APIs** | Get notified when data changes occur in CRM |
| **Query APIs (COQL)** | Fetch records using SQL-like SELECT queries |

### Why Use the API?

Common use cases for the Zoho CRM API include:

- **Data Synchronization**: Keep CRM data in sync with other business systems (ERP, accounting, marketing automation)
- **Custom Applications**: Build custom web or mobile applications that interact with CRM data
- **Automated Data Entry**: Import leads from websites, forms, or other sources automatically
- **Reporting**: Extract data for custom analytics and reporting
- **Process Automation**: Trigger actions in external systems based on CRM events

### Further Reading

- [Zoho CRM API V8 Documentation](https://www.zoho.com/crm/developer/docs/api/v8/)
- [Zoho Developer Hub](https://www.zoho.com/developer-hub/)

---

## 9.2 OAuth 2.0 Authentication

### Overview

Zoho CRM uses OAuth 2.0 protocol for authentication. OAuth 2.0 is an industry-standard protocol that enables third-party applications to gain delegated access to protected resources without requiring users to share their credentials.

### Benefits of OAuth 2.0

| Benefit | Description |
|---------|-------------|
| **No Password Storage** | Applications don't need to store user passwords |
| **Delegated Access** | Access only resources authorized by the user |
| **Revocable** | Users can revoke access at any time |
| **Token Expiration** | Access tokens expire, limiting exposure in case of breach |
| **Scoped Access** | Control exactly what resources an application can access |

### Key OAuth Terminology

| Term | Definition |
|------|------------|
| **Resource** | CRM data like Leads, Contacts, Deals, etc. |
| **Resource Server** | Zoho CRM server hosting protected resources |
| **Client** | Your application requesting access |
| **Authorization Server** | Zoho Accounts server that issues tokens |
| **Access Token** | Short-lived token to access protected resources |
| **Refresh Token** | Long-lived token to obtain new access tokens |
| **Grant Token** | One-time code exchanged for tokens (valid for 2 minutes) |
| **Scope** | Permissions defining what resources can be accessed |

### Authentication Flow Overview

```
┌─────────────────┐      ┌─────────────────┐      ┌─────────────────┐
│   Your App      │      │  Zoho Accounts  │      │   Zoho CRM      │
└────────┬────────┘      └────────┬────────┘      └────────┬────────┘
         │                        │                        │
         │  1. Authorization      │                        │
         │     Request            │                        │
         │───────────────────────>│                        │
         │                        │                        │
         │  2. User Login &       │                        │
         │     Consent            │                        │
         │<───────────────────────│                        │
         │                        │                        │
         │  3. Grant Token        │                        │
         │<───────────────────────│                        │
         │                        │                        │
         │  4. Exchange for       │                        │
         │     Access Token       │                        │
         │───────────────────────>│                        │
         │                        │                        │
         │  5. Access + Refresh   │                        │
         │     Tokens             │                        │
         │<───────────────────────│                        │
         │                        │                        │
         │  6. API Request with   │                        │
         │     Access Token       │                        │
         │─────────────────────────────────────────────────>
         │                        │                        │
         │  7. CRM Data           │                        │
         │<─────────────────────────────────────────────────
         │                        │                        │
```

### Data Center URLs

Zoho has multiple data centers. Use the appropriate URL based on your account's location:

| Data Center | Accounts URL | API Domain |
|-------------|--------------|------------|
| US | `https://accounts.zoho.com` | `https://www.zohoapis.com` |
| EU | `https://accounts.zoho.eu` | `https://www.zohoapis.eu` |
| India | `https://accounts.zoho.in` | `https://www.zohoapis.in` |
| Australia | `https://accounts.zoho.com.au` | `https://www.zohoapis.com.au` |
| Japan | `https://accounts.zoho.jp` | `https://www.zohoapis.jp` |
| China | `https://accounts.zoho.com.cn` | `https://www.zohoapis.com.cn` |
| Canada | `https://accounts.zohocloud.ca` | `https://www.zohoapis.ca` |

**Important**: Always use the same data center URL consistently throughout the authentication process.

---

## 9.3 Registering Your Application

### Step 1: Access the Developer Console

1. Go to [Zoho API Console](https://api-console.zoho.com/)
2. Sign in with your Zoho account
3. Click **GET STARTED** if this is your first time

### Step 2: Choose Client Type

Zoho supports different client types based on your application architecture:

| Client Type | Use Case | Redirect Required |
|-------------|----------|-------------------|
| **Server-based** | Web applications with backend servers | Yes |
| **Self Client** | Server-to-server integrations, scripts, testing | No |
| **Client-based** | JavaScript/browser-only applications | Yes |
| **Mobile** | iOS/Android mobile applications | Yes |
| **Device** | IoT devices, smart TVs, printers | No |

### Step 3: Register a Server-Based Application

For most integrations, use **Server-based** client type:

1. Click **ADD CLIENT** > **Server-based Applications**
2. Fill in the required details:

| Field | Description | Example |
|-------|-------------|---------|
| **Client Name** | Your application name | `TurboFix Integration` |
| **Homepage URL** | Your application's home page | `https://turbofix.example.com` |
| **Authorized Redirect URI** | URL to receive authorization code | `https://turbofix.example.com/oauth/callback` |

3. Click **CREATE**
4. Save the **Client ID** and **Client Secret** securely

### Step 4: Register a Self Client (For Testing/Scripts)

For quick testing or server-to-server integrations without user interaction:

1. Click **ADD CLIENT** > **Self Client**
2. Enter a client name
3. Click **CREATE**
4. Save the Client ID and Client Secret

### Security Best Practices

- **Never expose Client Secret** in client-side code (HTML, JavaScript)
- **Store credentials securely** using environment variables or secret management services
- **Use HTTPS** for all redirect URIs
- **Rotate secrets** periodically if you suspect compromise

### Common Registration Errors

| Error | Cause | Solution |
|-------|-------|----------|
| Invalid client name | Special characters used | Use only alphanumeric, underscore (_), and ampersand (&) |
| Invalid redirect URI | Missing protocol | Include `http://` or `https://` |
| Invalid JavaScript domain | Wrong format | Must start with `http://` or `https://` |

---

## 9.4 Access and Refresh Tokens

### Generating the Authorization Code (Grant Token)

#### For Server-Based Applications

Construct the authorization URL and redirect users to it:

```
https://accounts.zoho.com/oauth/v2/auth?
  scope=ZohoCRM.modules.ALL&
  client_id={your_client_id}&
  response_type=code&
  access_type=offline&
  redirect_uri={your_redirect_uri}
```

**Parameters**:

| Parameter | Required | Description |
|-----------|----------|-------------|
| `scope` | Yes | Permissions requested (see Section 9.5) |
| `client_id` | Yes | Your application's Client ID |
| `response_type` | Yes | Must be `code` |
| `access_type` | Yes | `offline` for refresh token, `online` for access only |
| `redirect_uri` | Yes | Must match registered redirect URI |
| `state` | No | Optional CSRF protection parameter |

When the user approves, Zoho redirects to your URI with the grant token:

```
https://turbofix.example.com/oauth/callback?code=1000.abc123xyz...
```

**Important**: The grant token is valid for only **2 minutes**.

#### For Self Client (No User Interaction)

1. Go to the API Console
2. Select your Self Client
3. Click **Generate Code**
4. Enter the required scope (e.g., `ZohoCRM.modules.ALL`)
5. Select **Time Duration** (1-10 minutes)
6. Click **CREATE**
7. Copy the generated code immediately

### Exchanging Grant Token for Access Token

Make a POST request to exchange the grant token:

**Endpoint**: `POST https://accounts.zoho.com/oauth/v2/token`

**Request (as form-data)**:

```bash
curl -X POST "https://accounts.zoho.com/oauth/v2/token" \
  -d "grant_type=authorization_code" \
  -d "client_id={your_client_id}" \
  -d "client_secret={your_client_secret}" \
  -d "redirect_uri={your_redirect_uri}" \
  -d "code={grant_token}"
```

**Response**:

```json
{
  "access_token": "1000.abc123...",
  "refresh_token": "1000.xyz789...",
  "api_domain": "https://www.zohoapis.com",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

**Response Fields**:

| Field | Description |
|-------|-------------|
| `access_token` | Token to make API calls (valid for 1 hour) |
| `refresh_token` | Token to generate new access tokens (long-lived) |
| `api_domain` | Base URL for API calls |
| `token_type` | Always "Bearer" |
| `expires_in` | Seconds until access token expires (3600 = 1 hour) |

### Refreshing Access Tokens

Access tokens expire after 1 hour. Use the refresh token to get a new access token:

**Endpoint**: `POST https://accounts.zoho.com/oauth/v2/token`

```bash
curl -X POST "https://accounts.zoho.com/oauth/v2/token" \
  -d "grant_type=refresh_token" \
  -d "client_id={your_client_id}" \
  -d "client_secret={your_client_secret}" \
  -d "refresh_token={your_refresh_token}"
```

**Response**:

```json
{
  "access_token": "1000.new_token...",
  "api_domain": "https://www.zohoapis.com",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

**Note**: Refresh tokens do not expire unless revoked. Store them securely.

### Client Credentials Flow (Simplified)

For simpler use cases, use the client credentials flow:

```bash
curl -X POST "https://accounts.zoho.com/oauth/v2/token" \
  -d "grant_type=client_credentials" \
  -d "client_id={your_client_id}" \
  -d "client_secret={your_client_secret}" \
  -d "scope={scope}" \
  -d "soid={organization_id}"
```

**Note**: This flow does not provide a refresh token.

### Common Token Errors

| Error | Cause | Solution |
|-------|-------|----------|
| `invalid_code` | Grant token expired or already used | Generate a new grant token |
| `invalid_client` | Wrong client ID/secret or DC mismatch | Verify credentials and use correct DC |
| `invalid_redirect_uri` | Redirect URI mismatch | Use exact URI registered in console |

---

## 9.5 API Scopes

### Understanding Scopes

Scopes define the specific permissions your application requests. They follow a standard format:

```
{service_name}.{scope_name}.{operation_type}
```

**Example**: `ZohoCRM.modules.leads.READ`

| Component | Description | Example |
|-----------|-------------|---------|
| Service Name | The Zoho service | `ZohoCRM` |
| Scope Name | Resource type | `modules`, `settings`, `users` |
| Operation Type | Permission level | `READ`, `CREATE`, `UPDATE`, `DELETE`, `ALL` |

### Common CRM Scopes

#### Module Scopes

| Scope | Permission |
|-------|------------|
| `ZohoCRM.modules.ALL` | Full access to all modules |
| `ZohoCRM.modules.leads.ALL` | Full access to Leads module |
| `ZohoCRM.modules.contacts.READ` | Read-only access to Contacts |
| `ZohoCRM.modules.deals.CREATE` | Create access for Deals |
| `ZohoCRM.modules.custom.ALL` | Access to custom modules |

#### Settings Scopes

| Scope | Permission |
|-------|------------|
| `ZohoCRM.settings.ALL` | Full access to all settings |
| `ZohoCRM.settings.modules.READ` | Read module metadata |
| `ZohoCRM.settings.fields.READ` | Read field metadata |
| `ZohoCRM.settings.profiles.READ` | Read profile information |

#### Other Scopes

| Scope | Permission |
|-------|------------|
| `ZohoCRM.users.ALL` | Access to user information |
| `ZohoCRM.org.ALL` | Access to organization data |
| `ZohoCRM.notifications.ALL` | Manage notification channels |
| `ZohoCRM.bulk.ALL` | Bulk read/write operations |
| `ZohoCRM.coql.READ` | Execute COQL queries |

### Multiple Scopes

Combine multiple scopes with commas:

```
scope=ZohoCRM.modules.leads.ALL,ZohoCRM.modules.contacts.ALL,ZohoCRM.settings.modules.READ
```

### Scope Best Practices

- **Principle of Least Privilege**: Request only the scopes you need
- **Granular Permissions**: Use specific module scopes instead of `modules.ALL` when possible
- **Read vs Write**: If you only need to read data, use `READ` scope
- **Document Requirements**: Clearly document which scopes your application needs and why

---

## 9.6 Making API Calls

### Request Structure

All Zoho CRM API requests follow this pattern:

**Headers**:

```
Authorization: Zoho-oauthtoken {access_token}
Content-Type: application/json
```

**Base URL**: Use the `api_domain` from your token response (e.g., `https://www.zohoapis.com`)

### Example: Get Records

**Request**:

```bash
curl -X GET "https://www.zohoapis.com/crm/v8/Leads" \
  -H "Authorization: Zoho-oauthtoken 1000.abc123..."
```

**Response**:

```json
{
  "data": [
    {
      "id": "5725767000000419001",
      "Company": "Zylker Inc",
      "First_Name": "John",
      "Last_Name": "Doe",
      "Email": "john.doe@zylker.com"
    }
  ],
  "info": {
    "per_page": 200,
    "count": 1,
    "page": 1,
    "more_records": false
  }
}
```

### Using Deluge (invokeurl)

Within Zoho CRM custom functions, use `invokeurl` to call external APIs:

```deluge
// Call an external API
response = invokeurl
[
    url: "https://api.example.com/data"
    type: GET
    headers: {"Authorization": "Bearer external_token", "Content-Type": "application/json"}
];
// Parse the response
data = response.toMap();
info data;
// Call with POST and body
postResponse = invokeurl
[
    url: "https://api.example.com/create"
    type: POST
    headers: {"Authorization": "Bearer external_token", "Content-Type": "application/json"}
    parameters: {"name": "Test", "value": 123}.toString()
];
```

### Using CRM Connections in Deluge

For calling Zoho CRM API from other Zoho apps:

```deluge
// Using a pre-configured connection
response = invokeurl
[
    url: "https://www.zohoapis.com/crm/v8/Leads"
    type: GET
    connection: "crm_oauth_connection"
];
info response;
```

### HTTP Methods

| Method | Purpose | Example Endpoint |
|--------|---------|------------------|
| `GET` | Retrieve records | `GET /crm/v8/Leads` |
| `POST` | Create records | `POST /crm/v8/Leads` |
| `PUT` | Update records | `PUT /crm/v8/Leads` |
| `DELETE` | Delete records | `DELETE /crm/v8/Leads?ids=123,456` |

---

## 9.7 Core API Operations

### Get Records

Retrieve records from a module:

```bash
# Get all Leads (paginated)
GET /crm/v8/Leads

# Get specific fields
GET /crm/v8/Leads?fields=First_Name,Last_Name,Email

# Pagination
GET /crm/v8/Leads?page=2&per_page=100

# Sort records
GET /crm/v8/Leads?sort_by=Created_Time&sort_order=desc
```

### Get Record by ID

```bash
GET /crm/v8/Leads/5725767000000419001
```

### Search Records

Use the Search API with criteria:

```bash
# Search by email
GET /crm/v8/Leads/search?email=john@example.com

# Search with criteria
GET /crm/v8/Leads/search?criteria=(Company:equals:Zylker)

# Multiple criteria with AND
GET /crm/v8/Leads/search?criteria=((Company:equals:Zylker)and(Lead_Status:equals:Contacted))
```

### Create Records

```bash
POST /crm/v8/Leads
Content-Type: application/json

{
  "data": [
    {
      "Company": "TurboFix Auto Care",
      "First_Name": "Sarah",
      "Last_Name": "Johnson",
      "Email": "sarah@turbofix.com",
      "Phone": "555-0123",
      "Lead_Source": "Website"
    }
  ]
}
```

**Response**:

```json
{
  "data": [
    {
      "code": "SUCCESS",
      "details": {
        "id": "5725767000000420001",
        "Created_By": {...},
        "Created_Time": "2024-01-15T10:30:00-08:00"
      },
      "message": "record added",
      "status": "success"
    }
  ]
}
```

### Update Records

```bash
PUT /crm/v8/Leads
Content-Type: application/json

{
  "data": [
    {
      "id": "5725767000000420001",
      "Lead_Status": "Contacted",
      "Description": "Interested in premium service package"
    }
  ]
}
```

### Upsert Records

Create or update based on duplicate check:

```bash
POST /crm/v8/Leads/upsert
Content-Type: application/json

{
  "data": [
    {
      "Email": "sarah@turbofix.com",
      "Lead_Status": "Qualified"
    }
  ],
  "duplicate_check_fields": ["Email"]
}
```

### Delete Records

```bash
DELETE /crm/v8/Leads?ids=5725767000000420001,5725767000000420002
```

### COQL (CRM Object Query Language)

Execute SQL-like queries:

```bash
POST /crm/v8/coql
Content-Type: application/json

{
  "select_query": "SELECT First_Name, Last_Name, Email FROM Leads WHERE Lead_Status = 'Qualified' LIMIT 100"
}
```

**Supported COQL Features**:

- `SELECT` with specific fields
- `WHERE` with conditions
- `ORDER BY` for sorting
- `LIMIT` and `OFFSET` for pagination
- `IN`, `BETWEEN`, `LIKE` operators

---

## 9.8 Webhooks for External Integration

### What Are Webhooks?

Webhooks allow Zoho CRM to send real-time notifications to external applications when specific events occur (record creation, update, deletion). Unlike polling the API, webhooks push data immediately when changes happen.

### Webhook vs API Polling

| Aspect | Webhooks | API Polling |
|--------|----------|-------------|
| Timing | Real-time | Scheduled intervals |
| Efficiency | Only triggered on events | Constant requests |
| API Credits | Doesn't consume credits | Consumes credits |
| Complexity | Requires endpoint setup | Simpler implementation |

### Creating a Webhook via UI

1. Go to **Setup** > **Automation** > **Actions** > **Webhooks**
2. Click **Configure Webhook**
3. Fill in the details:

| Field | Description |
|-------|-------------|
| Name | Descriptive name for the webhook |
| URL | External endpoint to receive data |
| Method | GET, POST, or PUT |
| Module | Which module triggers the webhook |
| Parameters | Data to send (CRM fields, custom values) |

### Webhook Configuration Options

**URL Parameters** (for GET requests):

```
https://api.example.com/webhook?lead_id=${!Leads.Id}&email=${!Leads.Email}
```

**Body Parameters** (for POST/PUT):

- **Form Data**: Key-value pairs
- **Raw Data**: JSON, XML, or custom format

**Custom Headers**:

```json
{
  "X-API-Key": "your-api-key",
  "Content-Type": "application/json"
}
```

### Creating Webhooks via API

```bash
POST /crm/v8/settings/automation/webhooks
Authorization: Zoho-oauthtoken {access_token}
Content-Type: application/json

{
  "webhooks": [
    {
      "name": "New Lead Notification",
      "url": "https://api.example.com/new-lead",
      "method": "POST",
      "module": {
        "api_name": "Leads"
      },
      "headers": {
        "custom_parameters": [
          {
            "name": "X-API-Key",
            "value": "your-api-key"
          }
        ],
        "module_parameters": [
          {
            "name": "lead_email",
            "value": "${!Leads.Email}"
          }
        ]
      },
      "body": {
        "type": "form_data",
        "form_data_content": {
          "module_parameters": [
            {
              "name": "lead_name",
              "value": "${!Leads.Full_Name}"
            },
            {
              "name": "lead_phone",
              "value": "${!Leads.Phone}"
            }
          ]
        }
      }
    }
  ]
}
```

### Merge Fields

Use merge fields to include dynamic CRM data:

| Merge Field | Description |
|-------------|-------------|
| `${!Module.Field}` | Field value from the record |
| `${!Leads.Id}` | Record ID |
| `${!Leads.Owner}` | Record owner |
| `${!Leads.Created_Time}` | Creation timestamp |

### Associating Webhooks with Workflow Rules

1. Create a Workflow Rule (Setup > Automation > Workflow Rules)
2. Define trigger conditions
3. Add **Instant Action** > **Webhook**
4. Select your configured webhook

### Notification APIs (Alternative to Webhooks)

Use Notification APIs to subscribe to CRM events:

```bash
POST /crm/v8/actions/watch
Content-Type: application/json

{
  "watch": [
    {
      "channel_id": "1000000068001",
      "events": ["Leads.create", "Leads.edit", "Leads.delete"],
      "channel_expiry": "2024-12-31T23:59:59+05:30",
      "notify_url": "https://api.example.com/notifications"
    }
  ]
}
```

---

## 9.9 API Rate Limits and Credits

### Credit-Based System

Zoho CRM API usage is measured in credits. Each API call consumes credits based on the operation:

| API Operation | Credits Consumed |
|---------------|------------------|
| Standard API call | 1 credit |
| Convert Lead | 5 credits |
| Bulk Read | 10 credits |
| Bulk Write | 10 credits |
| File Upload | 5 credits |

### Credit Limits by Edition

| Edition | Base Credits | Per User Bonus |
|---------|--------------|----------------|
| Free | 5,000/day | +250/user |
| Standard | 50,000/day | +250/user |
| Professional | 75,000/day | +250/user |
| Enterprise | 100,000/day | +500/user |
| Ultimate | 100,000/day | +1,000/user |

**Example**: Enterprise with 50 users = 100,000 + (50 × 500) = 125,000 credits/day

### Concurrency Limits

Concurrent requests are limited per edition:

| Edition | Max Concurrent Requests |
|---------|------------------------|
| Free | 5 |
| Standard | 10 |
| Professional | 15 |
| Enterprise | 20 |
| Ultimate | 25 |

### Sub-Concurrency Limits

Certain operations have additional limits:

| Operation | Max Concurrent |
|-----------|----------------|
| Convert Lead | 10 |
| Mass Update | 10 |
| Bulk Read/Write | 10 |

### Checking API Usage

View your API usage in CRM:

1. Go to **Setup** > **Developer Space** > **APIs**
2. Check the **Usage** section for daily consumption

### Rate Limit Headers

API responses include rate limit information:

```
X-RATELIMIT-LIMIT: 100000
X-RATELIMIT-REMAINING: 99500
X-RATELIMIT-RESET: 1705363200
```

### Handling Rate Limits

**HTTP 429 Response** indicates rate limit exceeded:

```json
{
  "code": "LIMIT_EXCEEDED",
  "message": "API limit reached for today",
  "status": "error"
}
```

**Best Practices**:

- Implement exponential backoff for retries
- Batch operations where possible (up to 100 records per request)
- Use Bulk APIs for large data operations
- Cache frequently accessed data
- Monitor usage and optimize queries

### Deluge Integration Task Credits

API calls made through Deluge integration tasks (e.g., `zoho.crm.searchRecords()`) also consume credits equivalent to the corresponding API call.

---

## 9.10 Best Practices and Troubleshooting

### Security Best Practices

| Practice | Implementation |
|----------|----------------|
| **Secure Storage** | Store Client Secret and Refresh Token in environment variables or secret managers |
| **HTTPS Only** | Always use HTTPS for redirect URIs and API calls |
| **Token Rotation** | Implement automatic access token refresh before expiry |
| **Scope Minimization** | Request only necessary scopes |
| **Audit Logging** | Log API calls for troubleshooting and security auditing |

### Performance Best Practices

```deluge
// BAD: Multiple API calls
for each lead in leadIds
{
    record = zoho.crm.getRecordById("Leads", lead);
    // Process record
}
// GOOD: Batch request
records = zoho.crm.getRecords("Leads", 1, 200);
for each record in records
{
    // Process record
}
```

**Recommendations**:

- Batch creates/updates (up to 100 records per request)
- Use `fields` parameter to fetch only needed fields
- Implement caching for static data
- Use COQL for complex queries instead of multiple API calls
- Leverage Bulk APIs for large data operations

### Error Handling

**Common HTTP Status Codes**:

| Code | Meaning | Action |
|------|---------|--------|
| 200 | Success | Process response |
| 201 | Created | Record created successfully |
| 204 | No Content | Delete successful |
| 400 | Bad Request | Check request format |
| 401 | Unauthorized | Refresh access token |
| 403 | Forbidden | Check scopes and permissions |
| 404 | Not Found | Verify record/module exists |
| 429 | Rate Limited | Implement backoff and retry |
| 500 | Server Error | Retry with backoff |

**Example Error Handling in Deluge**:

```deluge
try
{
    response = invokeurl
    [
        url: "https://www.zohoapis.com/crm/v8/Leads"
        type: GET
        connection: "crm_connection"
    ];
    
    if(response.get("data") != null)
    {
        leads = response.get("data");
        // Process leads
    }
    else if(response.get("code") != null)
    {
        errorCode = response.get("code");
        errorMessage = response.get("message");
        info "API Error: " + errorCode + " - " + errorMessage;
    }
}
catch(e)
{
    info "Exception: " + e;
}
```

### Common Errors and Solutions

| Error | Cause | Solution |
|-------|-------|----------|
| `INVALID_TOKEN` | Access token expired | Refresh the access token |
| `INVALID_CODE` | Grant token expired | Generate new grant token within 2 minutes |
| `INVALID_CLIENT` | Wrong Client ID/Secret | Verify credentials in API Console |
| `NO_PERMISSION` | Insufficient scope | Add required scope and regenerate tokens |
| `DUPLICATE_DATA` | Record already exists | Use upsert or check before creating |
| `MANDATORY_NOT_FOUND` | Required field missing | Include all mandatory fields |
| `INVALID_DATA` | Wrong data format | Check field data types |

### Debugging Tips

1. **Enable Logging**: Log all API requests and responses
2. **Use Postman**: Test API calls before implementing in code
3. **Check API Console**: Verify scopes and client configuration
4. **Validate JSON**: Use JSON validators for request bodies
5. **Test in Sandbox**: Use Zoho CRM Sandbox for testing (Enterprise+)

### Testing Your Integration

```deluge
// Test function to verify API connectivity
testApiConnection = void()
{
    try
    {
        // Test getting modules metadata
        response = invokeurl
        [
            url: "https://www.zohoapis.com/crm/v8/settings/modules"
            type: GET
            connection: "crm_connection"
        ];
        
        if(response.get("modules") != null)
        {
            info "API Connection Successful!";
            info "Available modules: " + response.get("modules").size();
        }
        else
        {
            info "API Response: " + response;
        }
    }
    catch(e)
    {
        info "Connection Failed: " + e;
    }
}
```

---

## Exercises

### Exercise 9.1: OAuth Setup

1. Register a Self Client in the Zoho API Console
2. Generate a grant token with scope `ZohoCRM.modules.leads.ALL`
3. Exchange the grant token for access and refresh tokens
4. Store the tokens securely

### Exercise 9.2: First API Call

Using your access token:

1. Make a GET request to retrieve all Leads
2. Create a new Lead with Company, First Name, Last Name, and Email
3. Update the Lead's status to "Contacted"
4. Verify the changes by fetching the record again

### Exercise 9.3: Webhook Integration

1. Create a webhook that sends Lead data to a test endpoint (use webhook.site for testing)
2. Configure the webhook with:
   - Lead Name
   - Email
   - Phone
   - Creation Time
3. Create a workflow rule to trigger the webhook on Lead creation
4. Test by creating a new Lead

### Exercise 9.4: Error Handling

Write a Deluge function that:

1. Attempts to fetch a record by ID
2. Handles the case where the record doesn't exist
3. Handles authentication errors
4. Logs all errors appropriately

---

## Knowledge Check

Before completing this module, ensure you can answer:

1. What authentication protocol does Zoho CRM API use?

2. What is the difference between an access token and a refresh token?

3. How long is an access token valid?

4. What is the purpose of API scopes?

5. How do you handle rate limiting in your integration?

6. What is the advantage of using webhooks over API polling?

7. How many records can you create/update in a single API call?

8. What HTTP status code indicates rate limiting?

---

## Summary

In this module, you learned:

- **API Overview**: Zoho CRM provides RESTful APIs for integrating with external applications

- **OAuth 2.0**: The authentication mechanism using Client ID, Client Secret, and tokens

- **Token Management**: How to generate, use, and refresh access tokens

- **Scopes**: Permissions that control what your application can access

- **API Operations**: CRUD operations, searching, and COQL queries

- **Webhooks**: Real-time notifications for CRM events

- **Rate Limits**: Credit-based system and how to optimize API usage

- **Best Practices**: Security, performance, and error handling strategies

**Key Principle**: The Zoho CRM API opens unlimited integration possibilities. Start with clear authentication, use appropriate scopes, handle errors gracefully, and monitor your API usage for a robust integration.

---

## Additional Resources

### Official Documentation

- [Zoho CRM API V8 Documentation](https://www.zoho.com/crm/developer/docs/api/v8/)
- [OAuth 2.0 Overview](https://www.zoho.com/crm/developer/docs/api/v8/oauth-overview.html)
- [API Scopes Reference](https://www.zoho.com/crm/developer/docs/api/v8/scopes.html)
- [Webhook Documentation](https://www.zoho.com/crm/developer/docs/api/v8/create-webhook.html)
- [API Limits](https://www.zoho.com/crm/developer/docs/api/v8/api-limits.html)

### Tools and Testing

- [Zoho API Console](https://api-console.zoho.com/)
- [Postman](https://www.postman.com/) - For testing API calls
- [Webhook.site](https://webhook.site/) - For testing webhooks

### Community Resources

- [Zoho Developer Community](https://help.zoho.com/portal/community/zoho-crm)
- [Zoho CRM API Directory](https://www.zoho.com/crm/developer/docs/api-directory.html)