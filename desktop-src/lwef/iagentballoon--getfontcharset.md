---
title: IAgentBalloon GetFontCharSet
description: IAgentBalloon GetFontCharSet
ms.assetid: 1ab5767a-31e3-449c-b242-f20b11336ca0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f544df6c09fb00d346015b610751dd23738820
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159986"
---
# <a name="iagentballoongetfontcharset"></a>IAgentBalloon::GetFontCharSet

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetFontCharSet(
   short * psFontCharSet  // character set displayed in word balloon
); 
```

Indica o conjunto de caracteres da fonte exibida em um balão de palavras.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*
</dt> <dd>

O endereço de um valor que recebe o conjunto de caracteres da fonte. A seguir estão algumas configurações comuns para o valor:



|     |                                                                                        |
|-----|----------------------------------------------------------------------------------------|
| 0   | Caracteres padrão do Windows (ANSI).                                                    |
| 1   | Conjunto de caracteres padrão.                                                                 |
| 2   | O conjunto de caracteres do símbolo.                                                              |
| 128 | DBCS (conjunto de caracteres de byte duplo) exclusivo para a versão japonesa do Windows.            |
| 129 | DBCS (conjunto de caracteres de byte duplo) exclusivo para a versão coreana do Windows.              |
| 134 | DBCS (conjunto de caracteres de byte duplo) exclusivo para a versão do Windows em chinês simplificado.  |
| 136 | DBCS (conjunto de caracteres de dois bytes) exclusivo da versão em Chinês tradicional do Windows. |
| 255 | Caracteres estendidos geralmente exibidos por aplicativos do MS-DOS.                          |



 

</dd> </dl>

Para outros valores de conjunto de caracteres, consulte a documentação do Platform SDK.

O conjunto de caracteres padrão usado no balão de palavras de um caractere é definido no editor de caracteres do Microsoft Agent. Você pode alterá-lo usando [**IAgentBalloon:: SetFontCharSet**](iagentballoon--setfontcharset.md). No entanto, o usuário pode substituir a configuração de conjunto de caracteres para todos os caracteres usando a folha de propriedades do Microsoft Agent.

## <a name="see-also"></a>Consulte Também

[**IAgentBalloon::SetFontCharSet**](iagentballoon--setfontcharset.md)


 

 




