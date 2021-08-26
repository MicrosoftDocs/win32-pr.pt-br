---
title: IAgentBalloon GetFontItalic
description: IAgentBalloon GetFontItalic
ms.assetid: 03f40210-71b3-4488-9a44-5a9322db010a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5535896cc3c40ae3cb04c3078621cc91df4869649cbe72cb106c3d99ec0299ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062016"
---
# <a name="iagentballoongetfontitalic"></a>IAgentBalloon::GetFontItalic

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

 

 




