---
title: SETPOSITION de IAgentCharacter
description: SETPOSITION de IAgentCharacter
ms.assetid: cc47b537-8154-4dfb-93e1-5ac3c3b50788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aee48ea26c714c570f7ae11b9b2dbc0fe92ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005298"
---
# <a name="iagentcharactersetposition"></a>IAgentCharacter:: SETPOSITION

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetPosition(
   long lLeft,  // screen coordinate of the left edge of character 
   long lTop    // screen coordinate of the top edge of character 
);
```

Define a posição do quadro de animação do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="lLeft"></span><span id="lleft"></span><span id="LLEFT"></span>*lLeft*
</dt> <dd>

Coordenada de tela da borda esquerda do quadro de animação de caracteres em pixels, em relação à origem da tela (superior esquerda).

</dd> <dt>

<span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*lTop*
</dt> <dd>

Coordenada de tela da borda superior do quadro de animação de caracteres em pixels, em relação à origem da tela (superior esquerda).

</dd> </dl>

A configuração dessa propriedade se aplica a todos os clientes do caractere. Embora o caractere apareça em uma janela de região com formato irregular, o local do caractere é baseado em seu quadro de animação retangular.

> [!Note]  
> Ao contrário do método [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) , essa função não é enfileirada.

 

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter:: GetPosition**](iagentcharacter--getposition.md)


 

 




