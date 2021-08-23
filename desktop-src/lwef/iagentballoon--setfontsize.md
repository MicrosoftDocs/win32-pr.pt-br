---
title: IAgentBalltern SetFontSize
description: IAgentBalltern SetFontSize
ms.assetid: c38779a6-bd7f-4d3a-9cb0-9d9fac1c7996
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb6e19d79429ddf98f67a281cd11aefb1dc6bc2e54b1289e36c7cfb5a62bd538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976466"
---
# <a name="iagentballoonsetfontsize"></a>IAgentBallball::SetFontSize

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in word balloon
); 
```

Define o tamanho da fonte exibida na palavra balão.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*
</dt> <dd>

Tamanho da fonte.

</dd> </dl>

O tamanho da fonte padrão usado no balão de palavras de um caractere é definido no Editor de Caracteres do Microsoft Agent. Você pode alterá-lo **com IAgentBallball::SetFontSize.** No entanto, o usuário pode substituir a configuração de tamanho da fonte para todos os caracteres usando a folha de propriedades do Microsoft Agent.

## <a name="see-also"></a>Consulte Também

[**IAgentBall widget::GetFontSize**](iagentballoon--getfontsize.md)


 

 




