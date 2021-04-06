---
description: As informações sobre cada evento são armazenadas no log de eventos em um registro de log de eventos. O registro de log de eventos inclui informações de hora, tipo e categoria. Para obter mais informações, consulte a estrutura EVENTLOGRECORD.
ms.assetid: 73731505-97f5-4985-8d00-c6ce8604902d
title: Registros de log de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cc6caf1011c06eda0dca240bb7a3478c549827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827954"
---
# <a name="event-log-records"></a><span data-ttu-id="4dc5b-105">Registros de log de eventos</span><span class="sxs-lookup"><span data-stu-id="4dc5b-105">Event Log Records</span></span>

<span data-ttu-id="4dc5b-106">As informações sobre cada evento são armazenadas no log de eventos em um *registro de log de eventos*.</span><span class="sxs-lookup"><span data-stu-id="4dc5b-106">Information about each event is stored in the event log in an *event log record*.</span></span> <span data-ttu-id="4dc5b-107">O registro de log de eventos inclui informações de hora, tipo e categoria.</span><span class="sxs-lookup"><span data-stu-id="4dc5b-107">The event log record includes time, type, and category information.</span></span> <span data-ttu-id="4dc5b-108">Para obter mais informações, consulte a estrutura [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) .</span><span class="sxs-lookup"><span data-stu-id="4dc5b-108">For more information, see the [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structure.</span></span>

<span data-ttu-id="4dc5b-109">O membro **RecordNumber** de [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) contém o número de registro do registro de log de eventos.</span><span class="sxs-lookup"><span data-stu-id="4dc5b-109">The **RecordNumber** member of [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) contains the record number for the event log record.</span></span> <span data-ttu-id="4dc5b-110">O primeiro registro gravado em um log de eventos é o número de registro 1 e outros registros são numerados em sequência.</span><span class="sxs-lookup"><span data-stu-id="4dc5b-110">The very first record written to an event log is record number 1, and other records are numbered sequentially.</span></span> <span data-ttu-id="4dc5b-111">Se o número do registro atingir o ULONG \_ Max, o próximo número de registro será 0, não 1; no entanto, você usará zero para buscar o registro.</span><span class="sxs-lookup"><span data-stu-id="4dc5b-111">If the record number reaches ULONG\_MAX, the next record number will be 0, not 1; however, you use zero to seek to the record.</span></span>

<span data-ttu-id="4dc5b-112">Se o valor do registro de [retenção](eventlog-key.md) for definido como zero, os registros de eventos serão substituídos quando o tamanho máximo do log for atingido.</span><span class="sxs-lookup"><span data-stu-id="4dc5b-112">If the [Retention](eventlog-key.md) registry value is set to zero, the event records are overwritten when the maximum log size is reached.</span></span> <span data-ttu-id="4dc5b-113">Portanto, o registro mais antigo em um log de eventos pode não ser o número de registro 1.</span><span class="sxs-lookup"><span data-stu-id="4dc5b-113">Therefore, the oldest record in an event log may not be record number 1.</span></span> <span data-ttu-id="4dc5b-114">Para identificar o registro mais antigo no log, chame a função [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord) .</span><span class="sxs-lookup"><span data-stu-id="4dc5b-114">To identify the oldest record in the log, call the [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord) function.</span></span> <span data-ttu-id="4dc5b-115">Em seguida, você pode chamar a função [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) e adicionar o valor retornado ao número de registro mais antigo para determinar o registro mais recente.</span><span class="sxs-lookup"><span data-stu-id="4dc5b-115">You can then call the [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) function and add the returned value to the oldest record number to determine the newest record.</span></span>

<span data-ttu-id="4dc5b-116">Você pode ler registros individuais do log de eventos usando a função [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) .</span><span class="sxs-lookup"><span data-stu-id="4dc5b-116">You can read individual records from the event log using the [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) function.</span></span> <span data-ttu-id="4dc5b-117">Para obter mais informações, consulte [consultando informações de evento](querying-for-event-source-messages.md).</span><span class="sxs-lookup"><span data-stu-id="4dc5b-117">For more information, see [Querying for Event Information](querying-for-event-source-messages.md).</span></span>

 

 



