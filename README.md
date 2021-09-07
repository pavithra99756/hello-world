import json
file = open('pharmacy.json', 'w')
json.dump(inventory, file )

#$print(json_inventory)

inventory = {
    1200 : {"item": "Amoxicillin" , "price" : 80 , "quantity" : 30 , "category": "Antibiotic" , "rating": 9},
    1201 : {"item": "Azithromycin" , "price" : 80 , "quantity" : 100 , "category": "Antibiotic" , "rating": 8},     
    1202 : {"item": "Paracetamol" , "price" : 40 , "quantity" : 10 , "category": "Antipyretic", "rating": 7}, 
    1203 : {"item": "Albuterol" , "price" : 10 , "quantity" : 100 , "category": "Dilator", "rating": 8}, 
    1204 : {"item": "Amoxicillin(s)" , "price" : 10 , "quantity" : 100 , "category": "AntiBActerial","rating": 7},   
    1205 : {"item": "Amoxicillin(m)" , "price" : 20 , "quantity" : 100 , "category": "AntiBActerial", "rating": 8}, 
    1206 : {"item": "Amocixillin(l)" , "price" : 40 , "quantity" : 50 , "category": "AntiBActerial", "rating": 6},   
    1207 : {"item": "Cefdinir(s)" , "price" : 10 , "quantity" : 300 , "category": "AntiBacterial", "rating": 5},   
    1207 : {"item": "Cefdinir(s)" , "price" : 10 , "quantity" : 300 , "category": "AntiBacterial", "rating": 5},   
    1208 : {"item": "Cefdinir(m)" , "price" : 40 , "quantity" : 400 , "category": "AntiBacterial","rating": 4},   
    1209 : {"item": "Cephalexin" , "price" : 10 , "quantity" : 500 , "category": "AntiBacterial","rating": 10},    
    1210 : {"item": "Fluticasone" , "price" : 1 , "quantity" : 1000 , "category": "Steroid", "rating": 9},    
    1211 : {"item": "Predisolone" , "price" : 1 , "quantity" : 1000 , "category": "Steroid","rating": 8}, 
    1212 : {"item": "Ibuprofen" , "price" : 10 , "quantity" : 200 , "category": "AntiInflammatory","rating": 7},     
    1213 : {"item": "Singulair" , "price" : 100 , "quantity" : 100 , "category": "AntiAllergent","rating": 2},      
    1214 : {"item": "Trimethoprim" , "price" : 5 , "quantity" : 200 , "category": "Antboitic","rating": 3},     
    1215 : {"item": "Tylenol" , "price" : 70 , "quantity" : 80 , "category": "PainKiller","rating": 4},     
    1216 : {"item": "Vicodin" , "price" : 30 , "quantity" : 80 , "category": "Painkiller","rating": 5},    
    1217 : {"item": "Mupirocin" , "price" : 100 , "quantity" : 90 , "category": "AntiBacterial","rating": 8},    
    1218 : {"item": "Nystatin" , "price" : 120 , "quantity" : 40 , "category": "AntiFungal","rating": 9},   
    1219 : {"item": "Dextromorphan(m)" , "price" : 20 , "quantity" : 100 , "category": "Antihistamine","rating": 8}, 
    1220 : {"item": "Dextromorphan(l)" , "price" : 50 , "quantity" : 300 , "category": "Antihistamine","rating": 10}, 
    1221 : {"item": "Phenilephrine" , "price" : 10 , "quantity" : 200 , "category": "Antihistamine","rating": 7}     
    
}

ui_product = int(input("Enter product ID:"))
ui_quantity = int(input("Enter Quantity:"))

product = inventory.get(ui_product)

if product:
  print('product name: ',product.get('item'))
  print('price per unit: ', product.get('price'))
  print('amount to be paid: ', ui_quantity*product.get('price'))
  product['quantity']-=ui_quantity
else:
  print('product not found')
[7:41 am, 07/09/2021] pavithra Mvj: {"1200": {"item": "Amoxicillin", "price": 80, "quantity": 30, "category": "Antibiotic", "rating": 9}, "1201": {"item": "Azithromycin", "price": 80, "quantity": 100, "category": "Antibiotic", "rating": 8}, "1202": {"item": "Paracetamol", "price": 40, "quantity": 10, "category": "Antipyretic", "rating": 7}, "1203": {"item": "Albuterol", "price": 10, "quantity": 100, "category": "Dilator", "rating": 8}, "1204": {"item": "Amoxicillin(s)", "price": 10, "quantity": 100, "category": "AntiBActerial", "rating": 7}, "1205": {"item": "Amoxicillin(m)", "price": 20, "quantity": 100, "category": "AntiBActerial", "rating": 8}, "1206": {"item": "Amocixillin(l)", "price": 40, "quantity": 50, "category": "AntiBActerial", "rating": 6}, "1207": {"item": "Cefdinir(s)", "price": 10, "quantity": 300, "category": "AntiBacterial", "rating": 5}, "1208": {"item": "Cefdinir(m)", "price": 40, "quantity": 400, "category": "AntiBacterial", "rating": 4}, "1209": {"item": "Cephalexin", "price": 10, "quantity": 500, "category": "AntiBacterial", "rating": 10}, "1210": {"item": "Fluticasone", "price": 1, "quantity": 1000, "category": "Steroid", "rating": 9}, "1211": {"item": "Predisolone", "price": 1, "quantity": 1000, "category": "Steroid", "rating": 8}, "1212": {"item": "Ibuprofen", "price": 10, "quantity": 200, "category": "AntiInflammatory", "rating": 7}, "1213": {"item": "Singulair", "price": 100, "quantity": 100, "category": "AntiAllergent", "rating": 2}, "1214": {"item": "Trimethoprim", "price": 5, "quantity": 200, "category": "Antboitic", "rating": 3}, "1215": {"item": "Tylenol", "price": 70, "quantity": 80, "category": "PainKiller", "rating": 4}, "1216": {"item": "Vicodin", "price": 30, "quantity": 80, "category": "Painkiller", "rating": 5}, "1217": {"item": "Mupirocin", "price": 100, "quantity": 90, "category": "AntiBacterial", "rating": 8}, "1218": {"item": "Nystatin", "price": 120, "quantity": 40, "category": "AntiFungal", "rating": 9}, "1219": {"item": "Dextromorphan(m)", "price": 20, "quantity": 100, "category": "Antihistamine", "rating": 8}, "1220": {"item": "Dextromorphan(l)", "price": 50, "quantity": 300, "category": "Antihistamine", "rating": 10}, "1221": {"item": "Phenilephrine", "price": 10, "quantity": 200, "category": "Antihistamine", "rating": 7},
