---
title: IAgentBalloon getnomedafonte
description: IAgentBalloon getnomedafonte
ms.assetid: 7d057571-bb6e-4b79-bc4a-5691779ace51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cb0bceae040f9261d2530b19d074df937dbdaf80d91a27f57b5cf9c1fd8f89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725307"
---
# <a name="iagentballoongetfontname"></a>IAgentBalloon:: getnomedafonte

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in word balloon
```

Recupera o valor da fonte exibida em um balão de palavras.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*
</dt> <dd>

O endereço de um BSTR que recebe o nome da fonte exibido em um balão de palavra.

</dd> </dl>

A fonte padrão usada em um balão de palavras de caracteres é definida no editor de caracteres do Microsoft Agent. Você pode alterá-lo com [**IAgentBalloon:: setnomedafonte**](https://www.bing.com/search?q=**IAgentBalloon::SetFontName**). O usuário pode substituir a configuração de fonte para todos os caracteres usando a folha de propriedades do Microsoft Agent.

 

 




