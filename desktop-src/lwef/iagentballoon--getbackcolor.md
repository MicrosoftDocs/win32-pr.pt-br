---
title: IAgentBalloon GetBackColor
description: IAgentBalloon GetBackColor
ms.assetid: 278ed645-0e6c-4a5d-bd85-3e3b7a1e3333
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cce886c9929892c89b56f162f784dc27a472209
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005716"
---
# <a name="iagentballoongetbackcolor"></a>IAgentBalloon:: GetBackColor

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetBackColor(
   long * plBGColor  // address of variable for background color displayed
);                   // in word balloon
```

Recupera o valor da cor do plano de fundo exibida em um balão de palavras.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*plBGColor*
</dt> <dd>

O endereço de uma variável que recebe a configuração de cor para o plano de fundo do balão.

</dd> </dl>

A cor do plano de fundo usada em um balão de palavras de caracteres é definida no editor de caracteres do Microsoft Agent. Ele não pode ser alterado por um aplicativo. No entanto, o usuário pode alterar a cor do plano de fundo dos balões de palavra para todos os caracteres por meio da folha de propriedades do Microsoft Agent.

## <a name="see-also"></a>Consulte Também

[**IAgentBalloon:: GetForeColor**](iagentballoon--getforecolor.md)


 

 




