---
description: Esse ControlEvent, pode ser usado para ativar ou desativar os recursos de reversão do instalador.
ms.assetid: 5279151c-a7cd-4f66-8d1b-d688b3b1cf82
title: EnableRollback ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc651ef90b46c87431453f50c7ee5a28953e4d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747551"
---
# <a name="enablerollback-controlevent"></a><span data-ttu-id="eb794-103">EnableRollback ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="eb794-103">EnableRollback ControlEvent</span></span>

<span data-ttu-id="eb794-104">Esse ControlEvent, pode ser usado para ativar ou desativar os recursos de reversão do instalador.</span><span class="sxs-lookup"><span data-stu-id="eb794-104">This ControlEvent can be used to turn on or turn off the installer's rollback capabilities.</span></span>

<span data-ttu-id="eb794-105">Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md)ou um [controle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="eb794-105">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="eb794-106">Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="eb794-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="eb794-107">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="eb794-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="eb794-108">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="eb794-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="eb794-109">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="eb794-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="eb794-110">Publicada por</span><span class="sxs-lookup"><span data-stu-id="eb794-110">Published By</span></span>

<span data-ttu-id="eb794-111">Esse ControlEvent, é publicado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="eb794-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="eb794-112">Argumento</span><span class="sxs-lookup"><span data-stu-id="eb794-112">Argument</span></span>

<span data-ttu-id="eb794-113">False desativa os recursos de reversão do instalador.</span><span class="sxs-lookup"><span data-stu-id="eb794-113">False turns off the installer's rollback capabilities.</span></span> <span data-ttu-id="eb794-114">True ativa os recursos de reversão do instalador.</span><span class="sxs-lookup"><span data-stu-id="eb794-114">True turns on the installer's rollback capabilities.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="eb794-115">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="eb794-115">Action on Subscribers</span></span>

<span data-ttu-id="eb794-116">Este ControlEvent, não executa uma ação nos assinantes.</span><span class="sxs-lookup"><span data-stu-id="eb794-116">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="eb794-117">Usos comum</span><span class="sxs-lookup"><span data-stu-id="eb794-117">Typical Use</span></span>

<span data-ttu-id="eb794-118">Pode ser usado para desativar os recursos de reversão se o instalador detectar que não há espaço em disco suficiente disponível para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="eb794-118">Can be used to turn off rollback capabilities if the installer detects that there is insufficient disk space available to complete the installation.</span></span> <span data-ttu-id="eb794-119">Para esse caso, o ControlEvent, deve ser usado com as propriedades [**OutOfDiskSpace**](outofdiskspace.md), [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)e [**PROMPTROLLBACKCOST**](promptrollbackcost.md) .</span><span class="sxs-lookup"><span data-stu-id="eb794-119">For this case, the ControlEvent should be used with the [**OutOfDiskSpace**](outofdiskspace.md), [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md), and the [**PROMPTROLLBACKCOST**](promptrollbackcost.md) properties.</span></span>

 

 



