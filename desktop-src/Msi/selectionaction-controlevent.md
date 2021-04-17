---
description: O controle SelectionTree usa esse evento para publicar uma cadeia de caracteres que descreve o item realçado. A cadeia de caracteres é uma das &\# 0034; Sel \* & \# 0034; cadeias de caracteres da tabela UIText. Esse evento deve ser criado na tabela EventMappings.
ms.assetid: 7770b46f-21c7-459f-9778-a86de70d467f
title: ControlEvent, selectionaction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda06826f6ac649e2278441c944cdea0332689af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769307"
---
# <a name="selectionaction-controlevent"></a><span data-ttu-id="d9665-105">ControlEvent, selectionaction</span><span class="sxs-lookup"><span data-stu-id="d9665-105">SelectionAction ControlEvent</span></span>

<span data-ttu-id="d9665-106">O [controle SelectionTree](selectiontree-control.md) usa esse evento para publicar uma cadeia de caracteres que descreve o item realçado.</span><span class="sxs-lookup"><span data-stu-id="d9665-106">The [SelectionTree control](selectiontree-control.md) uses this event to publish a string describing the highlighted item.</span></span> <span data-ttu-id="d9665-107">A cadeia de caracteres é uma das \* cadeias "SEL" da [tabela UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="d9665-107">The string is one of the "Sel\*" strings from the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="d9665-108">Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="d9665-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="d9665-109">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="d9665-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="d9665-110">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d9665-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="d9665-111">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="d9665-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="d9665-112">Esse evento só pode afetar controles que estão localizados na mesma caixa de diálogo que o controle SelectionTree.</span><span class="sxs-lookup"><span data-stu-id="d9665-112">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="d9665-113">Publicada por</span><span class="sxs-lookup"><span data-stu-id="d9665-113">Published By</span></span>

[<span data-ttu-id="d9665-114">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="d9665-114">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="d9665-115">Argumento</span><span class="sxs-lookup"><span data-stu-id="d9665-115">Argument</span></span>

<span data-ttu-id="d9665-116">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d9665-116">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="d9665-117">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="d9665-117">Action on Subscribers</span></span>

<span data-ttu-id="d9665-118">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d9665-118">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="d9665-119">Usos comum</span><span class="sxs-lookup"><span data-stu-id="d9665-119">Typical Use</span></span>

<span data-ttu-id="d9665-120">Um controle de [texto](text-control.md) na mesma caixa de diálogo modal que o SelectionTree deve assinar esse evento por meio da [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="d9665-120">A [Text](text-control.md) control in the same modal dialog box as the SelectionTree should subscribe to this event via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="d9665-121">O controle de texto exibe a explicação do item selecionado.</span><span class="sxs-lookup"><span data-stu-id="d9665-121">The Text Control displays the explanation of the selected item.</span></span>

 

 



