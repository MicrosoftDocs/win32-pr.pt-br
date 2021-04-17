---
title: IAgentNotifySinkEx ActiveClientChange
description: IAgentNotifySinkEx ActiveClientChange
ms.assetid: e953e803-c898-4c07-adc0-8b895b5e8473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96988f80d8a1799bf46f12bd38906e9357453f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105763019"
---
# <a name="iagentnotifysinkexactiveclientchange"></a>IAgentNotifySinkEx::ActiveClientChange

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT ActiveClientChange(
...long dwCharID,  // character ID
   long lStatus    // active state flag
);
```

Notifica um aplicativo cliente se seu cliente ativo não for mais o cliente ativo de um caractere.

-   Sem valor de retorno.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador do caractere para o qual o status do cliente ativo foi alterado.

</dd> <dt>

<span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*lStatus*
</dt> <dd>

Alteração de estado ativo do cliente, que pode ser uma combinação de qualquer um dos seguintes valores:



| Valor                                                              | Descrição                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| **const não assinada curto ativar não** **\_ ativo = 0;**<br/>   | O cliente não é o cliente ativo do caractere.                |
| **const não assinada curto** **Ativar \_ ativa = 1;**<br/>      | O cliente é o cliente ativo do caractere.                    |
| **const não assinada curto** **Ativar \_ INPUTACTIVE = 2;**<br/> | O cliente está em entrada-ativo (cliente ativo do caractere superior). |



 

</dd> </dl>

Quando vários aplicativos cliente compartilham o mesmo caractere, o cliente ativo do caractere recebe a entrada do mouse (por exemplo, o controle do Microsoft Agent clica ou arrasta eventos). Da mesma forma, quando vários caracteres são exibidos, o cliente ativo do caractere superior (também conhecido como o cliente de entrada-ativo) recebe eventos de [**comando IAgentNotifySink::**](iagentnotifysink--command.md) .

Quando o cliente ativo de um caractere é alterado, esse evento retorna a ID desse caractere e **true** se o aplicativo se tornou o cliente ativo do caractere ou **false** se não for mais o cliente ativo do caractere.

Um aplicativo cliente pode receber esse evento quando o usuário seleciona a entrada de outro aplicativo cliente no menu pop-up do caractere ou por comando de voz, o aplicativo cliente altera seu status ativo ou outro aplicativo cliente encerra sua conexão com o Microsoft Agent. O Agent envia esse evento somente para os aplicativos cliente que são diretamente afetados – aqueles que se tornam o cliente ativo ou que param de ser o cliente ativo.

Você pode usar o método [**Activate**](iagentcharacter--activate.md) para definir se seu aplicativo é o cliente ativo do caractere ou para tornar seu aplicativo o cliente de entrada-ativo (o que também torna o caractere mais alto).

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter:: ativar**](iagentcharacter--activate.md), [**IAgentCharacterEx:: getactive**](iagentcharacterex--getactive.md), [**IAgentNotifySink:: ActivateInputState**](iagentnotifysink--activateinputstate.md)


 

 





