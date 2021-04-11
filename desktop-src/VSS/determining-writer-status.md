---
description: Um solicitante precisa ter um entendimento bem definido sobre o status do gravador que participa dele durante a criação da cópia de sombra e durante as operações de backup e restauração.
ms.assetid: 676d5cff-bd28-43f0-a402-d184c96f0061
title: Determinando o status do gravador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719322a18808748e92d412c48c7b7628fdac9d51
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172603"
---
# <a name="determining-writer-status"></a><span data-ttu-id="59eaa-103">Determinando o status do gravador</span><span class="sxs-lookup"><span data-stu-id="59eaa-103">Determining Writer Status</span></span>

<span data-ttu-id="59eaa-104">Um solicitante precisa ter um entendimento bem definido sobre o status do gravador que participa dele durante a criação da cópia de sombra e durante as operações de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="59eaa-104">A requester needs to have a well-defined understanding about the status of the writer that participates with it during shadow copy creation, and during backup and restore operations.</span></span> <span data-ttu-id="59eaa-105">Para fazer isso, é recomendável:</span><span class="sxs-lookup"><span data-stu-id="59eaa-105">To do so, it is recommended:</span></span>

-   <span data-ttu-id="59eaa-106">Os solicitantes usam [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus), [**IVssBackupComponents:: GetWriterStatusCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatuscount)e [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus).</span><span class="sxs-lookup"><span data-stu-id="59eaa-106">Requesters use [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus), [**IVssBackupComponents::GetWriterStatusCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatuscount), and [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus).</span></span>
-   <span data-ttu-id="59eaa-107">Conforme descrito em [visão geral do processamento de um backup no VSS](overview-of-processing-a-backup-under-vss.md) e [visão geral do processamento de uma restauração no VSS](overview-of-processing-a-restore-under-vss.md), esses métodos são mais úteis quando chamados em uma sequência de backup ou restauração bem definida.</span><span class="sxs-lookup"><span data-stu-id="59eaa-107">As described in [Overview of Processing a Backup Under VSS](overview-of-processing-a-backup-under-vss.md) and [Overview of Processing a Restore Under VSS](overview-of-processing-a-restore-under-vss.md), these methods are most useful when called in a well-defined backup or restore sequence.</span></span> <span data-ttu-id="59eaa-108">Normalmente, isso significa que os gravadores devem ser consultados depois que um solicitante tiver concluído uma de suas tarefas e gerado um evento do VSS.</span><span class="sxs-lookup"><span data-stu-id="59eaa-108">Typically, this means that the writers should be queried after a requester has completed one of its tasks and generated a VSS event.</span></span>

    <span data-ttu-id="59eaa-109">Ao processar um backup, um solicitante deve consultar um gravador após a conclusão dos métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="59eaa-109">When processing a backup, a requester should query a writer following the completion of the following methods.</span></span> <span data-ttu-id="59eaa-110">Os solicitantes devem chamar [**GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) depois de chamar [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) para fazer com que a sessão de gravador seja definida como um estado concluído.</span><span class="sxs-lookup"><span data-stu-id="59eaa-110">Requesters must call [**GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) after calling [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) to cause the writer session to be set to a completed state.</span></span>

    > [!Note]  
    > <span data-ttu-id="59eaa-111">Isso só é necessário no Windows Server 2008 com Service Pack 2 (SP2) e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="59eaa-111">This is only necessary on Windows Server 2008 with Service Pack 2 (SP2) and earlier.</span></span>

     

    <dl> <dt>

[<span data-ttu-id="59eaa-112">**IVssBackupComponents::P repareForBackup**</span><span class="sxs-lookup"><span data-stu-id="59eaa-112">**IVssBackupComponents::PrepareForBackup**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)
</dt> <dt>

[<span data-ttu-id="59eaa-113">**IVssBackupComponents::D oSnapshotSet**</span><span class="sxs-lookup"><span data-stu-id="59eaa-113">**IVssBackupComponents::DoSnapshotSet**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)
</dt> <dt>

[<span data-ttu-id="59eaa-114">**IVssBackupComponents::BackupComplete**</span><span class="sxs-lookup"><span data-stu-id="59eaa-114">**IVssBackupComponents::BackupComplete**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)
</dt> </dl>

<span data-ttu-id="59eaa-115">Durante as operações de restauração, um solicitante deve consultar um gravador após a conclusão desses métodos:</span><span class="sxs-lookup"><span data-stu-id="59eaa-115">During restore operations, a requester should query a writer after completion of these methods:</span></span>
<dl> <dt>

[<span data-ttu-id="59eaa-116">**IVssBackupComponents: rerestaurar:P**</span><span class="sxs-lookup"><span data-stu-id="59eaa-116">**IVssBackupComponents::PreRestore**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)
</dt> <dt>

