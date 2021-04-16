---
description: 'Eventos de anulação podem ser gerados durante uma operação de backup em qualquer um dos seguintes casos:'
ms.assetid: c2e39cdd-0ff8-4030-9bec-9e003b4d9520
title: Anulando operações do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e4b82ba4227dfeb02e3da91c9bc1e77f10f492
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750571"
---
# <a name="aborting-vss-operations"></a>Anulando operações do VSS

Eventos de [*anulação*](vssgloss-a.md) podem ser gerados durante uma operação de backup em qualquer um dos seguintes casos:

-   Um solicitante gera explicitamente um [*evento Abort*](vssgloss-a.md) chamando [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).
-   Os manipuladores de eventos [*congelar*](vssgloss-f.md) e [*descongelar*](vssgloss-t.md) do gravador ([**CVssWriter:: OnFreeze**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onfreeze) e [**CVssWriter:: descongelar**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)) retornam **false** ou não podem ser concluídos na janela de tempo especificada em [**CVssWriter:: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize).
-   Há qualquer falha do provedor ou VSS durante a criação de uma cópia de sombra após o evento [*PrepareForSnapshot*](vssgloss-p.md) .

Não há suporte para anulações em operações de restauração.

## <a name="requester-handling-and-creation-of-abort-events"></a>Tratamento de solicitante e criação de eventos de anulação

Uma instância da interface [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) pode ser usada para apenas um backup, portanto, se ocorrer um erro ao processar um backup, geralmente é melhor liberar a instância atual e começar novamente.

Um solicitante deve sinalizar explicitamente que está anulando uma operação de backup (usando [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup)) somente após a preparação real para um backup, envolvendo gravadores ou a criação de uma cópia de sombra.

Efetivamente, isso significa que sempre que um solicitante precisar interromper uma operação de backup depois de gerar um evento [*PrepareForBackup*](vssgloss-p.md) chamando [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup), ele deverá chamar [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) e esperar seu retorno antes de liberar a instância de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) atual.

Por exemplo, se um gravador vetasse uma operação de backup, um solicitante deve usar [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup) para notificar todos os outros gravadores que a operação de backup não será concluída.

Antes de chamar [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup), ou se a chamada para **PrepareForBackup** falhar, um solicitante poderá liberar a instância atual da interface [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) sem a necessidade de gerar um evento Abort.

Por exemplo, se a instância atual do [**IVSSBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) estiver sendo usada apenas para obter informações chamando [**IVSSBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) e gerando um evento de [*identificação*](vssgloss-i.md) , depois que as informações tiverem sido retornadas, a instância do **IVSSBackupComponents** poderá simplesmente ser liberada.

Um solicitante gera um número de eventos ([*PrepareForSnapshot*](vssgloss-p.md), [*Freeze*](vssgloss-f.md), [*descongelar*](vssgloss-t.md)e [*pós-instantâneo*](vssgloss-p.md)) quando chama [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset). Ao manipular os eventos Freeze e descongelar, um escritor pode falhar e gerar um evento de anulação por conta própria. Falha ao manipular eventos PrepareForSnapshot e pós-instantâneo não gera um evento Abort.

Nem sempre é possível para um solicitante saber se um evento Abort foi gerado quando [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) indica falha. Portanto, um solicitante precisa encerrar uma operação de backup porque o status de **IVssBackupComponents::D osnapshotset** indica que um problema ainda deve chamar [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup).

Se um solicitante tiver chamado [**IVssBackupComponents:: AbortBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-abortbackup), não será necessário chamar [**IVssBackupComponents:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) antes de liberar uma instância de [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents).

## <a name="writer-handling-and-creation-of-abort-events"></a>Manipulação de gravador e criação de eventos de anulação

Conforme observado anteriormente, um gravador pode receber um evento de anulação de um solicitante ou o provedor pode disparar um próprio. Além disso, é possível que um gravador receba vários eventos de anulação em determinadas circunstâncias. Os desenvolvedores de gravador devem codificar qualquer implementação de [**CVssWriter:: OnAbort**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onabort) com isso em mente.

Ao manipular um evento de anulação, um gravador deve tentar restaurar qualquer processo que fosse gerenciado para seu estado normal de execução, bem como executar qualquer manipulação de erros e registro em log.

Isso pode significar que uma implementação de [**CVssWriter:: OnAbort**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onabort) pode ter que executar muitas, se não todas, das mesmas tarefas que o manipulador de eventos descongelar ([**CVssWriter:: descongelar**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw)) e o manipulador de eventos de pós-instantâneo ([**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)) e esses manipuladores podem ser chamados de dentro de **CVssWriter:: OnAbort**.

 

 



