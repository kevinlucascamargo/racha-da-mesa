# Racha da Mesa

Divisor de conta de bar entre amigos. Um arquivo HTML, sem servidor, sem cadastro,
sem enviar nada pra lugar nenhum.

**Acesse:** https://kevinlucascamargo.github.io/racha-da-mesa/

## Por que existe

Nasceu de uma planilha de Excel que fazia isso na mão, com uma aba por rolê. A planilha
funcionava, mas tinha os problemas clássicos de fórmula copiada de célula em célula:
intervalos de `SUM` que perdiam uma linha, um `/5` fixo enquanto a mesa tinha 4 pessoas,
e o rateio das porções que não entrava no total de ninguém.

## O que ele faz

- **Consumo individual** por pessoa, cada um com sua lista de itens e quantidades.
- **Rachado na mesa** para porções, rodízios e jarras — com escolha de quem participa
  de cada item. Quem não comeu, sai com um clique e o valor redivide.
- **Rateio exato em centavos.** R$ 10 entre 3 vira 3,34 / 3,33 / 3,33, nunca R$ 3,33
  para todo mundo com sete centavos sumindo.
- **Taxa de serviço e couvert**, com a possibilidade de isentar alguém individualmente.
  A taxa incide sobre consumo + rateio, que é como o restaurante cobra.
- **Conferência com a nota**: digite o valor da nota fiscal e ele diz se está sobrando
  ou faltando.
- **Resumo pro WhatsApp**: escolha quem pagou a conta e copie a lista de Pix pronta.
- **Vários rolês** salvos lado a lado, com um botão de duplicar que reaproveita a galera
  e as configurações.
- **Memória de cardápio**: os itens que você já lançou voltam a ser sugeridos com o
  último preço.

## Privacidade

Não existe backend. Nada do que você digita sai do seu aparelho, e quem abre o site
não vê nada do que você lançou.

O site guarda o rolê em `sessionStorage`, não em `localStorage`: **ao fechar a aba, o
navegador descarta tudo.** Atualizar a página no meio da divisão não perde nada, mas
fechar perde — de propósito, para não deixar a conta de ninguém esquecida no navegador
de um computador compartilhado.

Se quiser guardar o histórico dos rolês entre um dia e outro, baixe o `index.html` e
troque `sessionStorage` por `localStorage` na linha do `const STORE`.

## Rodar offline

Baixe o `index.html` e abra com dois cliques. As fontes estão embutidas no próprio
arquivo em base64, então ele funciona sem nenhuma conexão — nenhuma requisição de rede
é feita ao abrir.

## Licença

MIT — veja [LICENSE](LICENSE).
