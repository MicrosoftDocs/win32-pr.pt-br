---
title: IAgentUserInput
description: IAgentUserInput
ms.assetid: 59ce7337-6031-4449-8b29-fd0c6737c3e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37d195d6b5d1294c071a1b73d1da95548cb7a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365934"
---
# <a name="iagentuserinput"></a>IAgentUserInput

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Quando o servidor notifica o cliente de entrada-ativo com [**IAgentNotifySink:: Command**](iagentnotifysink--command.md), ele retorna informações por meio do objeto [**IAgentUserInput**](/windows/desktop/lwef/iagentuserinput) . **IAgentUserInput** define uma interface que permite que os aplicativos consultem esses valores.

**Métodos em ordem vtable**



| Métodos IAgentUserInput                                         | Descrição                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCount**](iagentuserinput--getcount.md)                   | Retorna o número de alternativas de comando retornadas em um evento de [**comando**](command-event.md) .                                         |
| [**Getitemid**](iagentuserinput--getitemid.md)                 | Retorna a ID para uma alternativa de [**comando**](command-event.md) específico.                                                              |
| [**GetItemConfidence**](iagentuserinput--getitemconfidence.md) | Retorna o valor da propriedade [**int**](confidence-property.md) para uma alternativa de [**comando**](command-event.md) específico. |
| [**GetItemText**](iagentuserinput--getitemtext.md)             | Retorna o valor do texto de [**voz**](voice-property.md) para uma alternativa de [**comando**](command-event.md) específico.                   |
| [**GetAllItemData**](iagentuserinput--getallitemdata.md)       | Retorna os dados para todas as alternativas de [**comando**](command-event.md) .                                                                  |



 

 

 