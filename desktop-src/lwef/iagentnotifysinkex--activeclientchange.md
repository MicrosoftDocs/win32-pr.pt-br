---
title: IAgentNotifySinkEx ActiveClientChange
description: IAgentNotifySinkEx ActiveClientChange
ms.assetid: e953e803-c898-4c07-adc0-8b895b5e8473
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50549c4b091a39614fd7ff6b15af0bc1436113dfd2e9b3d31ca86e6995a0e94d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961496"
---
# <a name="iagentnotifysinkexactiveclientchange"></a>IAgentNotifySinkEx::ActiveClientChange

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

Identificador do caractere para o qual o status ativo do cliente foi alterado.

</dd> <dt>

<span id="lStatus"></span><span id="lstatus"></span><span id="LSTATUS"></span>*lStatus*
</dt> <dd>

Alteração de estado ativo do cliente, que pode ser uma combinação de qualquer um dos seguintes valores:



| Valor                                                              | Descrição                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| **const unsigned short** **ACTIVATE \_ NOTACTIVE = 0;**<br/>   | Seu cliente não é o cliente ativo do caractere.                |
| **const unsigned short** **ACTIVATE ACTIVE = \_ 1;**<br/>      | Seu cliente é o cliente ativo do caractere.                    |
| **const unsigned short** **ACTIVATE \_ INPUTACTIVE = 2;**<br/> | Seu cliente está ativo de entrada (cliente ativo do caractere mais alto). |



 

</dd> </dl>

Quando vários aplicativos cliente compartilham o mesmo caractere, o cliente ativo do caractere recebe entrada do mouse (por exemplo, eventos de clique ou arrastar do controle do Microsoft Agent). Da mesma forma, quando vários caracteres são exibidos, o cliente ativo do caractere mais alto (também conhecido como cliente ativo de entrada) recebe eventos [**IAgentNotifySink::Command.**](iagentnotifysink--command.md)

Quando o cliente ativo de um caractere muda, esse evento passa a ID desse caractere e **True** se o aplicativo se tornou o cliente ativo do caractere ou **False** se ele não for mais o cliente ativo do caractere.

Um aplicativo cliente pode receber esse evento quando o usuário seleciona a entrada de outro aplicativo cliente no menu pop-up do caractere ou por comando de voz, o aplicativo cliente altera seu status ativo ou outro aplicativo cliente sai de sua conexão com o Microsoft Agent. O Agent envia esse evento somente para os aplicativos cliente que são afetados diretamente– aqueles que se tornam o cliente ativo ou param de ser o cliente ativo.

Você pode usar o método [**Activate**](iagentcharacter--activate.md) para definir se seu aplicativo é o cliente ativo do caractere ou para tornar seu aplicativo o cliente ativo de entrada (que também torna o caractere mais alto).

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter::Activate**](iagentcharacter--activate.md), [**IAgentCharacterEx::GetActive,**](iagentcharacterex--getactive.md) [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md)


 

 