[<span data-ttu-id="59eaa-117">**IVssBackupComponents::P ostRestore**</span><span class="sxs-lookup"><span data-stu-id="59eaa-117">**IVssBackupComponents::PostRestore**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore)
</dt> </dl>

-   <span data-ttu-id="59eaa-118">Chamadas para [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) que não fazem parte de uma sequência de backup ou restauração bem definida não fornecem uma imagem confiável do status do gravador, pois elas podem refletir condições que não indicam falha na operação atual, como:</span><span class="sxs-lookup"><span data-stu-id="59eaa-118">Calls to [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) that are not part of a well-defined backup or restore sequence do not provide a reliable picture of writer status, because they might reflect conditions that do not indicate failure in the current operation, such as:</span></span>
    -   <span data-ttu-id="59eaa-119">Uma falha de uma criação de cópia de sombra anterior</span><span class="sxs-lookup"><span data-stu-id="59eaa-119">A failure of a previous shadow copy creation</span></span>
    -   <span data-ttu-id="59eaa-120">Um erro em uma operação de backup ou restauração inicial</span><span class="sxs-lookup"><span data-stu-id="59eaa-120">An error in an early backup or restore operation</span></span>
    -   <span data-ttu-id="59eaa-121">Um gravador sem resposta que está processando um evento</span><span class="sxs-lookup"><span data-stu-id="59eaa-121">An unresponsive writer currently processing an event</span></span>

<span data-ttu-id="59eaa-122">Portanto, os desenvolvedores não devem contar com o status do gravador retornado por outros processos em seguida, o solicitante ou a tentativa de monitorar o progresso de uma instância da interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) com outra (possivelmente em um thread separado).</span><span class="sxs-lookup"><span data-stu-id="59eaa-122">Therefore, developers should not rely on writer status returned by processes other then the requester or attempt to monitor the progress of one instance of the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface with another (possibly in a separate thread).</span></span>

<span data-ttu-id="59eaa-123">Observe que para operações de backup, em que é necessário examinar documentos de metadados do gravador de gravadores, não há necessidade de uma chamada de solicitante para [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) após a geração e manipulação do evento de [*identificação*](vssgloss-i.md) causado por [**IVssBackupComponents:: GatherWriterMetdata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).</span><span class="sxs-lookup"><span data-stu-id="59eaa-123">Note that for backup operations, where it is necessary to examine writers' Writer Metadata Documents, there is no need for a requester call to [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) and [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) following the generation and handling of the [*Identify*](vssgloss-i.md) event caused by [**IVssBackupComponents::GatherWriterMetdata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata).</span></span>

<span data-ttu-id="59eaa-124">[**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) relata apenas o status dos gravadores cujos metadados foram fornecidos ao VSS pelos gravadores ' [*identificar*](vssgloss-i.md) manipuladores de eventos, [**CVssWriter:: onidentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) (e retornados ao solicitante por [**IVssBackupComponents:: GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) e [**IVssBackupComponents:: GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)).</span><span class="sxs-lookup"><span data-stu-id="59eaa-124">[**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) reports only the status of those writers whose metadata was provided to VSS by writers' [*Identify*](vssgloss-i.md) event handlers, [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) (and returned to the requester by [**IVssBackupComponents::GetWriterMetadataCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadatacount) and [**IVssBackupComponents::GetWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritermetadata)).</span></span>

<span data-ttu-id="59eaa-125">Se a implementação de um gravador de [**CVssWriter:: Onidentification**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) falhar, os metadados do gravador não serão parte da lista de documentos de metadados do gravador fornecidos ao VSS, nenhuma informação de status estará disponível e a chamada será redundante.</span><span class="sxs-lookup"><span data-stu-id="59eaa-125">If a writer's implementation of [**CVssWriter::OnIdentify**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onidentify) fails, that writer's metadata will not be part of the list of Writer Metadata Documents provided to VSS, no status information will be available, and the call would be redundant.</span></span>

<span data-ttu-id="59eaa-126">Para operações de restauração, em que o solicitante não precisa examinar os documentos de metadados do gravador dos gravadores em execução, chamar [**IVssBackupComponents:: GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) e [**IVssBackupComponents:: GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) pode ser uma maneira mais eficiente de determinar quais gravadores estão em execução.</span><span class="sxs-lookup"><span data-stu-id="59eaa-126">For restore operations, where the requester does not need to examine Writer Metadata Documents of executing writers, calling [**IVssBackupComponents::GatherWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwriterstatus) and [**IVssBackupComponents::GetWriterStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwriterstatus) may be a more efficient way to determine which writers are executing.</span></span>

 

 



