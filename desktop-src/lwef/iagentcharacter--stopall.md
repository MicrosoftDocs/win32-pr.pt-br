---
title: IAgentCharacter
description: IAgentCharacter
ms.assetid: cb0ce220-7b35-45c0-b587-30939d26740f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 558ca23b500ee2146470c8d595b2a5a64febf59a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120909"
---
# <a name="iagentcharacterstopall"></a>IAgentCharacter:: stopAll

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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


 

 





