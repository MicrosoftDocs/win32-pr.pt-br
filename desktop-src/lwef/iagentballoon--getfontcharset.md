---
title: IAgentBalloon GetFontCharSet
description: IAgentBalloon GetFontCharSet
ms.assetid: 1ab5767a-31e3-449c-b242-f20b11336ca0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f809fbd83e44259c96184c9f364a85151ec9ddde
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120401"
---
# <a name="iagentballoongetfontcharset"></a>IAgentBallball::GetFontCharSet

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetFontCharSet(
   short * psFontCharSet  // character set displayed in word balloon
); 
```

Indica o conjunto de caracteres da fonte exibida em um balão de palavra.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*
</dt> <dd>

O endereço de um valor que recebe o conjunto de caracteres da fonte. Veja a seguir algumas configurações comuns de valor:



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

O conjunto de caracteres padrão usado no balão de palavras de um caractere é definido no Editor de Caracteres do Microsoft Agent. Você pode alterá-lo [**usando IAgentBallball::SetFontCharSet**](iagentballoon--setfontcharset.md). No entanto, o usuário pode substituir a configuração de conjunto de caracteres para todos os caracteres usando a folha de propriedades do Microsoft Agent.

## <a name="see-also"></a>Consulte Também

[**IAgentBallball::SetFontCharSet**](iagentballoon--setfontcharset.md)


 

 




