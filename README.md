# Orbe | Gestão empresarial

Sistema web simples de gestão empresarial: reúne pedidos, clientes e negócios, notas fiscais e financeiro em um só lugar, com indicadores de vendas e de contas a receber.

**Autor:** Gabriel Faria de Queiroz
**Disciplina:** Análise e Projeto de Sistemas
**Repositório:** https://github.com/fariag4/Orbe.git

## Funcionalidades

- Cadastrar, editar, excluir, buscar e filtrar pedidos, clientes e notas fiscais
- Visão geral com totais e resumo de pedidos por status
- Financeiro: total lançado, recebido, em aberto e vencido, e lista de contas a receber
- Exportar pedidos, clientes e notas em CSV
- Backup e restauração em arquivo JSON
- Funciona offline: os dados ficam salvos no navegador (localStorage)

O Orbe apenas registra notas já emitidas. Não emite NF-e nem NFS-e.

## Tecnologias

- HTML, CSS e JavaScript puro, em um único arquivo (sem frameworks e sem servidor)
- Armazenamento no `localStorage` do navegador (chave `orbeData`)
- Exportação em CSV (UTF-8 com BOM, separador `;`, para abrir corretamente no Excel) e backup em JSON

## Como executar

Não precisa instalar nada. Baixe o repositório e abra o arquivo `orbe_gestao_empresarial.html` no navegador (Chrome, Firefox ou Edge).

```bash
git clone https://github.com/fariag4/Orbe.git
cd Orbe
# abra orbe_gestao_empresarial.html com um clique duplo
```

## Como usar

| Módulo | Para que serve |
| --- | --- |
| Visão geral | Totais de pedidos e clientes, valor vendido, valor a receber e pedidos recentes |
| Pedidos | Cadastro de pedidos com status (Pendente, Em andamento, Concluído, Cancelado) |
| Clientes e negócios | Cadastro de clientes e empresas com contato, documento e endereço |
| Notas fiscais | Lançamento de notas com vencimento, valor recebido e status (Pendente, Parcial, Pago) |
| Financeiro | Total lançado, recebido, em aberto, vencido e contas a receber |
| Segurança dos dados | Gerar backup, restaurar backup e limpar dados |

## Seus dados e o backup

Os dados ficam salvos no navegador e no dispositivo em que o arquivo foi aberto, e não são enviados para nenhum servidor. Para não perdê-los (por exemplo, ao limpar os dados do navegador) ou para levá-los a outro computador, use **Gerar backup** e guarde o arquivo `.json`. Para recuperar, use **Restaurar backup**: isso substitui todos os dados atuais.

## Limitações conhecidas

- Não há login nem compartilhamento: cada navegador tem seus próprios dados.
- O cliente de um pedido e o pedido de uma nota são ligados pelo nome e pelo número digitados, sem chave. Renomear um cliente não atualiza os pedidos dele.
- Não há alerta de número de pedido ou de nota duplicado.

## Documentação

A documentação de análise e projeto (requisitos, casos de uso e diagrama de classes) está em `docs/Orbe_Documentacao.pdf`.

## Convenção de commits

Mensagens semânticas (Conventional Commits): `feat:`, `fix:`, `docs:`, `refactor:`, `test:`.

Exemplos: `feat: adiciona exportação de pedidos em CSV`, `fix: unifica o cálculo do valor a receber`, `docs: adiciona diagrama de classes`.
