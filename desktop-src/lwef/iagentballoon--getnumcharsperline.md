---
title: IAgentBalloon GetNumCharsPerLine
description: IAgentBalloon GetNumCharsPerLine
ms.assetid: ae0c7fff-8c58-465e-9b4f-3260f7574b57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 887167584c46f075bc0696c46b2dde52eb27f8d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006104"
---
# <a name="iagentballoongetnumcharsperline"></a>IAgentBalloon::GetNumCharsPerLine

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetNumCharsPerLine(
   long * plCharsPerLine  // address of variable for characters per line
);                        // displayed in word balloon
```

Recupera o valor para o número médio de caracteres por linha exibidos em um balão de palavras.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbCharsPerLine"></span><span id="pbcharsperline"></span><span id="PBCHARSPERLINE"></span>*pbCharsPerLine*
</dt> <dd>

O endereço de uma variável que recebe o número de caracteres por linha.

</dd> </dl>

O servidor do Microsoft Agent rola automaticamente as linhas exibidas para a saída falada na palavra balão. O número médio de caracteres por linha para o balão de palavras de um caractere é definido no editor de caracteres do agente da Microsoft. Ele não pode ser alterado por um aplicativo.

## <a name="see-also"></a>Consulte Também

[**IAgentBalloon::GetNumLines**](iagentballoon--getnumlines.md)


 

 




