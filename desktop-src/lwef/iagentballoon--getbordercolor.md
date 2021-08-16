---
title: IAgentBalloon getbordercolor
description: IAgentBalloon getbordercolor
ms.assetid: e6c592c3-0e14-474f-a829-6028f2de5791
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ed636d5209402959adbb2a777577a87c8cc23f8eed4faeb8ac003981e5e2d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478630"
---
# <a name="iagentballoongetbordercolor"></a>IAgentBalloon:: getbordercolor

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetBorderColor (
  long * plBorderColor// address of variable for border color displayed
);                    // for word balloon
```

Recupera o valor da cor de borda exibida para um balão de palavras.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="plBorderColor"></span><span id="plbordercolor"></span><span id="PLBORDERCOLOR"></span>*plBorderColor*
</dt> <dd>

O endereço de uma variável que recebe a configuração de cor para a borda do balão.

</dd> </dl>

A cor da borda de um balão de palavras de caracteres é definida no editor de caracteres do Microsoft Agent. Ele não pode ser alterado por um aplicativo. No entanto, o usuário pode alterar a cor da borda dos balões de palavras para todos os caracteres por meio da folha de propriedades do Microsoft Agent.

## <a name="see-also"></a>Consulte Também

[**IAgentBalloon:: GetBackColor**](iagentballoon--getbackcolor.md), [ **IAgentBalloon:: GetForeColor**](iagentballoon--getforecolor.md)


 

 




