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
# <a name="reading-from-the-event-log"></a><span data-ttu-id="fe37f-103">Lendo no log de eventos</span><span class="sxs-lookup"><span data-stu-id="fe37f-103">Reading from the Event Log</span></span>

<span data-ttu-id="fe37f-104">Um aplicativo visualizador de eventos usa a função [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) para abrir o log de eventos para uma origem de evento.</span><span class="sxs-lookup"><span data-stu-id="fe37f-104">An event viewer application uses the [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) function to open the event log for an event source.</span></span> <span data-ttu-id="fe37f-105">O Visualizador de eventos pode usar a função [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) para ler registros de eventos do log.</span><span class="sxs-lookup"><span data-stu-id="fe37f-105">The event viewer can then use the [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) function to read event records from the log.</span></span> <span data-ttu-id="fe37f-106">**ReadEventLog** retorna um buffer que contém uma estrutura [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) e informações adicionais que descrevem um evento registrado.</span><span class="sxs-lookup"><span data-stu-id="fe37f-106">**ReadEventLog** returns a buffer containing an [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structure and additional information that describes a logged event.</span></span> <span data-ttu-id="fe37f-107">O diagrama a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="fe37f-107">The following diagram illustrates this process.</span></span>

![lendo no log de eventos](images/readlog.png)

<span data-ttu-id="fe37f-109">Para obter um exemplo de código, consulte [consultando informações de evento](querying-for-event-source-messages.md).</span><span class="sxs-lookup"><span data-stu-id="fe37f-109">For example code, see [Querying for Event Information](querying-for-event-source-messages.md).</span></span>

 

 



