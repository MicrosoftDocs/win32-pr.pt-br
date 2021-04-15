---
description: Os solicitantes controlam os recursos de uma cópia de sombra definindo seu contexto. Esse contexto indica se a cópia de sombra sobreviverá à operação atual e o grau de coordenação de gravador/provedor.
ms.assetid: adf79bc8-e893-444a-b750-d7ffd09de7c9
title: Configurações de contexto de cópia de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb41d0e2604dcf92d27f490175cdcbafd49822c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505742"
---
# <a name="shadow-copy-context-configurations"></a><span data-ttu-id="cd3e3-104">Configurações de contexto de cópia de sombra</span><span class="sxs-lookup"><span data-stu-id="cd3e3-104">Shadow Copy Context Configurations</span></span>

<span data-ttu-id="cd3e3-105">Os solicitantes controlam os recursos de uma cópia de sombra definindo seu contexto.</span><span class="sxs-lookup"><span data-stu-id="cd3e3-105">Requesters control a shadow copy's features by setting its context.</span></span> <span data-ttu-id="cd3e3-106">Esse contexto indica se a cópia de sombra sobreviverá à operação atual e o grau de coordenação de gravador/provedor.</span><span class="sxs-lookup"><span data-stu-id="cd3e3-106">This context indicates whether the shadow copy will survive the current operation, and the degree of writer/provider coordination.</span></span>

## <a name="persistence-and-shadow-copy-context"></a><span data-ttu-id="cd3e3-107">Contexto de persistência e cópia de sombra</span><span class="sxs-lookup"><span data-stu-id="cd3e3-107">Persistence and Shadow Copy Context</span></span>

<span data-ttu-id="cd3e3-108">Uma cópia de sombra pode ser [*persistente*](vssgloss-p.md), ou seja, a cópia de sombra não é excluída após o término de uma operação de backup ou o lançamento de um objeto [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) .</span><span class="sxs-lookup"><span data-stu-id="cd3e3-108">A shadow copy may be [*persistent*](vssgloss-p.md)—that is, the shadow copy is not deleted following the termination of a backup operation or the release of an [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) object.</span></span>

<span data-ttu-id="cd3e3-109">As cópias de sombra persistentes exigem contextos de [**\_ \_ \_ contexto de instantâneo**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) do VSS do **VSS \_ CTX \_ cliente \_ acessível**, **\_ \_ \_ reversão de aplicativo VSS CTX** ou **\_ \_ \_ reversão de nas CTX do VSS**.</span><span class="sxs-lookup"><span data-stu-id="cd3e3-109">Persistent shadow copies require [**\_VSS\_SNAPSHOT\_CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) contexts of **VSS\_CTX\_CLIENT\_ACCESSIBLE**, **VSS\_CTX\_APP\_ROLLBACK**, or **VSS\_CTX\_NAS\_ROLLBACK**.</span></span> <span data-ttu-id="cd3e3-110">Cópias de sombra persistentes só podem ser feitas para volumes NTFS.</span><span class="sxs-lookup"><span data-stu-id="cd3e3-110">Persistent shadow copies can be made only for NTFS volumes.</span></span>

<span data-ttu-id="cd3e3-111">Cópias de sombra não persistentes são criadas com contextos de backup do **VSS \_ CTX \_** ou backup de compartilhamento de **arquivos do VSS \_ CTX \_ \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="cd3e3-111">Nonpersistent shadow copies are created with contexts of **VSS\_CTX\_BACKUP** or **VSS\_CTX\_FILE\_SHARE\_BACKUP**.</span></span> <span data-ttu-id="cd3e3-112">Cópias de sombra não persistentes podem ser feitas para volumes NTFS e não NTFS.</span><span class="sxs-lookup"><span data-stu-id="cd3e3-112">Nonpersistent shadow copies can be made for NTFS and non-NTFS volumes.</span></span>

## <a name="writer-participation-and-shadow-copies"></a><span data-ttu-id="cd3e3-113">Participação no gravador e cópias de sombra</span><span class="sxs-lookup"><span data-stu-id="cd3e3-113">Writer Participation and Shadow Copies</span></span>

<span data-ttu-id="cd3e3-114">Um contexto de cópia de sombra pode ser classificado como envolvendo gravadores ou não envolvendo gravadores.</span><span class="sxs-lookup"><span data-stu-id="cd3e3-114">A shadow copy context can be classified as either involving writers or not involving writers.</span></span>

<span data-ttu-id="cd3e3-115">Os contextos de cópia de sombra que envolvem gravadores em sua criação incluem:</span><span class="sxs-lookup"><span data-stu-id="cd3e3-115">Shadow copy contexts that involve writers in their creation include:</span></span>

