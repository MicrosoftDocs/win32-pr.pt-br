---
title: GetBackColor de IAgentBallballballball
description: GetBackColor de IAgentBallballballball
ms.assetid: 278ed645-0e6c-4a5d-bd85-3e3b7a1e3333
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7c58a913332d01f2982c28003c146420d34a86e96f3c833f667c968bd22ef19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888416"
---
# <a name="iagentballoongetbackcolor"></a>IAgentBallball::GetBackColor

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetBackColor(
   long * plBGColor  // address of variable for background color displayed
);                   // in word balloon
```

Recupera o valor da cor da tela de fundo exibida em um balão de palavra.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*plBGColor*
</dt> <dd>

O endereço de uma variável que recebe a configuração de cor para a tela de fundo do balão.

</dd> </dl>

A cor da tela de fundo usada em um balão de palavra de caractere é definida no Editor de Caracteres do Microsoft Agent. Ele não pode ser alterado por um aplicativo. No entanto, o usuário pode alterar a cor da tela de fundo da palavra balão para todos os caracteres por meio da folha de propriedades do Microsoft Agent.

## <a name="see-also"></a>Consulte Também

[**IAgentBallball::GetForeColor**](iagentballoon--getforecolor.md)


 

 




