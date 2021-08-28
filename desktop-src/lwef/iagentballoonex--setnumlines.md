---
title: IAgentBallballballex SetNumLines
description: IAgentBallballballex SetNumLines
ms.assetid: 350fd273-a941-4454-a309-045d19ed8f59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3951cd4a8593d5e043e1571cdf24e14fdd9d93aef690c057860c2889022aa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848716"
---
# <a name="iagentballoonexsetnumlines"></a>IAgentBallballEx::SetNumLines

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetNumLines(
   long lLines,  // number of lines setting
);
```

Define o número de linhas de saída de texto que podem ser exibidas no balão de palavras do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.
-   Retornará E \_ INVALIDARG se o parâmetro for zero.

<dl> <dt>

<span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*lLines*
</dt> <dd>

Número de linhas a exibir na palavra balão.

</dd> </dl>

A configuração mínima é 1 e o máximo é 128. Se o texto especificado no método [**Speak**](speak-method.md) ou [**Think**](think-method.md) exceder o tamanho do balão atual, o Agent rolará automaticamente o texto no balão.

Esse método falhará se o bit de estilo de balão **SizeToText** estiver definido.

A configuração padrão é baseada em configurações quando o caractere é compilado com o Editor de Caracteres do Microsoft Agent.

## <a name="see-also"></a>Consulte Também

[**IAgentBallballstyle::GetNumLines,**](iagentballoon--getnumlines.md) [**IAgentBallballex::GetStyle,**](iagentballoonex--getstyle.md) [**IAgentBallballstyleEx::SetStyle**](iagentballoonex--setstyle.md)


 

 




