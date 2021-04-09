---
description: Esse evento notifica o instalador para fazer a transição de uma caixa de diálogo modal para outra caixa de diálogo. O instalador remove a caixa de diálogo atual e cria uma nova com o nome indicado no argumento.
ms.assetid: bd1aa465-55a0-4983-8c71-7e7075ee9dfb
title: NewDialog ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 439c459bc5bfe061cc7f888d9c0a3374afa9098b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091133"
---
# <a name="newdialog-controlevent"></a><span data-ttu-id="f4609-104">NewDialog ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="f4609-104">NewDialog ControlEvent</span></span>

<span data-ttu-id="f4609-105">Esse evento notifica o instalador para fazer a transição de uma caixa de diálogo modal para outra caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f4609-105">This event notifies the installer to transition a modal dialog box to another dialog box.</span></span> <span data-ttu-id="f4609-106">O instalador remove a caixa de diálogo atual e cria uma nova com o nome indicado no argumento.</span><span class="sxs-lookup"><span data-stu-id="f4609-106">The installer removes the present dialog box and creates the new one with the name indicated in the argument.</span></span>

<span data-ttu-id="f4609-107">Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md)ou um [controle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="f4609-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="f4609-108">Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="f4609-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="f4609-109">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="f4609-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="f4609-110">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f4609-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="f4609-111">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="f4609-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="f4609-112">Publicada por</span><span class="sxs-lookup"><span data-stu-id="f4609-112">Published By</span></span>

<span data-ttu-id="f4609-113">Esse ControlEvent, é publicado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="f4609-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="f4609-114">Argumento</span><span class="sxs-lookup"><span data-stu-id="f4609-114">Argument</span></span>

<span data-ttu-id="f4609-115">Uma cadeia de caracteres que é o nome da nova caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f4609-115">A string that is the name of the new dialog.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="f4609-116">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="f4609-116">Action on Subscribers</span></span>

<span data-ttu-id="f4609-117">Este ControlEvent, não executa uma ação nos assinantes.</span><span class="sxs-lookup"><span data-stu-id="f4609-117">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="f4609-118">Usos comum</span><span class="sxs-lookup"><span data-stu-id="f4609-118">Typical Use</span></span>

<span data-ttu-id="f4609-119">Um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo modal está vinculado a esse evento na tabela [ControlEvent,](controlevent-table.md) para sinalizar uma transição para a caixa de diálogo seguinte ou anterior da mesma sequência do assistente.</span><span class="sxs-lookup"><span data-stu-id="f4609-119">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to signal a transition to the next or previous dialog box of the same wizard sequence.</span></span>

 

 



