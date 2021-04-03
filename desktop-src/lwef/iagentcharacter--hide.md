---
title: Ocultar IAgentCharacter
description: Ocultar IAgentCharacter
ms.assetid: a8128fe8-9a3b-41a3-bfe3-82ace1baff6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcd0ef91eb4d2738f19fb594ac1ab186efaec6e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007471"
---
# <a name="iagentcharacterhide"></a>IAgentCharacter:: Hide

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Hide(
   long bFast,      // play Hiding state animation flag
   long * pdwReqID  // address of request ID
);
```

Oculta o caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida. Quando a função retorna, *pdwReqID* contém a ID da solicitação.

<dl> <dt>

<span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*
</dt> <dd>

Sinalizador de animação de estado **oculto** . Se esse parâmetro for **true**, a animação de **ocultação** não será reproduzida antes que o quadro de caracteres fique oculto; Se **for false**, a animação será reproduzida.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Endereço de uma variável que recebe a ID da solicitação de **ocultação** .

</dd> </dl>

O servidor enfileira a animação associada ao método **Hide** na fila do caractere. Isso permite que você o use para ocultar o caractere após uma sequência de outras animações. Você pode executar a ação imediatamente usando o método [**Stop**](iagentcharacter--stop.md) antes de chamar o método **Hide** .

Ao usar o protocolo HTTP para acessar dados de caracteres e animações, use o método [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) para garantir a disponibilidade da animação de estado **oculto** antes de chamar esse método.

Ocultar um caractere também pode resultar no disparo do evento [**IAgentNotifySink:: ActivateInputState**](iagentnotifysink--activateinputstate.md) de outro caractere visível.

Os caracteres ocultos não podem acessar o canal de áudio. O servidor passará um status de falha no evento [**RequestComplete**](iagentnotifysink--requestcomplete.md) se você gerar uma solicitação de animação e o caractere estiver oculto.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter:: mostrar**](iagentcharacter--show.md)


 

 