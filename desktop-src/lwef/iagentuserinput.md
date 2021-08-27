---
title: IAgentUserInput
description: IAgentUserInput
ms.assetid: 59ce7337-6031-4449-8b29-fd0c6737c3e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58ed14c9097a4bd5d3d743a5c026f3e13d6d5ed29a73edb619dd0b2e8bdae17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114646"
---
# <a name="iagentuserinput"></a>IAgentUserInput

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

Quando o servidor notifica o cliente de entrada-ativo com [**IAgentNotifySink:: Command**](iagentnotifysink--command.md), ele retorna informações por meio do objeto [**IAgentUserInput**](/windows/desktop/lwef/iagentuserinput) . **IAgentUserInput** define uma interface que permite que os aplicativos consultem esses valores.

**Métodos em ordem vtable**



| Métodos IAgentUserInput                                         | Descrição                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetCount**](iagentuserinput--getcount.md)                   | Retorna o número de alternativas de comando retornadas em um evento de [**comando**](command-event.md) .                                         |
| [**Getitemid**](iagentuserinput--getitemid.md)                 | Retorna a ID para uma alternativa de [**comando**](command-event.md) específico.                                                              |
| [**GetItemConfidence**](iagentuserinput--getitemconfidence.md) | Retorna o valor da propriedade [**int**](confidence-property.md) para uma alternativa de [**comando**](command-event.md) específico. |
| [**GetItemText**](iagentuserinput--getitemtext.md)             | Retorna o valor do texto de [**voz**](voice-property.md) para uma alternativa de [**comando**](command-event.md) específico.                   |
| [**GetAllItemData**](iagentuserinput--getallitemdata.md)       | Retorna os dados para todas as alternativas de [**comando**](command-event.md) .                                                                  |



 

 

 