---
title: IAgentCharacter SetPosition
description: IAgentCharacter SetPosition
ms.assetid: cc47b537-8154-4dfb-93e1-5ac3c3b50788
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e973ec08cdab89c2d8c2501bd9ea1778866f5f7fa1757fe746e44495e41c275a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665636"
---
# <a name="iagentcharactersetposition"></a>IAgentCharacter::SetPosition

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

Coordenada de tela da borda esquerda do quadro de animação de caracteres em pixels, em relação à origem da tela (superior esquerdo).

</dd> <dt>

<span id="lTop"></span><span id="ltop"></span><span id="LTOP"></span>*lTop*
</dt> <dd>

Coordenada de tela da borda superior do quadro de animação de caracteres em pixels, em relação à origem da tela (superior esquerdo).

</dd> </dl>

A configuração dessa propriedade se aplica a todos os clientes do caractere. Embora o caractere apareça em uma janela de região formaada de forma irregular, o local do caractere é baseado em seu quadro de animação retangular.

> [!Note]  
> Ao contrário [**do método MoveTo,**](https://www.bing.com/search?q=**MoveTo**) essa função não está na fila.

 

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter::GetPosition**](iagentcharacter--getposition.md)


 

 




