---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44279c0e-17f4-4109-bc12-af9064cd321e
title: P (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f018a19c1d00ff3c6530e7c45fbca2350df8fec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501731"
---
# <a name="p-volume-shadow-copy-service"></a><span data-ttu-id="17e6c-103">P (Serviço de Cópias de Sombra de Volume)</span><span class="sxs-lookup"><span data-stu-id="17e6c-103">P (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="17e6c-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) P Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="17e6c-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) P Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="17e6c-105"><span id="base.vssgloss_partial_file_support"></span><span id="BASE.VSSGLOSS_PARTIAL_FILE_SUPPORT"></span>**suporte a arquivos parciais**</span><span class="sxs-lookup"><span data-stu-id="17e6c-105"><span id="base.vssgloss_partial_file_support"></span><span id="BASE.VSSGLOSS_PARTIAL_FILE_SUPPORT"></span>**partial file support**</span></span>
</dt> <dd>

<span data-ttu-id="17e6c-106">A capacidade de implementar operações de backup modificando subseções dos arquivos envolvidos, em vez de trabalhar com os arquivos inteiros.</span><span class="sxs-lookup"><span data-stu-id="17e6c-106">The capacity to implement backup operations by modifying subsections of the files involved, rather than working with the entire files.</span></span> <span data-ttu-id="17e6c-107">Consulte também [*direcionamento direcionado*](vssgloss-d.md).</span><span class="sxs-lookup"><span data-stu-id="17e6c-107">See also [*directed targeting*](vssgloss-d.md).</span></span>

</dd> <dt>

<span data-ttu-id="17e6c-108"><span id="base.vssgloss_persistent_shadow_copy"></span><span id="BASE.VSSGLOSS_PERSISTENT_SHADOW_COPY"></span>**cópia de sombra persistente**</span><span class="sxs-lookup"><span data-stu-id="17e6c-108"><span id="base.vssgloss_persistent_shadow_copy"></span><span id="BASE.VSSGLOSS_PERSISTENT_SHADOW_COPY"></span>**persistent shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="17e6c-109">Uma cópia de sombra que não é excluída automaticamente quando o solicitante libera um objeto [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) ou quando o computador é reiniciado.</span><span class="sxs-lookup"><span data-stu-id="17e6c-109">A shadow copy that is not deleted automatically when the requester releases an [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) object or when the computer is restarted.</span></span> <span data-ttu-id="17e6c-110">Consulte também [*cópia de sombra de lançamento automático*](vssgloss-a.md), [*cópia de sombra*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="17e6c-110">See also [*auto-release shadow copy*](vssgloss-a.md), [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="17e6c-111"><span id="base.vssgloss_plex"></span><span id="BASE.VSSGLOSS_PLEX"></span>**Plexos**</span><span class="sxs-lookup"><span data-stu-id="17e6c-111"><span id="base.vssgloss_plex"></span><span id="BASE.VSSGLOSS_PLEX"></span>**Plex**</span></span>
</dt> <dd>

<span data-ttu-id="17e6c-112">Um tipo especial de volume de cópia de sombra que representa totalmente e completamente um volume de cópia de sombra sem a necessidade de qualquer volume original.</span><span class="sxs-lookup"><span data-stu-id="17e6c-112">A special type of shadow copy volume that fully and completely represents a shadow copy volume without the need for either original volume.</span></span> <span data-ttu-id="17e6c-113">Isso também é conhecido como espelho dividido, mas esta documentação usa o termo Plex.</span><span class="sxs-lookup"><span data-stu-id="17e6c-113">This is also commonly known as a split-mirror, but this documentation uses the term Plex.</span></span>

</dd> <dt>

<span data-ttu-id="17e6c-114"><span id="base.vssgloss_postrestore_event"></span><span id="BASE.VSSGLOSS_POSTRESTORE_EVENT"></span>**Evento de restauração**</span><span class="sxs-lookup"><span data-stu-id="17e6c-114"><span id="base.vssgloss_postrestore_event"></span><span id="BASE.VSSGLOSS_POSTRESTORE_EVENT"></span>**PostRestore event**</span></span>
</dt> <dd>

<span data-ttu-id="17e6c-115">Um evento do VSS que indica que uma restauração do VSS foi concluída.</span><span class="sxs-lookup"><span data-stu-id="17e6c-115">A VSS event indicating that a VSS restore has completed.</span></span>

</dd> <dt>

<span data-ttu-id="17e6c-116"><span id="base.vssgloss_postsnapshot_event"></span><span id="BASE.VSSGLOSS_POSTSNAPSHOT_EVENT"></span>**Evento de pós-instantâneo**</span><span class="sxs-lookup"><span data-stu-id="17e6c-116"><span id="base.vssgloss_postsnapshot_event"></span><span id="BASE.VSSGLOSS_POSTSNAPSHOT_EVENT"></span>**PostSnapshot event**</span></span>
</dt> <dd>

<span data-ttu-id="17e6c-117">Um evento do VSS que indica que uma cópia de sombra foi concluída.</span><span class="sxs-lookup"><span data-stu-id="17e6c-117">A VSS event indicating that a shadow copy has been completed.</span></span> <span data-ttu-id="17e6c-118">Consulte também [*cópia de sombra*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="17e6c-118">See also [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="17e6c-119"><span id="base.vssgloss_preparebackup_event"></span><span id="BASE.VSSGLOSS_PREPAREBACKUP_EVENT"></span>**Evento PrepareForBackup**</span><span class="sxs-lookup"><span data-stu-id="17e6c-119"><span id="base.vssgloss_preparebackup_event"></span><span id="BASE.VSSGLOSS_PREPAREBACKUP_EVENT"></span>**PrepareForBackup event**</span></span>
</dt> <dd>

<span data-ttu-id="17e6c-120">Um evento do VSS que indica que uma operação de backup está prestes a ocorrer.</span><span class="sxs-lookup"><span data-stu-id="17e6c-120">A VSS event indicating that a backup operation is about to take place.</span></span>

</dd> <dt>

<span data-ttu-id="17e6c-121"><span id="base.vssgloss_preparesnapshot_event"></span><span id="BASE.VSSGLOSS_PREPARESNAPSHOT_EVENT"></span>**Evento PrepareForSnapshot**</span><span class="sxs-lookup"><span data-stu-id="17e6c-121"><span id="base.vssgloss_preparesnapshot_event"></span><span id="BASE.VSSGLOSS_PREPARESNAPSHOT_EVENT"></span>**PrepareForSnapshot event**</span></span>
</dt> <dd>

<span data-ttu-id="17e6c-122">Um evento do VSS que indica que os gravadores devem tomar medidas para se preparar para uma operação de cópia de sombra futura.</span><span class="sxs-lookup"><span data-stu-id="17e6c-122">A VSS event indicating that writers should take steps to prepare for an upcoming shadow copy operation.</span></span> <span data-ttu-id="17e6c-123">Consulte também [*cópia de sombra*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="17e6c-123">See also [*shadow copy*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="17e6c-124"><span id="base.vssgloss_prerestore_event"></span><span id="BASE.VSSGLOSS_PRERESTORE_EVENT"></span>**Evento de prerestore**</span><span class="sxs-lookup"><span data-stu-id="17e6c-124"><span id="base.vssgloss_prerestore_event"></span><span id="BASE.VSSGLOSS_PRERESTORE_EVENT"></span>**PreRestore event**</span></span>
</dt> <dd>

<span data-ttu-id="17e6c-125">Um evento do VSS que indica que uma operação de restauração está prestes a ocorrer.</span><span class="sxs-lookup"><span data-stu-id="17e6c-125">A VSS event indicating that a restore operation is about to take place.</span></span>

</dd> <dt>

<span data-ttu-id="17e6c-126"><span id="base.vssgloss_provider"></span><span id="BASE.VSSGLOSS_PROVIDER"></span>**operador**</span><span class="sxs-lookup"><span data-stu-id="17e6c-126"><span id="base.vssgloss_provider"></span><span id="BASE.VSSGLOSS_PROVIDER"></span>**provider**</span></span>
</dt> <dd>

<span data-ttu-id="17e6c-127">Um objeto do sistema operacional que intercepta e gerencia solicitações de e/s para criar e representar cópias de sombra de volume para o sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="17e6c-127">An operating system object that intercepts and manages I/O requests to create and represent volume shadow copies to the file system.</span></span> <span data-ttu-id="17e6c-128">Consulte também [*provedor de hardware*](vssgloss-h.md), [*provedor de software*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="17e6c-128">See also [*hardware provider*](vssgloss-h.md), [*software provider*](vssgloss-s.md).</span></span>

</dd> </dl>

 

 



