---
description: 'A lista a seguir indica as adições e alterações na interface Serviço de Cópias de Sombra de Volume no Windows Server 2003 com Service Pack 1 (SP1):'
ms.assetid: 9e0dba98-5d23-444d-bd2f-cb72de8fb2d2
title: O que há de novo no VSS no Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 559b51d5b019d9d57aa154c4728ef5c8f4bb19d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461134"
---
# <a name="whats-new-in-vss-in-windows-server-2003-sp1"></a><span data-ttu-id="c2c6b-103">O que há de novo no VSS no Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="c2c6b-103">What's New in VSS in Windows Server 2003 SP1</span></span>

<span data-ttu-id="c2c6b-104">A lista a seguir indica as adições e alterações na interface Serviço de Cópias de Sombra de Volume no Windows Server 2003 com Service Pack 1 (SP1):</span><span class="sxs-lookup"><span data-stu-id="c2c6b-104">The following list indicates additions and changes to the Volume Shadow Copy Service interface in Windows Server 2003 with Service Pack 1 (SP1):</span></span>

## <a name="auto-recovery"></a><span data-ttu-id="c2c6b-105">Recuperação automática</span><span class="sxs-lookup"><span data-stu-id="c2c6b-105">Auto-recovery</span></span>

<span data-ttu-id="c2c6b-106">A [*recuperação automática*](vssgloss-a.md) permite aos gravadores um tempo para atualizar os componentes em uma cópia de sombra antes que a cópia de sombra seja alterada permanentemente para somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c2c6b-106">[*Auto-recovery*](vssgloss-a.md) allows writers a time to update components in a shadow copy before the shadow copy is permanently changed to read-only.</span></span> <span data-ttu-id="c2c6b-107">Por exemplo, um banco de dados pode precisar reverter todas as transações incompletas para todas as cópias de sombra (o gravador de banco de dados definiria o sinalizador de **\_ recuperação de \_ backup \_ do CF VSS** para os componentes do banco de dados).</span><span class="sxs-lookup"><span data-stu-id="c2c6b-107">For example, a database may need to rollback any incomplete transactions for all shadow copies (the database writer would set the **VSS\_CF\_BACKUP\_RECOVERY** flag for the database components).</span></span> <span data-ttu-id="c2c6b-108">A recuperação automática iniciada pelo solicitante permite uma restauração refinada (por exemplo, restaurar uma tabela em um banco de dados ou uma pasta em um servidor de email), ou a reversão para dar suporte a Data Mining para executar a análise que seria muito lenta para um servidor de produção (o solicitante adicionaria a **\_ \_ \_ \_ recuperação de reversão do atributo** de cópia de sombra do VSS.) A recuperação automática não é compatível com cópias de sombra transportáveis, mas há suporte para a mesma funcionalidade usando a [recuperação rápida usando volumes copiados de sombra transportável](fast-recovery-using-transportable-shadow-copied-volumes.md).</span><span class="sxs-lookup"><span data-stu-id="c2c6b-108">Auto-recovery initiated by the requester allows both fine-grained restore (for example restoring one table in a database or one folder on a mail server), or the rollback to support data mining to perform analysis that would be too slow for a production server (the requester would add **VSS\_VOLSNAP\_ATTR\_ROLLBACK\_RECOVERY** to the shadow copy context.) Auto-recovery is not compatible with transportable shadow copies, but the same functionality is supported by using [Fast Recovery Using Transportable Shadow Copied Volumes](fast-recovery-using-transportable-shadow-copied-volumes.md).</span></span>

<span data-ttu-id="c2c6b-109">Os seguintes elementos de programação têm alterações para dar suporte à recuperação automática:</span><span class="sxs-lookup"><span data-stu-id="c2c6b-109">The following programming elements have changes to support auto-recovery:</span></span>

<span data-ttu-id="c2c6b-110">Métodos de classe</span><span class="sxs-lookup"><span data-stu-id="c2c6b-110">Class methods</span></span>

