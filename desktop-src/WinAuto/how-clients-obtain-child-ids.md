---
title: Como os clientes obtêm IDs filho
description: Como os clientes obtêm IDs filho
ms.assetid: 8e5786fe-5123-4262-b0b8-5c9aff4787bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a67322a80a00c7cc65463ef50e5d1b470fc0b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641205"
---
# <a name="how-clients-obtain-child-ids"></a><span data-ttu-id="95996-103">Como os clientes obtêm IDs filho</span><span class="sxs-lookup"><span data-stu-id="95996-103">How Clients Obtain Child IDs</span></span>

<span data-ttu-id="95996-104">Os desenvolvedores de cliente podem obter a ID filho de um objeto das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="95996-104">Client developers can get an object's child ID in the following ways:</span></span>

-   <span data-ttu-id="95996-105">Chame [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren).</span><span class="sxs-lookup"><span data-stu-id="95996-105">Call [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren).</span></span> <span data-ttu-id="95996-106">Essa função recupera uma matriz de estruturas [**Variant**](variant-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="95996-106">This function retrieves an array of [**VARIANT**](variant-structure.md) structures.</span></span>
-   <span data-ttu-id="95996-107">Consulte o objeto para ver se ele dá suporte à interface [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="95996-107">Query the object to see if it supports the [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) interface.</span></span> <span data-ttu-id="95996-108">Se estiver presente, use [**IEnumVARIANT:: Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) obter IDs filho.</span><span class="sxs-lookup"><span data-stu-id="95996-108">If it is present, use [**IEnumVARIANT::Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) obtain child IDs.</span></span>
-   <span data-ttu-id="95996-109">Colete as IDs filho chamando o método [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) do objeto pai.</span><span class="sxs-lookup"><span data-stu-id="95996-109">Collect the child IDs by calling the parent object's [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) method.</span></span>

> [!Note]  
> <span data-ttu-id="95996-110">É responsabilidade do cliente liberar a memória usada para as estruturas de [**variante**](variant-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="95996-110">It is the responsibility of the client to free the memory used for the [**VARIANT**](variant-structure.md) structures.</span></span> <span data-ttu-id="95996-111">Os clientes também devem chamar [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) em qualquer interface [**IDispatch**](idispatch-interface.md) retornada.</span><span class="sxs-lookup"><span data-stu-id="95996-111">Clients also must call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on any [**IDispatch**](idispatch-interface.md) interface that is returned.</span></span>

 

 

 