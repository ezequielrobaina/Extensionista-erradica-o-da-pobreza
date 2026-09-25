# Extensionista-erradica-o-da-pobreza


# ============================================================
# PROJETO: ERRADICAÇÃO DA POBREZA
# Fluxo: APLICAR -> VERIFICAR -> ANALISAR -> RESULTADO
# ============================================================

def aplicar():
    print("\n" + "=" * 60)
    print("ETAPA 1 - APLICAR")
    print("=" * 60)

    print("""
Transferência de renda eficiente:
- Fortalecer programas sociais;
- Garantir acesso à educação;
- Ampliar o acesso à saúde;
- Incentivar a qualificação profissional;
- Apoiar a geração de emprego e renda;
- Promover inclusão digital;
- Apoiar pequenos empreendedores.
    """)

    input("Pressione ENTER para continuar...")


def verificar():
    print("\n" + "=" * 60)
    print("ETAPA 2 - VERIFICAR")
    print("=" * 60)

    print("""
Nesta etapa são verificados os principais problemas
relacionados à pobreza:

1. Falta de renda;
2. Desemprego;
3. Falta de acesso à educação;
4. Falta de acesso à saúde;
5. Desigualdade social;
6. Falta de qualificação profissional;
7. Falta de oportunidades.
    """)

    input("Pressione ENTER para continuar...")


def analisar():
    print("\n" + "=" * 60)
    print("ETAPA 3 - ANALISAR")
    print("=" * 60)

    try:
        pessoas = int(input(
            "\nDigite o número de pessoas em situação de pobreza: "
        ))

        empregos = int(input(
            "Digite o número de pessoas que conseguiram emprego: "
        ))

        qualificacao = int(input(
            "Digite o número de pessoas que receberam qualificação: "
        ))

        if pessoas < 0 or empregos < 0 or qualificacao < 0:
            print("\nOs valores não podem ser negativos.")
            return

        print("\n--- ANÁLISE DOS DADOS ---")
        print(f"Pessoas em situação de pobreza: {pessoas}")
        print(f"Pessoas que conseguiram emprego: {empregos}")
        print(f"Pessoas qualificadas: {qualificacao}")

        if pessoas == 0:
            print("\nNão foram identificadas pessoas em situação de pobreza.")
        else:
            percentual_emprego = (empregos / pessoas) * 100
            percentual_qualificacao = (qualificacao / pessoas) * 100

            print(
                f"\nPercentual com emprego: "
                f"{percentual_emprego:.2f}%"
            )

            print(
                f"Percentual com qualificação: "
                f"{percentual_qualificacao:.2f}%"
            )

            if percentual_emprego >= 70 and percentual_qualificacao >= 70:
                print("\nSituação: AVANÇO SIGNIFICATIVO")
            elif percentual_emprego >= 40 or percentual_qualificacao >= 40:
                print("\nSituação: AVANÇO MODERADO")
            else:
                print("\nSituação: NECESSITA DE MAIS AÇÕES")

    except ValueError:
        print("\nDigite somente números válidos.")

    input("\nPressione ENTER para continuar...")


def resultado():
    print("\n" + "=" * 60)
    print("RESULTADO FINAL")
    print("=" * 60)

    print("""
              ERRADICAÇÃO DA POBREZA

                    ↓
             APLICAR AÇÕES
                    ↓
             VERIFICAR DADOS
                    ↓
             ANALISAR RESULTADOS
                    ↓
        CRIAR NOVAS ESTRATÉGIAS
                    ↓
        REDUZIR A DESIGUALDADE
                    ↓
          ERRADICAÇÃO DA POBREZA
    """)


def programa():
    while True:
        print("\n")
        print("=" * 60)
        print("       PROJETO DE ERRADICAÇÃO DA POBREZA")
        print("=" * 60)

        print("""
1 - Aplicar ações
2 - Verificar problemas
3 - Analisar dados
4 - Ver resultado final
0 - Sair
        """)

        opcao = input("Escolha uma opção: ")

        if opcao == "1":
            aplicar()

        elif opcao == "2":
            verificar()

        elif opcao == "3":
            analisar()

        elif opcao == "4":
            resultado()

        elif opcao == "0":
            print("\nPrograma encerrado.")
            break

        else:
            print("\nOpção inválida. Tente novamente.")


# Iniciar o programa
programa()
