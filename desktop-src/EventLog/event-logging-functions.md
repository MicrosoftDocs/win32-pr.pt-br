---
description: As funções a seguir são usadas com o log de eventos.
ms.assetid: fd5c12ec-3a3d-4b75-a573-0b27ae7a890b
title: Funções de log de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6ba5e43286a65b9d3456edc9cd80e8812bd9a32975ec63158c0717b41c6894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069586"
---
# <a name="event-logging-functions"></a>Funções de log de eventos

As funções a seguir são usadas com o log de eventos.



| Função                                                         | Descrição                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**BackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                         | Salva o log de eventos especificado em um arquivo de backup.                                                     |
| [**ClearEventLog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                           | Limpa o log de eventos especificado e, opcionalmente, salva a cópia atual do log em um arquivo de backup.  |
| [**CloseEventLog**](/windows/desktop/api/Winbase/nf-winbase-closeeventlog)                           | Fecha um identificador de leitura para o log de eventos especificado.                                                    |
| [**DeregisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)           | Fecha um identificador de gravação no log de eventos especificado.                                                   |
| [**GetEventLogInformation**](/windows/desktop/api/Winbase/nf-winbase-geteventloginformation)         | Recupera informações sobre o log de eventos especificado.                                                |
| [**GetNumberOfEventLogRecords**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) | Recupera o número de registros no log de eventos especificado.                                         |
| [**GetOldestEventLogRecord**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord)       | Recupera o número de registro absoluto do registro mais antigo no log de eventos especificado.               |
| [**NotifyChangeEventLog**](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)             | Permite que um aplicativo receba notificação quando um evento é gravado no log de eventos especificado. |
| [**OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga)                 | Abre um identificador para um log de eventos de backup.                                                               |
| [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga)                             | Abre um identificador para o log de eventos especificado.                                                          |
| [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                             | Lê um número inteiro de entradas do log de eventos especificado.                                       |
| [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)               | Recupera um identificador registrado para o log de eventos especificado.                                           |
| [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                               | Grava uma entrada no final do log de eventos especificado.                                              |



 

 

 



