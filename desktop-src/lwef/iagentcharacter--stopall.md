---
title: IAgentCharacter
description: IAgentCharacter
ms.assetid: cb0ce220-7b35-45c0-b587-30939d26740f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ff1811e7b7ee323ef57e21dbeea4e6ea9d33dc8bc735327ec9ba5afc2ce299b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609775"
---
# <a name="iagentcharacterstopall"></a>IAgentCharacter:: stopAll

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT StopAll();
   long lType,  // request type
```

Interrompe todas as animações (solicitações) e as remove da fila de animação do caractere.

<dl> <dt>

<span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*
</dt> <dd>

Um campo de bits que indica os tipos de solicitações a serem interrompidas (e removidas da fila de caracteres), compostas a partir do seguinte:



| Valor                                                                                  |  Descrição                                                                                                        |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| const tipo de interrupção **longa não assinado** **\_ \_ tudo = 0xFFFFFFFF;**<br/>              | Interrompe todas as solicitações de animação, incluindo solicitações de [**preparação**](iagentcharacter--prepare.md) não enfileiradas. |
| **const** **\_ tipo \_** longo de parada não assinado<br/>             | Interrompe todas as solicitações de reprodução.                                                                                 |
| const de tipo de interrupção **longa não assinado constante** **\_ \_ mover = 0x00000002;**<br/>             | Interrompe todas as solicitações de [**movimentação**](https://www.bing.com/search?q=**Move**) .                                               |
| const tipo de interrupção **longa não assinado** , **\_ \_ Fale = 0x00000004;**<br/>            | Interrompe todas as solicitações de [**fala**](iagentcharacter--speak.md) .                                              |
| **const tipo longo de parada sem sinal de constante** **\_ \_ Prepare = 0x00000008;**<br/>          | Interrompe todas as solicitações de [**preparação**](iagentcharacter--prepare.md) enfileiradas.                                   |
| **const tipo longo de interrupção não assinado** **\_ \_ NONQUEUEDPREPARE = 0x00000010;**<br/> | Interrompe todas as solicitações de [**preparação**](iagentcharacter--prepare.md) não enfileiradas.                               |
| const tipo de interrupção **longa sem sinal** **\_ \_ visível = 0x00000020;**<br/>          | Interrompe todas as solicitações de [**ocultar**](iagentcharacter--hide.md) ou [**Mostrar**](iagentcharacter--show.md) .       |



 

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter:: Stop**](iagentcharacter--stop.md)


 

 





