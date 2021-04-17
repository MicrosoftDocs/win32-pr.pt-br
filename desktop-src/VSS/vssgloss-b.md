---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d7d9c8bf-993f-469c-aea1-5d86ca856690
title: B (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20cabdfa5260f65d1176f6f1d12ac1d805b9dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296363"
---
# <a name="b-volume-shadow-copy-service"></a><span data-ttu-id="f0f34-103">B (Serviço de Cópias de Sombra de Volume)</span><span class="sxs-lookup"><span data-stu-id="f0f34-103">B (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="f0f34-104">[A](vssgloss-a.md) B [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="f0f34-104">[A](vssgloss-a.md) B [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="f0f34-105"><span id="base.vssgloss_back_end_level_applications"></span><span id="BASE.VSSGLOSS_BACK_END_LEVEL_APPLICATIONS"></span>**aplicativos de nível de back-end**</span><span class="sxs-lookup"><span data-stu-id="f0f34-105"><span id="base.vssgloss_back_end_level_applications"></span><span id="BASE.VSSGLOSS_BACK_END_LEVEL_APPLICATIONS"></span>**back-end level applications**</span></span>
</dt> <dd>

<span data-ttu-id="f0f34-106">Indica o ponto em que um gravador é notificado de um congelamento pelo VSS.</span><span class="sxs-lookup"><span data-stu-id="f0f34-106">Indicates the point at which a writer is notified of a freeze by VSS.</span></span> <span data-ttu-id="f0f34-107">Gravadores que são inicializados como aplicativos de nível back-end são notificados depois que os gravadores são inicializados como aplicativos de nível front-end e antes daqueles inicializados como aplicativos de nível de sistema.</span><span class="sxs-lookup"><span data-stu-id="f0f34-107">Writers that are initialized as back-end level applications are notified after writers initialized as front-end level applications and prior to those initialized as system-level applications.</span></span> <span data-ttu-id="f0f34-108">Consulte também [*nível de aplicativo*](vssgloss-a.md), [*aplicativos de nível front-end*](vssgloss-f.md), [*aplicativos de nível de sistema*](vssgloss-s.md), [*gravador*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="f0f34-108">See also [*application level*](vssgloss-a.md), [*front-end level applications*](vssgloss-f.md), [*system-level applications*](vssgloss-s.md), [*writer*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0f34-109"><span id="base.vssgloss_backupcomplete_event"></span><span id="BASE.VSSGLOSS_BACKUPCOMPLETE_EVENT"></span>**Evento BackupComplete**</span><span class="sxs-lookup"><span data-stu-id="f0f34-109"><span id="base.vssgloss_backupcomplete_event"></span><span id="BASE.VSSGLOSS_BACKUPCOMPLETE_EVENT"></span>**BackupComplete event**</span></span>
</dt> <dd>

<span data-ttu-id="f0f34-110">Um evento do VSS que indica que um backup do VSS foi concluído.</span><span class="sxs-lookup"><span data-stu-id="f0f34-110">A VSS event indicating that a VSS backup has completed.</span></span> <span data-ttu-id="f0f34-111">Esse evento deve ser seguido por um evento BackupShutdown em operação normal.</span><span class="sxs-lookup"><span data-stu-id="f0f34-111">This event should be followed by a BackupShutdown event under normal operation.</span></span> <span data-ttu-id="f0f34-112">Consulte também *evento BackupShutdown*.</span><span class="sxs-lookup"><span data-stu-id="f0f34-112">See also *BackupShutdown event*.</span></span>

</dd> <dt>

<span data-ttu-id="f0f34-113"><span id="base.vssgloss_backup_components_document"></span><span id="BASE.VSSGLOSS_BACKUP_COMPONENTS_DOCUMENT"></span>**Documento de componentes de backup**</span><span class="sxs-lookup"><span data-stu-id="f0f34-113"><span id="base.vssgloss_backup_components_document"></span><span id="BASE.VSSGLOSS_BACKUP_COMPONENTS_DOCUMENT"></span>**Backup Components Document**</span></span>
</dt> <dd>

<span data-ttu-id="f0f34-114">Um documento XML criado por um solicitante (usando a interface **IVssBackupComponents** ) no decorrer da configuração de uma operação de restauração ou backup.</span><span class="sxs-lookup"><span data-stu-id="f0f34-114">An XML document created by a requester (using the **IVssBackupComponents** interface) in the course of setting up a restore or backup operation.</span></span> <span data-ttu-id="f0f34-115">O Documento de Componentes de Backup contém uma lista dos componentes explicitamente incluídos, de um ou mais gravadores, que participam de uma operação de backup ou restauração.</span><span class="sxs-lookup"><span data-stu-id="f0f34-115">The Backup Components Document contains a list of those explicitly included components, from one or more writers, participating in a backup or restore operation.</span></span> <span data-ttu-id="f0f34-116">Ele não contém informações de componentes implicitamente incluídos.</span><span class="sxs-lookup"><span data-stu-id="f0f34-116">It does not contain implicitly included component information.</span></span> <span data-ttu-id="f0f34-117">Por outro lado, um Documento de Metadados do Gravador contém somente os componentes do gravador que podem participar de um backup.</span><span class="sxs-lookup"><span data-stu-id="f0f34-117">In contrast, a Writer Metadata Document contains only writer components that may participate in a backup.</span></span>

<span data-ttu-id="f0f34-118">Um documento de componentes de backup pode ser salvo em disco.</span><span class="sxs-lookup"><span data-stu-id="f0f34-118">A Backup Components Document can be saved to disk.</span></span> <span data-ttu-id="f0f34-119">Consulte também [*inclusão de componente explícita*](vssgloss-e.md), [*inclusão de componente implícita*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="f0f34-119">See also [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="f0f34-120"><span id="base.vssgloss_backup_set"></span><span id="BASE.VSSGLOSS_BACKUP_SET"></span>**conjunto de backup**</span><span class="sxs-lookup"><span data-stu-id="f0f34-120"><span id="base.vssgloss_backup_set"></span><span id="BASE.VSSGLOSS_BACKUP_SET"></span>**backup set**</span></span>
</dt> <dd>

<span data-ttu-id="f0f34-121">Os arquivos cujo backup será feito.</span><span class="sxs-lookup"><span data-stu-id="f0f34-121">Those files to be backed up.</span></span> <span data-ttu-id="f0f34-122">Ele inclui os arquivos selecionados pela inclusão em um componente, aqueles indicados por instruções include no nível do gravador, menos os arquivos que foram explicitamente incluídos.</span><span class="sxs-lookup"><span data-stu-id="f0f34-122">It includes files selected by inclusion in a component, those indicated by writer-level include statements, less those files that have been explicitly included.</span></span>

</dd> <dt>

<span data-ttu-id="f0f34-123"><span id="base.vssgloss_backupshutdown_event"></span><span id="BASE.VSSGLOSS_BACKUPSHUTDOWN_EVENT"></span>**Evento BackupShutdown**</span><span class="sxs-lookup"><span data-stu-id="f0f34-123"><span id="base.vssgloss_backupshutdown_event"></span><span id="BASE.VSSGLOSS_BACKUPSHUTDOWN_EVENT"></span>**BackupShutdown event**</span></span>
</dt> <dd>

<span data-ttu-id="f0f34-124">Um evento do VSS que indica que um aplicativo de backup em conformidade foi desligado.</span><span class="sxs-lookup"><span data-stu-id="f0f34-124">A VSS event indicating that a compliant backup application has shut down.</span></span> <span data-ttu-id="f0f34-125">Normalmente, isso é precedido por um evento BackupComplete.</span><span class="sxs-lookup"><span data-stu-id="f0f34-125">Normally, this is preceded by a BackupComplete event.</span></span> <span data-ttu-id="f0f34-126">No entanto, se um backup for encerrado inesperadamente, esse evento poderá ser gerado sem um evento BackupComplete anterior.</span><span class="sxs-lookup"><span data-stu-id="f0f34-126">However, if a backup terminates unexpectedly, this event can be generated without a preceding BackupComplete event.</span></span> <span data-ttu-id="f0f34-127">Consulte também *evento BackupComplete*.</span><span class="sxs-lookup"><span data-stu-id="f0f34-127">See also *BackupComplete event*.</span></span>

</dd> <dt>

<span data-ttu-id="f0f34-128"><span id="base.vssgloss_backup_stamp"></span><span id="BASE.VSSGLOSS_BACKUP_STAMP"></span>**carimbo de backup**</span><span class="sxs-lookup"><span data-stu-id="f0f34-128"><span id="base.vssgloss_backup_stamp"></span><span id="BASE.VSSGLOSS_BACKUP_STAMP"></span>**backup stamp**</span></span>
</dt> <dd>

<span data-ttu-id="f0f34-129">Uma cadeia de caracteres que contém informações sobre quando um backup ocorreu.</span><span class="sxs-lookup"><span data-stu-id="f0f34-129">A string containing information as to when a backup took place.</span></span> <span data-ttu-id="f0f34-130">O VSS não coloca nenhuma restrição no formato dessa cadeia de caracteres, exceto que ele é inteligível para todas as instâncias de gravador de uma determinada classe.</span><span class="sxs-lookup"><span data-stu-id="f0f34-130">VSS places no restriction on the format of this string, except that it be intelligible to all the writer instances of a given class.</span></span> <span data-ttu-id="f0f34-131">Ele pode conter informações de data e hora, números de sequência lógica ou qualquer outra informação que permitirá que um escritor da mesma classe determine quando o último backup ocorre.</span><span class="sxs-lookup"><span data-stu-id="f0f34-131">It may contain time and date information, logical sequence numbers, or any other information that will allow a writer of the same class to determine when the last backup has take place.</span></span>

</dd> </dl>

 

 



