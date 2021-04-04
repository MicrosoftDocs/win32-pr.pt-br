---
title: IAgentBalloon GetFontUnderline
description: IAgentBalloon GetFontUnderline
ms.assetid: 19886e94-8095-4650-bd88-34ea9d96ddaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5acf35453209679dc96c85b3017fbe76b19d53b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006105"
---
# <a name="iagentballoongetfontunderline"></a>IAgentBalloon::GetFontUnderline

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetFontUnderline(
   long * pbFontUnderline  // address of variable for underline setting
);                         // for font displayed in word balloon 
```

Indica se a fonte usada em um balão de palavra tem o estilo de sublinhado definido.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbFontUnderline"></span><span id="pbfontunderline"></span><span id="PBFONTUNDERLINE"></span>*pbFontUnderline*
</dt> <dd>

O endereço de um valor que recebe **true** se o estilo de sublinhado da fonte for definido e **false** se não.

</dd> </dl>

O estilo de fonte usado em um balão de palavras de caracteres é definido no editor de caracteres do agente da Microsoft. Ele não pode ser alterado por um aplicativo. No entanto, o usuário pode substituir as configurações de fonte para todos os caracteres usando a folha de propriedades do Microsoft Agent.

 

 




