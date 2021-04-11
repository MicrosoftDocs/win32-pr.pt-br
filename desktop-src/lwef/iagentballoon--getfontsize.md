---
title: IAgentBalloon getfontize
description: IAgentBalloon getfontize
ms.assetid: 4d342ee9-abb4-431b-bd28-f62ab76705ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14b1a921f1f5c9927f58ab9e561569ba3bc98fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160454"
---
# <a name="iagentballoongetfontsize"></a>IAgentBalloon:: getfontize

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in word balloon 
```

Recupera o valor do tamanho da fonte exibida em um balão de palavras.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*
</dt> <dd>

O endereço de um valor que recebe o tamanho da fonte.

</dd> </dl>

O tamanho de fonte padrão usado em um balão de palavras de caracteres é definido no editor de caracteres do agente da Microsoft. Você pode alterá-lo com [**IAgentBalloon:: Setfontize**](https://www.bing.com/search?q=**IAgentBalloon::SetFontSize**). No entanto, o usuário pode substituir as configurações de tamanho da fonte para todos os caracteres usando a folha de propriedades do Microsoft Agent.

 

 




