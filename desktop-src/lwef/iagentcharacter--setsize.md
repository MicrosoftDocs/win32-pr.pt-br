---
title: SetSize IAgentCharacter
description: SetSize IAgentCharacter
ms.assetid: 8324ab84-2b59-4459-b375-700d72b621bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39d5b33afa7ff59516b793f194a0ba186c2e002
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636797"
---
# <a name="iagentcharactersetsize"></a>IAgentCharacter:: SetSize

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetSize(
   long * lWidth,  // width of the character frame
   long * lHeight  // height of the character frame
);
```

Define o tamanho do quadro de animação do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*
</dt> <dd>

A largura do quadro de animação do caractere em pixels.

</dd> <dt>

<span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*
</dt> <dd>

A altura do quadro de animação do caractere em pixels.

</dd> </dl>

A alteração do tamanho do quadro do caractere dimensiona o caractere para o tamanho definido com esse método. A configuração dessa propriedade se aplica a todos os clientes do caractere.

Embora o caractere apareça em uma janela de região com formato irregular, o local do caractere é baseado em seu quadro de animação retangular.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter::GetSize**](iagentcharacter--getsize.md)


 

 




