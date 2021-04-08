---
description: O controle SelectionTree usa o evento SelectionPath para publicar o caminho para o item realçado.
ms.assetid: 755e5bf2-42c4-4213-9bb7-4f15ad22041f
title: SelectionPath ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8314b12d14e10ccf96c7db9db32e63172050c0bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921906"
---
# <a name="selectionpath-controlevent"></a><span data-ttu-id="fd3ee-103">SelectionPath ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="fd3ee-103">SelectionPath ControlEvent</span></span>

<span data-ttu-id="fd3ee-104">O [controle SelectionTree](selectiontree-control.md) usa o evento SelectionPath para publicar o caminho para o item realçado.</span><span class="sxs-lookup"><span data-stu-id="fd3ee-104">The [SelectionTree control](selectiontree-control.md) uses the SelectionPath event to publish the path for the highlighted item.</span></span> <span data-ttu-id="fd3ee-105">Se o item for selecionado para ser executado da origem, esse será o caminho da origem.</span><span class="sxs-lookup"><span data-stu-id="fd3ee-105">If the item is selected to run from source, then this is the path of the source.</span></span> <span data-ttu-id="fd3ee-106">Se o item estiver selecionado como ausente, a cadeia de caracteres será a cadeia de caracteres **AbsentPath** da [tabela UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="fd3ee-106">If the item is selected to be absent, then the string is the **AbsentPath** string from the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="fd3ee-107">Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="fd3ee-107">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="fd3ee-108">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="fd3ee-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="fd3ee-109">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fd3ee-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="fd3ee-110">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="fd3ee-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="fd3ee-111">Esse evento só pode afetar controles que estão localizados na mesma caixa de diálogo que o controle SelectionTree.</span><span class="sxs-lookup"><span data-stu-id="fd3ee-111">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="fd3ee-112">Publicada por</span><span class="sxs-lookup"><span data-stu-id="fd3ee-112">Published By</span></span>

[<span data-ttu-id="fd3ee-113">SelectionTree</span><span class="sxs-lookup"><span data-stu-id="fd3ee-113">SelectionTree</span></span>](selectiontree-control.md)

## <a name="argument"></a><span data-ttu-id="fd3ee-114">Argumento</span><span class="sxs-lookup"><span data-stu-id="fd3ee-114">Argument</span></span>

<span data-ttu-id="fd3ee-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="fd3ee-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="fd3ee-116">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="fd3ee-116">Action on Subscribers</span></span>

<span data-ttu-id="fd3ee-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="fd3ee-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="fd3ee-118">Usos comum</span><span class="sxs-lookup"><span data-stu-id="fd3ee-118">Typical Use</span></span>

<span data-ttu-id="fd3ee-119">Um controle de [texto](text-control.md) na mesma caixa de diálogo modal que o SelectionTree deve assinar o evento por meio da [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="fd3ee-119">A [Text](text-control.md) control on the same modal dialog as the SelectionTree should subscribe to the event via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="fd3ee-120">O controle de texto exibe o caminho do item realçado.</span><span class="sxs-lookup"><span data-stu-id="fd3ee-120">The Text Control displays the path of the highlighted item.</span></span>

 

 



