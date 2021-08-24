---
title: GetStatus do IAgentAudioOutputPropertiesEx
description: GetStatus do IAgentAudioOutputPropertiesEx
ms.assetid: 29bf1379-eebe-4b8b-b8d0-b86d2da78b64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feb161a72b536f85a8a82923841e2cd14ecd9e3525ab993f8b7c71f34630b0d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601306"
---
# <a name="iagentaudiooutputpropertiesexgetstatus"></a>IAgentAudioOutputPropertiesEx:: GetStatus

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetStatus(
   long * plStatus,  // address of audio channel status
);
```

Recupera o status do canal de áudio.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="plStatus"></span><span id="plstatus"></span><span id="PLSTATUS"></span>*plStatus*
</dt> <dd>

Status do canal de saída de áudio, que pode ser um dos seguintes valores:



| Valor                                                                         | Descrição                                                                                                    |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| const status de áudio **curto sem sinal** **\_ \_ disponível = 0;**<br/>         | O canal de saída de áudio está disponível (não ocupado).                                                              |
| const status de áudio **curto não assinado** **\_ \_ noáudio = 1;**<br/>           | Não há suporte para saída de áudio; por exemplo, como não há placa de som.                             |
| const status de áudio **curto não assinado** **\_ \_ CANTOPENAUDIO = 2;**<br/>     | O canal de saída de áudio não pode ser aberto (está ocupado); por exemplo, como outro aplicativo está reproduzindo áudio. |
| const status de áudio **curto sem sinal** **\_ \_ userfalando = 3;**<br/>      | O canal de saída de áudio está ocupado porque o servidor está processando a entrada de fala do usuário                            |
| const status de áudio **curto não assinado** **\_ \_ CHARACTERSPEAKING = 4;**<br/> | O canal de saída de áudio está ocupado porque um caractere está falando no momento.                                    |
| const status de áudio **curto não assinado** **\_ \_ SROVERRIDEABLE = 5;**<br/>    | O canal de saída de áudio não está ocupado, mas está aguardando a entrada de fala do usuário.                                 |
| const erro de status de áudio **curto não assinado** **\_ \_ = 6;**<br/>             | Houve algum outro problema (desconhecido) ao tentar acessar o canal de saída de áudio.                       |



 

</dd> </dl>

Essa configuração permite que o aplicativo cliente consulte o estado do canal de saída de áudio. Você pode usar isso para determinar se seu caractere deve falar ou tentar ativar o modo de escuta (usando **IAgentCharacterEx:: Listen**).

 

 





