---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7eb1d433-21db-45cc-a141-13a89993e30c
title: E (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97425100d8e2e3d0add6ea0e6fd1de67bc6f4ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783663"
---
# <a name="e-volume-shadow-copy-service"></a><span data-ttu-id="7a37c-103">E (Serviço de Cópias de Sombra de Volume)</span><span class="sxs-lookup"><span data-stu-id="7a37c-103">E (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="7a37c-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) E [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="7a37c-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) E [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="7a37c-105"><span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**inclusão de componente explícita**</span><span class="sxs-lookup"><span data-stu-id="7a37c-105"><span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**explicit component inclusion**</span></span>
</dt> <dd>

<span data-ttu-id="7a37c-106">Adicionar informações de um componente ao documento de componentes de backup de um solicitante quando ele participa de uma operação de backup ou restauração.</span><span class="sxs-lookup"><span data-stu-id="7a37c-106">Adding of a component's information to a requester's Backup Components Document when it participates in a backup or restore operation.</span></span> <span data-ttu-id="7a37c-107">Os solicitantes usam o [**componente IVssBackupComponents::**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) Addpara incluir explicitamente um componente em uma operação de backup e [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) ou [**IVssBackupComponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) para incluir explicitamente um componente em uma operação de restauração.</span><span class="sxs-lookup"><span data-stu-id="7a37c-107">Requesters use [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) to explicitly include a component in a backup operation, and [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) or [**IVssBackupComponents::AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) to explicitly include a component in a restore operation.</span></span>

<span data-ttu-id="7a37c-108">Se for feito backup ou restauração de qualquer componente de um gravador, todos os componentes não selecionáveis sem nenhum ancestral selecionável deverão ser incluídos explicitamente em uma operação de backup ou restauração.</span><span class="sxs-lookup"><span data-stu-id="7a37c-108">If any component of a writer is backed up or restored, all nonselectable components without any selectable ancestors must be explicitly included in a backup or restore operation.</span></span>

<span data-ttu-id="7a37c-109">Componentes selecionáveis sem ancestrais selecionáveis escolhidos por um solicitante para participação em um backup ou restauração devem ser incluídos explicitamente na operação.</span><span class="sxs-lookup"><span data-stu-id="7a37c-109">Selectable components without selectable ancestors chosen by a requester for participation in a backup or restore must be explicitly included in the operation.</span></span>

<span data-ttu-id="7a37c-110">Os componentes não selecionáveis com um ancestral selecionável nunca são incluídos explicitamente.</span><span class="sxs-lookup"><span data-stu-id="7a37c-110">Nonselectable components with a selectable ancestor are never explicitly included.</span></span>

<span data-ttu-id="7a37c-111">Os componentes selecionáveis com um ancestral selecionável podem ser incluídos explicitamente ou podem ser incluídos implicitamente se o ancestral for incluído explicitamente.</span><span class="sxs-lookup"><span data-stu-id="7a37c-111">Selectable components with a selectable ancestor may be included explicitly, or may be included implicitly if the ancestor is included explicitly.</span></span>

</dd> <dt>

<span data-ttu-id="7a37c-112"><span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**cópia de sombra exposta**</span><span class="sxs-lookup"><span data-stu-id="7a37c-112"><span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**exposed shadow copy**</span></span>
</dt> <dd>

<span data-ttu-id="7a37c-113">Uma cópia de sombra de volume que é montada em um sistema e está disponível para processos que não sejam aquele que o gerencia.</span><span class="sxs-lookup"><span data-stu-id="7a37c-113">A volume shadow copy that is mounted on a system and available to processes other than the one that manages it.</span></span> <span data-ttu-id="7a37c-114">Um volume de cópia de sombra montado sob uma letra da unidade ou um local do diretório é conhecido como "exposto localmente".</span><span class="sxs-lookup"><span data-stu-id="7a37c-114">A shadow copy volume mounted under a drive letter or a directory location is referred to as "locally exposed."</span></span> <span data-ttu-id="7a37c-115">Um volume de cópia de sombra acessível por meio de um compartilhamento (exceto para cópias de sombra acessíveis pelo cliente) é conhecido como "exposto remotamente".</span><span class="sxs-lookup"><span data-stu-id="7a37c-115">A shadow copy volume accessible through a share (except for client-accessible shadow copies) is referred to as "remotely exposed."</span></span> <span data-ttu-id="7a37c-116">Todas as cópias de sombra expostas também são cópias de sombra em superfície.</span><span class="sxs-lookup"><span data-stu-id="7a37c-116">All exposed shadow copies are also surfaced shadow copies.</span></span> <span data-ttu-id="7a37c-117">Consulte também [*cópia de sombra acessível ao cliente*](vssgloss-c.md), [*cópia de sombra*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="7a37c-117">See also [*client accessible shadow copy*](vssgloss-c.md), [*shadow copy*](vssgloss-s.md).</span></span>

</dd> </dl>

 

 



