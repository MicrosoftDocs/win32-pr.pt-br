---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c4f826bc-ea80-4fd5-99da-630e7ae56dd7
title: S (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5979d30f0b88762a2d022a89063ee44bd91a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781076"
---
# <a name="s-volume-shadow-copy-service"></a><span data-ttu-id="f4688-103">S (Serviço de Cópias de Sombra de Volume)</span><span class="sxs-lookup"><span data-stu-id="f4688-103">S (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="f4688-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) S [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="f4688-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) S [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="f4688-105"><span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**seleção de backup**</span><span class="sxs-lookup"><span data-stu-id="f4688-105"><span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**selectability for backup**</span></span>
</dt> <dd>

<span data-ttu-id="f4688-106">Um componente é considerado selecionável para backup se sua inclusão explícita em uma operação de backup for opcional.</span><span class="sxs-lookup"><span data-stu-id="f4688-106">A component is said to be selectable for backup if its explicit inclusion in a backup operation is optional.</span></span> <span data-ttu-id="f4688-107">A seleção de backup será habilitada se o valor do membro **bSelectable** da estrutura [**\_ COMPONENTINFO do VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) for **true**.</span><span class="sxs-lookup"><span data-stu-id="f4688-107">Selectability for backup is enabled if the value of the **bSelectable** member of the [**VSS\_COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) structure is **true**.</span></span> <span data-ttu-id="f4688-108">Não há valor padrão para a seleção de um componente para backup; um gravador sempre deve definir esse valor explicitamente.</span><span class="sxs-lookup"><span data-stu-id="f4688-108">There is no default value for a component's selectability for backup; a writer must always set this value explicitly.</span></span>

<span data-ttu-id="f4688-109">Os gravadores também usam a seleção para restauração para organizar a participação do componente nas operações de restauração.</span><span class="sxs-lookup"><span data-stu-id="f4688-109">Writers also use selectability for restore to organize their component's participation in restore operations.</span></span>

<span data-ttu-id="f4688-110">Consulte também *componente selecionável*, *seleção para restauração*, [*inclusão explícita de componentes*](vssgloss-e.md), [*inclusão de componente implícita*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="f4688-110">See also *selectable component*, *selectability for restore*, [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4688-111"><span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**seleção de restauração**</span><span class="sxs-lookup"><span data-stu-id="f4688-111"><span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**selectability for restore**</span></span>
</dt> <dd>

<span data-ttu-id="f4688-112">Um componente é considerado selecionável para restauração se puder ser feito o backup implicitamente como parte de um conjunto de componentes e, posteriormente, restaurado individualmente sem o restante do conjunto de componentes.</span><span class="sxs-lookup"><span data-stu-id="f4688-112">A component is said to be selectable for restore if it can be implicitly backed up as part of a component set, and then later individually restored without the rest of the component set.</span></span> <span data-ttu-id="f4688-113">A seleção de restauração será habilitada se o valor do membro **bSelectableForRestore** da estrutura [**\_ COMPONENTINFO do VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) for **true**.</span><span class="sxs-lookup"><span data-stu-id="f4688-113">Selectability for restore is enabled if the value of the **bSelectableForRestore** member of the [**VSS\_COMPONENTINFO**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) structure is **true**.</span></span> <span data-ttu-id="f4688-114">Por padrão, a seleção de um componente para restauração é **falsa**.</span><span class="sxs-lookup"><span data-stu-id="f4688-114">By default, a component's selectability for restore is **false**.</span></span> <span data-ttu-id="f4688-115">A seleção de restauração tem significado apenas quando um componente não foi adicionado ao documento de backup.</span><span class="sxs-lookup"><span data-stu-id="f4688-115">Selectability for restore has meaning only when a component has not been added to the backup document.</span></span>

<span data-ttu-id="f4688-116">Consulte também *componente selecionável*, *seleção para backup*, [*inclusão de componente explícita*](vssgloss-e.md), [*inclusão de componente implícita*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="f4688-116">See also *selectable component*, *selectability for backup*, [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4688-117"><span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**componente selecionável**</span><span class="sxs-lookup"><span data-stu-id="f4688-117"><span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**selectable component**</span></span>
</dt> <dd>

<span data-ttu-id="f4688-118">Um componente é considerado selecionável se sua inclusão explícita em uma operação de backup ou restauração for opcional.</span><span class="sxs-lookup"><span data-stu-id="f4688-118">A component is said to be selectable if its explicit inclusion in a backup or restore operation is optional.</span></span>

<span data-ttu-id="f4688-119">A seleção de backup e a seleção de restauração são independentes umas das outras — um componente pode ser selecionável para ambas as operações, para restauração e não para backup, ou para backup e não restauração.</span><span class="sxs-lookup"><span data-stu-id="f4688-119">Selectability for backup and selectability for restore are independent of each other—a component may be selectable for both operations, for restore and not backup, or for backup and not restore.</span></span>

<span data-ttu-id="f4688-120">Os gravadores também usam a seleção para organizar seus componentes em grupos:</span><span class="sxs-lookup"><span data-stu-id="f4688-120">Writers also use selectability to organize their components into groups:</span></span>

-   <span data-ttu-id="f4688-121">Componentes não selecionáveis sem ancestrais selecionáveis em seus caminhos lógicos devem sempre ser incluídos explicitamente se for necessário fazer backup ou restauração de um gravador.</span><span class="sxs-lookup"><span data-stu-id="f4688-121">Nonselectable components with no selectable ancestors in their logical paths must always be explicitly included if a writer is to be backed up or restored.</span></span>
-   <span data-ttu-id="f4688-122">Os componentes não selecionáveis com ancestrais selecionáveis só serão incluídos em um backup ou restauração se pelo menos um ancestral selecionável estiver incluído.</span><span class="sxs-lookup"><span data-stu-id="f4688-122">Nonselectable components with selectable ancestors will only be included in a backup or restore if at least one selectable ancestor is included.</span></span>
-   <span data-ttu-id="f4688-123">Componentes selecionáveis sem ancestrais selecionáveis só podem ser incluídos em uma operação de backup ou restauração explicitamente.</span><span class="sxs-lookup"><span data-stu-id="f4688-123">Selectable components without selectable ancestors can only be included in a backup or restore operation explicitly.</span></span>
-   <span data-ttu-id="f4688-124">Componentes selecionáveis com ancestrais selecionáveis podem ser incluídos explicitamente em uma operação de backup ou restauração, ou podem ser incluídos implicitamente se um de seus ancestrais selecionáveis estiver incluído.</span><span class="sxs-lookup"><span data-stu-id="f4688-124">Selectable components with selectable ancestors can be explicitly included in a backup or restore operation, or can be implicitly included if one of their selectable ancestors is included.</span></span>

<span data-ttu-id="f4688-125">Consulte também [*componentes*](vssgloss-c.md), *a seleção de backup*, a *seleção de restauração, a* [*inclusão explícita de componentes*](vssgloss-e.md), a inclusão de [*componentes implícitos*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="f4688-125">See also [*components*](vssgloss-c.md), *selectability for backup*, *selectability for restore*, [*explicit component inclusion*](vssgloss-e.md), [*implicit component inclusion*](vssgloss-i.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4688-126"><span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**cópia de sombra**</span><span class="sxs-lookup"><span data-stu-id="f4688-126"><span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="f4688-127">Uma réplica de ponto no tempo somente leitura do conteúdo de um volume original.</span><span class="sxs-lookup"><span data-stu-id="f4688-127">A read-only point-in-time replica of an original volume's contents.</span></span> <span data-ttu-id="f4688-128">Cada cópia de sombra é codificada por um GUID persistente.</span><span class="sxs-lookup"><span data-stu-id="f4688-128">Each shadow copy is keyed by a persistent GUID.</span></span> <span data-ttu-id="f4688-129">Também chamada de cópia de sombra de volume.</span><span class="sxs-lookup"><span data-stu-id="f4688-129">Also called a volume shadow copy.</span></span> <span data-ttu-id="f4688-130">Consulte também *conjunto de cópias de sombra*.</span><span class="sxs-lookup"><span data-stu-id="f4688-130">See also *shadow copy set*.</span></span>

</dd> <dt>

<span data-ttu-id="f4688-131"><span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**Cópias de Sombra para Pastas Compartilhadas**</span><span class="sxs-lookup"><span data-stu-id="f4688-131"><span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**Shadow Copies for Shared Folders**</span></span>
</dt> <dd>

<span data-ttu-id="f4688-132">Um recurso do Windows que cria cópias de backup simples e online de volumes usando o VSS.</span><span class="sxs-lookup"><span data-stu-id="f4688-132">A feature of Windows that creates lightweight, online backup copies of volumes using VSS.</span></span> <span data-ttu-id="f4688-133">Os clientes podem acessar esses backups por meio do shell do Windows para ver versões antigas de arquivos e desfazer erros sem a necessidade de uma restauração completa.</span><span class="sxs-lookup"><span data-stu-id="f4688-133">Clients can access these backups through the Windows shell to see old versions of files and undo mistakes without requiring a full restore.</span></span> <span data-ttu-id="f4688-134">Consulte também [*cópia de sombra acessível ao cliente*](vssgloss-c.md).</span><span class="sxs-lookup"><span data-stu-id="f4688-134">See also [*client accessible shadow copy*](vssgloss-c.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4688-135"><span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**conjunto de cópias de sombra**</span><span class="sxs-lookup"><span data-stu-id="f4688-135"><span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**shadow copy set**</span></span>
</dt> <dd>

<span data-ttu-id="f4688-136">Uma coleção de cópias de sombra de volume criadas ao mesmo tempo e identificada por um valor de ID de conjunto de cópias de sombra (um GUID persistente) comum.</span><span class="sxs-lookup"><span data-stu-id="f4688-136">A collection of volume shadow copies created at the same time and identified by a common shadow copy set ID (a persistent GUID) value.</span></span> <span data-ttu-id="f4688-137">Esse é o mecanismo usado para permitir que uma operação de cópia de sombra seja gerenciada entre volumes.</span><span class="sxs-lookup"><span data-stu-id="f4688-137">This is the mechanism used to allow a shadow copy operation to be managed across volumes.</span></span> <span data-ttu-id="f4688-138">Consulte também *cópia de sombra*.</span><span class="sxs-lookup"><span data-stu-id="f4688-138">See also *shadow copy*.</span></span>

</dd> <dt>

<span data-ttu-id="f4688-139"><span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**provedor de software**</span><span class="sxs-lookup"><span data-stu-id="f4688-139"><span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**software provider**</span></span>
</dt> <dd>

<span data-ttu-id="f4688-140">Um provedor que intercepta solicitações de e/s no nível de software entre o sistema de arquivos e o Gerenciador de volumes.</span><span class="sxs-lookup"><span data-stu-id="f4688-140">A provider that intercepts I/O requests at the software level between the file system and the volume manager.</span></span> <span data-ttu-id="f4688-141">Consulte também [*provedor de hardware*](vssgloss-h.md), [*provedor*](vssgloss-p.md).</span><span class="sxs-lookup"><span data-stu-id="f4688-141">See also [*hardware provider*](vssgloss-h.md), [*provider*](vssgloss-p.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4688-142"><span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**subcomponente**</span><span class="sxs-lookup"><span data-stu-id="f4688-142"><span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**subcomponent**</span></span>
</dt> <dd>

<span data-ttu-id="f4688-143">Qualquer componente que tenha um caminho lógico contendo um componente do pai selecionável (para backup ou restauração).</span><span class="sxs-lookup"><span data-stu-id="f4688-143">Any component that has a logical path containing a selectable (for either backup or restore) parent component.</span></span> <span data-ttu-id="f4688-144">Os subcomponentes devem ter um caminho lógico no formato {nome do componente \_ } \\ {nome do subcomponente \_ }.</span><span class="sxs-lookup"><span data-stu-id="f4688-144">Subcomponents must have a logical path of the form {component\_name}\\{subcomponent\_name}.</span></span> <span data-ttu-id="f4688-145">Se o ancestral de um subcomponente selecionável (para backup ou restauração) for explicitamente incluído em um backup ou restauração, o subcomponente será incluído implicitamente na operação.</span><span class="sxs-lookup"><span data-stu-id="f4688-145">If a subcomponent's selectable (for either backup or restore) ancestor is explicitly included in a backup or restore, then the subcomponent is implicitly included in the operation.</span></span> <span data-ttu-id="f4688-146">Os subcomponentes incluídos implicitamente não têm seus dados incluídos no documento de componentes de backup, independentemente de serem selecionáveis (para restauração ou backup) ou não.</span><span class="sxs-lookup"><span data-stu-id="f4688-146">Implicitly included subcomponents do not have their data included in the Backup Components Document—regardless of whether they are selectable (for either restore or backup) or not.</span></span> <span data-ttu-id="f4688-147">Consulte também [*componente*](vssgloss-c.md), [*caminho lógico*](vssgloss-l.md).</span><span class="sxs-lookup"><span data-stu-id="f4688-147">See also [*component*](vssgloss-c.md), [*logical path*](vssgloss-l.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4688-148"><span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**cópia de sombra na superfície**</span><span class="sxs-lookup"><span data-stu-id="f4688-148"><span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**surfaced shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="f4688-149">Um volume copiado de sombra visível para o namespace do Gerenciador de montagem do sistema — significando que **FindFirstVolume** e **FindNextVolume** podem encontrá-lo e que as notificações de chegada e saída do volume são geradas.</span><span class="sxs-lookup"><span data-stu-id="f4688-149">A shadow copied volume visible to a system's Mount Manager namespace—meaning **FindFirstVolume** and **FindNextVolume** can find it and that volume arrival and departure notifications are generated.</span></span> <span data-ttu-id="f4688-150">Todas as cópias de sombra expostas também são cópias de sombra em superfície.</span><span class="sxs-lookup"><span data-stu-id="f4688-150">All exposed shadow copies are also surfaced shadow copies.</span></span> <span data-ttu-id="f4688-151">No entanto, uma cópia de sombra em superfície não precisa ser exposta.</span><span class="sxs-lookup"><span data-stu-id="f4688-151">However, a surfaced shadow copy need not be exposed.</span></span> <span data-ttu-id="f4688-152">Se uma cópia de sombra for transportável, ela não poderá ser exposta.</span><span class="sxs-lookup"><span data-stu-id="f4688-152">If a shadow copy is transportable, it cannot be surfaced.</span></span> <span data-ttu-id="f4688-153">Consulte também [*cópia de sombra exposta*](vssgloss-e.md), [*cópia de sombra transportável*](vssgloss-t.md).</span><span class="sxs-lookup"><span data-stu-id="f4688-153">See also [*exposed shadow copy*](vssgloss-e.md), [*transportable shadow copy*](vssgloss-t.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4688-154"><span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**Proteção de arquivo do sistema**</span><span class="sxs-lookup"><span data-stu-id="f4688-154"><span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**System File Protection**</span></span>
</dt> <dd>

<span data-ttu-id="f4688-155">Consulte [*proteção de arquivos do Windows*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="f4688-155">See [*Windows File Protection*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4688-156"><span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**aplicativos de nível de sistema**</span><span class="sxs-lookup"><span data-stu-id="f4688-156"><span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**system-level applications**</span></span>
</dt> <dd>

<span data-ttu-id="f4688-157">Indica o ponto no qual o VSS notifica um escritor de um congelamento.</span><span class="sxs-lookup"><span data-stu-id="f4688-157">Indicates the point at which VSS notifies a writer of a freeze.</span></span> <span data-ttu-id="f4688-158">Gravadores que são inicializados como aplicativos de nível de sistema são notificados depois que os gravadores são inicializados como aplicativos de nível front-end ou como aplicativos de nível back-end.</span><span class="sxs-lookup"><span data-stu-id="f4688-158">Writers that are initialized as system-level applications are notified after writers initialized either as front-end level applications or as back-end level applications.</span></span> <span data-ttu-id="f4688-159">Consulte também [*nível de aplicativo*](vssgloss-a.md), [*aplicativos de nível de back-end*](vssgloss-b.md), [*aplicativos de nível front-end*](vssgloss-f.md).</span><span class="sxs-lookup"><span data-stu-id="f4688-159">See also [*application level*](vssgloss-a.md), [*back-end level applications*](vssgloss-b.md), [*front-end level applications*](vssgloss-f.md).</span></span>

</dd> <dt>

<span data-ttu-id="f4688-160"><span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**provedor do sistema**</span><span class="sxs-lookup"><span data-stu-id="f4688-160"><span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**system provider**</span></span>
</dt> <dd>

<span data-ttu-id="f4688-161">O provedor pré-instalado padrão fornecido como parte do Windows.</span><span class="sxs-lookup"><span data-stu-id="f4688-161">The default preinstalled provider provided as part of Windows.</span></span>

</dd> <dt>

<span data-ttu-id="f4688-162"><span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**Pasta volume do sistema**</span><span class="sxs-lookup"><span data-stu-id="f4688-162"><span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**System Volume Folder**</span></span>
</dt> <dd>

<span data-ttu-id="f4688-163">Um diretório compartilhado que armazena as cópias compartilhadas dos arquivos públicos de um domínio, ou seja, os arquivos que são replicados entre todos os controladores de domínio no domínio.</span><span class="sxs-lookup"><span data-stu-id="f4688-163">A shared directory that stores the shared copies of a domain's public files—that is, those files that are replicated among all domain controllers in the domain.</span></span>

</dd> </dl>

 

 



