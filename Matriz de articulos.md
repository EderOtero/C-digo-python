# Matriz de artículos
# [Código, Nombre, Stock Actual, Stock Mínimo]

inventario = [
    [101, "Teclado", 5, 4],
    [102, "Mouse", 7, 10],
    [103, "Monitor", 3, 8],
    [104, "Impresora", 7, 7],
    [105, "Laptop", 1, 1]
]

# Función para calcular la cantidad a pedir
def calcular_pedido(stock_actual, stock_minimo):
    if stock_actual < stock_minimo:
        return stock_minimo - stock_actual
    else:
        return 0

# Mostrar lista de pedidos
print("LISTA DE REABASTECIMIENTO\n")

for articulo in inventario:
    codigo = articulo[0]
    nombre = articulo[1]
    stock_actual = articulo[2]
    stock_minimo = articulo[3]

    cantidad_pedir = calcular_pedido(stock_actual, stock_minimo)

    print(f"Artículo: {nombre}")
    print(f"Código: {codigo}")
    print(f"Cantidad a pedir: {cantidad_pedir}")
    print("---------------------------")
