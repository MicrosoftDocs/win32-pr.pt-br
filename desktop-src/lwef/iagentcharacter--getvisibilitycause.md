---
title: IAgentCharacter GetVisibilityCause
description: IAgentCharacter GetVisibilityCause
ms.assetid: 46f681de-1c99-4f90-a3fe-aae04bb75339
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6013385144b82b79a0f17ae6443b094a9d9c8a4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364500"
---
# <a name="iagentcharactergetvisibilitycause"></a>IAgentCharacter::GetVisibilityCause

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetVisibilityCause(
   long * pdwCause  // address of variable for cause of character visible state
);
```

Recupera a causa do estado visível do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*
</dt> <dd>

Endereço de uma variável que recebe a causa da alteração do estado da última visibilidade do caractere e será um dos seguintes:



| Valor                                                                   | Descrição                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **const NeverShown curto não assinado** **= 0;**<br/>                 | O caractere não foi mostrado.                                                               |
| **const UserHid curto não assinado** **= 1;**<br/>                    | O usuário ocultou o caractere com o menu pop-up de ícone da barra de tarefas do caractere ou usando a entrada de fala. |
| **const não assinada curto não assinado** **= 2;**<br/>                 | O usuário mostrou o caractere.                                                                  |
| **const ProgramHid curto não assinado** **= 3;**<br/>                 | O aplicativo ocultou o caractere.                                                         |
| **const ProgramShowed curto não assinado** **= 4;**<br/>              | Seu aplicativo mostrou o caractere.                                                      |
| **const OtherProgramHid curto não assinado** **= 5;**<br/>            | Outro aplicativo ocultou o caractere.                                                      |
| **const OtherProgramShowed curto não assinado** **= 6;**<br/>         | Outro aplicativo mostrou o caractere.                                                   |
| **const UserHidViaCharacterMenu curto sem sinal** **= 7**<br/>     | O usuário ocultou o caractere com o menu pop-up do caractere.                                    |
| **const UserHidViaTaskbarIcon Short sem sinal** **= UserHid**<br/> | O usuário ocultou o caractere com o menu pop-up de ícone da barra de tarefas do caractere ou usando a entrada de fala. |



 

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentNotifySink:: Visiblestate**](iagentnotifysink--visiblestate.md)


 

 





