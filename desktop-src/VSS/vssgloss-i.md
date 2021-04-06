---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ebf8d0a7-e465-4f9f-9e3d-b97dbcf321b8
title: I (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b043c340de5d1703587b83f72851db76d367832a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647159"
---
# <a name="i-volume-shadow-copy-service"></a><span data-ttu-id="5dd0e-103">I (Serviço de Cópias de Sombra de Volume)</span><span class="sxs-lookup"><span data-stu-id="5dd0e-103">I (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="5dd0e-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) i J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="5dd0e-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) I J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="5dd0e-105"><span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**Identificar evento**</span><span class="sxs-lookup"><span data-stu-id="5dd0e-105"><span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**Identify event**</span></span>
</dt> <dd>

<span data-ttu-id="5dd0e-106">Um evento do VSS que indica que um gravador ou um solicitante precisa consultar o gravador atual.</span><span class="sxs-lookup"><span data-stu-id="5dd0e-106">A VSS event indicating that a writer or a requester needs to query the current writer.</span></span> <span data-ttu-id="5dd0e-107">Ele é usado para construir as informações de metadados do gravador atual.</span><span class="sxs-lookup"><span data-stu-id="5dd0e-107">It is used to construct the current writer's metadata information.</span></span> <span data-ttu-id="5dd0e-108">Consulte também [*solicitante*](vssgloss-r.md), [*gravador*](vssgloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="5dd0e-108">See also [*requester*](vssgloss-r.md), [*writer*](vssgloss-w.md).</span></span>

</dd> <dt>

<span data-ttu-id="5dd0e-109"><span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**inclusão de componente implícita**</span><span class="sxs-lookup"><span data-stu-id="5dd0e-109"><span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**implicit component inclusion**</span></span>
</dt> <dd>

<span data-ttu-id="5dd0e-110">Não adicionar informações de um componente ao documento de componentes de backup de um solicitante quando ele participa de uma operação de backup ou restauração.</span><span class="sxs-lookup"><span data-stu-id="5dd0e-110">Not adding a component's information to a requester's Backup Components Document when it participates in a backup or restore operation.</span></span>

<span data-ttu-id="5dd0e-111">Os componentes não selecionáveis com um ancestral selecionável só serão incluídos implicitamente se seu ancestral estiver incluído.</span><span class="sxs-lookup"><span data-stu-id="5dd0e-111">Nonselectable components with a selectable ancestor are only implicitly included if their ancestor is included.</span></span>

<span data-ttu-id="5dd0e-112">Os componentes selecionáveis com um ancestral selecionável podem ser incluídos implicitamente, se o ancestral estiver incluído ou pode ser incluído explicitamente.</span><span class="sxs-lookup"><span data-stu-id="5dd0e-112">Selectable components with a selectable ancestor may be included implicitly, if the ancestor is included, or may be included explicitly.</span></span>

<span data-ttu-id="5dd0e-113">Os componentes não selecionáveis sem nenhum antepassado selecionável nunca são incluídos implicitamente em uma operação de backup ou restauração — todos esses componentes devem ser explicitamente adicionados ao documento de componentes de backup se qualquer um dos componentes do escritor participarem.</span><span class="sxs-lookup"><span data-stu-id="5dd0e-113">Nonselectable components without any selectable ancestors are never implicitly included in a backup or restore operation—all such components must be explicitly added to the Backup Components Document if any of the writer's components participate.</span></span>

<span data-ttu-id="5dd0e-114">Componentes selecionáveis sem ancestrais selecionáveis escolhidos por um solicitante para participação em um backup ou restauração não podem ser incluídos implicitamente na operação, mas devem ser adicionados explicitamente ao documento de componentes de backup.</span><span class="sxs-lookup"><span data-stu-id="5dd0e-114">Selectable components without selectable ancestors chosen by a requester for participation in a backup or restore cannot be implicitly included in the operation, but must be explicitly added to the Backup Components Document.</span></span>

</dd> <dt>

<span data-ttu-id="5dd0e-115"><span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**operações de backup incremental**</span><span class="sxs-lookup"><span data-stu-id="5dd0e-115"><span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**incremental backup operations**</span></span>
</dt> <dd>

<span data-ttu-id="5dd0e-116">Uma operação de backup ou restauração é executada somente em arquivos criados ou alterados desde que o último backup completo, incremental ou diferencial foi salvo.</span><span class="sxs-lookup"><span data-stu-id="5dd0e-116">A backup or restore operation is performed only on files created or changed since the last full, incremental, or differential backup was saved.</span></span> <span data-ttu-id="5dd0e-117">Consulte também [*operações de backup diferencial*](vssgloss-d.md).</span><span class="sxs-lookup"><span data-stu-id="5dd0e-117">See also [*differential backup operations*](vssgloss-d.md).</span></span>

</dd> </dl>

 

 



