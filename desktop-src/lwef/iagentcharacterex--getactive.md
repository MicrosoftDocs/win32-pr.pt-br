---
title: IAgentCharacterEx getactive
description: IAgentCharacterEx getactive
ms.assetid: b14ae69a-a50e-4488-b5a7-33702e6555eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1dab89ee9ba89c5982e34844917334d97169b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822888"
---
# <a name="iagentcharacterexgetactive"></a>IAgentCharacterEx:: getactive

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetActive(
   short * psState  // address of active state setting
);
```

Recupera se o aplicativo cliente é o cliente ativo do caractere e se o caractere está no nível mais alto.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*psState*
</dt> <dd>

Endereço de uma variável que recebe um dos seguintes valores para a configuração de Estado:



| Valor                                                              | Descrição                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| **const não assinada curto ativar não** **\_ ativo = 0;**<br/>   | O cliente não é o cliente ativo do caractere.                |
| **const não assinada curto** **Ativar \_ ativa = 1;**<br/>      | O cliente é o cliente ativo do caractere.                    |
| **const não assinada curto** **Ativar \_ INPUTACTIVE = 2;**<br/> | O cliente está em entrada-ativo (cliente ativo do caractere superior). |



 

</dd> </dl>

Essa configuração permite que você saiba se você é o cliente ativo do caractere ou se o caractere é o caractere ativo de entrada. Quando vários aplicativos cliente compartilham o mesmo caractere, o cliente ativo do caractere recebe a entrada do mouse (por exemplo, o controle do Microsoft Agent clica ou arrasta eventos). Da mesma forma, quando vários caracteres são exibidos, o cliente ativo do caractere superior (também conhecido como o cliente de entrada-ativo) recebe eventos de [**comando IAgentNotifySink::**](iagentnotifysink--command.md) .

Use o método [**Activate**](iagentcharacter--activate.md) para definir se seu aplicativo é o cliente ativo do caractere ou para tornar seu aplicativo o cliente de entrada ativo (o que também torna o caractere mais alto).

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter:: Activate**](iagentcharacter--activate.md), [ **IAgentNotifySinkEx:: ActiveClientChange**](iagentnotifysinkex--activeclientchange.md)


 

 





