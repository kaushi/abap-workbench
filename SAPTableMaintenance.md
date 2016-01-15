# Create & Maintain Table (SE11) #

This wiki guides you how to create and maintain tables.

### ABAP Dictionary: Initial Screen ###

Go to ABAP Dictionary
_Tools > ABAP Workbench > Development > ABAP Dictionary_

Type the name of the table in **_Database Table_** text box.

Choose **_Display_**, **_Change_** or **_Create_**.

### Dictionary: Maintain Table Screen ###

Click on the delivery class.

The delivery class controls the transport of table data when installing or upgrading, in a client copy and when transporting between customer systems.

There are the following delivery classes:
  * A : Application table (master and transaction data).
  * C : Customer table, data is maintained by the customer only.
  * L : Table for storing temporary data.
  * G : Customer table, SAP may insert new data records, but may not overwrite or delete existing data records. The customer namespace must be defined in table TRESC.
  * E : System table with its own namespaces for customer entries. The customer namespace must be defined in table TRESC.
  * S : System table, data changes have the same status as program changes.
  * W : System table (e.g. table of the development environment) whose data is transported with its own transport objects.

You can choose the option **_Customized table_**

On **_Object Directory Entry_** dialog, select the package to save.

Go to **_Technical Settings_**

### Dictionary : Maintain Technical Settings ###

The technical settings define how the table is created on the database.

Set the Local Storage Parameters:

Choose **APPL2** from the **_Data Class_** dropdown box.

Select the Size **_Category_** (0-4).

Click **Save** and **Active** button.