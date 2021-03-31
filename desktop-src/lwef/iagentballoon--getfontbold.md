---
title: IAgentBalloon GetFontBold
description: IAgentBalloon GetFontBold
ms.assetid: 5a55f771-d68e-4f66-8001-47c141661b06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858f6f42964db1bdd7ae548d308c6f6668b05631
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159985"
---
# <a name="iagentballoongetfontbold"></a>IAgentBalloon::GetFontBold

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetFontBold(
   long * pbFontBold  // address of variable for bold setting for
);                    // font displayed in word balloon 
```

Indica se a fonte usada em um balão de palavra está em negrito.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbFontBold"></span><span id="pbfontbold"></span><span id="PBFONTBOLD"></span>*pbFontBold*
</dt> <dd>

O endereço de um valor que recebe **true** se a fonte for Bold e **false** se não estiver em negrito.

</dd> </dl>

O estilo de fonte usado em um balão de palavras de caracteres é definido no editor de caracteres do agente da Microsoft. Ele não pode ser alterado por um aplicativo. No entanto, o usuário pode substituir as configurações de fonte de todos os caracteres por meio da folha de propriedades do Microsoft Agent.

 

 




