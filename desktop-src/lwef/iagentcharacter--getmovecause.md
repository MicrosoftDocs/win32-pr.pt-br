---
title: IAgentCharacter GetMoveCause
description: IAgentCharacter GetMoveCause
ms.assetid: 36cdd3bc-65b6-469f-9344-93403c1d24e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 381d0f695fb1d183cced20609fc70abc0bfca0e51ddf2f904ae320a6c4844f06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962267"
---
# <a name="iagentcharactergetmovecause"></a>IAgentCharacter::GetMoveCause

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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


 

 





