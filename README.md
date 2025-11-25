Estoque System — Versão 1.0

Descrição
Sistema básico de controle de estoque desenvolvido em Python, focado em operações fundamentais de entrada e saída de materiais.
A versão 1.0 utiliza estrutura interna em memória (dicionários) e serve como base para evoluções futuras, como persistência em CSV, logs, integrações externas e interface gráfica.
O objetivo é de aplicar o conhecimento adquirido ao longo da jornada de aprendizado, de forma a solidificar os conceitos e aplicações.

Funcionalidades

 - Cadastro de materiais
   - Criação de itens novos
   - Prevenção de duplicidade via ItemAlreadyExistsError
 - Entrada de estoque
   - Incremento de quantidade
   - Validação do item antes da operação
 - Saída de estoque
   - Decremento de quantidade
   - Verificação automática de estoque insuficiente
   - Levantamento de ItemQuantityError quando necessário
 - Consulta de itens
   - Acesso a um material pelo nome
   - Erro dedicado quando o item não existe (NoItemError)
 - Listagem geral
   - Exibe todos os itens disponíveis e suas quantidades;
   - Log de entradas e saídas;
   - Relatório geral com quantidade atual do material e histórico de entradas e saídas.

Arquitetura

Armazenamento em memória usando dict
Classe principal responsável pelas operações de estoque

Exceções customizadas:

 - NoItemError
 - ItemAlreadyExistsError
 - NotEnoughStockError
A lógica foi estruturada de forma modular para facilitar refatorações nas próximas versões.


Limitações da Versão 1.0
  - Dados não persistem após encerrar o programa;
  - Ausência de logs, interface gráfica e API;
  - Tratamentos mais robustos serão adicionados na versão 2.0.

Roadmap estimado (sujeito à mudanças)
  v2.0:
  - Persistência em CSV;
  - CRUD reestruturado;
  - Preparação para SQL;
  - Sugestões automáticas ao detectar item inexistente.

  v3.0:
  - Controle de Usuários;
  - Refino das auditorias;
  - Logs de ações tomadas;
  - Aplicação de conceitos de políticas básicas de segurança.

  v4.0:
  - interface funcional;
  - integração com o backend existente;
  - telas de cadastro, movimentação, relatórios;
  - correção de bugs de interação;
  - testes manuais intensos.

  v5.0:
  - modelagem do banco;
  - migração dos dados;
  - reescrever CRUD inteiro para SQL;
  - adaptar GUI;
  - criar camada de persistência;
  - testes.

  v6.0
  - estruturação do banco para BI;
  - criação dos relatórios;
  - limpeza de inconsistências;
  - ajustes nos logs;
