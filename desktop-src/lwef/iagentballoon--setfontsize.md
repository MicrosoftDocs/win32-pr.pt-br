---
title: IAgentBalloon setfontize
description: IAgentBalloon setfontize
ms.assetid: c38779a6-bd7f-4d3a-9cb0-9d9fac1c7996
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4984382408739e2d093226d04b1c99582a1a25d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292751"
---
# <a name="iagentballoonsetfontsize"></a>IAgentBalloon:: setfontize

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

O tamanho de fonte padrão usado no balão de palavras de um caractere é definido no editor de caracteres do agente da Microsoft. Você pode alterá-lo com **IAgentBalloon:: Setfontize**. No entanto, o usuário pode substituir a configuração de tamanho da fonte para todos os caracteres usando a folha de propriedades do Microsoft Agent.

## <a name="see-also"></a>Consulte Também

[**IAgentBalloon:: getfontize**](iagentballoon--getfontsize.md)


 

 




