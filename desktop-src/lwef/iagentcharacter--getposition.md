---
title: IAgentCharacter GetPosition
description: IAgentCharacter GetPosition
ms.assetid: 79343337-2700-48cb-a09d-1a356ea560e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a63e75111b7694fcb993e141b8534e8f174efd1a1a252f250167ecb597149f7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609986"
---
# <a name="iagentcharactergetposition"></a>IAgentCharacter::GetPosition

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of character 
   long * plTop    // address of variable for top edge of character 
);
```

Recupera a posição do quadro de animação do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*
</dt> <dd>

Endereço de uma variável que recebe a coordenada de tela da borda esquerda do quadro de animação de caracteres em pixels, em relação à origem da tela (superior esquerdo).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

Endereço de uma variável que recebe a coordenada de tela da borda superior do quadro de animação de caracteres em pixels, em relação à origem da tela (superior esquerdo).

</dd> </dl>

Embora o caractere apareça em uma janela de região formaada de forma irregular, o local do caractere é baseado em seu quadro de animação retangular.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter::SetPosition**](iagentcharacter--setposition.md), [ **IAgentCharacter::GetSize**](iagentcharacter--getsize.md)


 

 




