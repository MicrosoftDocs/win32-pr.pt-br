---
title: Interrupção de IAgentCharacter
description: Interrupção de IAgentCharacter
ms.assetid: ae05d317-e2d9-4d11-a6df-f9b25e43467a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17c9f19f716b15a48ec3cdb064aa4c0fdbbd1774
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917167"
---
# <a name="iagentcharacterinterrupt"></a>IAgentCharacter:: Interrupt

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Interrupt(
   long dwReqID,    // request ID to interrupt
   long * pdwReqID  // address of request ID
);
```

Interrompe a animação especificada (solicitação) de outro caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida. Quando a função retorna, *pdwReqID* contém a ID da solicitação.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

Uma ID da solicitação a ser interrompida.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Endereço de uma variável que recebe a ID da solicitação de **interrupção** .

</dd> </dl>

Se você carregar vários caracteres, poderá usar esse método para sincronizar a animação entre os caracteres. Por exemplo, se outro caractere estiver em uma animação de looping, esse método irá parar a animação de looping e iniciar a próxima animação na fila do caractere.

A **interrupção** interrompe a animação existente, mas não libera a fila de animação do caractere. Ele inicia a próxima animação na fila do caractere. Para interromper e liberar a fila de um caractere, use o método [**Stop**](/windows/desktop/lwef/iagentcharacter--stop) .

Você não pode usar esse método para ter uma interrupção de caractere em si porque o servidor do Microsoft Agent enfileira o método de **interrupção** na fila de animação do caractere. Portanto, você só pode usar a **interrupção** para interromper a animação de outro caractere que você carregou.

 

 