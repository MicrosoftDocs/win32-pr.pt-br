---
title: Getvoice IAgentCommands
description: Getvoice IAgentCommands
ms.assetid: ef8983bc-c70c-48c7-9c5f-1dae61028d90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b1915512c89611267df3788e5dcaa84fb0874a4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104366014"
---
# <a name="iagentcommandsgetvoice"></a>IAgentCommands:: getvoice

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Commands collection
);
```

Recupera o valor da propriedade de [**voz**](voice-property.md) para uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*
</dt> <dd>

O endereço de um BSTR que recebe o valor da configuração de texto de [**voz**](voice-property.md) para uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentCommands:: setvoice**](iagentcommands--setvoice.md), [**IAgentCommands:: getCaption**](iagentcommands--getcaption.md), [**IAgentCommands:: getVisible**](iagentcommands--getvisible.md)


 

 