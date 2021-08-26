---
description: As funções OpenEventLog, OpenBackupEventLog, RegisterEventSource, DeregisterEventSource e CloseEventLog abrem e fecham os alças do log de eventos.
ms.assetid: e42a66c2-2f1e-46f8-99c7-4701075c8ec3
title: Operações de registro em log de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221218bdfa4fc5e4fc6a905353cde33357c4088119031062c074c75d4b8136dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901399"
---
# <a name="event-logging-operations"></a>Operações de registro em log de eventos

As [**funções OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga), [**OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga), [**RegisterEventSource,**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) [**DeregisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)e [**CloseEventLog**](/windows/desktop/api/Winbase/nf-winbase-closeeventlog) abrem e fecham os alças do log de eventos.

A tabela a seguir mostra as operações que podem ser executadas em um log de eventos aberto e a função correspondente para cada operação.



| Operação | Função                                                                                                                     |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| Backup    | [**BackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                                                                                     |
| Limpar     | [**ClearEventLog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                                                                                       |
| Monitoramento   | [**NotifyChangeEventLog**](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)                                                                         |
| Consulta     | [**GetOldestEventLogRecord,**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord) [ **GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) |
| Ler      | [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                                                                                         |
| Gravar     | [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                                                                                           |



 

As [**funções OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) e [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) levam um nome de servidor opcional como um parâmetro para que as operações possam ser executadas no servidor remoto. Use [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) para ler ou executar operações administrativas (backup, limpar, monitorar e consultar) no log e use [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea) para escrever no log.

Cada chamada para uma função de registro em log de eventos é uma operação atômica. Quando você lê do log de eventos, somente registros de eventos inteiros são retornados. Quando você grava no log de eventos, cada registro de evento tem a garantia de ser gravado sequencialmente como um registro completo no log. A lista a seguir descreve como o serviço de registro em log de eventos lida com condições especiais:

-   O serviço de registro em log de eventos recebe uma operação de leitura e uma operação de gravação ao mesmo tempo: se a posição de leitura estiver no final do arquivo, a operação de leitura falhará com um status de "fim do arquivo" (se a operação de gravação não tiver sido concluída) ou retornará o novo registro (se a operação de gravação tiver sido concluída).
-   O serviço de registro em log de eventos conclui uma operação clara antes de receber uma operação de leitura: a operação de leitura falha com o status "fim do arquivo".
-   O serviço de registro em log de eventos conclui uma operação clara antes de receber uma operação de gravação: a operação clear trunca o log e, em seguida, a operação de gravação adiciona o novo registro no início do log.

 

 



