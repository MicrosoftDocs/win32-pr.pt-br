---
title: IAgentBalloon GetNumLines
description: IAgentBalloon GetNumLines
ms.assetid: 82deeed0-d4a7-46e4-9077-edd933dcf4e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d66c18d75af77a2559efc86f775710fb32e6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364407"
---
# <a name="iagentballoongetnumlines"></a>IAgentBalloon::GetNumLines

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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


 

 




