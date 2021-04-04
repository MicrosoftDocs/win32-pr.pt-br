---
title: IAgentBalloon setnomedafonte
description: IAgentBalloon setnomedafonte
ms.assetid: 6babf5f6-2abd-46c2-ade0-899a8e4488bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f983064c5df8cde8322658bbd0c713bbf238ecf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006103"
---
# <a name="iagentballoonsetfontname"></a>IAgentBalloon:: setnomedafontename

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font displayed in word balloon
);
                   
```

Define a fonte exibida no balão de palavras.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*
</dt> <dd>

Um BSTR que define a fonte exibida no balão de palavras.

</dd> </dl>

A fonte padrão usada no balão de palavras de um caractere é definida no editor de caracteres do Microsoft Agent. Você pode alterá-lo com **IAgentBalloon:: setnomedafonte**. No entanto, o usuário pode substituir a configuração de fonte para todos os caracteres usando a folha de propriedades do Microsoft Agent.

## <a name="see-also"></a>Consulte Também

[**IAgentBalloon:: getVisible**](iagentballoon--getvisible.md)


 

 




