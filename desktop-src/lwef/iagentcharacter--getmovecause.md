---
title: IAgentCharacter GetMoveCause
description: IAgentCharacter GetMoveCause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be943cf3b25b789838215f0209b16e67d5b50659
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119672"
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



| Valor                                                               | Descrição                                                                                     |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const unsigned short** **NeverMoved = 0;**<br/>        | O caractere não foi movido.                                                        |
| **const unsigned short** **UserMoved = 1;**<br/>         | O usuário arrastou o caractere.                                                          |
| **const unsigned short** **ProgramMoved = 2;**<br/>      | Seu aplicativo moveu o caractere.                                                |
| **const unsigned short** **OtherProgramMoved = 3;**<br/> | Outro aplicativo moveu o caractere.                                             |
| **const unsigned short** **SystemMoved = 4**<br/>        | O servidor moveu o caractere para mantê-lo na tela após uma alteração na resolução da tela. |



 

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentNotifySink::Move**](iagentnotifysink--move.md)


 

 





