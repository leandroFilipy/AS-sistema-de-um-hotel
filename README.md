# 🏨 Sistema de Reserva de Hotel – Diagrama de Casos de Uso

Este projeto representa o diagrama de **Casos de Uso** de um sistema para gerenciamento de reservas em um hotel. O objetivo é organizar as funcionalidades e as interações entre os atores do sistema, tanto primários quanto secundários.

## 📄 Descrição Geral

O sistema tem como principal funcionalidade o gerenciamento de **reservas de quartos**, desde a busca inicial pelo cliente até o pagamento e possíveis ações de administração e recepção. O diagrama define claramente as permissões e responsabilidades de cada ator.

## 👥 Atores Envolvidos

### 🎭 Atores Primários

- **Usuário**: Papel genérico do qual herdam os perfis de cliente, recepcionista e administrador. Possui a funcionalidade de login.
- **Cliente**: Pode:
  - Pesquisar quartos
  - Realizar reservas (<<extend>> da pesquisa)
  - Efetuar pagamento ao reservar (<<include>>)
  - Cancelar a reserva caso não haja pagamento (<<extend>>)

- **Administrador**: Tem acesso às seguintes funções:
  - Configurar o sistema
  - Gerenciar cadastros
  - Acessar relatórios
  - Gerenciar quartos

- **Recepcionista**: Responsável por:
  - Gerenciar reservas
    - Fazer check-in (herança)
    - Fazer check-out (herança)
    - Cancelar reservas (herança)

### 🔗 Atores Secundários

- **Banco de Dados**: Responsável por armazenar os relatórios, registros e cadastros de usuários.
- **API de Pagamentos**: Encapsula o processamento dos pagamentos efetuados pelos clientes.

## 📌 Relações entre os Casos de Uso

- `<<include>>`: Usado para indicar que um caso de uso **sempre** inclui outro (ex: Pagamento incluso na Reserva).
- `<<extend>>`: Usado para representar um comportamento **opcional** ou **condicional** (ex: Cancelar reserva se não houver pagamento).

## 🧭 Organização Geral

A estrutura segue os princípios da UML com:

- Relações de **herança entre atores** (Usuário → Cliente, Administrador, Recepcionista)
- **Generalizações** de ações (gerenciar reservas → check-in, check-out, cancelar)
- Interação com sistemas externos (banco de dados e API de pagamentos)

## 👨‍💻 Autores

- Daniel Vinicius Rios Sismer  
- Leandro Filipy de Lima  
- José Azarías Pérez Torres  

## 📋 Licença

Este projeto foi desenvolvido com fins educacionais, podendo ser reutilizado e adaptado para outras aplicações de estudo ou protótipos de sistemas.

---
