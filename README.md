import datetime

class Funcionario:
    def __init__(self, num_registro, nome, idade, data_contratacao, local_trabalho, salario, escala_trabalho):
        self.num_registro = num_registro
        self.nome = nome
        self.idade = idade
        self.data_contratacao = data_contratacao
        self.local_trabalho = local_trabalho
        self.salario = salario
        self.escala_trabalho = escala_trabalho

class RHSystem:
    def __init__(self):
        self.funcionarios = []

    def cadastrar_funcionario(self, num_registro, nome, idade, data_contratacao, local_trabalho, salario, escala_trabalho):
        funcionario = Funcionario(num_registro, nome, idade, data_contratacao, local_trabalho, salario, escala_trabalho)
        self.funcionarios.append(funcionario)
        print("Funcionário cadastrado com sucesso!")

# Exemplo de uso
if __name__ == "__main__":
    sistema_rh = RHSystem()

    # Cadastro de novo funcionário
    sistema_rh.cadastrar_funcionario(001, "Maria", 30, datetime.date(2023, 4, 15), "Escritório A", 4000, "Segunda a Sexta")
    sistema_rh.cadastrar_funcionario(002, "José", 25, datetime.date(2023, 4, 20), "Escritório B", 3500, "Segunda a Sexta")

    # Verificar funcionários cadastrados
    print("Funcionários cadastrados:")
    for funcionario in sistema_rh.funcionarios:
        print("Número de Registro:", funcionario.num_registro)
        print("Nome:", funcionario.nome)
        print("Idade:", funcionario.idade)
        print("Data de Contratação:", funcionario.data_contratacao)
        print("Local de Trabalho:", funcionario.local_trabalho)
        print("Salário:", funcionario.salario)
        print("Escala de Trabalho:", funcionario.escala_trabalho)
        print()
