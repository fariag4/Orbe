# Orbe | Gestão empresarial

Sistema web simples de gestão empresarial: reúne pedidos, clientes e negócios, notas fiscais e financeiro em um só lugar, com indicadores de vendas e de contas a receber.

**Autor:** Gabriel Faria de Queiroz
**Disciplina:** Análise e Projeto de Sistemas
**Documentação completa:** `docs/Orbe_Documentacao.pdf`

## Funcionalidades

- Cadastrar, editar, excluir, buscar e filtrar pedidos, clientes e notas fiscais
- Visão geral com totais e resumo de pedidos por status
- Financeiro: total lançado, recebido, em aberto e vencido, e lista de contas a receber
- Exportar pedidos, clientes e notas em CSV
- Backup e restauração em arquivo JSON
- Funciona offline: os dados ficam salvos no navegador (localStorage)

O Orbe apenas registra notas já emitidas. Não emite NF-e nem NFS-e.

## Como executar

Não precisa instalar nada. Baixe o repositório e abra o arquivo `orbe_gestao_empresarial.html` no navegador (Chrome, Firefox ou Edge).

```bash
git clone https://github.com/fariag4/Orbe.git
cd Orbe
# abra orbe_gestao_empresarial.html com um clique duplo
```

Os dados ficam salvos no navegador e no dispositivo em que o arquivo foi aberto. Use o botão "Backup" para guardar uma cópia e transferi-la para outro computador.

## Estrutura

```
├── orbe_gestao_empresarial.html   sistema (interface + lógica)
├── docs/
│   └── Orbe_Documentacao.pdf      documentação de análise e projeto
└── README.md
```

## Convenção de commits

Mensagens semânticas (Conventional Commits): `feat:`, `fix:`, `docs:`, `refactor:`, `test:`.

Exemplos: `feat: adiciona exportação de pedidos em CSV`, `fix: unifica o cálculo do valor a receber`, `docs: adiciona diagrama de classes`.
