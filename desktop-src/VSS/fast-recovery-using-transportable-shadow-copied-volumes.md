---
description: As cópias de sombra transportáveis podem ser usadas para facilitar uma recuperação rápida.
ms.assetid: 2eaffcf7-01b2-44ce-8bc4-fd9fa42c8a8c
title: Recuperação rápida usando volumes copiados de sombra transportável
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a588395de36b0e6773eacf7f46a45452a69c13c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770546"
---
# <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a><span data-ttu-id="f896f-103">Recuperação rápida usando volumes copiados de sombra transportável</span><span class="sxs-lookup"><span data-stu-id="f896f-103">Fast Recovery Using Transportable Shadow Copied Volumes</span></span>

<span data-ttu-id="f896f-104">As [*cópias de sombra transportáveis*](vssgloss-t.md) podem ser usadas para facilitar uma *recuperação rápida*.</span><span class="sxs-lookup"><span data-stu-id="f896f-104">[*Transportable shadow copies*](vssgloss-t.md) can be used to facilitate a *fast recovery*.</span></span>

<span data-ttu-id="f896f-105">A recuperação rápida pode ser usada para reverter rapidamente para uma cópia de sombra anterior.</span><span class="sxs-lookup"><span data-stu-id="f896f-105">Fast recovery can be used to quickly revert to an earlier shadow copy.</span></span> <span data-ttu-id="f896f-106">As etapas envolvidas são:</span><span class="sxs-lookup"><span data-stu-id="f896f-106">The steps involved are:</span></span>

1.  <span data-ttu-id="f896f-107">Crie a cópia de sombra transportável dos LUNs apropriados.</span><span class="sxs-lookup"><span data-stu-id="f896f-107">Create the transportable shadow copy of the appropriate LUNs.</span></span> <span data-ttu-id="f896f-108">A cópia de sombra pode ser [*persistente*](vssgloss-p.md) ou não persistente.</span><span class="sxs-lookup"><span data-stu-id="f896f-108">The shadow copy can be either [*persistent*](vssgloss-p.md) or nonpersistent.</span></span>
2.  <span data-ttu-id="f896f-109">Remover os LUNs originais</span><span class="sxs-lookup"><span data-stu-id="f896f-109">Remove the original LUNs</span></span>
    1.  <span data-ttu-id="f896f-110">Se o computador estiver dentro de um cluster, marque os recursos de disco afetados como offline ou habilite o [modo de manutenção](/previous-versions/windows/desktop/mscs/maintaining-physical-disk-resources) para esses recursos de disco.</span><span class="sxs-lookup"><span data-stu-id="f896f-110">If the computer is inside a cluster, mark the affected disk resources as offline, or enable the [maintenance mode](/previous-versions/windows/desktop/mscs/maintaining-physical-disk-resources) for these disk resources.</span></span>
    2.  <span data-ttu-id="f896f-111">Mascarar os LUNs afetados deste computador (e todos os outros nós se o computador estiver em um cluster).</span><span class="sxs-lookup"><span data-stu-id="f896f-111">Mask the affected LUNs from this computer (and all other nodes if the computer is in a cluster).</span></span>
3.  <span data-ttu-id="f896f-112">Importe a cópia de sombra usando o método [**IVssBackupComponents:: ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) .</span><span class="sxs-lookup"><span data-stu-id="f896f-112">Import the shadow copy using the [**IVssBackupComponents::ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) method.</span></span>
4.  <span data-ttu-id="f896f-113">Quebre a cópia de sombra usando o método [**IVssBackupComponents:: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) .</span><span class="sxs-lookup"><span data-stu-id="f896f-113">Break the shadow copy using the [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) method.</span></span>
5.  <span data-ttu-id="f896f-114">Marque os novos volumes de cópia de sombra como leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="f896f-114">Mark the new shadow copy volumes as read/write.</span></span>
6.  <span data-ttu-id="f896f-115">Se o computador estiver em um cluster, expor os novos LUNs de cópia de sombra como os LUNs originais.</span><span class="sxs-lookup"><span data-stu-id="f896f-115">If the computer is in a cluster, expose the new shadow copy LUNs as the original LUNs.</span></span>
    1.  <span data-ttu-id="f896f-116">Desmascarar os LUNs de cópia de sombra para os outros nós no cluster.</span><span class="sxs-lookup"><span data-stu-id="f896f-116">Unmask the shadow copy LUNs to the other nodes in the cluster.</span></span>
    2.  <span data-ttu-id="f896f-117">Marque os recursos que foram marcados anteriormente como offline ou desabilite o modo de manutenção para esses recursos de disco.</span><span class="sxs-lookup"><span data-stu-id="f896f-117">Mark the resources that were previously marked as offline as online, or disable the maintenance mode for those disk resources.</span></span>

> [!Note]  
> <span data-ttu-id="f896f-118">As cópias de sombra transportáveis em um cluster não têm suporte antes do Windows Server 2003 com Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="f896f-118">Transportable shadow copies in a cluster are not supported before Windows Server 2003 with Service Pack 1 (SP1).</span></span> <span data-ttu-id="f896f-119">Isso só é suportado com LUNs compatíveis, que têm pelo menos uma página VPD (dados vitais do produto) SCSI 0x83 \_ identificador de armazenamento do tipo 1, 2 ou 8 e Associação 0, e os LUNs devem manter um disco básico com particionamento MBR.</span><span class="sxs-lookup"><span data-stu-id="f896f-119">This is only supported with compliant LUNs, which have at least one SCSI Vital Product Data (VPD) page 0x83 STORAGE\_IDENTIFIER of type 1,2, or 8, and association 0, and the LUNs must maintain a basic disk with MBR partitioning.</span></span>

 

 

 
