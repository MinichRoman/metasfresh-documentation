---
title: How do I pick a sales order for shipments using handling units? (Picking Terminal)
layout: default
tags:
  - Sales
  - Order Picking (Picking Terminal)
lang: en
sequence: 10
ref: order_picking_terminal
---

## Overview
In metasfresh, you can choose and pick *handling units* ([HUs](Handling_Unit_System)) to prepare shipments. The picked quantities are deducted from stock afterwards.<br>
You can check your stock inventory at any time in the "[Handling Unit Editor](Menu)".

## Requirements
- [Create a sales order](SalesOrder_recording) and [complete it](DocumentProcessingComplete).

## Steps
1. Open "Picking Terminal" from the [menu](Menu).
1. ***Optional:*** [Use the filtering function](Filtering_function), to help you find the desired product for which you want to pick an HU.
1. From the [list view](ViewModes#list-view), [select](RecordSelection) the product.
1. [Start the quick action](StartAction#quick-actions) "Pick". The picking window opens up.
1. In the left pane of the picking window, [select](RecordSelection) the sales order to be picked.
1. In the right pane, [select](RecordSelection) a picking slot, e.g., "101.0", and [start the quick action](StartAction#quick-actions) "Open HU selection window".
1. [Select](RecordSelection) an HU and [start the quick action](StartAction#quick-actions) "Pick HU". The HU will now be moved to the picking slot 101.0.
 >**Note:** If the required HU isn't listed, check if a [filter](Filtering_function) is set and clear it to see more suggestions.

1. [Select](RecordSelection) the HU line and [start the quick action](StartAction#quick-actions) "Process picking". This makes the HU line read-only.
 >**Note:** The HU line must be selected for the quick action to become available.<br><br>
 ![](../DE/assets/Kommissionierung_HU_auswählen.png)

1. Click "Done" to close the picking window.

## Next Steps
- [Create a shipment with picked quantities](Ship_salesorder_picked_qty).

## Example
![](../DE/assets/Auftrag_kommissionieren.gif)
