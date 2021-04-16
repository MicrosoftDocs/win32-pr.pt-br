---
description: O evento ValidateProductID define a propriedade ProductID como a ID do produto completo. Se a validação não for bem-sucedida, esse evento colocará uma mensagem de erro e uma caixa de diálogo modal para uma entrada de usuário da ID do produto.
ms.assetid: 44002cae-154a-4938-a15c-456c293e94fb
title: ValidateProductID ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b86cacfc4561fe9e4d94436724b42a78d3d8792
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754335"
---
# <a name="validateproductid-controlevent"></a><span data-ttu-id="9ba38-104">ValidateProductID ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="9ba38-104">ValidateProductID ControlEvent</span></span>

<span data-ttu-id="9ba38-105">O evento ValidateProductID define a propriedade [**ProductID**](productid.md) como a ID do produto completo.</span><span class="sxs-lookup"><span data-stu-id="9ba38-105">The ValidateProductID event sets the [**ProductID**](productid.md) property to the full Product ID.</span></span> <span data-ttu-id="9ba38-106">Se a validação não for bem-sucedida, esse evento colocará uma mensagem de erro e uma caixa de diálogo modal para uma entrada de usuário da ID do produto.</span><span class="sxs-lookup"><span data-stu-id="9ba38-106">If the validation is unsuccessful, then this event puts up an error message and modal dialog box for a user entry of the Product ID.</span></span>

<span data-ttu-id="9ba38-107">Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md)ou um [controle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="9ba38-107">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="9ba38-108">Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="9ba38-108">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="9ba38-109">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="9ba38-109">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="9ba38-110">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9ba38-110">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="9ba38-111">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="9ba38-111">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="9ba38-112">Publicada por</span><span class="sxs-lookup"><span data-stu-id="9ba38-112">Published By</span></span>

<span data-ttu-id="9ba38-113">Esse ControlEvent, é publicado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="9ba38-113">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="9ba38-114">Argumento</span><span class="sxs-lookup"><span data-stu-id="9ba38-114">Argument</span></span>

<span data-ttu-id="9ba38-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="9ba38-115">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="9ba38-116">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="9ba38-116">Action on Subscribers</span></span>

<span data-ttu-id="9ba38-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="9ba38-117">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="9ba38-118">Usos comum</span><span class="sxs-lookup"><span data-stu-id="9ba38-118">Typical Use</span></span>

<span data-ttu-id="9ba38-119">Um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo modal está vinculado a esse evento e é usado para verificar a entrada do usuário da ID do produto.</span><span class="sxs-lookup"><span data-stu-id="9ba38-119">A [PushButton](pushbutton-control.md) control on a modal dialog box is tied to this event and is used to check the user's entry of the Product ID.</span></span> <span data-ttu-id="9ba38-120">Se a entrada do usuário for válida, a próxima caixa de diálogo será aberta.</span><span class="sxs-lookup"><span data-stu-id="9ba38-120">If the user's entry is valid, then the next dialog box will open.</span></span>

 

 



