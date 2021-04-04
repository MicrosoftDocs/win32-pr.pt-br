---
title: IAgentCommand sethabilitado
description: IAgentCommand sethabilitado
ms.assetid: e0a724b4-3613-400f-a801-efc8bf66e355
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8377307d66257f7a9b74ac82512edc6e4ec64034
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007422"
---
# <a name="iagentcommandsetenabled"></a>IAgentCommand:: sethabilitado

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetEnabled(
   long bEnabled  // Enabled setting for Command
);
```

Define a propriedade [**Enabled**](enabled-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object).

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Um valor booliano que define o valor da configuração [**habilitada**](enabled-property.md) de um [**comando**](/windows/desktop/lwef/the-command-object). **True** habilita o **comando**; **False** desabilita. Um **comando** desabilitado não pode ser selecionado.

</dd> </dl>

Um [**comando**](/windows/desktop/lwef/the-command-object) deve ter sua propriedade [**Enabled**](enabled-property.md) definida como **true** para ser selecionável. Ele também deve ter sua propriedade [**Caption**](caption-property.md) definida e sua propriedade [**Visible**](visible-property.md) definida como **true** para aparecer no menu pop-up do caractere. Para fazer com que o **comando** apareça na **janela de comandos de voz**, você deve definir sua propriedade de [**voz**](voice-property.md).

## <a name="see-also"></a>Consulte Também

[**IAgentCommand:: getCaption**](iagentcommand--getcaption.md), [**IAgentCommand:: setvoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Adicionar**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)


 

 