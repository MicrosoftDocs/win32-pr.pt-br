---
description: As funções a seguir são usadas com o log de eventos.
ms.assetid: fd5c12ec-3a3d-4b75-a573-0b27ae7a890b
title: Funções de log de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437899684861c5fc7ddbfe98c2499dc07bd9da8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787119"
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



 

 

 



