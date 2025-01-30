import os

def mostrar_codigo(ruta_script):
    # ... (código sin cambios)

def mostrar_menu():
    ruta_base = os.path.dirname(__file__)
    opciones = {}
    contador = 1

    # Busca scripts en el directorio actual y subdirectorios
    for root, _, files in os.walk(ruta_base):
        for file in files:
            if file.endswith(".py") and file != "Dashboard.py":
                ruta_script = os.path.join(root, file)
                opciones[str(contador)] = os.path.relpath(ruta_script, ruta_base)  # Ruta relativa
                contador += 1

    while True:
        # ... (código para mostrar el menú y manejar la entrada del usuario)
