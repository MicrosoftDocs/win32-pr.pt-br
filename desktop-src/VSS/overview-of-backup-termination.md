---
description: A tabela a seguir mostra a sequência de ações e eventos necessários para que uma operação de backup seja encerrada. Para obter mais informações, consulte Visão geral do processamento de um backup no VSS.
ms.assetid: 12dcb2d1-614b-4c4c-a47c-342f79b20a62
title: Visão geral da terminação de backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52fd57822a62cf3fa39cee2b17d79ae2545afa07bd722d26cacda68cba3b6695
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937964"
---
# <a name="overview-of-backup-termination"></a>Visão geral da terminação de backup

A tabela a seguir mostra a sequência de ações e eventos necessários para que uma operação de backup seja encerrada. Para obter mais informações, consulte [Visão geral do processamento de um backup no VSS.](overview-of-processing-a-backup-under-vss.md)



| Ação do solicitante                                                                                                                                                                                                              | Evento                                                                 | Ação do autor                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| O solicitante encerra a cópia de sombra liberando a interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) ou chamando [**IVssBackupComponents::D eleteSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots). | Nenhum                                                                  | Nenhum                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) é lançado chamando [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).                                                                                                   | [*BackupShutdown*](vssgloss-b.md) | O autor trata o evento com [**CVssWriter::OnBackupShutdown,**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onbackupshutdown)que permite limpar qualquer estado relacionado ao conjunto de cópias de sombra. Se a operação de backup falhou, ou seja, ela não gerou um evento [**BackupComplete,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) o autor também pode ter que executar o tratamento de erro. Consulte [Manipulando eventos BackupShutdown](handling-backupshutdown-events.md) para obter mais informações. |



 

Como uma interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) não pode ser reutilizável e o destruidor da interface encerra as cópias de sombra, normalmente não há motivo para chamar [**IVssBackupComponents::D eleteSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots). Esse método foi projetado para ser usado em conjunto com o tratamento de erros e a anulação de backups (consulte [Anulando operações vss](aborting-vss-operations.md)).

 

 
