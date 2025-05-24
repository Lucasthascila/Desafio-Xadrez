# desafio_xadrez.py

class Tabuleiro:
    def _init_(self):
        self.tabuleiro = self.criar_tabuleiro_inicial()

    def criar_tabuleiro_inicial(self):
        return [
            ["t", "c", "b", "d", "r", "b", "c", "t"],
            ["p"] * 8,
            ["."] * 8,
            ["."] * 8,
            ["."] * 8,
            ["."] * 8,
            ["P"] * 8,
            ["T", "C", "B", "D", "R", "B", "C", "T"]
        ]

    def mostrar(self):
        print("  a b c d e f g h")
        for i, linha in enumerate(self.tabuleiro):
            print(f"{8 - i} {' '.join(linha)} {8 - i}")
        print("  a b c d e f g h")


if _name_ == "_main_":
    tabuleiro = Tabuleiro()
    tabuleiro.mostrar()

    print("\nEsse é o tabuleiro inicial de xadrez. Você pode expandir esse programa adicionando movimentação de peças, regras e detecção de xeque.")
