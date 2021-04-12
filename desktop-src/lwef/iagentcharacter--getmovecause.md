---
title: IAgentCharacter GetMoveCause
description: IAgentCharacter GetMoveCause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612fcbfd4470d17e2365373458a8ded899a8180a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364504"
---
# <a name="iagentcharactergetmovecause"></a>IAgentCharacter::GetMoveCause

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetMoveCause(
   long * pdwCause  // address of variable for cause of character move
);
```

Recupera a causa da última movimentação do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*
</dt> <dd>

Endereço de uma variável que recebe a causa da última movimentação do caractere e será um dos seguintes:



|                                                                |                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const NeverMoved curto não assinado** **= 0;**<br/>        | O caractere não foi movido.                                                        |
| **const não assinada curto-** **movida = 1;**<br/>         | O usuário arrastou o caractere.                                                          |
| **const ProgramMoved curto não assinado** **= 2;**<br/>      | Seu aplicativo moveu o caractere.                                                |
| **const OtherProgramMoved curto não assinado** **= 3;**<br/> | Outro aplicativo moveu o caractere.                                             |
| **const SystemMoved curto sem sinal** **= 4**<br/>        | O servidor moveu o caractere para mantê-lo na tela após uma alteração de resolução de tela. |



 

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentNotifySink:: mover**](iagentnotifysink--move.md)


 

 





