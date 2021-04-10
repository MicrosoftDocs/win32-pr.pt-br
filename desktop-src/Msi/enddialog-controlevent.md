---
description: Esse evento notifica o instalador para remover uma caixa de diálogo modal. Em todos os casos, o instalador remove a caixa de diálogo atual.
ms.assetid: 74a28696-6387-4d62-8955-4708ba5872bb
title: EndDialog ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08449bffe29093e32066e92e1b8fc739efa02d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169862"
---
# <a name="enddialog-controlevent"></a><span data-ttu-id="7a4ac-104">EndDialog ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="7a4ac-104">EndDialog ControlEvent</span></span>

<span data-ttu-id="7a4ac-105">Esse evento notifica o instalador para remover uma caixa de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="7a4ac-105">This event notifies the installer to remove a modal dialog box.</span></span> <span data-ttu-id="7a4ac-106">Em todos os casos, o instalador remove a caixa de diálogo atual.</span><span class="sxs-lookup"><span data-stu-id="7a4ac-106">In all cases the installer removes the present dialog box.</span></span>

<span data-ttu-id="7a4ac-107">Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md)ou um [controle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="7a4ac-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="7a4ac-108">Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="7a4ac-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="7a4ac-109">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="7a4ac-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="7a4ac-110">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7a4ac-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="7a4ac-111">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="7a4ac-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="7a4ac-112">A tabela a seguir lista a ação do evento resultante de diferentes argumentos inseridos na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="7a4ac-112">The following table lists the action of the event resulting from different arguments entered into the [ControlEvent table](controlevent-table.md).</span></span>



| <span data-ttu-id="7a4ac-113">Argumento</span><span class="sxs-lookup"><span data-stu-id="7a4ac-113">Argument</span></span> | <span data-ttu-id="7a4ac-114">Ação do instalador</span><span class="sxs-lookup"><span data-stu-id="7a4ac-114">Action by the installer</span></span>                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a4ac-115">Fechar</span><span class="sxs-lookup"><span data-stu-id="7a4ac-115">Exit</span></span>     | <span data-ttu-id="7a4ac-116">A sequência do assistente é fechada e o controle retorna para o instalador com o valor UserExit.</span><span class="sxs-lookup"><span data-stu-id="7a4ac-116">The wizard sequence is closed and the control returns to the installer with the UserExit value.</span></span> <span data-ttu-id="7a4ac-117">Esse argumento não pode ser usado em uma caixa de diálogo que seja filho de outra caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7a4ac-117">This argument cannot be used in a dialog box that is a child of another dialog box.</span></span> |
| <span data-ttu-id="7a4ac-118">Tentar novamente</span><span class="sxs-lookup"><span data-stu-id="7a4ac-118">Retry</span></span>    | <span data-ttu-id="7a4ac-119">A sequência do assistente é fechada e o controle retorna ao instalador com o valor de suspensão.</span><span class="sxs-lookup"><span data-stu-id="7a4ac-119">The wizard sequence is closed and the control returns to the installer with the Suspend value.</span></span> <span data-ttu-id="7a4ac-120">Esse argumento não pode ser usado em uma caixa de diálogo que seja filho de outra caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7a4ac-120">This argument cannot be used in a dialog box that is a child of another dialog box.</span></span>  |
| <span data-ttu-id="7a4ac-121">Ignorar</span><span class="sxs-lookup"><span data-stu-id="7a4ac-121">Ignore</span></span>   | <span data-ttu-id="7a4ac-122">A sequência do assistente é fechada e o controle retorna ao instalador com o valor concluído.</span><span class="sxs-lookup"><span data-stu-id="7a4ac-122">The wizard sequence is closed and the control returns to the installer with the Finished value.</span></span> <span data-ttu-id="7a4ac-123">Esse argumento não pode ser usado em uma caixa de diálogo que seja filho de outra caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="7a4ac-123">This argument cannot be used in a dialog box that is a child of another dialog box.</span></span> |
| <span data-ttu-id="7a4ac-124">Retorno</span><span class="sxs-lookup"><span data-stu-id="7a4ac-124">Return</span></span>   | <span data-ttu-id="7a4ac-125">O controle retorna ao pai da caixa de diálogo atual ou, se não houver nenhum pai, o controle retornará ao instalador com o valor de êxito.</span><span class="sxs-lookup"><span data-stu-id="7a4ac-125">The control returns to the parent of the present dialog box, or if there is no parent, the control returns to the installer with the Success value.</span></span>                                 |



 

## <a name="published-by"></a><span data-ttu-id="7a4ac-126">Publicada por</span><span class="sxs-lookup"><span data-stu-id="7a4ac-126">Published By</span></span>

<span data-ttu-id="7a4ac-127">Esse ControlEvent, é publicado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="7a4ac-127">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="7a4ac-128">Argumento</span><span class="sxs-lookup"><span data-stu-id="7a4ac-128">Argument</span></span>

<span data-ttu-id="7a4ac-129">Em caixas de diálogo normais, a coluna Argument da [tabela ControlEvent,](controlevent-table.md) pode ser "Return", "Exit", "retry" ou "ignore".</span><span class="sxs-lookup"><span data-stu-id="7a4ac-129">On regular dialog boxes the Argument column of the [ControlEvent table](controlevent-table.md) can be "Return", "Exit", "Retry", or "Ignore".</span></span>

<span data-ttu-id="7a4ac-130">Nas caixas de diálogo de erro, a coluna Argument da [tabela ControlEvent,](controlevent-table.md) pode ser "ErrorOk", "ErrorCancel", "ErrorAbort", "ErrorRetry", "ErrorIgnore", "ErrorYes" ou "ErrorNo".</span><span class="sxs-lookup"><span data-stu-id="7a4ac-130">On error dialog boxes the Argument column of the [ControlEvent table](controlevent-table.md) can be "ErrorOk", "ErrorCancel", "ErrorAbort", "ErrorRetry", "ErrorIgnore", "ErrorYes", or "ErrorNo".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="7a4ac-131">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="7a4ac-131">Action on Subscribers</span></span>

<span data-ttu-id="7a4ac-132">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="7a4ac-132">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="7a4ac-133">Usos comum</span><span class="sxs-lookup"><span data-stu-id="7a4ac-133">Typical Use</span></span>

<span data-ttu-id="7a4ac-134">Um controle de [supressão](pushbutton-control.md) em uma caixa de diálogo modal está vinculado a esse evento na tabela [ControlEvent,](controlevent-table.md) para fechar um diálogo.</span><span class="sxs-lookup"><span data-stu-id="7a4ac-134">A [PushButton](pushbutton-control.md) control on a modal dialog is tied to this event in the [ControlEvent](controlevent-table.md) table to close a dialog box.</span></span>

 

 



