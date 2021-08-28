---
title: IAgentCommandsEx SetVoiceCaption
description: IAgentCommandsEx SetVoiceCaption
ms.assetid: f13c9ca5-70c9-42d0-b53c-45dc8980a24c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85de69b4b594f93adfb0ff554819243c94986420a79c35e8d7a64a3c2eaccb6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716136"
---
# <a name="iagentcommandsexsetvoicecaption"></a>IAgentCommandsEx::SetVoiceCaption

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

Define o [**texto VoiceCaption**](voicecaption-property.md) exibido para o [**objeto Command.**](/windows/desktop/lwef/the-command-object)

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

Um BSTR que especifica o texto da propriedade [**VoiceCaption**](voicecaption-property.md) para um [**Comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Se você definir um [**objeto Command**](/windows/desktop/lwef/the-command-object) em uma coleção [**Commands**](/windows/desktop/lwef/the-commands-collection-object) e definir sua propriedade [**Voice,**](voice-property.md) normalmente também definirá sua [**propriedade VoiceCaption.**](voicecaption-property.md) Esse texto será exibido na Janela Comandos de Voz quando o aplicativo cliente estiver ativo de entrada e o caractere estiver visível. Se essa propriedade não estiver definida, a configuração da propriedade [**Legenda**](caption-property.md) determinará o texto exibido. Quando a propriedade **VoiceCaption ou** **Caption** não é definida, o comando não aparece na Janela Comandos de Voz.

## <a name="see-also"></a>Consulte Também

[**IAgentCommandsEx::GetVoiceCaption**](iagentcommandsex--getvoicecaption.md)


 

 