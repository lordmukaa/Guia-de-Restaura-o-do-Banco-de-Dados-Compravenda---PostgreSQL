# Dump de Banco de Dados - Compravenda

Este repositório contém o dump de um banco de dados PostgreSQL relacionado ao sistema de "Compravenda". O arquivo pode ser utilizado para restaurar o banco de dados em um ambiente PostgreSQL para fins de desenvolvimento ou teste.

## Como Restaurar o Banco de Dados

Para restaurar o banco de dados em uma instância PostgreSQL, siga os passos abaixo:

### Pré-requisitos

- **PostgreSQL** instalado em sua máquina.
- Um banco de dados vazio criado para restaurar o dump.

### Passos para Restaurar

1. **Clone o repositório** para sua máquina local:
    ```bash
    git clone https://github.com/seu-usuario/seu-repositorio.git
    ```

2. **Acesse o diretório** onde o arquivo dump está localizado:
    ```bash
    cd seu-repositorio
    ```

3. **Restaurar o dump** no banco de dados PostgreSQL:
    ```bash
    pg_restore -U seu_usuario -d nome_do_banco --clean --no-owner dump-compravenda
    ```

    Substitua `seu_usuario` pelo nome de usuário PostgreSQL e `nome_do_banco` pelo nome do banco de dados onde deseja restaurar o dump.

4. **Verifique** se a restauração foi bem-sucedida acessando o banco de dados e consultando as tabelas.

### Observações

- Este dump foi criado usando PostgreSQL versão `14.13` no Ubuntu. É recomendável utilizar uma versão semelhante para evitar problemas de compatibilidade.
- As configurações de `ENCODING` e `standard_conforming_strings` estão definidas no arquivo dump e serão aplicadas automaticamente durante a restauração.

## Licença

Este projeto está licenciado sob os termos da licença MIT. Consulte o arquivo `LICENSE` para mais detalhes.
