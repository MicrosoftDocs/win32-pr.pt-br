---
title: IAgentCharacter GetSize
description: IAgentCharacter GetSize
ms.assetid: bc2d6fe4-5945-4a35-b603-409c66f8aa2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af078eb9980399793e00f8bd3deaefef7f048a900423c1ee50ac8d4f4a310b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962226"
---
# <a name="iagentcharactergetsize"></a>IAgentCharacter::GetSize

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for character width 
   long * plHeight  // address of variable for character height
);
```

Recupera o tamanho do quadro de animação do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

Endereço de uma variável que recebe a largura do quadro de animação de caracteres em pixels, em relação à origem da tela (superior esquerda).

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

Endereço de uma variável que recebe a altura do quadro de animação de caracteres em pixels, em relação à origem da tela (superior esquerda).

</dd> </dl>

Embora o caractere apareça em uma janela de região com formato irregular, o local do caractere é baseado em seu quadro de animação retangular.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter:: SetSize**](iagentcharacter--setsize.md)


 

 




