---
title: IAgentCharacter MoveTo
description: IAgentCharacter MoveTo
ms.assetid: 4e24d2f8-1df2-47ca-a1e9-b9d29708207d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ea5a0e288e4b7d9782f1b463fdbcccf01b0da9314894be1a60c556392e25e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848536"
---
# <a name="iagentcharactermoveto"></a>IAgentCharacter::MoveTo

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT MoveTo(
   short x,         // x-coordinate of new location
   short y,         // y-coordinate of new location
   long lSpeed,     // speed to move the character
   long * pdwReqID  // address of request ID
);
```

Reproduz a animação **de** estado De movimentação associada e move o quadro de caracteres para o local especificado.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida. Quando a função retorna, essa variável contém a ID da solicitação.

<dl> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

A coordenada X da nova posição em pixels, em relação à origem da tela (superior esquerdo). O local de um caractere é baseado no canto superior esquerdo do quadro de animação.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

A coordenada Y da nova posição em pixels, em relação à origem da tela (superior esquerdo). O local de um caractere é baseado no canto superior esquerdo do quadro de animação.

</dd> <dt>

<span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*lSpeed*
</dt> <dd>

Um parâmetro que especifica em milissegundos a rapidez com que o quadro do caractere se move. O valor recomendado é 1000. Especificar zero (0) move o quadro sem a reprodução de uma animação.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Endereço de uma variável que recebe a ID [**da solicitação MoveTo.**](https://www.bing.com/search?q=**MoveTo**)

</dd> </dl>

Ao usar o protocolo HTTP para acessar caracteres e dados de  animação, use o método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para garantir a disponibilidade das animações de estado De movimentação antes de chamar esse método. Mesmo que a animação não seja carregada, o servidor ainda move o quadro.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter::SetPosition**](iagentcharacter--setposition.md)


 

 