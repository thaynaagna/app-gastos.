# app-gastos.
💰 Controle seus gastos mensais de forma simples! Adicione categorias, registre valores e veja o resumo total. Use direto no celular, rápido e fácil! 📱✨

def bot_gastos():

    print("💰 Cálculo de Gastos Mensais 💰")
    
    gastos = {}
    total = 0

    while True:
        categoria = input("\n👉 Digite a categoria do gasto (ex: 🍔 Alimentação,🚌 Transporte,🎮 Lazer,) ou 'sair' para finalizar: ").strip()
        
        if categoria.lower() == "sair":
            break
        
        try:
            valor = float(input(f"💵 Digite o valor gasto em {categoria}: R$ "))
            gastos[categoria] = gastos.get(categoria, 0) + valor
            total += valor 
            print(f"✅ Gasto de R$ {valor:.2f} adicionado em {categoria}!")
        except ValueError:
            
            print("=============================================================================")
    
    print("\n📌 === Resumo dos Gastos Mensais === 📌")
    for cat, val in gastos.items():
        print(f"➡️ {cat.capitalize()}: R$ {val:.2f}")
    print(f"\n💲 Total: R$ {total:.2f}")





if __name__ == "__main__":
    bot_gastos()
    bot_gastos() 
