---
title: Escuta IAgentNotifySinkEx
description: Escuta IAgentNotifySinkEx
ms.assetid: e303b299-0dd0-419a-87a9-1490fe6cf54a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fee8f931030cbd68cd148fc57360d8b0ccf7624
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498724"
---
# <a name="iagentnotifysinkexlisteningstate"></a>IAgentNotifySinkEx:: Listeningstate

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT ListeningState(
   long dwCharacterID,  // character ID
   long bListening,     // listening mode state
   long dwCause         // cause  
);
```

Notifica um aplicativo cliente quando o modo de escuta é alterado.

-   Sem valor de retorno.

<dl> <dt>

<span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*dwCharacterID*
</dt> <dd>

O caractere para o qual o estado de escuta foi alterado.

</dd> <dt>

<span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*bListening*
</dt> <dd>

O estado do modo de escuta. **Verdadeiro** indica que o modo de escuta foi iniciado; **False**, que o modo de escuta terminou.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

A causa do evento, que pode ser um dos valores a seguir.



| Valor                                                                             | Descrição                                                                    |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| **const LSCOMPLETE Long sem sinal** **\_ causa \_ PROGRAMDISABLED = 1;**<br/>    | O modo de escuta foi desativado pelo código do programa.                                 |
| **const LSCOMPLETE Long sem sinal** **\_ causa \_ PROGRAMTIMEDOUT = 2;**<br/>    | O modo de escuta (ativado pelo código do programa) atingiu o tempo limite.                          |
| **const LSCOMPLETE Long sem sinal** **\_ causa \_ USERTIMEDOUT = 3;**<br/>       | O modo de escuta (ativado pela chave de escuta) atingiu o tempo limite.                     |
| **const LSCOMPLETE Long sem sinal** **\_ causa \_ USERRELEASEDKEY = 4;**<br/>    | O modo de escuta foi desativado porque o usuário liberou a chave de escuta.     |
| **const LSCOMPLETE Long sem sinal** **\_ causa \_ USERUTTERANCEENDED = 5;**<br/> | O modo de escuta foi desativado porque o usuário terminou de falar.              |
| **const LSCOMPLETE Long sem sinal** **\_ causa \_ CLIENTDEACTIVATED = 6;**<br/>  | O modo de escuta foi desativado porque o cliente ativo de entrada foi desativado. |
| **const LSCOMPLETE Long sem sinal** **\_ causa \_ DEFAULTCHARCHANGE = 7**<br/>   | O modo de escuta foi desativado porque o caractere padrão foi alterado.       |
| **const LSCOMPLETE longo sem sinal** **\_ causa o \_ userdesabilitoud = 8**<br/>        | O modo de escuta foi desativado porque o usuário desabilitou a entrada de fala.          |



 

</dd> </dl>

Esse evento é enviado a todos os clientes quando o modo de escuta começa depois que o usuário pressiona a tecla de escuta ou quando seu tempo limite termina, ou quando o cliente de entrada-ativo chama o método [**IAgentCharacterEx:: Listen**](iagentcharacterex--listen.md) com **true** ou **false**.

O evento retorna valores para os clientes que atualmente têm esse caractere carregado. Todos os outros clientes recebem um caractere nulo (cadeia de caracteres vazia).

## <a name="see-also"></a>Consulte Também

[**IAgentCharacterEx:: escutar**](iagentcharacterex--listen.md)


 

 





