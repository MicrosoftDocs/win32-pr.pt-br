---
title: IAgentCharacter SetSize
description: IAgentCharacter SetSize
ms.assetid: 8324ab84-2b59-4459-b375-700d72b621bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089226f98969594a1d19afc7f3bb529c30943e06ec4083364dc5ae2f9850c9c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848516"
---
# <a name="iagentcharactersetsize"></a>IAgentCharacter::SetSize

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

Alterar o tamanho do quadro do caractere dimensiona o caractere para o conjunto de tamanhos com esse método. A configuração dessa propriedade se aplica a todos os clientes do caractere.

Embora o caractere apareça em uma janela de região formaada de forma irregular, o local do caractere é baseado em seu quadro de animação retangular.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter::GetSize**](iagentcharacter--getsize.md)


 

 




