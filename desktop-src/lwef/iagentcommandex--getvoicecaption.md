---
title: IAgentCommandEx GetVoiceCaption
description: IAgentCommandEx GetVoiceCaption
ms.assetid: a81accfd-c137-4347-8ead-4ed5e7148751
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d093a971331c6c5cddf467e770dae69960ae0d616ddc9b37863a46d25becb7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105414"
---
# <a name="iagentcommandexgetvoicecaption"></a>IAgentCommandEx::GetVoiceCaption

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetVoiceCaption(
   BSTR * pbszVoiceCaption  // address of command's voice caption text
);
```

Recupera o [**VoiceCaption para**](voicecaption-property.md) um [**comando**](/windows/desktop/lwef/the-command-object).

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszVoiceCaption*
</dt> <dd>

O endereço de um BSTR que recebe o valor do texto [**Legenda**](caption-property.md) exibido para um [**Comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

O [**VoiceCaption é**](voicecaption-property.md) o texto que aparece para um objeto [**Command**](/windows/desktop/lwef/the-command-object) na Janela Comandos de Voz quando o aplicativo cliente está ativo de entrada.

## <a name="see-also"></a>Consulte Também

[**IAgentCommandEx::SetVoiceCaption**](iagentcommandex--setvoicecaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommandsEx::AddEx,**](iagentcommandsex--addex.md) [**IAgentCommandsEx::InsertEx,**](iagentcommandsex--insertex.md) [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)


 

 