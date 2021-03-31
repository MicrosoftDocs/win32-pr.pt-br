---
title: IAgentCommandWindow setVisible
description: IAgentCommandWindow setVisible
ms.assetid: 44f3fc2d-937a-4890-8dad-e0f29da4c6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ddff54f4869cbe36016f30d775eeea017ae6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005714"
---
# <a name="iagentcommandwindowsetvisible"></a>IAgentCommandWindow:: setVisible

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // Voice Commands Window Visible setting 
);
```

Defina a propriedade [**Visible**](visible-property.md) para a janela de comandos de voz.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Configuração da propriedade [**visível**](visible-property.md) . Um valor **true** exibe a janela de comandos de voz; **False** oculta-o.

</dd> </dl>

O usuário pode substituir essa propriedade.

## <a name="see-also"></a>Consulte Também

[**IAgentCommandWindow:: getVisible**](iagentcommandwindow--getvisible.md)


 

 




