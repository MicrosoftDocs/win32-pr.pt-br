---
title: IAgentBalloonEx SetNumCharsPerLine
description: IAgentBalloonEx SetNumCharsPerLine
ms.assetid: 44025b6b-ed42-4476-b841-c244accf0f83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a44abe14de6bb1cef631a51b4516d083657016
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292651"
---
# <a name="iagentballoonexsetnumcharsperline"></a>IAgentBalloonEx::SetNumCharsPerLine

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetNumCharsPerLine(
   long lCharsPerLine,  // number of characters per line setting
);
```

Define o número de caracteres por linha que podem ser exibidos no balão de palavras do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.
-   Retorna E \_ INVALIDARG se o parâmetro for menor que oito.

<dl> <dt>

<span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*lCharsPerLine*
</dt> <dd>

Número de linhas a serem exibidas na palavra balão.

</dd> </dl>

A configuração mínima é 8 e o máximo é 255. Se o texto especificado no método [**Speak**](speak-method.md) ou [**Think**](think-method.md) exceder o tamanho do balão atual, o Agent rolará automaticamente o texto no balão.

A configuração padrão é baseada em configurações quando o caractere é compilado com o editor de caracteres do Microsoft Agent.

## <a name="see-also"></a>Consulte Também

[**IAgentBalloon::GetNumCharsPerLine**](iagentballoon--getnumcharsperline.md)


 

 




