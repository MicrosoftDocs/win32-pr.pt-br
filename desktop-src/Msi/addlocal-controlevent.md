---
description: Esse evento notifica o instalador, enquanto mantém a caixa de diálogo presente em execução, que um recurso ou todos os recursos devem ser executados localmente.
ms.assetid: 074f347e-37d3-4365-a25d-caa0392a0dbc
title: ControlEvent, ADDLOCAL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 112975d31e341c06a21609b173b9682283e71610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764671"
---
# <a name="addlocal-controlevent"></a><span data-ttu-id="cd5af-103">ControlEvent, ADDLOCAL</span><span class="sxs-lookup"><span data-stu-id="cd5af-103">AddLocal ControlEvent</span></span>

<span data-ttu-id="cd5af-104">Esse evento notifica o instalador, enquanto mantém a caixa de diálogo presente em execução, que um recurso ou todos os recursos devem ser executados localmente.</span><span class="sxs-lookup"><span data-stu-id="cd5af-104">This event notifies the installer, while keeping the present dialog running, that a feature or all features are to be run locally.</span></span> <span data-ttu-id="cd5af-105">Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md), [controle de caixa de seleção](checkbox-control.md)ou um [controle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="cd5af-105">This event can be published by a [PushButton Control](pushbutton-control.md), [Checkbox Control](checkbox-control.md), or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="cd5af-106">Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="cd5af-106">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="cd5af-107">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="cd5af-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="cd5af-108">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="cd5af-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="cd5af-109">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="cd5af-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="cd5af-110">Publicada por</span><span class="sxs-lookup"><span data-stu-id="cd5af-110">Published By</span></span>

<span data-ttu-id="cd5af-111">Esse ControlEvent, é publicado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="cd5af-111">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="cd5af-112">Argumento</span><span class="sxs-lookup"><span data-stu-id="cd5af-112">Argument</span></span>

<span data-ttu-id="cd5af-113">Uma cadeia de caracteres, o nome do recurso ou "todos".</span><span class="sxs-lookup"><span data-stu-id="cd5af-113">A string, either the name of the feature or "ALL".</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="cd5af-114">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="cd5af-114">Action on Subscribers</span></span>

<span data-ttu-id="cd5af-115">Este ControlEvent, não executa uma ação nos assinantes.</span><span class="sxs-lookup"><span data-stu-id="cd5af-115">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="cd5af-116">Usos comum</span><span class="sxs-lookup"><span data-stu-id="cd5af-116">Typical Use</span></span>

<span data-ttu-id="cd5af-117">Um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo modal está vinculado a esse evento e usado para notificar o instalador sem interromper a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="cd5af-117">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event and used to notify the installer without stopping the dialog box.</span></span>

 

 



