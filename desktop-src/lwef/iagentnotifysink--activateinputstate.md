---
title: IAgentNotifySink ActivateInputState
description: IAgentNotifySink ActivateInputState
ms.assetid: 2476e475-d80c-47e9-bb60-e0fca41becc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5821f5943bb87f9c19a66125028604fa5d116a7e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160157"
---
# <a name="iagentnotifysinkactivateinputstate"></a>IAgentNotifySink::ActivateInputState

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT ActivateInputState(
   long dwCharID,   // character ID
   long bActivated  // input activation flag
);                          
```

Notifica um aplicativo cliente de que o estado ativo de entrada de um caractere foi alterado.

-   Sem valor de retorno.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador do caractere cujo estado de ativação de entrada foi alterado.

</dd> <dt>

<span id="bActivated"></span><span id="bactivated"></span><span id="BACTIVATED"></span>*bActivated*
</dt> <dd>

Sinalizador de entrada ativa. Esse valor booliano é **true** se o caractere referido por *dwCharID* ficou ativo de entrada; e **false** se o caractere perdeu seu estado ativo de entrada.

</dd> </dl>

 

 




