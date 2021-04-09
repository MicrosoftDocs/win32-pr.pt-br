---
title: IAgentCommand AutoCaption
description: IAgentCommand AutoCaption
ms.assetid: f4fdd37a-28b4-4e00-885c-58addedec659
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88453f54ffa59b413f30d27c58aa6cd2dcc6e12e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007469"
---
# <a name="iagentcommandsetcaption"></a>IAgentCommand:: SetCaption

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Command
);
```

Define o texto de [**legenda**](caption-property.md) exibido para um [**comando**](/windows/desktop/lwef/the-command-object).

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

Um BSTR que especifica o texto para a propriedade [**Caption**](caption-property.md) de um [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Definir a propriedade [**Caption**](caption-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object) define como ele será exibido no menu pop-up do caractere quando sua propriedade [**Visible**](visible-property.md) é definida como **true** e seu aplicativo não é o cliente de entrada-ativo. Para especificar uma tecla de acesso (mnemônico não embutido) para sua **legenda**, inclua um caractere de e comercial (&) antes desse caractere. Para torná-lo selecionável, sua propriedade [**Enabled**](enabled-property.md) deve ser definida como **true**.

## <a name="see-also"></a>Consulte Também

[**IAgentCommand:: getCaption**](iagentcommand--getcaption.md), [**IAgentCommand:: sethabilitated**](iagentcommand--setenabled.md), [**IAgentCommand:: setvisível**](iagentcommand--setvisible.md), [**IAgentCommand:: setvoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Adicionar**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)


 

 