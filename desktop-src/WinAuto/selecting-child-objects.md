---
title: Selecionando objetos filho
description: Os clientes chamam o método accSelect IAccessible para modificar a seleção ou o foco do teclado entre os filhos em um objeto. As constantes SELFLAG especificadas com a chamada definem a operação a ser executada.
ms.assetid: 5e7ad1e9-b1b2-4e76-93e8-b58251930621
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d6f898f7da7beb047d3e781ad46cf383b3dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291917"
---
# <a name="selecting-child-objects"></a><span data-ttu-id="0d150-104">Selecionando objetos filho</span><span class="sxs-lookup"><span data-stu-id="0d150-104">Selecting Child Objects</span></span>

<span data-ttu-id="0d150-105">Os clientes chamam o método [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) para modificar a seleção ou o foco do teclado entre os filhos em um objeto.</span><span class="sxs-lookup"><span data-stu-id="0d150-105">Clients call the [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) method to modify selection or keyboard focus among the children in an object.</span></span> <span data-ttu-id="0d150-106">As [constantes SELFLAG](selflag.md) especificadas com a chamada definem a operação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="0d150-106">The [SELFLAG Constants](selflag.md) specified with the call define the operation to perform.</span></span>

<span data-ttu-id="0d150-107">Se [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) for chamado com o sinalizador [**SELFLAG \_ TAKEFOCUS**](selflag.md) em um objeto filho que tem um **HWND**, o sinalizador terá efeito somente se o pai do objeto tiver o foco.</span><span class="sxs-lookup"><span data-stu-id="0d150-107">If [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) is called with the [**SELFLAG\_TAKEFOCUS**](selflag.md) flag on a child object that has an **HWND**, the flag takes effect only if the object's parent has the focus.</span></span>

## <a name="performing-complex-selection-operations"></a><span data-ttu-id="0d150-108">Executando operações de seleção complexas</span><span class="sxs-lookup"><span data-stu-id="0d150-108">Performing Complex Selection Operations</span></span>

<span data-ttu-id="0d150-109">O seguinte descreve quais valores de SELFLAG especificar ao chamar [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) para executar operações de seleção complexas.</span><span class="sxs-lookup"><span data-stu-id="0d150-109">The following describes which SELFLAG values to specify when calling [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) to perform complex selection operations.</span></span>

<span data-ttu-id="0d150-110">**Para simular um clique**</span><span class="sxs-lookup"><span data-stu-id="0d150-110">**To simulate a click**</span></span>

-   <span data-ttu-id="0d150-111">[**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ TAKESELECTION**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="0d150-111">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_TAKESELECTION**](selflag.md)</span></span>

<span data-ttu-id="0d150-112">**Para selecionar um item de destino simulando CTRL + clique**</span><span class="sxs-lookup"><span data-stu-id="0d150-112">**To select a target item by simulating CTRL + click**</span></span>

-   <span data-ttu-id="0d150-113">[**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ addseleções**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="0d150-113">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_ADDSELECTION**](selflag.md)</span></span>

<span data-ttu-id="0d150-114">**Para cancelar a seleção de um item de destino simulando CTRL + clique**</span><span class="sxs-lookup"><span data-stu-id="0d150-114">**To cancel selection of a target item by simulating CTRL + click**</span></span>

-   <span data-ttu-id="0d150-115">[**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ REMOVESELECTION**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="0d150-115">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_REMOVESELECTION**](selflag.md)</span></span>

<span data-ttu-id="0d150-116">**Para simular SHIFT + clique**</span><span class="sxs-lookup"><span data-stu-id="0d150-116">**To simulate SHIFT + click**</span></span>

-   <span data-ttu-id="0d150-117">[**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ EXTENDSELECTION**](selflag.md)</span><span class="sxs-lookup"><span data-stu-id="0d150-117">[**SELFLAG\_TAKEFOCUS**](selflag.md) \| [**SELFLAG\_EXTENDSELECTION**](selflag.md)</span></span>

<span data-ttu-id="0d150-118">**Para selecionar um intervalo de objetos e colocar o foco no último objeto**</span><span class="sxs-lookup"><span data-stu-id="0d150-118">**To select a range of objects and put focus on the last object**</span></span>

1.  <span data-ttu-id="0d150-119">Especifique [**SELFLAG \_ TAKEFOCUS**](selflag.md) no objeto inicial para definir a âncora de seleção.</span><span class="sxs-lookup"><span data-stu-id="0d150-119">Specify [**SELFLAG\_TAKEFOCUS**](selflag.md) on the starting object to set the selection anchor.</span></span>
2.  <span data-ttu-id="0d150-120">Chame [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) novamente e especifique [**SELFLAG \_ EXTENDSELECTION**](selflag.md) \| [**SELFLAG \_ TAKEFOCUS**](selflag.md) no último objeto.</span><span class="sxs-lookup"><span data-stu-id="0d150-120">Call [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) again and specify [**SELFLAG\_EXTENDSELECTION**](selflag.md) \| [**SELFLAG\_TAKEFOCUS**](selflag.md) on the last object.</span></span>

<span data-ttu-id="0d150-121">**Para desmarcar todos os objetos**</span><span class="sxs-lookup"><span data-stu-id="0d150-121">**To deselect all objects**</span></span>

1.  <span data-ttu-id="0d150-122">Especifique [**SELFLAG \_ TAKESELECTION**](selflag.md) em qualquer objeto.</span><span class="sxs-lookup"><span data-stu-id="0d150-122">Specify [**SELFLAG\_TAKESELECTION**](selflag.md) on any object.</span></span> <span data-ttu-id="0d150-123">Esse sinalizador anula a seleção de todos os objetos selecionados, exceto aquele selecionado.</span><span class="sxs-lookup"><span data-stu-id="0d150-123">This flag deselects all selected objects except the one just selected.</span></span>
2.  <span data-ttu-id="0d150-124">Chame [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) novamente e especifique [**SELFLAG \_ REMOVESELECTION**](selflag.md) no objeto restante.</span><span class="sxs-lookup"><span data-stu-id="0d150-124">Call [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) again and specify [**SELFLAG\_REMOVESELECTION**](selflag.md) on the remaining object.</span></span>

 

 




