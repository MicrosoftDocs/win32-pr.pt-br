---
description: A caixa de diálogo é redefinida. Em outras palavras, todos os controles na caixa de diálogo são chamados para desfazer as alterações de propriedade que eles executaram. Esse evento redefine todos os valores de propriedade para o que eles eram quando a caixa de diálogo foi criada.
ms.assetid: 6449abb8-54cb-4400-9eb2-b7e7f1564747
title: Redefinir ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 889f1b0f984f14b7522707db4ffbd958bff9c32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755074"
---
# <a name="reset-controlevent"></a><span data-ttu-id="d2bda-105">Redefinir ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="d2bda-105">Reset ControlEvent</span></span>

<span data-ttu-id="d2bda-106">A caixa de diálogo é redefinida.</span><span class="sxs-lookup"><span data-stu-id="d2bda-106">The dialog box is reset.</span></span> <span data-ttu-id="d2bda-107">Em outras palavras, todos os controles na caixa de diálogo são chamados para desfazer as alterações de propriedade que eles executaram.</span><span class="sxs-lookup"><span data-stu-id="d2bda-107">In other words, all the controls on the dialog box are called to undo the property changes they have performed.</span></span> <span data-ttu-id="d2bda-108">Esse evento redefine todos os valores de propriedade para o que eles eram quando a caixa de diálogo foi criada.</span><span class="sxs-lookup"><span data-stu-id="d2bda-108">This event resets all the property values to what they were when the dialog box was created.</span></span>

<span data-ttu-id="d2bda-109">Esse evento pode ser publicado por um [controle de pressão](pushbutton-control.md)ou um [controle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="d2bda-109">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="d2bda-110">Esse evento deve ser criado na [tabela ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="d2bda-110">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="d2bda-111">Este ControlEvent, requer que a interface do usuário seja executada no nível [*completo da interface do*](f-gly.md) usuário.</span><span class="sxs-lookup"><span data-stu-id="d2bda-111">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="d2bda-112">Esse evento não funcionará com uma interface [*do usuário reduzida*](r-gly.md) ou uma [*interface do usuário básica*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d2bda-112">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="d2bda-113">Para obter informações, consulte [níveis de interface do usuário](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="d2bda-113">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="d2bda-114">Há um caso, o que deve ocorrer raramente na prática, que não é tratado corretamente por esse ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="d2bda-114">There is a case, which should occur rarely in practice, that is not handled properly by this ControlEvent.</span></span> <span data-ttu-id="d2bda-115">Se houver dois ou mais controles na mesma caixa de diálogo vinculado indiretamente à mesma propriedade e pelo menos um deles começar a ter alguma outra propriedade, esse valor de propriedade, às vezes, será redefinido para seu segundo valor.</span><span class="sxs-lookup"><span data-stu-id="d2bda-115">If there are two or more controls on the same dialog box linked indirectly to the same property and at least one of them started having some other property, then this property value will sometimes be reset to its second value.</span></span>

## <a name="published-by"></a><span data-ttu-id="d2bda-116">Publicada por</span><span class="sxs-lookup"><span data-stu-id="d2bda-116">Published By</span></span>

<span data-ttu-id="d2bda-117">Esse ControlEvent, é publicado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="d2bda-117">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="d2bda-118">Argumento</span><span class="sxs-lookup"><span data-stu-id="d2bda-118">Argument</span></span>

<span data-ttu-id="d2bda-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d2bda-119">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="d2bda-120">Ação nos assinantes</span><span class="sxs-lookup"><span data-stu-id="d2bda-120">Action on Subscribers</span></span>

<span data-ttu-id="d2bda-121">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d2bda-121">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="d2bda-122">Usos comum</span><span class="sxs-lookup"><span data-stu-id="d2bda-122">Typical Use</span></span>

<span data-ttu-id="d2bda-123">Um controle de [pressão](pushbutton-control.md) em uma caixa de diálogo modal é usado para redefinir todos os valores na caixa de diálogo e para cancelar todas as alterações na página.</span><span class="sxs-lookup"><span data-stu-id="d2bda-123">A [PushButton](pushbutton-control.md) control on a modal dialog box is used to reset all the values on the dialog box and to cancel all the changes on the page.</span></span>

 

 



