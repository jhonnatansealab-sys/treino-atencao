# Treino de atenção

Cinco jogos de navegador para treinar atenção, controle de impulsos, memória de trabalho e flexibilidade mental. O objetivo é ajudar colaboradores a se prepararem melhor para testes psicossociais.

Cada jogo é um único arquivo HTML, sem bibliotecas externas e sem etapa de build. Funciona offline e em celular.

## Jogos

| Jogo | O que treina | Objetivo | Duração aproximada |
|---|---|---|---|
| [Cancelamento de alvos](cancelamento/index.html) | Atenção concentrada | Marcar todos os "d" com dois traços numa grade, sem marcar os parecidos | 45 a 90 s |
| [Go / No-Go](gonogo/index.html) | Atenção sustentada e controle de impulsos | Clicar no círculo verde e não clicar no vermelho | cerca de 2 min |
| [N-Back](nback/index.html) | Memória de trabalho | Dizer se a posição do quadrado é igual à de N passos atrás (1, 2 ou 3) | cerca de 1 min |
| [Stroop](stroop/index.html) | Atenção seletiva | Dizer a cor da tinta da palavra, ignorando o que ela diz | cerca de 2 min |
| [Trilha alternada](trilha/index.html) | Atenção alternada e flexibilidade mental | Ligar 1, A, 2, B, 3, C... em ordem, no menor tempo | 1 a 2 min |

A página inicial (`index.html`) lista os cinco jogos.

## Como usar

### Localmente

Abra o `index.html` na raiz com um duplo clique. Não precisa de servidor nem de instalação.

### Publicado no Cloudflare Pages

1. No painel do Cloudflare, vá em **Workers & Pages**, depois **Create**, **Pages** e **Connect to Git**.
2. Escolha este repositório.
3. Configure:
   - **Production branch:** `main`
   - **Framework preset:** None
   - **Build command:** vazio
   - **Build output directory:** `/`
4. Clique em **Save and Deploy**.

A cada push na `main`, o Cloudflare publica a nova versão.

## Estrutura

```
index.html            página inicial com os cinco jogos
cancelamento/         Cancelamento de alvos
gonogo/               Go / No-Go
nback/                N-Back
stroop/               Stroop
trilha/               Trilha alternada
```

## Privacidade

- Nenhum dado é enviado para servidores. Os jogos não fazem requisições de rede.
- O histórico das últimas sessões de cada jogo é salvo no `localStorage` do navegador de quem joga, só naquele aparelho e navegador.
- Cada jogo tem um botão para apagar esse histórico.
- Por isso, quem administra o projeto não vê o desempenho individual dos colaboradores. Consolidar resultados exigiria uma etapa à parte, com os cuidados da LGPD.

## Observações

- Os jogos são ferramentas de treino. Não substituem uma avaliação psicológica e não reproduzem testes oficiais.
- A transferência de um treino para o teste real é moderada. Funciona melhor com sessões curtas e frequentes, de 5 a 10 minutos.
- Tempos, proporções de estímulos e faixas de sugestão de nível foram definidos como estimativas e podem ser ajustados no código de cada jogo.
- O som do Go/No-Go e do Stroop é gerado no próprio navegador e pode ser desligado no jogo.
