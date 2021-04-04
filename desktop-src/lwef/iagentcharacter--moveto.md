---
title: IAgentCharacter MoveTo
description: IAgentCharacter MoveTo
ms.assetid: 4e24d2f8-1df2-47ca-a1e9-b9d29708207d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d1ba423dc637895216ff03e2adec2862bbf27d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007423"
---
# <a name="iagentcharactermoveto"></a>IAgentCharacter:: MoveTo

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT MoveTo(
   short x,         // x-coordinate of new location
   short y,         // y-coordinate of new location
   long lSpeed,     // speed to move the character
   long * pdwReqID  // address of request ID
);
```

Reproduz a animação de estado de **movimentação** associada e move o quadro de caracteres para o local especificado.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida. Quando a função retorna, essa variável contém a ID da solicitação.

<dl> <dt>

<span id="x"></span><span id="X"></span>*w.x.y.*
</dt> <dd>

A coordenada x da nova posição em pixels, relativa à origem da tela (superior esquerda). O local de um caractere é baseado no canto superior esquerdo de seu quadro de animação.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Iar*
</dt> <dd>

A coordenada y da nova posição em pixels, em relação à origem da tela (superior esquerda). O local de um caractere é baseado no canto superior esquerdo de seu quadro de animação.

</dd> <dt>

<span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*lSpeed*
</dt> <dd>

Um parâmetro que especifica em milissegundos a velocidade com que o quadro do caractere se move. O valor recomendado é 1000. A especificação de zero (0) move o quadro sem reproduzir uma animação.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Endereço de uma variável que recebe a ID da solicitação [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) .

</dd> </dl>

Ao usar o protocolo HTTP para acessar dados de caracteres e animações, use o método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para garantir a disponibilidade das animações de estado de **movimentação** antes de chamar esse método. Mesmo que a animação não seja carregada, o servidor ainda moverá o quadro.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter:: SETPOSITION**](iagentcharacter--setposition.md)


 

 