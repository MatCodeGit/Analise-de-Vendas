# Analise-de-Vendas

#importar o pandas

import pandas as pd


# Carregar um arquivo Excel ou CSV

caminho = r"C:\Users\MFS0625\Desktop\Py para dados\analise_vendas_2026.xlsx"
df = pd.read_excel("analise_vendas_2026.xlsx", sheet_name="Base_Vendas")

# informa quantas linhas da base mostrar.
print(df.head())




