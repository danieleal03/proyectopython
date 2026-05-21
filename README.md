# proyectopython
programa para tienda
menu=[["Numero","Nombre","Categoria","Precio"],
      [1,"Pizza","Comida",1000],
      [2,"Hamburguesa","Comida",800],
        [3,"Coca-cola","Bebida",500],
        [4,"Agua","Bebida",300],
        [5,"Helado","Postre",400],
        [6,"Pastel","Postre",600]
]

print(menu)

def precio_final(Numero):
    for producto in menu[1:]:
        if producto[0]==Numero:
            Nombre=producto[1]
            Categoria=producto[2]
            Precio=producto[3]
            if Categoria=="Comida" and Precio<1000:
                    precio_final=Precio-(Precio*0.15)
            else:
                    precio_final=Precio

            print("Producto:",Nombre)
            print("Categoria:",Categoria)
            print("Precio original:",Precio)            
            return "Precio final:" + str(precio_final)  
          
    return "Producto no encontrado"
        
Numero=int(input("Ingrese el numero del producto: "))
print(precio_final(Numero))
