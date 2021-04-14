---
title: IAgentBalloonEx SetNumLines
description: IAgentBalloonEx SetNumLines
ms.assetid: 350fd273-a941-4454-a309-045d19ed8f59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45c012d0193a0bd21ba203418920b87b2fac81b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453680"
---
# <a name="iagentballoonexsetnumlines"></a>IAgentBalloonEx::SetNumLines

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetNumLines(
   long lLines,  // number of lines setting
);
```

Define o número de linhas de saída de texto que podem ser exibidas no balão de palavras do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.
-   Retorna E \_ INVALIDARG se o parâmetro for zero.

<dl> <dt>

<span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*lLines*
</dt> <dd>

Número de linhas a serem exibidas na palavra balão.

</dd> </dl>

A configuração mínima é 1 e o máximo é 128. Se o texto especificado no método [**Speak**](speak-method.md) ou [**Think**](think-method.md) exceder o tamanho do balão atual, o Agent rolará automaticamente o texto no balão.

Esse método falhará se o bit do estilo de balão **SizeToText** estiver definido.

A configuração padrão é baseada em configurações quando o caractere é compilado com o editor de caracteres do Microsoft Agent.

## <a name="see-also"></a>Consulte Também

[**IAgentBalloon:: GetNumLines**](iagentballoon--getnumlines.md), [**IAgentBalloonEx:: GetStyle**](iagentballoonex--getstyle.md), [**IAgentBalloonEx:: SetStyle**](iagentballoonex--setstyle.md)


 

 




