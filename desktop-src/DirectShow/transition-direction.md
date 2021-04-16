---
description: Direção da transição
ms.assetid: d18525de-bb75-4c5e-b387-cfec7ba03df7
title: Direção da transição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01d43ec4258d2f23c8b8961e3e1b8fd3d554b057
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104559830"
---
# <a name="transition-direction"></a>Direção da transição

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Uma transição vai de entrada A para entrada B e de hora t ₀ para t ₁. Portanto, a *direção* de uma transição pode significar uma destas duas coisas:

-   O mapeamento de camadas da linha do tempo para entradas.
-   A progressão ao longo do tempo.

A primeira é a *direção de entrada* e a segunda é a *direção do progresso*. Você pode controlar ambas as direções.

-   Direção de entrada: por padrão, uma transição vai da composição das camadas de prioridade inferior para a camada que contém a transição. Para inverter essa direção, chame o método [**IAMTimelineTrans:: SetSwapInputs**](iamtimelinetrans-setswapinputs.md) .
-   Direção do progresso: a maioria das transições dá suporte a uma propriedade de **progresso** padrão, que especifica qual porcentagem da transição é refletida na saída em um determinado momento. Por padrão, o valor da propriedade **Progress** passa de 0,0 para 1,0 ao longo da duração da transição. Para inverter o progresso, defina a propriedade **Progress** para ir de 1,0 para 0,0.

O diagrama a seguir ilustra a diferença entre a direção de entrada e a direção do progresso. Ele mostra quatro variações em uma transição de [apagamento SMPTE](smpte-wipe-transition.md) padrão.

![instruções de apagamento](images/wipedirections.png)

A transição reside no Track 1. Por padrão, o apagamento vai da esquerda para a direita e do Track 0 para o Track 1. A troca de entradas faz com que o apagamento continue do Track 1 para acompanhar 0, mas ainda da esquerda para a direita. A reversão do progresso faz a transição passar da direita para a esquerda. Você pode combinar ambos, conforme mostrado na extrema esquerda.

Para obter mais informações sobre como o DES renderiza as transições, consulte [o modelo de linha do tempo](the-timeline-model.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com efeitos e transições](working-with-effects-and-transitions.md)
</dt> </dl>

 

 



