---
title: IAgentBalloon GetFontUnderline
description: IAgentBalloon GetFontUnderline
ms.assetid: 19886e94-8095-4650-bd88-34ea9d96ddaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 325f383aa76c55068ca7244b4ce0f822602651fa196ee336060fcc21fe3ab068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962356"
---
# <a name="iagentballoongetfontunderline"></a>IAgentBallunder::GetFontUnderline

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetFontUnderline(
   long * pbFontUnderline  // address of variable for underline setting
);                         // for font displayed in word balloon 
```

Indica se a fonte usada em um balão de palavra tem o estilo sublinhado definido.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbFontUnderline"></span><span id="pbfontunderline"></span><span id="PBFONTUNDERLINE"></span>*pbFontUnderline*
</dt> <dd>

O endereço de um valor que receberá **True se** o estilo de sublinhado da fonte estiver definido e **False** se não.

</dd> </dl>

O estilo de fonte usado em um balão de palavra de caractere é definido no Editor de Caracteres do Microsoft Agent. Ele não pode ser alterado por um aplicativo. No entanto, o usuário pode substituir as configurações de fonte para todos os caracteres usando a folha de propriedades do Microsoft Agent.

 

 




