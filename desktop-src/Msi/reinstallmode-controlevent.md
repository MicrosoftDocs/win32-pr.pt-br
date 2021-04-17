---
description: Permite que o autor especifique o modo de validação ou os modos durante uma reinstalação e enquanto a caixa de diálogo atual está em execução.
ms.assetid: d7cd41c6-c019-49d6-b593-a1d31c8f5a81
title: Reinstalar o ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ff5ff662b2880a3f4ab0fb79738b49cdeeccd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749781"
---
# <a name="reinstallmode-controlevent"></a><span data-ttu-id="0b69d-103">Reinstalar o ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="0b69d-103">ReinstallMode ControlEvent</span></span>

<span data-ttu-id="0b69d-104">A reinstalação do ControlEventallows o autor para especificar o modo de validação ou os modos durante uma reinstalação e enquanto a caixa de diálogo atual está em execução.</span><span class="sxs-lookup"><span data-stu-id="0b69d-104">The ReinstallMode ControlEventallows the author to specify the validation mode or modes during a reinstallation, and while the current dialog box is running.</span></span>

<span data-ttu-id="0b69d-105">Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md) ou um [controle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="0b69d-105">This event can be published by a [PushButton Control](pushbutton-control.md) or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="0b69d-106">Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md)e requer que a interface do usuário seja executada no nível [*completo da interface*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="0b69d-106">This event should be authored into the [ControlEvent table](controlevent-table.md), and requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="0b69d-107">Esse evento não funciona com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0b69d-107">This event does not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="0b69d-108">Para obter mais informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="0b69d-108">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="0b69d-109">Publicada por</span><span class="sxs-lookup"><span data-stu-id="0b69d-109">Published By</span></span>

<span data-ttu-id="0b69d-110">Esse ControlEvent, é publicado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="0b69d-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="0b69d-111">Argumento</span><span class="sxs-lookup"><span data-stu-id="0b69d-111">Argument</span></span>

<span data-ttu-id="0b69d-112">Uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0b69d-112">A string.</span></span> <span data-ttu-id="0b69d-113">Para obter uma lista de valores possíveis, consulte Propriedade [**REinstallmode**](reinstallmode.md) .</span><span class="sxs-lookup"><span data-stu-id="0b69d-113">For a list of possible values, see [**REINSTALLMODE**](reinstallmode.md) property.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="0b69d-114">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="0b69d-114">Action on Subscribers</span></span>

<span data-ttu-id="0b69d-115">Este ControlEvent, não executa uma ação nos assinantes.</span><span class="sxs-lookup"><span data-stu-id="0b69d-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="0b69d-116">Usos comum</span><span class="sxs-lookup"><span data-stu-id="0b69d-116">Typical Use</span></span>

<span data-ttu-id="0b69d-117">Esse evento é vinculado a um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="0b69d-117">This event is tied to a [PushButton](pushbutton-control.md) control on a modal dialog box.</span></span> <span data-ttu-id="0b69d-118">O mesmo controle de [pressão](pushbutton-control.md) também deve ser vinculado a um ControlEvent, de [reinstalação](reinstall-controlevent.md) .</span><span class="sxs-lookup"><span data-stu-id="0b69d-118">The same [PushButton](pushbutton-control.md) control should also be tied to a [Reinstall](reinstall-controlevent.md) ControlEvent.</span></span>

 

 



