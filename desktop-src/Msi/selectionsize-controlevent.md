---
description: O controle SelectionTree usa o evento SelectionSize para publicar o tamanho do item realçado.
ms.assetid: 1ef161b6-f127-45ad-a312-d2adcb5124ef
title: SelectionSize ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c11829661f0120fa5906a04f081e6c979b37180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169841"
---
# <a name="selectionsize-controlevent"></a><span data-ttu-id="9bf70-103">SelectionSize ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="9bf70-103">SelectionSize ControlEvent</span></span>

<span data-ttu-id="9bf70-104">O [controle SelectionTree](selectiontree-control.md) usa o evento SelectionSize para publicar o tamanho do item realçado.</span><span class="sxs-lookup"><span data-stu-id="9bf70-104">The [SelectionTree control](selectiontree-control.md) uses the SelectionSize event to publish the size of the highlighted item.</span></span> <span data-ttu-id="9bf70-105">Se for um item pai, o número de filhos selecionados também será publicado.</span><span class="sxs-lookup"><span data-stu-id="9bf70-105">If it is a parent item, then the number of children selected is also published.</span></span> <span data-ttu-id="9bf70-106">A cadeia de caracteres é uma das cadeias de **SelChildCostPos**, **SelChildCostNeg**, **SelParentCostPosPos**, **SelParentCostPosNeg**, **SelParentCostNegPos** ou **SelParentCostNegNeg** da [tabela UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="9bf70-106">The string is one of the **SelChildCostPos**, **SelChildCostNeg**, **SelParentCostPosPos**, **SelParentCostPosNeg**, **SelParentCostNegPos** or **SelParentCostNegNeg** strings from the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="9bf70-107">Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="9bf70-107">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="9bf70-108">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="9bf70-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="9bf70-109">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9bf70-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="9bf70-110">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="9bf70-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="9bf70-111">Esse evento só pode afetar controles que estão localizados na mesma caixa de diálogo que o controle SelectionTree.</span><span class="sxs-lookup"><span data-stu-id="9bf70-111">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="9bf70-112">Publicada por</span><span class="sxs-lookup"><span data-stu-id="9bf70-112">Published By</span></span>

[<span data-ttu-id="9bf70-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="9bf70-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="9bf70-114">Argumento</span><span class="sxs-lookup"><span data-stu-id="9bf70-114">Argument</span></span>

<span data-ttu-id="9bf70-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="9bf70-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="9bf70-116">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="9bf70-116">Action on Subscribers</span></span>

<span data-ttu-id="9bf70-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="9bf70-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="9bf70-118">Usos comum</span><span class="sxs-lookup"><span data-stu-id="9bf70-118">Typical Use</span></span>

<span data-ttu-id="9bf70-119">Um controle de [texto](text-control.md) na mesma caixa de diálogo modal que o controle SelectionTree por meio da [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="9bf70-119">A [Text](text-control.md) control on the same modal dialog as the SelectionTree Control via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="9bf70-120">O controle de texto usa esse evento para exibir o tamanho do item realçado.</span><span class="sxs-lookup"><span data-stu-id="9bf70-120">The Text Control uses this event to display the size of the highlighted item.</span></span>

 

 



