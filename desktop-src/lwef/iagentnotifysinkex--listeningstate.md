---
title: IAgentNotifySinkEx ListeningState
description: IAgentNotifySinkEx ListeningState
ms.assetid: e303b299-0dd0-419a-87a9-1490fe6cf54a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21d3926741f83f66ab6133874ec47783976c0ddb6d3fbd2ee91c6e584813147a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692602"
---
# <a name="iagentnotifysinkexlisteningstate"></a>IAgentNotifySinkEx::ListeningState

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT ListeningState(
   long dwCharacterID,  // character ID
   long bListening,     // listening mode state
   long dwCause         // cause  
);
```

Notifica um aplicativo cliente quando o modo de escuta muda.

-   Sem valor de retorno.

<dl> <dt>

<span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*dwCharacterID*
</dt> <dd>

O caractere para o qual o estado de escuta foi alterado.

</dd> <dt>

<span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*bListening*
</dt> <dd>

O estado do modo de escuta. **True** indica que o modo de escuta foi iniciado; **False**, que o modo de escuta terminou.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

A causa do evento, que pode ser um dos valores a seguir.



| Valor                                                                             | Descrição                                                                    |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ PROGRAMDISABLED = 1;**<br/>    | O modo de escuta foi desligado pelo código do programa.                                 |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ PROGRAMTIMEDOUT = 2;**<br/>    | O modo de escuta (ligado pelo código do programa) tempou.                          |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ USERTIMEDOUT = 3;**<br/>       | O modo de escuta (ligado pela tecla De escuta) tempou.                     |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ USERRELEASEDKEY = 4;**<br/>    | O modo de escuta foi desligado porque o usuário liberou a tecla Listening.     |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ USERUTTERANCEENDED = 5;**<br/> | O modo de escuta foi desligado porque o usuário terminou de falar.              |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ CLIENTDEACTIVATED = 6;**<br/>  | O modo de escuta foi desativado porque o cliente ativo de entrada foi desativado. |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ DEFAULTCHARCHANGE = 7**<br/>   | O modo de escuta foi desligado porque o caractere padrão foi alterado.       |
| **const unsigned long** **LSCOMPLETE \_ CAUSE \_ USERDISABLED = 8**<br/>        | O modo de escuta foi desativado porque o usuário desabilitou a entrada de fala.          |



 

</dd> </dl>

Esse evento é enviado a todos os clientes quando o modo de escuta começa depois que o usuário pressiona a tecla Listening ou quando seu tempo-final termina ou quando o cliente ativo de entrada chama o método [**IAgentCharacterEx::Listen**](iagentcharacterex--listen.md) com **True** ou **False.**

O evento retorna valores para os clientes que atualmente têm esse caractere carregado. Todos os outros clientes recebem um caractere nulo (cadeia de caracteres vazia).

## <a name="see-also"></a>Consulte Também

[**IAgentCharacterEx::Listen**](iagentcharacterex--listen.md)


 

 





