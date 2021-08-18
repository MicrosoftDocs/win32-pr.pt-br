---
description: 'Eventos de anulação podem ser gerados durante uma operação de backup em qualquer um dos seguintes casos:'
ms.assetid: c2e39cdd-0ff8-4030-9bec-9e003b4d9520
title: Anulando operações vss
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120ef8fb16c23d77a24526aad0fd62e56c1888a76dc2de884140094c6591cd78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998266"
---
# <a name="aborting-vss-operations"></a>Anulando operações vss

[*Eventos*](vssgloss-a.md) de anulação podem ser gerados durante uma operação de backup em qualquer um dos seguintes casos:

-   Um solicitante gera explicitamente um evento [*Abort*](vssgloss-a.md) chamando [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).
-   Os manipuladores de eventos [*Freeze*](vssgloss-f.md) and [*Thaw*](vssgloss-t.md) de um autor ([**CVssWriter::OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) e [**CVssWriter::OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)) retornam **false** ou não podem ser concluídos na janela de tempo especificada em [**CVssWriter::Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize).
-   Há qualquer falha do provedor ou vss durante a criação de uma cópia de sombra após o [*evento PrepareForSnapshot.*](vssgloss-p.md)

Não há suporte para anulações para operações de restauração.

## <a name="requester-handling-and-creation-of-abort-events"></a>Tratamento e criação de eventos de anulação do solicitante

Uma instância da interface [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) pode ser usada para apenas um backup, portanto, se ocorrer um erro no processamento de um backup, geralmente é melhor liberar a instância atual e começar de novo.

Um solicitante deve sinalizar explicitamente que está anulando uma operação de backup (usando [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)) somente após a preparação real para um backup, envolvendo os autores ou a criação de uma cópia de sombra.

Na verdade, isso significa que sempre que um solicitante precisar interromper uma operação de backup depois de gerar um evento [*PrepareForBackup*](vssgloss-p.md) chamando [**IVssBackupComponents::P repareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup), ele deverá chamar [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) e aguardar seu retorno antes de liberar a instância [**atual do IVSSBackupComponents.**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents)

Por exemplo, se um autor vetou uma operação de backup, um solicitante deve usar [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) para notificar todos os outros autores de que a operação de backup não será concluída.

Antes de chamar [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)ou se a chamada para **PrepareForBackup** falhar, um solicitante pode liberar a instância atual da interface [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) sem a necessidade de gerar um evento Abort.

Por exemplo, se a instância atual de [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) estiver sendo usada simplesmente para obter informações chamando [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) e gerando um evento [*Identify,*](vssgloss-i.md) depois que as informações retornarem, a instância de **IVSSBackupComponents** poderá simplesmente ser liberada.

Um solicitante gera vários eventos ([*PrepareForSnapshot,*](vssgloss-p.md) [*Freeze,*](vssgloss-f.md) [*Thaw*](vssgloss-t.md)e [*PostSnapshot*](vssgloss-p.md)) quando chama [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Ao manipular os eventos de Congelamento e Descongelamento, um autor pode falhar e gerar um evento Abort por conta própria. A falha ao manipular eventos PrepareForSnapshot e PostSnapshot não gera um evento Abort.

Nem sempre é possível que um solicitante saiba se um evento Abort foi gerado quando [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) indica falha. Portanto, um solicitante que precisa encerrar uma operação de backup porque o status de **IVssBackupComponents::D oSnapshotSet** indica que um problema ainda deve chamar [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).

Se um solicitante tiver chamado [**IVssBackupComponents::AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup), não será necessário chamar [**IVssBackupComponents::BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) antes de liberar uma instância [**de IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents).

## <a name="writer-handling-and-creation-of-abort-events"></a>Manipulação de autor e criação de eventos de anulação

Conforme mencionado anteriormente, um autor pode receber um evento Abort de um solicitante ou o provedor pode disparar um em si. Além disso, é possível que um autor receba vários eventos abort em determinadas circunstâncias. Os desenvolvedores de autor devem codificar [**qualquer implementação de CVssWriter::OnAbort**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onabort) com isso em mente.

Ao manipular um evento Abort, um autor deve tentar restaurar qualquer processo gerenciado para seu estado de execução normal, bem como executar qualquer tratamento de erro e registro em log.

Isso pode significar que uma implementação de [**CVssWriter::OnAbort**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onabort) pode ter que executar muitas, se não todas, das mesmas tarefas que o manipulador de eventos Thaw ([**CVssWriter::OnThaw**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)) e o manipulador de eventos PostSnapshot ([**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)), e esses manipuladores podem ser chamados de dentro **de CVssWriter::OnAbort**.

 

 



