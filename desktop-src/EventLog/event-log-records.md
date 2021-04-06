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
# <a name="event-log-records"></a>Registros de log de eventos

As informações sobre cada evento são armazenadas no log de eventos em um *registro de log de eventos*. O registro de log de eventos inclui informações de hora, tipo e categoria. Para obter mais informações, consulte a estrutura [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) .

O membro **RecordNumber** de [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) contém o número de registro do registro de log de eventos. O primeiro registro gravado em um log de eventos é o número de registro 1 e outros registros são numerados em sequência. Se o número do registro atingir o ULONG \_ Max, o próximo número de registro será 0, não 1; no entanto, você usará zero para buscar o registro.

Se o valor do registro de [retenção](eventlog-key.md) for definido como zero, os registros de eventos serão substituídos quando o tamanho máximo do log for atingido. Portanto, o registro mais antigo em um log de eventos pode não ser o número de registro 1. Para identificar o registro mais antigo no log, chame a função [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord) . Em seguida, você pode chamar a função [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) e adicionar o valor retornado ao número de registro mais antigo para determinar o registro mais recente.

Você pode ler registros individuais do log de eventos usando a função [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) . Para obter mais informações, consulte [consultando informações de evento](querying-for-event-source-messages.md).

 

 



