---
description: A tabela a seguir mostra a sequência de ações e eventos que são necessários para que uma operação de backup seja encerrada. Para obter mais informações, consulte Visão geral do processamento de um backup em VSS.
ms.assetid: 12dcb2d1-614b-4c4c-a47c-342f79b20a62
title: Visão geral do encerramento do backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9268bd8fd4ec51be2ee7a891d4dffb3a5cb1b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763764"
---
# <a name="overview-of-backup-termination"></a>Visão geral do encerramento do backup

A tabela a seguir mostra a sequência de ações e eventos que são necessários para que uma operação de backup seja encerrada. Para obter mais informações, consulte [visão geral do processamento de um backup em VSS](overview-of-processing-a-backup-under-vss.md).



| Ação do solicitante                                                                                                                                                                                                              | Evento                                                                 | Ação do gravador                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| O solicitante encerra a cópia de sombra, liberando a interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) ou chamando [**IVssBackupComponents::D eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots). | Nenhum                                                                  | Nenhum                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| O [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) é liberado chamando [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).                                                                                                   | [*BackupShutdown*](vssgloss-b.md) | O gravador manipula o evento com [**CVssWriter:: OnBackupShutdown**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown), que permite limpar qualquer estado relacionado ao conjunto de cópias de sombra. Se a operação de backup falhou, ou seja, não gerou um evento [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) , o gravador também pode ter que executar o tratamento de erros. Consulte [manipulando eventos BackupShutdown](handling-backupshutdown-events.md) para obter mais informações. |



 

Como uma interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) não pode ser reutilizada e o destruidor da interface encerra as cópias de sombra, normalmente não há motivo para chamar [**IVssBackupComponents::D eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots). Esse método foi projetado para ser usado em conjunto com o tratamento de erros e a anulação de backups (consulte [anulando operações do VSS](aborting-vss-operations.md)).

 

 
