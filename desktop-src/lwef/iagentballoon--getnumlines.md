---
title: IAgentBalloon GetNumLines
description: IAgentBalloon GetNumLines
ms.assetid: 82deeed0-d4a7-46e4-9077-edd933dcf4e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461ebc4fa7c7e0ae9080544e9114db9f8c179925dae665925d893288f95de027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478620"
---
# <a name="iagentballoongetnumlines"></a>IAgentBalloon::GetNumLines

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetNumLines(
   long * pcLines  // address of variable for number of lines 
);                  // displayed in word balloon
```

Recupera o valor do número de linhas exibidas em um balão de palavras.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pcLines"></span><span id="pclines"></span><span id="PCLINES"></span>*pcLines*
</dt> <dd>

O endereço de uma variável que recebe o número de linhas exibidas.

</dd> </dl>

O servidor do Microsoft Agent rola automaticamente as linhas exibidas para a saída falada na palavra balão. O número de linhas para um balão de palavras de caracteres é definido no editor de caracteres do Microsoft Agent. Ele não pode ser alterado por um aplicativo.

## <a name="see-also"></a>Consulte Também

[**IAgentBalloon::GetNumCharsPerLine**](iagentballoon--getnumcharsperline.md)


 

 




