---
description: O controle SelectionTree usa o evento SelectionNoItems para excluir texto de descrição de item obsoleto ou para desabilitar botões que se tornaram inúteis. Esse evento deve ser criado na tabela EventMappings.
ms.assetid: a79abd77-a6e5-4a1f-8a63-51644151404a
title: SelectionNoItems ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6544dfcaad3d22b63d71703ea95d1aa4f09a1efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749573"
---
# <a name="selectionnoitems-controlevent"></a><span data-ttu-id="13adb-104">SelectionNoItems ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="13adb-104">SelectionNoItems ControlEvent</span></span>

<span data-ttu-id="13adb-105">O [controle SelectionTree](selectiontree-control.md) usa o evento SelectionNoItems para excluir texto de descrição de item obsoleto ou para desabilitar botões que se tornaram inúteis.</span><span class="sxs-lookup"><span data-stu-id="13adb-105">The [SelectionTree control](selectiontree-control.md) uses the SelectionNoItems event to delete obsolete item description text or to disable buttons that have become useless.</span></span> <span data-ttu-id="13adb-106">Esse evento deve ser criado na [tabela EventMappings](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="13adb-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="13adb-107">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="13adb-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="13adb-108">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="13adb-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="13adb-109">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="13adb-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="13adb-110">Esse evento só pode afetar controles que estão localizados na mesma caixa de diálogo que o controle SelectionTree.</span><span class="sxs-lookup"><span data-stu-id="13adb-110">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="13adb-111">Publicada por</span><span class="sxs-lookup"><span data-stu-id="13adb-111">Published By</span></span>

<span data-ttu-id="13adb-112">[SelectionTree controle](selectiontree-control.md) se a seleção não tiver nós.</span><span class="sxs-lookup"><span data-stu-id="13adb-112">[SelectionTree control](selectiontree-control.md) if the selection has no nodes.</span></span>

## <a name="argument"></a><span data-ttu-id="13adb-113">Argumento</span><span class="sxs-lookup"><span data-stu-id="13adb-113">Argument</span></span>

<span data-ttu-id="13adb-114">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="13adb-114">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="13adb-115">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="13adb-115">Action on Subscribers</span></span>

<span data-ttu-id="13adb-116">Exclui o texto de descrição do item obsoleto ou desabilita os botões obsoletos.</span><span class="sxs-lookup"><span data-stu-id="13adb-116">Deletes obsolete item description text or disables obsolete buttons.</span></span>

## <a name="typical-use"></a><span data-ttu-id="13adb-117">Usos comum</span><span class="sxs-lookup"><span data-stu-id="13adb-117">Typical Use</span></span>

<span data-ttu-id="13adb-118">Pode ser usado para desabilitar os botões Avançar, redefinir e DiskCost na caixa de [diálogo de seleção](selection-dialog.md) quando uma seleção não tem nós e esses botões se tornam inúteis.</span><span class="sxs-lookup"><span data-stu-id="13adb-118">May be used to disable the Next, Reset, and DiskCost buttons on the [Selection Dialog](selection-dialog.md) when a selection has no nodes and these buttons become useless.</span></span>

 

 



