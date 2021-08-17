---
title: IAgentCommandWindow setVisible
description: IAgentCommandWindow setVisible
ms.assetid: 44f3fc2d-937a-4890-8dad-e0f29da4c6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b8d06c40fd88b525cadf9f90a1edd4edaaf3a9e9be7ccdcfa98dd6abf8b833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692639"
---
# <a name="iagentcommandwindowsetvisible"></a>IAgentCommandWindow:: setVisible

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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


 

 




