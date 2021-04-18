---
title: IAgentBalloon SetFontCharSet
description: IAgentBalloon SetFontCharSet
ms.assetid: ce1b152d-c8af-47ec-9e6b-5768dbcf3566
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6202aa144d13c3c7435be03721a3f8fd4878b93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105793314"
---
# <a name="iagentballoonsetfontcharset"></a>IAgentBalloon::SetFontCharSet

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetFontCharSet(
   short sFontCharSet  // character set displayed in word balloon
); 
```

Define o conjunto de caracteres da fonte exibida na palavra balão.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*
</dt> <dd>

O conjunto de caracteres da fonte. A seguir estão algumas configurações comuns para o valor:



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

O conjunto de caracteres padrão usado no balão de palavras de um caractere é definido no editor de caracteres do Microsoft Agent. Você pode alterá-lo com [**IAgentBalloon:: SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**). No entanto, o usuário pode substituir a configuração de conjunto de caracteres para todos os caracteres usando a folha de propriedades do Microsoft Agent. Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

## <a name="see-also"></a>Consulte Também

[**IAgentBalloon::GetFontCharSet**](iagentballoon--getfontcharset.md)


 

 




