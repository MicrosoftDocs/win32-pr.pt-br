---
title: IAgentCommand SetEnabled
description: IAgentCommand SetEnabled
ms.assetid: e0a724b4-3613-400f-a801-efc8bf66e355
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da164b6603d93496e3381ccc6938a3b6d8f520bcea887cfd11f031cec7d845a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976306"
---
# <a name="iagentcommandsetenabled"></a>IAgentCommand::SetEnabled

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetEnabled(
   long bEnabled  // Enabled setting for Command
);
```

Define a [**propriedade Enabled**](enabled-property.md) para um [**Comando**](/windows/desktop/lwef/the-command-object).

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Um valor booliana que define o valor da [**configuração Habilitado**](enabled-property.md) de um [**Comando**](/windows/desktop/lwef/the-command-object). **True** habilita o **comando**; **False** desabilita-o. Um **Comando desabilitado** não pode ser selecionado.

</dd> </dl>

Um [**Comando**](/windows/desktop/lwef/the-command-object) deve ter sua [**propriedade Enabled**](enabled-property.md) definida como **True** para ser selecionável. Ele também deve ter sua [**propriedade Caption**](caption-property.md) definida e sua propriedade [**Visible**](visible-property.md) definida como **True** para aparecer no menu pop-up do caractere. Para fazer com **que o Comando** apareça na janela Comandos de **Voz**, você deve definir sua [**propriedade Voz.**](voice-property.md)

## <a name="see-also"></a>Consulte Também

[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetVoice,**](iagentcommand--setvoice.md) [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)


 

 