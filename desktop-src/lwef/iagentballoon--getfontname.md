---
title: IAgentBalloon getnomedafonte
description: IAgentBalloon getnomedafonte
ms.assetid: 7d057571-bb6e-4b79-bc4a-5691779ace51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73f29ad981fb4b10249b17e55c92fb286552eedc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364410"
---
# <a name="iagentballoongetfontname"></a>IAgentBalloon:: getnomedafonte

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

 

 




