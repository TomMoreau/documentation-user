=====================================
Proceed to inter-warehouses transfers
=====================================

When owning several warehouses, you might need to transfer goods from one warehouse to another.
Proceeding to such behavior is called *inter-warehouses transfers*. If this action is physically
easy to perform, the administrative part can be arduous. Fortunately, Odoo comes with an intuitive
flow helping save time when registering those transfers.

Configuration
=============

First of all, go to :menuselection:`Configuration --> Settings` and enable **Storage Locations**.
Then, hit save.

.. image:: inter_warehouse/feature-storage-location.png
   :align: center
   :alt: Image of the storage location feature being enabled.

.. tip::
   If you want to manage several routes within your warehouses, then tick the **Multi-Step Routes**
   and check :doc:`use-routes`.

Creating a new warehouse
========================

The next step is to create your new warehouse. To do so, go to :menuselection:`Configuration -->
Warehouse Management --> Warehouses`. Once there, click on **Create**.

Fill out a **Warehouse Name** and a **Short Name**. The short name is 5 characters maximum.

.. image:: inter_warehouse/create-new-warehouse.png
   :align: center
   :alt: View of a new warehouse being created.

.. tip::
   Note that the **Short Name** is important as it appears on your transfer orders and other
   warehouse documents. It might be smart to use an understandable one (e.g.: WH/[first letters of
   location]).

Now, go back to your dashboard. There, new operations related to your warehouse have been
automatically generated.

.. image:: inter_warehouse/new-transfer-types.png
   :align: center
   :alt: Inventory app dashboard displaying new transfer type for the recently created warehouse.

Creating a new inventory
========================

If you create a new warehouse, you might already have an existing inventory in it. In that case, you
should create an inventory in Odoo. If this is not the case, you can skip this step.

Into the inventory application, select :menuselection:`Operations --> Inventory Adjustment`.
Then, create a new inventory by clicking on **Create**. Fill in the **Inventory Reference**,
**Date** and make sure to select the right warehouse and location.

.. image:: inter_warehouse/annual-inventory.png
   :align: center
   :alt: View of the inventory adjustment form before hitting the start button.

Next, click on **Start Inventory**. You will be able to input your existing products in the new
window. Select add an item and indicate the **Real Quantity** available in the warehouse.
The theoretical quantity can not be changed as it represents a computed one from purchase and sales
orders.

.. image:: inter_warehouse/in-progress-annual-inventory.png
   :align: center
   :alt: View of the actual physical inventory of the new warehouse.

.. tip::
   Don't forget to validate your inventory once you have recorded the state of all your products.

Create an internal transfer
===========================

The final step is to create your internal transfer. If you want to transfer 8 units of a product
from your first warehouse to another one, proceed as follows:

From your dashboard, select a internal movement of one of the two warehouses. To do so, click on
:menuselection:`More  --> Planned Transfer`.

.. image:: inter_warehouse/internal-transfer-choice.png
   :align: center
   :alt: View of the choice between planned transfer and immediate transfer.

On the new window, select the source location zone (in this case your "old warehouse") and the
destination location zone (in this case your "new" warehouse).

Add the products you want to transfer by clicking on **Add an Item** and don't forget to
**Save** and **Mark as TODO** once you are done.

.. image:: inter_warehouse/planned-internal-transfer.png
   :align: center
   :alt: View of the internal transfer form.

If you selected **Immediate Transfer**, Odoo would have processed the transfer automatically after
your click on **Validate**.

If you select **Mark as TODO**, Odoo puts the transfer in **Waiting Availability** status.
Click on **Reserve** to reserve the amount of products in your source warehouse.

It is also possible to manually transfer each product:

- Via your dashboard, select the transfer order in the source location.

.. image:: inter_warehouse/in-progress-internal-transfer.png
   :align: center
   :alt: View of the dashboard with a zoom of the pending internal transfer.

- Select the right transfer order.

.. image:: inter_warehouse/internal-transfers-list.png
   :align: center
   :alt: View of the pending internal transfers list.

- Click on the little pencil logo in the lower right corner in order to open the operation details
  window. In this new window you can manually indicate how many products you process.

.. image:: inter_warehouse/backorder.png
   :align: center
   :alt: View of a backorder pop-up window because all products are not moved at the same time.

.. tip::
   If you decide to partially process the transfer order (e.g. a part of the products can't be
   shipped yet due to an unexpected event), Odoo automatically asks if you wish to create a
   **backorder**. Create a backorder if you expect to process the remaining products later,
   do not create a backorder if you will not supply/receive the remaining products.