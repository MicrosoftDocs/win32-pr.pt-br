---
description: Um aplicativo visualizador de eventos usa a função OpenEventLog para abrir o log de eventos para uma origem de evento.
ms.assetid: f10ea874-66a6-446a-a18a-0c008c2da64f
title: Lendo no log de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4642c003d31c986be55a819b513f1c28c784af2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010858"
---
# <a name="reading-from-the-event-log"></a>Lendo no log de eventos

Um aplicativo visualizador de eventos usa a função [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) para abrir o log de eventos para uma origem de evento. O Visualizador de eventos pode usar a função [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) para ler registros de eventos do log. **ReadEventLog** retorna um buffer que contém uma estrutura [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) e informações adicionais que descrevem um evento registrado. O diagrama a seguir ilustra esse processo.

![lendo no log de eventos](images/readlog.png)

Para obter um exemplo de código, consulte [consultando informações de evento](querying-for-event-source-messages.md).

 

 



