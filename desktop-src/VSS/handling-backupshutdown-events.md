---
description: É possível que um aplicativo de backup (solicitante) seja encerrado e não gere um evento BackupComplete.
ms.assetid: 8e6a1f4f-ba62-46ea-965e-b0c6526ece89
title: Manipulando eventos BackupShutdown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e60a063a11f0a492407daed31ace4a62aec2a13fe824e110de272d58b84bea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998246"
---
# <a name="handling-backupshutdown-events"></a>Manipulando eventos BackupShutdown

É possível que um aplicativo de backup (solicitante) seja encerrado e não gere um evento [*BackupComplete*](vssgloss-b.md) . O aplicativo de backup pode falhar ou ser encerrado (do Gerenciador de tarefas, por exemplo) e não ser capaz de chamar [**IVssBackupComponents:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete).

Portanto, a infraestrutura do VSS (em vez do solicitante) gera um evento [*BackupShutdown*](vssgloss-b.md) sempre que uma instância de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) que participa de um backup é liberada, independentemente de ser liberada pelo solicitante ou pelo sistema.

Se um backup continuar corretamente, um gravador receberá um evento BackupComplete seguido de um evento BackupShutdown.

Se a operação for anulada (o solicitante gera um [*evento de anulação*](vssgloss-a.md) chamando [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)) ou falhar abruptamente, um gravador poderá receber apenas um evento BackupShutdown e não poderá receber outros eventos que executam operações de limpeza. Cabe a um escritor determinar se um evento BackupShutdown segue uma sequência adequada de eventos ou representa uma falha inesperada das operações de backup.

O manipulador de eventos BackupShutdown, [**CVssWriter:: OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown), recebe a \_ ID do VSS (GUID) do conjunto de cópias de sombra da operação de backup que está sendo desligada. O gravador pode usar isso para determinar qual operação de backup está sendo desligada, se tiver armazenado a ID do conjunto de cópias de sombra durante sua sequência de backup (por exemplo, de dentro de [**CVssWriter:: OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze), [**CVssWriter:: descongelar**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)ou [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)) usando [**CVssWriter:: GetCurrentSnapshotSetId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcurrentsnapshotsetid).

No entanto, um gravador não deve chamar [**CVssWriter:: GetCurrentSnapshotSetId**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getcurrentsnapshotsetid) de dentro de [**CVssWriter:: OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown). Além disso, **CVssWriter:: GetCurrentSnapshotSetId** não pode ser chamado depois de [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot) retornar.

É possível que o gravador esteja envolvido em várias operações de backup e, se um evento BackupShutdown for chamado devido a um desligamento abrupta de um solicitante, a \_ ID do VSS retornada poderá ser a de outra operação de backup na qual o gravador estava participando.

 

 



