---
title: IAgentNotifySink Visiblestate
description: IAgentNotifySink Visiblestate
ms.assetid: b0346296-74e9-448f-aa6d-a9fb1e645f05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3525c079ecd1b566ac2230f06e3effa1ceb7a694
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105764470"
---
# <a name="iagentnotifysinkvisiblestate"></a>IAgentNotifySink:: Visiblestate

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT VisibleState(
   long dwCharID,  // character ID
   long bVisible,  // visibility flag
   long dwCause,   // cause of visible state
);                          
```

Notifica um aplicativo cliente quando o estado de visibilidade do caractere é alterado.

-   Sem valor de retorno.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador do caractere cujo estado de visibilidade é alterado.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Sinalizador de visibilidade. Esse valor booliano é **true** quando o caractere se torna visível e **false** quando o caractere se torna oculto.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

Causa da última alteração no estado de visibilidade do caractere. O parâmetro pode ser um dos seguintes:



| Valor                                                                   | Descrição                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **const NeverShown curto não assinado** **= 0;**<br/>                 | O caractere não foi mostrado.                                                               |
| **const UserHid curto não assinado** **= 1;**<br/>                    | O usuário ocultou o caractere com o menu pop-up de ícone da barra de tarefas do caractere ou com entrada de fala. |
| **const não assinada curto não assinado** **= 2;**<br/>                 | O usuário mostrou o caractere.                                                                  |
| **const ProgramHid curto não assinado** **= 3;**<br/>                 | O aplicativo ocultou o caractere.                                                         |
| **const ProgramShowed curto não assinado** **= 4;**<br/>              | Seu aplicativo mostrou o caractere.                                                      |
| **const OtherProgramHid curto não assinado** **= 5;**<br/>            | Outro aplicativo ocultou o caractere.                                                      |
| **const OtherProgramShowed curto não assinado** **= 6;**<br/>         | Outro aplicativo mostrou o caractere.                                                   |
| **const UserHidViaCharacterMenu curto sem sinal** **= 7**<br/>     | O usuário ocultou o caractere com o menu pop-up do caractere.                                    |
| **const UserHidViaTaskbarIcon Short sem sinal** **= UserHid**<br/> | O usuário ocultou o caractere com o menu pop-up de ícone da barra de tarefas do caractere ou usando a entrada de fala. |



 

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter:: getVisible**](iagentcharacter--getvisible.md), [ **IAgentCharacter:: GetVisibilityCause**](iagentcharacter--getvisibilitycause.md)


 

 





