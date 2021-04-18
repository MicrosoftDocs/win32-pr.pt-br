---
title: IAgentCommandsEx SetVoiceCaption
description: IAgentCommandsEx SetVoiceCaption
ms.assetid: f13c9ca5-70c9-42d0-b53c-45dc8980a24c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fcc0f3ce98ff0187b7ed2f01b7131cc8e101bd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105815591"
---
# <a name="iagentcommandsexsetvoicecaption"></a>IAgentCommandsEx::SetVoiceCaption

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

Define o texto [**VoiceCaption**](voicecaption-property.md) exibido para o objeto de [**comando**](/windows/desktop/lwef/the-command-object) .

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

Um BSTR que especifica o texto para a propriedade [**VoiceCaption**](voicecaption-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Se você definir um objeto de [**comando**](/windows/desktop/lwef/the-command-object) em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) e definir sua propriedade de [**voz**](voice-property.md) , normalmente também definirá sua propriedade [**VoiceCaption**](voicecaption-property.md) . Esse texto será exibido na janela de comandos de voz quando o aplicativo cliente for de entrada-ativo e o caractere estiver visível. Se essa propriedade não for definida, a configuração da propriedade [**Caption**](caption-property.md) determinará o texto exibido. Quando nem a propriedade **VoiceCaption** ou **Caption** for definida, o comando não aparecerá na janela comandos de voz.

## <a name="see-also"></a>Consulte Também

[**IAgentCommandsEx::GetVoiceCaption**](iagentcommandsex--getvoicecaption.md)


 

 