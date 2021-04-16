---
title: IAgentBalloon GetFontItalic
description: IAgentBalloon GetFontItalic
ms.assetid: 03f40210-71b3-4488-9a44-5a9322db010a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c1a0e1e649e325e84d4a78eee087e102e8d1e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105772563"
---
# <a name="iagentballoongetfontitalic"></a>IAgentBalloon::GetFontItalic

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetFontItalic(
   long * pbFontItalic  // address of variable for italic setting for 
);                      // font displayed in word balloon 
```

Indica se a fonte usada em um balão de palavras está em itálico.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbFontItalic"></span><span id="pbfontitalic"></span><span id="PBFONTITALIC"></span>*pbFontItalic*
</dt> <dd>

O endereço de um valor que recebe **true** se a fonte for Italic e **false** se não estiver em itálico.

</dd> </dl>

O estilo de fonte usado no balão de palavras de um caractere é definido no editor de caracteres do Microsoft Agent. Ele não pode ser alterado por um aplicativo. No entanto, o usuário pode substituir as configurações de fonte de todos os caracteres por meio da folha de propriedades do Microsoft Agent.

 

 




