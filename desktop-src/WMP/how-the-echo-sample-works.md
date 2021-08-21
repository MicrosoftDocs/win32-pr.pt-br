---
title: Como funciona o exemplo de eco
description: Como funciona o exemplo de eco
ms.assetid: 554afc08-6e4f-427c-8a09-0d1ebf3ca8dc
keywords:
- plug-ins Windows Media Player, visão geral do Echo sample
- plug-ins, visão geral do eco de exemplo
- plug-ins de processamento de sinal digital, visão geral do eco de exemplo
- Plug-ins do DSP, visão geral do eco de exemplo
- Exemplo de plug-in do eco DSP, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290cb56bbf1900dbcc09874213490f80cdc3af179ff243a2867bb232c3bb85c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338951"
---
# <a name="how-the-echo-sample-works"></a>Como funciona o exemplo de eco

O código cria o efeito de eco alocando um buffer grande o suficiente para conter exatamente a quantidade de dados de áudio que podem ser processados no período especificado pelo valor de tempo de atraso. O tamanho do buffer é calculado, em bytes, pela seguinte fórmula:

tamanho do buffer = tempo de atraso \* /taxa de amostragem/alinhamento de bloco de 1000 \*

O tempo de atraso é em milissegundos. Os valores de taxa de amostra e alinhamento de bloco são fornecidos em uma estrutura WAVEFORMATEX. A taxa de amostra está em exemplos por segundo; dividir por 1000 produz amostras por milissegundo. O alinhamento de bloco é igual ao produto do número de canais (1 para mono, 2 para estéreo) e o número de bits por amostra (8 ou 16) dividido por 8 (bits por byte).

Além da variável de ponteiro que aponta para o cabeçalho do buffer de atraso, o código cria um ponteiro móvel que percorre os dados no buffer em sincronização com o loop de processamento na função **DoProcessOutput** . Quando o ponteiro móvel atinge o final do buffer de atraso, ele volta ao início do buffer. Um buffer usado dessa maneira é chamado de buffer circular.

depois que o buffer de atraso existir e Windows Media Player tiver alocado um buffer de entrada para fornecer dados de áudio e um buffer de saída para receber dados de áudio processados, o processamento de eco continuará da seguinte maneira:

1.  Insira um loop que permita o processamento de cada amostra de áudio no buffer de entrada.
2.  Recupere um exemplo do buffer de entrada. Em seguida, mova o ponteiro de buffer de entrada para a próxima amostra para se preparar para a próxima iteração do loop.
3.  Recupere um exemplo do buffer de atraso.
4.  Copie o exemplo do buffer de entrada para o mesmo local no buffer de atraso do qual a amostra do último atraso foi recuperada.
5.  Mova o ponteiro de buffer de atraso para a próxima amostra. Se o ponteiro mover após o final do buffer, mova-o para o cabeçalho do buffer.
6.  Combine o exemplo do buffer de entrada com o exemplo do buffer de atraso.
7.  Copie o resultado para o buffer de saída. Em seguida, mova o ponteiro de buffer de saída para a próxima unidade para se preparar para a próxima iteração do loop.
8.  Repita até que todos os exemplos sejam processados.

Quando um exemplo de entrada recuperado na etapa 2 é copiado para o buffer de atraso na etapa 4, ele permanece lá até que o ponteiro móvel percorra cada exemplo no buffer de atraso e, finalmente, retorne à mesma posição. Como o tamanho do buffer de atraso é projetado para corresponder ao tempo de atraso, o tempo decorrido entre o exemplo que está sendo copiado para o buffer de atraso e o exemplo que está sendo recuperado mais uma vez é igual ao atraso especificado (além de qualquer latência introduzida pelo processamento real).

Quando um fluxo é iniciado, nenhum dado de atraso é gerado até que o tempo de atraso tenha decorrido. Portanto, é importante que o buffer de atraso inicialmente contenha silêncio. Se o buffer de atraso contiver dados aleatórios, o usuário ouvirá o ruído de branco até que o plug-in gere dados de atraso suficientes para substituir todo o buffer de atraso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do eco de exemplo**](echo-sample-overview.md)
</dt> </dl>

 

 




