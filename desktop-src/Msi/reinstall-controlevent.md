---
description: Permite que o autor inicie uma reinstalação de alguns ou todos os recursos, enquanto a caixa de diálogo atual está em execução.
ms.assetid: bc667f20-3abe-4ef3-b51e-dc74da63f651
title: Reinstalar o ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1d2adece3f89dbe57b77f2345d1714ece64b271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756723"
---
# <a name="reinstall-controlevent"></a><span data-ttu-id="93899-103">Reinstalar o ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="93899-103">Reinstall ControlEvent</span></span>

<span data-ttu-id="93899-104">A reinstalação ControlEventallows o autor para iniciar uma reinstalação de alguns ou todos os recursos, enquanto a caixa de diálogo atual está em execução.</span><span class="sxs-lookup"><span data-stu-id="93899-104">The Reinstall ControlEventallows the author to initiate a reinstall of some or all features, while the current dialog box is running.</span></span>

<span data-ttu-id="93899-105">Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md) ou um [controle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="93899-105">This event can be published by a [PushButton control](pushbutton-control.md) or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="93899-106">Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md)e requer que a interface do usuário seja executada no nível [*completo da interface*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="93899-106">This event should be authored into the [ControlEvent table](controlevent-table.md), and requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="93899-107">Esse evento não funciona com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="93899-107">This event does not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="93899-108">Para obter mais informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="93899-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="93899-109">Publicada por</span><span class="sxs-lookup"><span data-stu-id="93899-109">Published By</span></span>

<span data-ttu-id="93899-110">Esse ControlEvent, é publicado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="93899-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="93899-111">Argumento</span><span class="sxs-lookup"><span data-stu-id="93899-111">Argument</span></span>

<span data-ttu-id="93899-112">Uma cadeia de caracteres que é o nome do recurso ou "todos".</span><span class="sxs-lookup"><span data-stu-id="93899-112">A string that is either the name of the feature or "ALL".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="93899-113">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="93899-113">Action on Subscribers</span></span>

<span data-ttu-id="93899-114">Este ControlEvent, não executa uma ação nos assinantes.</span><span class="sxs-lookup"><span data-stu-id="93899-114">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="93899-115">Usos comum</span><span class="sxs-lookup"><span data-stu-id="93899-115">Typical Use</span></span>

<span data-ttu-id="93899-116">Esse evento é vinculado a um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="93899-116">This event is tied to a [PushButton](pushbutton-control.md) control on a modal dialog box.</span></span> <span data-ttu-id="93899-117">O mesmo controle de [pressão](pushbutton-control.md) também deve ser vinculado a um ControlEvent, [REINSTALLMODE](reinstallmode-controlevent.md) .</span><span class="sxs-lookup"><span data-stu-id="93899-117">The same [PushButton](pushbutton-control.md) control should also be tied to a [ReinstallMode](reinstallmode-controlevent.md) ControlEvent.</span></span>

 

 