-   [<span data-ttu-id="c2c6b-111">**CVssWriter::GetSnapshotDeviceName**</span><span class="sxs-lookup"><span data-stu-id="c2c6b-111">**CVssWriter::GetSnapshotDeviceName**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)
-   [<span data-ttu-id="c2c6b-112">**CVssWriter::OnPostSnapshot**</span><span class="sxs-lookup"><span data-stu-id="c2c6b-112">**CVssWriter::OnPostSnapshot**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)

<span data-ttu-id="c2c6b-113">Enumerações</span><span class="sxs-lookup"><span data-stu-id="c2c6b-113">Enumerations</span></span>

-   [<span data-ttu-id="c2c6b-114">**\_sinalizadores de componente do VSS \_**</span><span class="sxs-lookup"><span data-stu-id="c2c6b-114">**VSS\_COMPONENT\_FLAGS**</span></span>](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
-   [<span data-ttu-id="c2c6b-115">**\_\_atributos de \_ instantâneo de volume do VSS \_**</span><span class="sxs-lookup"><span data-stu-id="c2c6b-115">**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)

<span data-ttu-id="c2c6b-116">Métodos de interface</span><span class="sxs-lookup"><span data-stu-id="c2c6b-116">Interface methods</span></span>

-   [<span data-ttu-id="c2c6b-117">**IVssProviderCreateSnapshotSet::P reFinalCommitSnapshots**</span><span class="sxs-lookup"><span data-stu-id="c2c6b-117">**IVssProviderCreateSnapshotSet::PreFinalCommitSnapshots**</span></span>](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-prefinalcommitsnapshots)
-   [<span data-ttu-id="c2c6b-118">**IVssProviderCreateSnapshotSet::P ostFinalCommitSnapshots**</span><span class="sxs-lookup"><span data-stu-id="c2c6b-118">**IVssProviderCreateSnapshotSet::PostFinalCommitSnapshots**</span></span>](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postfinalcommitsnapshots)

## <a name="full-support-for-transportable-shadow-copies"></a><span data-ttu-id="c2c6b-119">Suporte completo para cópias de sombra transportáveis</span><span class="sxs-lookup"><span data-stu-id="c2c6b-119">Full Support for Transportable Shadow Copies</span></span>

<span data-ttu-id="c2c6b-120">As cópias de sombra transportáveis têm suporte em todas as edições do Windows Server 2003 com SP1.</span><span class="sxs-lookup"><span data-stu-id="c2c6b-120">Transportable shadow copies are supported in all editions of Windows Server 2003 with SP1.</span></span> <span data-ttu-id="c2c6b-121">Para obter mais informações, consulte [importando volumes copiados de sombra transportável](importing-transportable-shadow-copied-volumes.md).</span><span class="sxs-lookup"><span data-stu-id="c2c6b-121">For more information, see [Importing Transportable Shadow Copied Volumes](importing-transportable-shadow-copied-volumes.md).</span></span>

## <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a><span data-ttu-id="c2c6b-122">Recuperação rápida usando volumes copiados de sombra transportável</span><span class="sxs-lookup"><span data-stu-id="c2c6b-122">Fast Recovery Using Transportable Shadow Copied Volumes</span></span>

[<span data-ttu-id="c2c6b-123">Recuperação rápida usando volumes copiados de sombra transportável</span><span class="sxs-lookup"><span data-stu-id="c2c6b-123">Fast Recovery Using Transportable Shadow Copied Volumes</span></span>](fast-recovery-using-transportable-shadow-copied-volumes.md)

## <a name="shadow-copy-storage-area-management"></a><span data-ttu-id="c2c6b-124">Gerenciamento de área de armazenamento de cópias de sombra</span><span class="sxs-lookup"><span data-stu-id="c2c6b-124">Shadow copy storage area management</span></span>

[<span data-ttu-id="c2c6b-125">**IVssSnapshotMgmt2**</span><span class="sxs-lookup"><span data-stu-id="c2c6b-125">**IVssSnapshotMgmt2**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 



