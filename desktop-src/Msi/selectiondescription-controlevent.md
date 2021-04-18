---
description: O controle SelectionTree usa o evento SelectionDescription para publicar uma cadeia de caracteres que contém a descrição do item realçado. Essa cadeia de caracteres é o campo de descrição da tabela de recursos. Esse evento deve ser criado na tabela EventMappings.
ms.assetid: 29ae9aec-764f-4ff2-9c08-805538130cb1
title: SelectionDescription ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901db4efbed03341243d1b978dab0b8759fbc02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753435"
---
# <a name="selectiondescription-controlevent"></a><span data-ttu-id="c8ac6-105">SelectionDescription ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="c8ac6-105">SelectionDescription ControlEvent</span></span>

<span data-ttu-id="c8ac6-106">O [controle SelectionTree](selectiontree-control.md) usa o evento SelectionDescription para publicar uma cadeia de caracteres que contém a descrição do item realçado.</span><span class="sxs-lookup"><span data-stu-id="c8ac6-106">The [SelectionTree control](selectiontree-control.md) uses the SelectionDescription event to publish a string that contains the description for the highlighted item.</span></span> <span data-ttu-id="c8ac6-107">Essa cadeia de caracteres é o campo de **Descrição** da [tabela de recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="c8ac6-107">This string is the **Description** field of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="c8ac6-108">Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="c8ac6-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="c8ac6-109">Esse evento só pode afetar controles que estão localizados na mesma caixa de diálogo que o [controle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="c8ac6-109">This event can only affect controls that are located on the same dialog box as the [SelectionTree control](selectiontree-control.md).</span></span>

<span data-ttu-id="c8ac6-110">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="c8ac6-110">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="c8ac6-111">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c8ac6-111">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="c8ac6-112">Para obter mais informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="c8ac6-112">For more information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="c8ac6-113">Publicada por</span><span class="sxs-lookup"><span data-stu-id="c8ac6-113">Published By</span></span>

[<span data-ttu-id="c8ac6-114">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="c8ac6-114">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="c8ac6-115">Argumento</span><span class="sxs-lookup"><span data-stu-id="c8ac6-115">Argument</span></span>

<span data-ttu-id="c8ac6-116">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="c8ac6-116">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="c8ac6-117">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="c8ac6-117">Action on Subscribers</span></span>

<span data-ttu-id="c8ac6-118">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="c8ac6-118">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="c8ac6-119">Usos comum</span><span class="sxs-lookup"><span data-stu-id="c8ac6-119">Typical Use</span></span>

<span data-ttu-id="c8ac6-120">Um controle de [texto](text-control.md) na mesma caixa de diálogo modal que o SelectionTree assina esse ControlEvent, por meio da [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="c8ac6-120">A [Text](text-control.md) control on the same modal dialog as the SelectionTree subscribes to this ControlEvent via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="c8ac6-121">O controle de texto usa esse evento para exibir a descrição do item realçado.</span><span class="sxs-lookup"><span data-stu-id="c8ac6-121">The Text Control uses this event to display the description of the highlighted item.</span></span>

 

 



