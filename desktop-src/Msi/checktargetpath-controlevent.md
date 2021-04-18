---
description: Esse evento notifica o instalador que ele precisa verificar se o caminho selecionado é válido. Se o caminho não for válido, esse evento bloqueará ControlEvents adicionais associados ao controle.
ms.assetid: b7c1de6e-5738-4ecb-a033-9379d79dddb9
title: CheckTargetPath ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49301dbe1fcc6becc1bc757a0fe487061e1dcdbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756739"
---
# <a name="checktargetpath-controlevent"></a><span data-ttu-id="1fbd8-104">CheckTargetPath ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="1fbd8-104">CheckTargetPath ControlEvent</span></span>

<span data-ttu-id="1fbd8-105">Esse evento notifica o instalador que ele precisa verificar se o caminho selecionado é válido.</span><span class="sxs-lookup"><span data-stu-id="1fbd8-105">This event notifies the installer that it has to verify that the selected path is valid.</span></span> <span data-ttu-id="1fbd8-106">Se o caminho não for válido, esse evento bloqueará ControlEvents adicionais associados ao controle.</span><span class="sxs-lookup"><span data-stu-id="1fbd8-106">If the path is not valid, then this event blocks further ControlEvents associated with the control.</span></span>

<span data-ttu-id="1fbd8-107">Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md)ou um [controle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="1fbd8-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="1fbd8-108">Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="1fbd8-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="1fbd8-109">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="1fbd8-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="1fbd8-110">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="1fbd8-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="1fbd8-111">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="1fbd8-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="1fbd8-112">Publicada por</span><span class="sxs-lookup"><span data-stu-id="1fbd8-112">Published By</span></span>

<span data-ttu-id="1fbd8-113">Esse ControlEvent, é publicado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="1fbd8-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="1fbd8-114">Argumento</span><span class="sxs-lookup"><span data-stu-id="1fbd8-114">Argument</span></span>

<span data-ttu-id="1fbd8-115">O nome da propriedade que contém o caminho.</span><span class="sxs-lookup"><span data-stu-id="1fbd8-115">The name of the property containing the path.</span></span> <span data-ttu-id="1fbd8-116">Se a propriedade for indireta, o nome da propriedade será colocado entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="1fbd8-116">If the property is indirected, then the property name is enclosed in square brackets.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="1fbd8-117">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="1fbd8-117">Action on Subscribers</span></span>

<span data-ttu-id="1fbd8-118">Este ControlEvent, não executa uma ação nos assinantes.</span><span class="sxs-lookup"><span data-stu-id="1fbd8-118">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="1fbd8-119">Usos comum</span><span class="sxs-lookup"><span data-stu-id="1fbd8-119">Typical Use</span></span>

<span data-ttu-id="1fbd8-120">Um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo de procura está vinculado a esse evento na tabela [ControlEvent,](controlevent-table.md) para verificar o caminho selecionado antes de retornar à caixa de diálogo de seleção.</span><span class="sxs-lookup"><span data-stu-id="1fbd8-120">A [PushButton](pushbutton-control.md) control on a browse dialog box is tied to this event in the [ControlEvent](controlevent-table.md) table to check the selected path before returning to the selection dialog box.</span></span>

 

 



