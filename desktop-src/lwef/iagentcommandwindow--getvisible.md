---
title: IAgentCommandWindow getVisible
description: IAgentCommandWindow getVisible
ms.assetid: a69a2aaa-5a3a-46b8-b505-49609a2aa5ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66c6d7bf2ee59512f478fd8daa7cee882515690
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105785933"
---
# <a name="iagentcommandwindowgetvisible"></a>IAgentCommandWindow:: getVisible

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for Visible setting for 
);                   // Voice Commands Window
```

Determina se a janela de comandos de voz está visível ou oculta.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Endereço de uma variável que recebe **true** se a janela de comandos de voz estiver visível ou **false** se estiver oculta.

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentCommandWindow:: setVisible**](iagentcommandwindow--setvisible.md)


 

 