-   <span data-ttu-id="cd3e3-116">**reversão do \_ aplicativo VSS CTX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd3e3-116">**VSS\_CTX\_APP\_ROLLBACK**</span></span>
-   <span data-ttu-id="cd3e3-117">**BACKUP do VSS \_ CTX \_**</span><span class="sxs-lookup"><span data-stu-id="cd3e3-117">**VSS\_CTX\_BACKUP**</span></span>
-   <span data-ttu-id="cd3e3-118">**\_ \_ gravadores acessíveis ao cliente VSS CTX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd3e3-118">**VSS\_CTX\_CLIENT\_ACCESSIBLE\_WRITERS**</span></span>

<span data-ttu-id="cd3e3-119">Aqueles que não envolvem gravadores em sua criação incluem:</span><span class="sxs-lookup"><span data-stu-id="cd3e3-119">Those that do not involve writers in their creation include:</span></span>

-   <span data-ttu-id="cd3e3-120">**VSS \_ CTX \_ cliente \_ acessível**</span><span class="sxs-lookup"><span data-stu-id="cd3e3-120">**VSS\_CTX\_CLIENT\_ACCESSIBLE**</span></span>
-   <span data-ttu-id="cd3e3-121">**\_backup de \_ compartilhamento de arquivos CTX \_ VSS \_**</span><span class="sxs-lookup"><span data-stu-id="cd3e3-121">**VSS\_CTX\_FILE\_SHARE\_BACKUP**</span></span>
-   <span data-ttu-id="cd3e3-122">**reversão de nas do VSS \_ CTX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd3e3-122">**VSS\_CTX\_NAS\_ROLLBACK**</span></span>

<span data-ttu-id="cd3e3-123">Um contexto pode ser usado com ambos os tipos de cópias de sombra, mas não pode ser usado na criação de uma cópia de sombra:</span><span class="sxs-lookup"><span data-stu-id="cd3e3-123">One context can be used with both types of shadow copies, but cannot be used in creating a shadow copy:</span></span>

-   <span data-ttu-id="cd3e3-124">**\_CTX VSS \_ All**</span><span class="sxs-lookup"><span data-stu-id="cd3e3-124">**VSS\_CTX\_ALL**</span></span>

<span data-ttu-id="cd3e3-125">Não há suporte para a criação de uma cópia de sombra com um contexto de **\_ CTX VSS \_ All** (usando [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) e [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)).</span><span class="sxs-lookup"><span data-stu-id="cd3e3-125">Creating a shadow copy with a context of **VSS\_CTX\_ALL** (using [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) and [**IVssBackupComponents::DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)) is not supported.</span></span>

<span data-ttu-id="cd3e3-126">As operações que dão suporte a um contexto de **CTX do VSS são \_ \_ todas** as operações administrativas [**IVssBackupComponents:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query), [**IVssBackupComponents::D Eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots), [**IVssBackupComponents:: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset)e [**IVssBackupComponents:: ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot).</span><span class="sxs-lookup"><span data-stu-id="cd3e3-126">Operations that support a context of **VSS\_CTX\_ALL** are the administrative operations [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query), [**IVssBackupComponents::DeleteSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots), [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset), and [**IVssBackupComponents::ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot).</span></span>

## <a name="obtaining-shadow-copy-information"></a><span data-ttu-id="cd3e3-127">Obtendo informações de cópia de sombra</span><span class="sxs-lookup"><span data-stu-id="cd3e3-127">Obtaining Shadow Copy Information</span></span>

<span data-ttu-id="cd3e3-128">Se um solicitante souber o GUID de identificação de uma cópia de sombra (sua **\_ ID VSS**), ele poderá obter informações sobre o contexto de uma cópia de sombra específica (identificada por sua **\_ ID do VSS**) ao desempacotar a estrutura de [**\_ \_ prop snapshot do VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) retornada por uma chamada para [**IVssBackupComponents:: getinstantâneoproperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).</span><span class="sxs-lookup"><span data-stu-id="cd3e3-128">If a requester knows the identifying GUID of a shadow copy (its **VSS\_ID**), it can obtain information about the context of a specific shadow copy (identified by its **VSS\_ID**) by unpacking the [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure returned by a call to [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).</span></span>

<span data-ttu-id="cd3e3-129">Para obter informações de contexto sobre todas as cópias de sombra em um sistema, um solicitante examina o membro **m \_ lSnapshotAttributes** do membro **obj. snap** do [**\_ objeto VSS \_ prop**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (que é uma estrutura de [**\_ \_ prop instantâneo de VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) ) obtida usando [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) para iterar sobre a lista de objetos retornados por uma chamada para [**IVssBackupComponents:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span><span class="sxs-lookup"><span data-stu-id="cd3e3-129">To obtain context information about all shadow copies on a system, a requester examines the **m\_lSnapshotAttributes** member of the **Obj.Snap** member of the [**VSS\_OBJECT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (which is a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure) structure obtained by using [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) to iterate over the list of objects returned by a call to [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span></span>

 

 



