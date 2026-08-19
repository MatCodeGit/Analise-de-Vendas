# Analise-de-Vendas

import pandas as pd

# ---------------------------------------------------------
# 1. CARREGAR OS DADOS
# ---------------------------------------------------------
df = pd.read_excel("analise_vendas_2026.xlsx", sheet_name="Base_Vendas")

# Configuração para mostrar todas as colunas
pd.set_option("display.max_columns", None)


# ---------------------------------------------------------
# 2. TRATAMENTO E TRADUÇÃO DE DADOS
# ---------------------------------------------------------
# Recalcula o Faturamento para corrigir os NaN do Excel
df["Faturamento Total"] = df["Preco_Unitario"] * df["Quantidade"]

print("--- PRIMEIRAS LINHAS DA BASE ---")
print(df.head())


# ---------------------------------------------------------
# 3. ANÁLISE DE NEGÓCIO (Sua primeira entrega!)
# ---------------------------------------------------------
# Pergunta do Gestor: Quanto faturamos por Região?
faturamento_regiao = df.groupby("Regiao")["Faturamento Total"].sum().reset_index()

print("\n--- FATURAMENTO TOTAL POR REGIÃO ---")
print(faturamento_regiao)
