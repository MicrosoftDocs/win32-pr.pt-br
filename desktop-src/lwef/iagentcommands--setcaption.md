---
title: IAgentCommands AutoCaption
description: IAgentCommands AutoCaption
ms.assetid: 042f7366-0071-40a5-a47c-81c02cdbe3a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8c472bfbfd82235e21c28e24e7e0ce03223ff8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365874"
---
# <a name="iagentcommandssetcaption"></a>IAgentCommands:: SetCaption

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Commands collection
);
```

Define o texto de [**legenda**](caption-property.md) exibido para uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

Um BSTR que especifica o valor da propriedade [**Caption**](caption-property.md) para uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

Definir a propriedade [**Caption**](caption-property.md) para uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) define como ela será exibida no menu pop-up do caractere quando sua propriedade [**Visible**](visible-property.md) é definida como **true** e seu aplicativo não é o cliente de entrada-ativo. Para especificar uma tecla de acesso (mnemônico não embutido) para sua **legenda**, inclua um caractere de e comercial (&) antes desse caractere.

Se você definir comandos para uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) que tenha sua [**legenda**](caption-property.md) definida, normalmente também definirá uma **legenda** para sua coleção de **comandos** .

## <a name="see-also"></a>Consulte Também

[**IAgentCommands:: getCaption**](iagentcommands--getcaption.md), [**IAgentCommands:: setvisível**](iagentcommands--setvisible.md), [**IAgentCommands:: setvoice**](iagentcommands--setvoice.md)


 

 