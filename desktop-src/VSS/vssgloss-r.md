---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2442a788-2e70-44c1-9c38-901c1c18a742
title: R (Serviço de Cópias de Sombra de Volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5846454ef5d58acf8f1c546b5e1bbce379d0b103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811379"
---
# <a name="r-volume-shadow-copy-service"></a><span data-ttu-id="d7df0-103">R (Serviço de Cópias de Sombra de Volume)</span><span class="sxs-lookup"><span data-stu-id="d7df0-103">R (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="d7df0-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q R [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="d7df0-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q R [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="d7df0-105"><span id="base.vssgloss_requester"></span><span id="BASE.VSSGLOSS_REQUESTER"></span>**solicitante**</span><span class="sxs-lookup"><span data-stu-id="d7df0-105"><span id="base.vssgloss_requester"></span><span id="BASE.VSSGLOSS_REQUESTER"></span>**requester**</span></span>
</dt> <dd>

<span data-ttu-id="d7df0-106">Minimamente, qualquer processo que interaja com o VSS para criar e gerenciar cópias de sombra e conjuntos de cópias de sombra de um ou mais volumes.</span><span class="sxs-lookup"><span data-stu-id="d7df0-106">Minimally, any process that interacts with VSS to create and manage shadow copies and shadow copy sets of one or more volumes.</span></span>

<span data-ttu-id="d7df0-107">Normalmente, um solicitante gerencia cópias de sombra para dar suporte a outras funcionalidades, como operações de backup e restauração e espelhamento de disco.</span><span class="sxs-lookup"><span data-stu-id="d7df0-107">Typically, a requester manages shadow copies to support some other functionality, such as backup and restore operations and disk mirroring.</span></span> <span data-ttu-id="d7df0-108">Consulte também [*cópia de sombra*](vssgloss-s.md), [*conjunto de cópias de sombra*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="d7df0-108">See also [*shadow copy*](vssgloss-s.md), [*shadow copy set*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="d7df0-109"><span id="base.vssgloss_restore_method"></span><span id="BASE.VSSGLOSS_RESTORE_METHOD"></span>**método de restauração**</span><span class="sxs-lookup"><span data-stu-id="d7df0-109"><span id="base.vssgloss_restore_method"></span><span id="BASE.VSSGLOSS_RESTORE_METHOD"></span>**restore method**</span></span>
</dt> <dd>

<span data-ttu-id="d7df0-110">Uma especificação do método de processo de restauração.</span><span class="sxs-lookup"><span data-stu-id="d7df0-110">A specification of the restore process method.</span></span> <span data-ttu-id="d7df0-111">Ele controla esses problemas como se os arquivos são substituídos na restauração.</span><span class="sxs-lookup"><span data-stu-id="d7df0-111">It controls such issues as whether files are overwritten on restore.</span></span> <span data-ttu-id="d7df0-112">Se uma configuração de método de restauração estiver em conflito com aquelas do destino de restauração, o destino de restauração terá precedência.</span><span class="sxs-lookup"><span data-stu-id="d7df0-112">If a restore method setting is in conflict with those of the restore target, then the restore target takes precedence.</span></span> <span data-ttu-id="d7df0-113">Consulte também *restaurar destino*.</span><span class="sxs-lookup"><span data-stu-id="d7df0-113">See also *restore target*.</span></span>

</dd> <dt>

<span data-ttu-id="d7df0-114"><span id="base.vssgloss_restore_target"></span><span id="BASE.VSSGLOSS_RESTORE_TARGET"></span>**restaurar destino**</span><span class="sxs-lookup"><span data-stu-id="d7df0-114"><span id="base.vssgloss_restore_target"></span><span id="BASE.VSSGLOSS_RESTORE_TARGET"></span>**restore target**</span></span>
</dt> <dd>

<span data-ttu-id="d7df0-115">No VSS, um destino de restauração é uma especificação de como um solicitante deve restaurar um arquivo, por exemplo, se ele deve substituir os arquivos existentes.</span><span class="sxs-lookup"><span data-stu-id="d7df0-115">Under VSS, a restore target is a specification of how a requester should restore a file, for example, if it should overwrite existing files.</span></span>

</dd> </dl>

 

 



