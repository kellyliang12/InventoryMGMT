# INFS2605 Assignment - InventoryManager by *Hello World*
An inventory manager application to track orders from various suppliers built on OpenJDK 11.0.8 and OpenJFX 11 platform with SQLite as a datastore. The application has prefilled data for testing.

## Running the application ##
To run the application, please use an IDE (prefereabbly NetBeans) to **clean and build the project before running** it.
Additionally, *ensure that OpenJDK 11 and OpenJFX 11 are installed in your machine*.

## Logging in ##
The following accounts can be used to log into InventoryManager.
Username | Password | User Type 
-------- | -------- | ---------
**jack.chu** | **d0ve** | Employee
**sven** | **metaball** | Supplier (*Nestly*)
**hpc141** | **password** | Supplier (*DaireFarmers*)

Select the appropriate radio button for employee or supplier login. A supplier has limited access, preventing them to create new orders or edit orders from another supplier.

## Dashboard ##
The dashboard is the homepage of the application. Users can view orders in a table and view pie chart of the order status. Filters on both these views can be imposed bsed on product or order status. Additionally, users can do the following functions:
* **View all suppliers** by clicking the *View all suppliers* button on the toolbar [*employees only*]
* **Reload** the page by clicking the :arrows_counterclockwise: button on the toolbar to reset the filters
* View the **About** page by clicking on the :grey_exclamation: button, a new window will appear.
* **Logout** by clicking the *Logout* button, the login page will reappear.
* **Create a new order** by clicking on the *:heavy_plus_sign: Create a new order* button, a new window will appear.
* **Edit an order** by first selecting an order from the table and then clicking on the button with the :pencil2:, a new window will appear [*suppliers can only edit orders associated with them*].

### Creating a new order ###
To create orders with only **one item**, fill out the product, quantity, supplier and status fields then click on the *Create order* button. The status field is set to *Order placed* as deafult.

To create orders with **multiple items**, add each order item using the :heavy_plus_sign: button. This will insert the items into the order. To delete an order item, select the row from the table then click on the :wastebasket: button. Once staisfied, select a supplier and status, and clikc on *Create order*. A filled product and quantity field will also be added to the order even if it has not been added to the table. It is not possible to have multiple orders of the same product in the same order.

Error checks have been implemented to check inputs.

### Editing an order ###
Products placed on the same order is displayed in a table on the screen. Select the row which prefills the fields to edit. Then click on :heavy_check_mark: to submit changes, the table will reflect these changes. :wastebasket: deletes the selected order item. New order items can also be inseted by filling the fields and clicking on :heavy_plus_sign:.

Supplier and status can be changed by selecting its values using the combobox. Note: suppliers cannot change the order's supplier. Confirm these changes by pressing the enter key or the *Confirm* button. A confirmation screen will popup.

Orders can be deleted with the *Delete Order* button.
> Note: deleting an order deletes all order items associated with that order.

When an order is edited, the user and timestamp will be recorded and displayed for tracking changes.

## Supplier screen ###
A table displays suppliers along with their data. Similarly to the dashboard, employees are able to refresh, logout, access the about screen. Employees can also:
* **Switch to dashboard** by clicking on :house:.
* **Create a new supplier** by clicking on :heavy_plus_sign:, a new window will appear.
* **Edit a supplier** by selecting the supplier from the table and clikcing on :pencil2:, a new window will appear.

### Creating a new supplier ###
Creating a new supplier is as simple as filling out the three text fields and clicking on *Add Supplier* . The supplier_id is autogenerated.

### Editing an existing supplier ###
Once in the edit screen page, edit the supplier by changing the textfield values and clicking on *confirm*.
> Note: changing the supplier name will also reflect on orders.

A supplier can be deleted by clicking on :wastebasket:.
> Note: deleting a supplier will also delete its associated orders.

## Future improvements ##
These are future improvements that we have in mind:
- [ ] Sign-up function,
- [ ] Responsive winows,
- [ ] Password hashing,
- [ ] Dark mode,
- [ ] Split address fields into components,
- [ ] Customisable fields (i.e. users can choose to add price).
