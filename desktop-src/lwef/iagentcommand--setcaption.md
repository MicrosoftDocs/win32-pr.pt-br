---
title: IAgentCommand AutoCaption
description: IAgentCommand AutoCaption
ms.assetid: f4fdd37a-28b4-4e00-885c-58addedec659
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ffccf42a972ec9635c929fb954d58bfaff967af364d24ae505e1dbb2bd8772
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976356"
---
# <a name="iagentcommandsetcaption"></a>IAgentCommand:: SetCaption

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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


 

 