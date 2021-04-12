---
title: IAgentBalloon GetFontStrikethru
description: IAgentBalloon GetFontStrikethru
ms.assetid: b5c253e8-dca7-44a6-b63b-a33e6e793a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2001ec0125949144843d500f125b3502e94723db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364408"
---
# <a name="iagentballoongetfontstrikethru"></a>IAgentBalloon::GetFontStrikethru

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetFontStrikethru(
   long * pbFontStrikethru  // address of variable for strikethrough setting 
);                          // for font displayed in word balloon 
```

Indica se a fonte usada em um balão de palavra tem o estilo tachado definido.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbFontStrikethru"></span><span id="pbfontstrikethru"></span><span id="PBFONTSTRIKETHRU"></span>*pbFontStrikethru*
</dt> <dd>

O endereço de um valor que recebe **true** se o estilo tachado da fonte for definido e **false** se não.

</dd> </dl>

O estilo de fonte usado em um balão de palavras de caracteres é definido no editor de caracteres do agente da Microsoft. Ele não pode ser alterado por um aplicativo. No entanto, o usuário pode substituir as configurações de fonte para todos os caracteres usando a folha de propriedades do Microsoft Agent.

 

 




