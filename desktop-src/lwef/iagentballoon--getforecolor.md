---
title: GetForeColor IAgentBalloon
description: GetForeColor IAgentBalloon
ms.assetid: b06ad924-66b6-42a6-8c97-5bc4c46f6e2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b7a251471b0281661b087dbfb9b141c54ff9dc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105768310"
---
# <a name="iagentballoongetforecolor"></a>IAgentBalloon:: GetForeColor

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetForeColor(
   long * plFGColor // address of variable for foreground color displayed
);                  // in word balloon
```

Recupera o valor da cor de primeiro plano exibida em um balão de palavras.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="plFGColor"></span><span id="plfgcolor"></span><span id="PLFGCOLOR"></span>*plFGColor*
</dt> <dd>

O endereço de uma variável que recebe a configuração de cor do primeiro plano do balão.

</dd> </dl>

A cor de primeiro plano usada em um balão de palavras de caracteres é definida no editor de caracteres do Microsoft Agent. Ele não pode ser alterado por um aplicativo. No entanto, o usuário pode substituir a cor de primeiro plano dos balões de palavras de todos os caracteres por meio da folha de propriedades do Microsoft Agent.

## <a name="see-also"></a>Consulte Também

[**IAgentBalloon:: GetBackColor**](iagentballoon--getbackcolor.md)


 

 




