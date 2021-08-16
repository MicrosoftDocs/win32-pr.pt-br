---
description: Direção da transição
ms.assetid: d18525de-bb75-4c5e-b387-cfec7ba03df7
title: Direção da transição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2097f13225c7691780646d77a18d048a48e31eda498955bdc53a0c954728c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951485"
---
# <a name="transition-direction"></a>Direção da transição

\[Essa API não tem suporte e pode ser alterada ou não disponível no futuro.\]

Uma transição passa da entrada A para a entrada B e da hora t para t. Portanto, a *direção* de uma transição pode significar uma das duas coisas:

-   O mapeamento de camadas de linha do tempo para entradas.
-   A progressão ao longo do tempo.

A primeira é a direção *de entrada* e a segunda é a direção *do progresso.* Você pode controlar as duas direções.

-   Direção de entrada: por padrão, uma transição passa da composição das camadas de prioridade mais baixa para a camada que contém a transição. Para inverter essa direção, chame o [**método IAMTimelineTrans::SetSwapInputs.**](iamtimelinetrans-setswapinputs.md)
-   Direção do progresso: a maioria das transições dá suporte a uma propriedade **Progress** padrão, que especifica qual percentual da transição é refletida na saída em um determinado momento. Por padrão, o valor da **propriedade Progress** vai de 0,0 a 1,0 durante a transição. Para reverter o progresso, de definir **a propriedade Progress** para ir de 1,0 a 0,0.

O diagrama a seguir ilustra a diferença entre a direção de entrada e a direção do progresso. Ele mostra quatro variações em uma transição [de apagando SMPTE](smpte-wipe-transition.md) padrão.

![instruções de apagamento](images/wipedirections.png)

A transição reside na faixa 1. Por padrão, o apagamento vai da esquerda para a direita e da faixa 0 para a faixa 1. A troca de entradas faz com que o apagamento passe da faixa 1 para a faixa 0, mas ainda da esquerda para a direita. Reverter o progresso faz com que a transição vá da direita para a esquerda. Você pode combinar ambos, conforme mostrado na extrema esquerda.

Para obter mais informações sobre como o DES renderiza transições, consulte [O modelo de linha do tempo](the-timeline-model.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com efeitos e transições](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



