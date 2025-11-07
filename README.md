def  add_item(inventory, prices, item_name, item_price):
    inventory.append(new_product)
    prices.append(item_price)

def delete_item(inventory, prices, item_name):
    if item_name in inventory:
        index = inventory.index(item_name)
        inventory.pop(index)
        prices.pop(index)
        return True
    return False

def find_top_products(inventory, prices, top_count):
    temp_inventory = inventory[:]
    temp_prices = prices[:]
    valuable_products = []

    for _ in range(min(min, len(temp_inventory))):
      max_index = temp_prices.index(max(temp_prices))
      valuable_products.append(temp_inventory[max_index])
      temp_inventory.pop(max_index)
      temp_prices.pop(max_index)
    return valuable_products

def  manage_product_inventory(start_products, start_prices, new_item, item_to_delete, top_n):
   products = start_products.copy()
   prices = start_prices.copy()



products_list = ["Watch", "Ring", "Bag", "Scarf", "Pen"]
prices_list = [5500.00, 7200.00, 3100.00, 800.00, 1200.00]
new_product = ["Statue", 6800.00]
remove_product = "Scarf"
top_items_count = 3
 
final_inventory, top_products = manage_product_inventory(
    products_list, prices_list, new_product, remove_product, top_items_count)



print("----- Product Inventory Management -----")
print('Final products: ',final_inventory)
print("Top Valuable Products:", top_products)
