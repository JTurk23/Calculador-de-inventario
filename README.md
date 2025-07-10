1- Descargar inventario de la semana
2- correr Google colab y eliminar duplicados, y solo mantener
 Item Number,	Item Description, Eaches/Weight Per Case, Actual Quantity
3 - Descargar Archivo en formato Excel y pegarlo en el inventario1MACRO

Luego,
4 - Desde Weekly Offering Lockdown Tool - 2025-W29, la pestana Official PCK Import. Copiar pagina y pegarla en excel.
5 - correr en otro colab y solo mantener columnas y cambiar nombres# Keep only the columns you want

columns_to_keep = [
    'Week',
    'Slot',
    'Name',
    'SKU Name',
    'Purchasing Picks 2P',
    'Purchasing Picks 4P',
    'Full SKU',
    'Category',
    'Storage Location',
    'SKU Type'
]

df = df[columns_to_keep]

# Rename the columns as specified
df = df.rename(columns={
    'Slot': 'Recipe',
    'Purchasing Picks 2P': '2p_Qty',
    'Purchasing Picks 4P': '4p_Qty',  # Note: Fixing typo from your message (4P vs 4P)
    'Full SKU': 'Item Number',
    'SKU Name': 'Item Description'
})

# Verify the changes
print(df.info())
print(df.head())


6 - Descargar Archivo en formato Excel y pegarlo en el inventario1MACRO
7 - Descargar en un archivo excel el plan de produccion de kitting
8  - Pegar el archivo inventario1MACRO, en la pestana Kitting_Plan
9 - Correr en Requirements  ver resultados.
