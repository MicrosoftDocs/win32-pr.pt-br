---
description: A participação de um gravador em uma operação de backup ou restauração, e quais dos seus dados são salvos, depende de quais dos seus componentes são incluídos explicitamente como parte do documento de componentes de backup de um solicitante e da relação entre esses componentes e o caminho lógico de outros componentes dentro do documento de metadados do gravador.
ms.assetid: e8920cca-d944-437f-bf6a-7ce8d518746a
title: Trabalhando com caminhos lógicos e de seleção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42bc29d629df86562bc9b764b1d83bb8bb511d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781483"
---
# <a name="working-with-selectability-and-logical-paths"></a><span data-ttu-id="fadc4-103">Trabalhando com caminhos lógicos e de seleção</span><span class="sxs-lookup"><span data-stu-id="fadc4-103">Working with Selectability and Logical Paths</span></span>

<span data-ttu-id="fadc4-104">A participação de um gravador em uma operação de backup ou restauração, e quais dos seus dados são salvos, depende de quais dos seus componentes são [*incluídos explicitamente*](vssgloss-e.md) como parte do documento de componentes de backup de um solicitante e da relação entre esses componentes e o caminho lógico de outros componentes dentro do documento de metadados do gravador.</span><span class="sxs-lookup"><span data-stu-id="fadc4-104">A writer's participation in a backup or restore operation, and which of its data are saved, depends on which of its components are [*explicitly included*](vssgloss-e.md) as part of a requester's Backup Components Document and the relationship between those components and the logical path of other components within the Writer Metadata Document.</span></span>

<span data-ttu-id="fadc4-105">Gravadores sem componentes adicionados ao documento de componente de backup de um solicitante antes da geração de um evento [*PrepareForBackup*](vssgloss-p.md) (no caso de operações de backup) ou de um evento de [**prerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) (no caso de operações de restauração) não recebem eventos após esse ponto e não participarão da operação de backup ou restauração.</span><span class="sxs-lookup"><span data-stu-id="fadc4-105">Writers with no components added to a requester's Backup Component Document prior to the generation of a [*PrepareForBackup*](vssgloss-p.md) event (in the case of backup operations) or of a [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) event (in the case of restore operations) receive no events after this point and will not participate in the backup or restore operation.</span></span>

<span data-ttu-id="fadc4-106">No entanto, a liberdade de um solicitante de incluir ou excluir um determinado componente em um backup ou restauração é governada pelo seguinte:</span><span class="sxs-lookup"><span data-stu-id="fadc4-106">However, a requester's freedom to include or exclude any given component in a backup or restore is governed by the following:</span></span>

-   <span data-ttu-id="fadc4-107">Qualquer hierarquia que exista entre os componentes gerenciados por um gravador e expressa por [ *caminhos lógicos*](vssgloss-l.md)</span><span class="sxs-lookup"><span data-stu-id="fadc4-107">Any hierarchy that exists between the components managed by a writer and expressed by [*logical paths*](vssgloss-l.md)</span></span>
-   <span data-ttu-id="fadc4-108">Se o componente é designado como [ *selecionável para backup*](vssgloss-s.md)</span><span class="sxs-lookup"><span data-stu-id="fadc4-108">Whether the component is designated as being [*selectable for backup*](vssgloss-s.md)</span></span>
-   <span data-ttu-id="fadc4-109">Se ele é designado como [ *selecionável para restauração*](vssgloss-s.md)</span><span class="sxs-lookup"><span data-stu-id="fadc4-109">Whether it is designated as being [*selectable for restore*](vssgloss-s.md)</span></span>
-   <span data-ttu-id="fadc4-110">Se existe uma dependência explícita entre um determinado componente em um determinado gravador e outros componentes em outros gravadores</span><span class="sxs-lookup"><span data-stu-id="fadc4-110">Whether an explicit dependency exists between a given component in a given writer and other components in other writers</span></span>

<span data-ttu-id="fadc4-111">Mais informações sobre esses problemas estão nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="fadc4-111">More information on these issues is in the following topics:</span></span>

-   [<span data-ttu-id="fadc4-112">Caminho lógico de componentes</span><span class="sxs-lookup"><span data-stu-id="fadc4-112">Logical Pathing of Components</span></span>](logical-pathing-of-components.md)
-   [<span data-ttu-id="fadc4-113">Trabalhando com a seleção para backup</span><span class="sxs-lookup"><span data-stu-id="fadc4-113">Working with Selectability for Backup</span></span>](working-with-selectability-for-backup.md)
-   [<span data-ttu-id="fadc4-114">Trabalhando com a seleção para restauração e subcomponentes</span><span class="sxs-lookup"><span data-stu-id="fadc4-114">Working with Selectability For Restore and Subcomponents</span></span>](working-with-selectability-for-restore-and-subcomponents.md)
-   [<span data-ttu-id="fadc4-115">Seleção e trabalho com propriedades de componente</span><span class="sxs-lookup"><span data-stu-id="fadc4-115">Selectability and Working with Component Properties</span></span>](selectability-and-working-with-component-properties.md)
-   [<span data-ttu-id="fadc4-116">Dependências entre componentes gerenciados por diferentes gravadores</span><span class="sxs-lookup"><span data-stu-id="fadc4-116">Dependencies between Components Managed by Different Writers</span></span>](dependencies-between-components-managed-by-different-writers.md)

 

 



