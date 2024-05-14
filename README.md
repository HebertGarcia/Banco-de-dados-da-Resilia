# Sistema de Gerenciamento de Curso Resilia

Este é um sistema de gerenciamento de curso desenvolvido para a plataforma Resilia. Ele permite o cadastro de cursos, alunos, facilitadores, módulos, turmas e o acompanhamento do progresso dos alunos.

## Estrutura do Banco de Dados

O banco de dados é organizado em um esquema chamado resilia, que contém as seguintes tabelas:

- **Cursos**: Armazena informações sobre os cursos oferecidos.<br>
- **Alunos**: Contém dados dos alunos matriculados nos cursos.<br>
- **Facilitadores**: Registra informações sobre os facilitadores que ministram as aulas.<br>
- **Módulos**: Guarda detalhes sobre os módulos dos cursos.<br>
- **Turmas**: Registra as turmas criadas para cada curso.<br>
- **Alunos_Turmas**: Tabela de relacionamento entre alunos e turmas.<br>
- **Facilitadores_Turmas**: Tabela de relacionamento entre facilitadores e turmas.<br>
- **Porcentagem_Evasao_Por_Turma**: View que mostra a porcentagem de evasão por turma.<br>
- **Log_Status_Alunos**: Tabela para registrar atualizações de status dos alunos.<br>
- **Trigger atualizacao_status_aluno**: Trigger que popula a tabela Log_Status_Alunos.

## Funcionalidades Principais

- **Criação de Tabelas e Procedimentos Armazenados**: Utiliza procedimentos armazenados para criar as tabelas e inserir dados iniciais.<br>
- **Consulta de Dados**: Fornece consultas para obter informações como o total de alunos, facilitadores em múltiplas turmas e alunos matriculados em cada turma.<br>
- **Visualização de Porcentagem de Evasão**: Mostra a porcentagem de evasão por turma.<br>
- **Registros de Atualização de Status**: Registra as atualizações de status dos alunos em uma tabela de log.<br>
- **Trigger para Atualização de Status**: Associa uma trigger à tabela de alunos para registrar automaticamente as atualizações de status.<br>
- **Perguntas Estratégicas**: Fornece consultas para responder perguntas estratégicas da empresa.

## Uso

Para utilizar o sistema, basta executar os scripts SQL fornecidos neste repositório em um ambiente PostgreSQL.

### Pré-requisitos

PostgreSQL instalado e configurado.<br>
Cliente SQL (por exemplo, pgAdmin) para executar os scripts.

### Passos

1. Execute o script `criar_tabelas_resilia.sql` para criar as tabelas e procedimentos armazenados.<br>
2. Execute o script `inserir_dados_resilia.sql` para inserir dados iniciais.<br>
3. Execute o script `inserir_relacionamentos_resilia.sql` para estabelecer os relacionamentos entre os dados.<br>
4. Explore as consultas fornecidas para obter insights sobre os dados do sistema.

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir uma issue para relatar problemas ou propor melhorias.

## Licença

Este projeto está licenciado sob a Licença MIT. Consulte o arquivo LICENSE para obter mais detalhes.
