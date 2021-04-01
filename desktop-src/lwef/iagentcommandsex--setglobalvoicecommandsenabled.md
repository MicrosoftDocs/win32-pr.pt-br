---
title: IAgentCommandsEx SetGlobalVoiceCommandsEnabled
description: IAgentCommandsEx SetGlobalVoiceCommandsEnabled
ms.assetid: f456b1d3-60aa-4b90-90d0-6c695947fa8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87a576a36d3df4b3ddf0ca71f5709a712a3c9e1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084504"
---
# <a name="iagentcommandsexsetglobalvoicecommandsenabled"></a>IAgentCommandsEx::SetGlobalVoiceCommandsEnabled

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetGlobalVoiceCommandsEnabled(
 long bEnable  // Enabled setting for Agent's global voice commands
);
```

Define a propriedade [**Enabled**](enabled-property.md) para a gramática de voz dos comandos globais do Microsoft Agent.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bEnable"></span><span id="benable"></span><span id="BENABLE"></span>*bEnable*
</dt> <dd>

Um valor booliano que define se a gramática de voz dos comandos globais do agente está habilitada. **Verdadeiro** habilita a gramática de voz; **False** desabilita.

</dd> </dl>

O Microsoft Agent adiciona automaticamente parâmetros de voz (gramática) para abrir e fechar a janela de comandos de voz e para mostrar e ocultar o caractere. Quando definido como **false**, o Agent desabilita qualquer parâmetro de voz para esses comandos, bem como os parâmetros de voz para a [**legenda**](caption-property.md) dos objetos de [**comando**](/windows/desktop/lwef/the-command-object) do outro cliente. Isso permite que você os elimine da gramática ativa atual do seu cliente. No entanto, como isso potencialmente bloqueia o acesso de voz a outros clientes, redefina essa propriedade como **true** depois de processar a entrada de voz do usuário.

Desabilitar a propriedade não afeta o menu pop-up do caractere. Os comandos globais adicionados pelo servidor ainda serão exibidos. Você não pode removê-los do menu pop-up.

## <a name="see-also"></a>Consulte Também

[**IAgentCommandsEx::GetGlobalVoiceCommandsEnabled**](iagentcommandsex--getglobalvoicecommandsenabled.md)


 

 