---
title: IAgentBalloon SetFontCharSet
description: IAgentBalloon SetFontCharSet
ms.assetid: ce1b152d-c8af-47ec-9e6b-5768dbcf3566
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cc462895ff9f19f7e722660608a268af13446f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120201"
---
# <a name="iagentballoonsetfontcharset"></a>IAgentBallball::SetFontCharSet

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

O conjunto de caracteres da fonte. Veja a seguir algumas configurações comuns de valor:



| Valor    | Conjunto de caracteres                                                                                       |
|-----|----------------------------------------------------------------------------------------|
| 0   | CARACTEREs padrão do Windows (ANSI).                                                    |
| 1   | Conjunto de caracteres padrão.                                                                 |
| 2   | O conjunto de caracteres de símbolo.                                                              |
| 128 | DBCS (conjunto de caracteres de byte duplo) exclusivo para a versão em japonês do Windows.            |
| 129 | DBCS (conjunto de caracteres de byte duplo) exclusivo para a versão em coreano do Windows.              |
| 134 | DBCS (conjunto de caracteres de byte duplo) exclusivo para a versão simplificada em chinês do Windows.  |
| 136 | DBCS (conjunto de caracteres de byte duplo) exclusivo para a versão tradicional em chinês do Windows. |
| 255 | Caracteres estendidos geralmente exibidos por aplicativos MS-DOS.                          |



 

</dd> </dl>

Para outros valores de conjunto de caracteres, consulte a documentação do SDK da Plataforma.

O conjunto de caracteres padrão usado no balão de palavras de um caractere é definido no Editor de Caracteres do Microsoft Agent. Você pode alterá-lo com [**IAgentBallball::SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**). No entanto, o usuário pode substituir a configuração de conjunto de caracteres para todos os caracteres usando a folha de propriedades do Microsoft Agent. Essa propriedade se aplica somente ao uso do caractere pelo aplicativo cliente; A configuração não afeta outros clientes do caractere ou outros caracteres do aplicativo cliente.

## <a name="see-also"></a>Consulte Também

[**IAgentBallball::GetFontCharSet**](iagentballoon--getfontcharset.md)


 

 




