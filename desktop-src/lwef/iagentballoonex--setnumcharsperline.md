---
title: IAgentBalloonEx SetNumCharsPerLine
description: IAgentBalloonEx SetNumCharsPerLine
ms.assetid: 44025b6b-ed42-4476-b841-c244accf0f83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098a89500606482914bfb31303a2cd79cac88f6d96d17abec58c75759f7abedc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976456"
---
# <a name="iagentballoonexsetnumcharsperline"></a>IAgentBallballEx::SetNumCharsPerLine

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetNumCharsPerLine(
   long lCharsPerLine,  // number of characters per line setting
);
```

Define o número de caracteres por linha que podem ser exibidos no balão de palavras do caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.
-   Retornará E \_ INVALIDARG se o parâmetro for menor que oito.

<dl> <dt>

<span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*lCharsPerLine*
</dt> <dd>

Número de linhas a exibir na palavra balão.

</dd> </dl>

A configuração mínima é 8 e o máximo é 255. Se o texto especificado no método [**Speak**](speak-method.md) ou [**Think**](think-method.md) exceder o tamanho do balão atual, o Agent rolará automaticamente o texto no balão.

A configuração padrão é baseada em configurações quando o caractere é compilado com o Editor de Caracteres do Microsoft Agent.

## <a name="see-also"></a>Consulte Também

[**IAgentBallball::GetNumCharsPerLine**](iagentballoon--getnumcharsperline.md)


 

 




