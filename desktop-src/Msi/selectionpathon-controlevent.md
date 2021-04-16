---
description: O controle SelectionTree usa o evento SelectionPathOn para publicar um valor booliano que indica se há um caminho de seleção associado ao recurso selecionado no momento. Esse evento deve ser criado na tabela EventMappings.
ms.assetid: 441b9416-066a-429b-92d2-555584a20fa2
title: SelectionPathOn ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9882ea534a0d4c91a0107ce3949363350a17fbea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757506"
---
# <a name="selectionpathon-controlevent"></a><span data-ttu-id="ee2c3-104">SelectionPathOn ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="ee2c3-104">SelectionPathOn ControlEvent</span></span>

<span data-ttu-id="ee2c3-105">O [controle SelectionTree](selectiontree-control.md) usa o evento SelectionPathOn para publicar um valor booliano que indica se há um caminho de seleção associado ao recurso selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="ee2c3-105">The [SelectionTree control](selectiontree-control.md) uses the SelectionPathOn event to publish a Boolean value indicating whether there is a selection path associated with the currently selected feature.</span></span> <span data-ttu-id="ee2c3-106">Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="ee2c3-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="ee2c3-107">Esse evento só pode afetar controles que estão localizados na mesma caixa de diálogo que o controle SelectionTree.</span><span class="sxs-lookup"><span data-stu-id="ee2c3-107">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

<span data-ttu-id="ee2c3-108">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="ee2c3-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="ee2c3-109">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ee2c3-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="ee2c3-110">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="ee2c3-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="ee2c3-111">O SelectionPathOn ControlEvent, nunca é publicado durante uma [instalação de manutenção](maintenance-installation.md).</span><span class="sxs-lookup"><span data-stu-id="ee2c3-111">The SelectionPathOn ControlEvent is never published during a [Maintenance Installation](maintenance-installation.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="ee2c3-112">Publicada por</span><span class="sxs-lookup"><span data-stu-id="ee2c3-112">Published By</span></span>

[<span data-ttu-id="ee2c3-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="ee2c3-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="ee2c3-114">Argumento</span><span class="sxs-lookup"><span data-stu-id="ee2c3-114">Argument</span></span>

<span data-ttu-id="ee2c3-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="ee2c3-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="ee2c3-116">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="ee2c3-116">Action on Subscribers</span></span>

<span data-ttu-id="ee2c3-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="ee2c3-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="ee2c3-118">Usos comum</span><span class="sxs-lookup"><span data-stu-id="ee2c3-118">Typical Use</span></span>

<span data-ttu-id="ee2c3-119">Um controle de [texto](text-control.md) na mesma caixa de diálogo modal que o SelectionTree deve assinar o evento por meio da [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="ee2c3-119">A [Text](text-control.md) control on the same modal dialog as the SelectionTree should subscribe to the event via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="ee2c3-120">O controle de texto exibe a legenda do caminho de seleção.</span><span class="sxs-lookup"><span data-stu-id="ee2c3-120">The Text Control displays the caption of the selection path.</span></span> <span data-ttu-id="ee2c3-121">Esse controle de texto é visível ou oculto, dependendo do evento.</span><span class="sxs-lookup"><span data-stu-id="ee2c3-121">This text control is visible or hidden depending on the event.</span></span>

 

 



