---
description: Os tópicos a seguir descrevem como usar a API do ETW para rastreamento de eventos.
ms.assetid: 7362874a-8206-4973-bb79-a9eaff55feb4
title: Usando o rastreamento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5141c19838796c0ec29f9eb20add689d56b97757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164742"
---
# <a name="using-event-tracing"></a>Usando o rastreamento de eventos

Os tópicos a seguir descrevem como usar a API do ETW para rastreamento de eventos.



| Tópico                                                                          | Descrição                                                                                                             |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Controlando sessões de rastreamento de eventos](controlling-event-tracing-sessions.md)   | Descreve como gerenciar sessões de rastreamento de eventos.                                                                         |
| [Fornecendo eventos](providing-events.md)                                       | Descreve como registrar e instrumentar um provedor de rastreamento de eventos.                                                       |
| [Consumindo eventos](consuming-events.md)                                       | Descreve como implementar funções de retorno de chamada usadas para consumir e processar eventos de um arquivo de log de rastreamento ou em tempo real. |
| [Pré-processador de rastreamento de software do Windows](windows-software-trace-preprocessor.md) | Fornece um mecanismo eficiente para registrar e consumir eventos que ocorrem durante a execução de um aplicativo ou driver.  |



 

Inclua o arquivo de cabeçalho Wmistr. h antes de incluir o arquivo de cabeçalho Evntrace. h.

 

 



