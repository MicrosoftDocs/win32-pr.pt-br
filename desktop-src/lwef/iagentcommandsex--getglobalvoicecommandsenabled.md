---
title: IAgentCommandsEx GetGlobalVoiceCommandsEnabled
description: IAgentCommandsEx GetGlobalVoiceCommandsEnabled
ms.assetid: 9c8fa978-a02b-4dfc-8cf7-e066c5b75122
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea7275bfe28190e06782cb2564dbf4868dd2c096
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365935"
---
# <a name="iagentcommandsexgetglobalvoicecommandsenabled"></a>IAgentCommandsEx::GetGlobalVoiceCommandsEnabled

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetGlobalVoiceCommandsEnabled(
   long * pbEnabled  // address of the global voice command setting
);
```

Recupera se a gramática de voz para comandos globais do agente está habilitada.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

O endereço que receberá **true** se a gramática de voz para comandos globais do agente estiver habilitada; **false** se estiver desabilitado.

</dd> </dl>

O Microsoft Agent adiciona automaticamente parâmetros de voz (gramática) para abrir e fechar a janela de comandos de voz e para mostrar e ocultar o caractere. Quando esse método retorna **false**, quaisquer parâmetros de voz para esses comandos, bem como os parâmetros de voz para a [**legenda**](caption-property.md) dos objetos de [**comando**](/windows/desktop/lwef/the-command-object) de outros clientes, não são incluídos na gramática. Isso permite que você os elimine da gramática ativa atual do seu cliente. No entanto, essa configuração não reflete a inclusão desses comandos no menu pop-up do caractere.

## <a name="see-also"></a>Consulte Também

[**IAgentCommandsEx::SetGlobalVoiceCommandsEnabled**](iagentcommandsex--setglobalvoicecommandsenabled.md)


 

 