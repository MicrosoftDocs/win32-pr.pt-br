---
title: IAgentCommandEx SetVoiceCaption
description: IAgentCommandEx SetVoiceCaption
ms.assetid: 672fdc13-25d3-4ced-b295-2b687767c17f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358514dd33fc97a98f9b63107eabc98e0387bab8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007382"
---
# <a name="iagentcommandexsetvoicecaption"></a>IAgentCommandEx::SetVoiceCaption

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

Define o texto [**VoiceCaption**](voicecaption-property.md) exibido para um [**comando**](/windows/desktop/lwef/the-command-object).

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

Um BSTR que especifica o texto para a propriedade [**VoiceCaption**](voicecaption-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Se você definir um objeto de [**comando**](/windows/desktop/lwef/the-command-object) em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) e definir sua propriedade de [**voz**](voice-property.md) , normalmente também definirá sua propriedade [**VoiceCaption**](voicecaption-property.md) . Esse texto será exibido na janela comandos de voz quando o aplicativo cliente estiver ativo na entrada. Se essa propriedade não for definida, a configuração da propriedade [**Caption**](caption-property.md) determinará o texto exibido. Quando nem o **VoiceCaption** ou a propriedade é definida, o comando não aparece na janela de comandos de voz.

[**Legenda**](caption-property.md)

## <a name="see-also"></a>Consulte Também

[**IAgentCommand:: getCaption**](iagentcommand--getcaption.md), [**IAgentCommand:: sethabilited**](iagentcommand--setenabled.md), [**IAgentCommand:: setvisível**](iagentcommand--setvisible.md), [**IAgentCommand:: setvoice**](iagentcommand--setvoice.md), [**IAgentCommandsEx:: AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx:: InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)


 

 