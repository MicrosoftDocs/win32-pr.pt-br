---
title: IAgentCommands SetCaption
description: IAgentCommands SetCaption
ms.assetid: 042f7366-0071-40a5-a47c-81c02cdbe3a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b38138d218804461afc782efc14ff3685f55d2f737db6fdb21c39021efbcb36e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665466"
---
# <a name="iagentcommandssetcaption"></a>IAgentCommands::SetCaption

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Commands collection
);
```

Define o [**texto Legenda**](caption-property.md) exibido para uma coleção [**comandos.**](/windows/desktop/lwef/the-commands-collection-object)

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

Um BSTR que especifica o valor da propriedade [**Caption**](caption-property.md) para uma coleção [**commands.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> </dl>

Definir a propriedade [**Legenda**](caption-property.md) para uma coleção [**de**](/windows/desktop/lwef/the-commands-collection-object) Comandos define como ela será exibida no menu pop-up do caractere quando sua propriedade [**Visible**](visible-property.md) estiver definida como **True** e seu aplicativo não for o cliente ativo de entrada. Para especificar uma chave de acesso (mnemônico não emlindado) para a **Legenda**, inclua um caractere & (entese) antes desse caractere.

Se você definir comandos para uma coleção [**De**](/windows/desktop/lwef/the-commands-collection-object) comandos que tem sua [**Legenda**](caption-property.md) definida, normalmente também definirá uma **Legenda** para sua coleção **de Comandos.**

## <a name="see-also"></a>Consulte Também

[**IAgentCommands::GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands::SetVisible**](iagentcommands--setvisible.md), [**IAgentCommands::SetVoice**](iagentcommands--setvoice.md)


 

 