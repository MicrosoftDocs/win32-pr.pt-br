---
title: IAgentCharacterEx GetActive
description: IAgentCharacterEx GetActive
ms.assetid: b14ae69a-a50e-4488-b5a7-33702e6555eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533f9cb05143d4948fbcae1f8d9ed74a7216c5a2520b28f4c299321bcbac4272
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478020"
---
# <a name="iagentcharacterexgetactive"></a>IAgentCharacterEx::GetActive

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetActive(
   short * psState  // address of active state setting
);
```

Recupera se o aplicativo cliente é o cliente ativo do caractere e se o caractere é o mais alto.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="psState"></span><span id="psstate"></span><span id="PSSTATE"></span>*psState*
</dt> <dd>

Endereço de uma variável que recebe um dos seguintes valores para a configuração de estado:



| Valor                                                              | Descrição                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| **const unsigned short** **ACTIVATE \_ NOTACTIVE = 0;**<br/>   | Seu cliente não é o cliente ativo do caractere.                |
| **const unsigned short** **ACTIVATE ACTIVE = \_ 1;**<br/>      | Seu cliente é o cliente ativo do caractere.                    |
| **const unsigned short** **ACTIVATE \_ INPUTACTIVE = 2;**<br/> | Seu cliente está ativo de entrada (cliente ativo do caractere mais alto). |



 

</dd> </dl>

Essa configuração permite que você saiba se você é o cliente ativo do caractere ou se o caractere é o caractere ativo de entrada. Quando vários aplicativos cliente compartilham o mesmo caractere, o cliente ativo do caractere recebe entrada do mouse (por exemplo, eventos de clique ou arrastar do controle do Microsoft Agent). Da mesma forma, quando vários caracteres são exibidos, o cliente ativo do caractere mais alto (também conhecido como cliente ativo de entrada) recebe eventos [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

Use o [**método Activate**](iagentcharacter--activate.md) para definir se seu aplicativo é o cliente ativo do caractere ou para tornar seu aplicativo o cliente ativo de entrada (que também torna o caractere mais alto).

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter::Activate**](iagentcharacter--activate.md), [ **IAgentNotifySinkEx::ActiveClientChange**](iagentnotifysinkex--activeclientchange.md)


 

 





