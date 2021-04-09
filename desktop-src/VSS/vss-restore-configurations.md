---
description: A restauração de arquivos em um sistema em execução pode ser problemática. É importante que a execução de aplicativos (gravadores) indique o que fazer quando surgirem dificuldades durante restaurações, por exemplo, se o arquivo que está sendo restaurado estiver em uso no momento.
ms.assetid: 2cb963a8-7077-4419-96d8-cba0fd011e4f
title: Configurações de restauração do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f13acfc59f250a859e9c62f2df2e1b1b982608ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090443"
---
# <a name="vss-restore-configurations"></a><span data-ttu-id="6f7aa-104">Configurações de restauração do VSS</span><span class="sxs-lookup"><span data-stu-id="6f7aa-104">VSS Restore Configurations</span></span>

<span data-ttu-id="6f7aa-105">A restauração de arquivos em um sistema em execução pode ser problemática.</span><span class="sxs-lookup"><span data-stu-id="6f7aa-105">File restoration on a running system can be problematic.</span></span> <span data-ttu-id="6f7aa-106">É importante que a execução de aplicativos (gravadores) indique o que fazer quando surgirem dificuldades durante restaurações, por exemplo, se o arquivo que está sendo restaurado estiver em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="6f7aa-106">It is important that running applications (writers) indicate what to do when difficulties arise during restores, for instance, if the file being restored is currently in use.</span></span>

<span data-ttu-id="6f7aa-107">No VSS, os gravadores têm duas maneiras complementares de gerenciar restaurações —[*métodos de restauração*](vssgloss-r.md) e [*destinos de restauração*](vssgloss-r.md).</span><span class="sxs-lookup"><span data-stu-id="6f7aa-107">Under VSS, writers have two complementary ways of managing restores—[*restore methods*](vssgloss-r.md) and [*restore targets*](vssgloss-r.md).</span></span>

<span data-ttu-id="6f7aa-108">Além disso, os solicitantes podem optar por restaurar os arquivos para os locais não especificados anteriormente e notificar os gravadores (consulte [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)).</span><span class="sxs-lookup"><span data-stu-id="6f7aa-108">In addition, requesters can choose to restore files to previously unspecified locations and notify writers (see [**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)).</span></span>

<span data-ttu-id="6f7aa-109">O método Restore (também chama o destino de restauração original) é especificado por um gravador em um horário de backup e define uma definição de todo o gravador do método a ser usado para restaurar todos os seus componentes no futuro.</span><span class="sxs-lookup"><span data-stu-id="6f7aa-109">The restore method (also call the original restore target) is specified by a writer at a backup time, and sets a writer-wide definition of the method to be used to restore all its components in the future.</span></span> <span data-ttu-id="6f7aa-110">Todos os arquivos e componentes gerenciados por um gravador compartilham o mesmo método de restauração.</span><span class="sxs-lookup"><span data-stu-id="6f7aa-110">All files and components managed by a writer share the same restore method.</span></span>

<span data-ttu-id="6f7aa-111">Os destinos de restauração permitem que os gravadores alterem como os componentes específicos devem ser restaurados no momento da restauração.</span><span class="sxs-lookup"><span data-stu-id="6f7aa-111">Restore targets allow writers to change how specific components are to be restored at restore time.</span></span> <span data-ttu-id="6f7aa-112">Ao contrário dos métodos de restauração, os destinos de restauração são definidos para um conjunto de componentes.</span><span class="sxs-lookup"><span data-stu-id="6f7aa-112">Unlike restore methods, restore targets are defined for a component set.</span></span>

<span data-ttu-id="6f7aa-113">Uma discussão detalhada sobre o uso de métodos de restauração e destinos de restauração é encontrada nos tópicos listados abaixo:</span><span class="sxs-lookup"><span data-stu-id="6f7aa-113">A detailed discussion of the usage of restore methods and restore targets is found in the topics listed below:</span></span>

-   [<span data-ttu-id="6f7aa-114">Estado de restauração do VSS</span><span class="sxs-lookup"><span data-stu-id="6f7aa-114">VSS Restore State</span></span>](vss-restore-state.md)
-   [<span data-ttu-id="6f7aa-115">Definição de métodos de restauração do VSS</span><span class="sxs-lookup"><span data-stu-id="6f7aa-115">Setting VSS Restore Methods</span></span>](setting-vss-restore-methods.md)
-   [<span data-ttu-id="6f7aa-116">Definindo destinos de restauração do VSS</span><span class="sxs-lookup"><span data-stu-id="6f7aa-116">Setting VSS Restore Targets</span></span>](setting-vss-restore-targets.md)
-   [<span data-ttu-id="6f7aa-117">Definindo opções de restauração do VSS</span><span class="sxs-lookup"><span data-stu-id="6f7aa-117">Setting VSS Restore Options</span></span>](setting-vss-restore-options.md)

<span data-ttu-id="6f7aa-118">(Para obter informações sobre restaurações que não usam esses mecanismos, consulte [restaurações sem participação no gravador](restores-without-writer-participation.md).)</span><span class="sxs-lookup"><span data-stu-id="6f7aa-118">(For information on restores that do not use these mechanisms, see [Restores without Writer Participation](restores-without-writer-participation.md).)</span></span>

 

 



