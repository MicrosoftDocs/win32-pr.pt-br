---
title: Recuperando um objeto IAccessible
description: O Microsoft Acessibilidade Ativa fornece funções como AccessibleObjectFromWindow e AccessibleObjectFromPoint que permitem aos clientes recuperar objetos acessíveis.
ms.assetid: 971cbead-128b-465a-8e77-2a20217f8d0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89237916597f27c7179fce9516df1e0ecf43a6db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291887"
---
# <a name="retrieving-an-iaccessible-object"></a><span data-ttu-id="40cca-103">Recuperando um objeto IAccessible</span><span class="sxs-lookup"><span data-stu-id="40cca-103">Retrieving an IAccessible Object</span></span>

<span data-ttu-id="40cca-104">O Microsoft Acessibilidade Ativa fornece funções como [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) e [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) que permitem aos clientes recuperar objetos acessíveis.</span><span class="sxs-lookup"><span data-stu-id="40cca-104">Microsoft Active Accessibility provides functions such as [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) and [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) that allow clients to retrieve accessible objects.</span></span> <span data-ttu-id="40cca-105">Essas funções retornam um ponteiro de interface [**IDispatch**](idispatch-interface.md) ou [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) por meio do qual os clientes obtêm informações sobre o objeto acessível.</span><span class="sxs-lookup"><span data-stu-id="40cca-105">These functions return either an [**IDispatch**](idispatch-interface.md) or [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer through which clients get information about the accessible object.</span></span>

<span data-ttu-id="40cca-106">Quando um cliente chama [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) ou qualquer uma das outras funções \**AccessibleObjectFrom \* \* \* X* que recuperam uma interface para um objeto, o Microsoft acessibilidade ativa envia a mensagem da janela do [**WM \_ GetObject**](wm-getobject.md) para o procedimento de janela aplicável no aplicativo apropriado.</span><span class="sxs-lookup"><span data-stu-id="40cca-106">When a client calls [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) or any of the other \**AccessibleObjectFrom\*\*\*X* functions that retrieve an interface to an object, Microsoft Active Accessibility sends the [**WM\_GETOBJECT**](wm-getobject.md) window message to the applicable window procedure within the appropriate application.</span></span> <span data-ttu-id="40cca-107">Para fornecer informações aos clientes, os servidores devem responder à mensagem do **WM \_ GetObject** .</span><span class="sxs-lookup"><span data-stu-id="40cca-107">To provide information to clients, servers must respond to the **WM\_GETOBJECT** message.</span></span>

<span data-ttu-id="40cca-108">Para coletar informações específicas sobre um elemento de interface do usuário, os clientes devem primeiro recuperar uma interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para o elemento.</span><span class="sxs-lookup"><span data-stu-id="40cca-108">To collect specific information about a UI element, clients must first retrieve an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for the element.</span></span> <span data-ttu-id="40cca-109">Para recuperar o objeto **IAccessible** de um elemento, os clientes podem usar uma das seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="40cca-109">To retrieve an element's **IAccessible** object, clients can use one of the following functions:</span></span>

-   [<span data-ttu-id="40cca-110">**AccessibleObjectFromPoint**</span><span class="sxs-lookup"><span data-stu-id="40cca-110">**AccessibleObjectFromPoint**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [<span data-ttu-id="40cca-111">**AccessibleObjectFromWindow**</span><span class="sxs-lookup"><span data-stu-id="40cca-111">**AccessibleObjectFromWindow**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [<span data-ttu-id="40cca-112">**AccessibleObjectFromEvent**</span><span class="sxs-lookup"><span data-stu-id="40cca-112">**AccessibleObjectFromEvent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)

<span data-ttu-id="40cca-113">**Para recuperar um ponteiro de interface IAccessible**</span><span class="sxs-lookup"><span data-stu-id="40cca-113">**To retrieve an IAccessible Interface Pointer**</span></span>

1.  <span data-ttu-id="40cca-114">O cliente chama uma das funções \*\*AccessibleObjectFrom \*\* \* \* X.</span><span class="sxs-lookup"><span data-stu-id="40cca-114">Client calls one of the \**AccessibleObjectFrom\*\*\*X* functions.</span></span>
2.  <span data-ttu-id="40cca-115">Oleacc.dll envia uma mensagem do [**WM \_ GetObject**](wm-getobject.md) para o servidor.</span><span class="sxs-lookup"><span data-stu-id="40cca-115">Oleacc.dll sends a [**WM\_GETOBJECT**](wm-getobject.md) message to server.</span></span>
3.  <span data-ttu-id="40cca-116">O servidor determina qual elemento de interface do usuário corresponde à solicitação.</span><span class="sxs-lookup"><span data-stu-id="40cca-116">The server determines which UI element corresponds to the request.</span></span>
4.  <span data-ttu-id="40cca-117">O servidor retorna zero para solicitar um proxy de Oleacc.dll,</span><span class="sxs-lookup"><span data-stu-id="40cca-117">The server either returns zero to request an Oleacc.dll proxy,</span></span>

    <span data-ttu-id="40cca-118">Ou</span><span class="sxs-lookup"><span data-stu-id="40cca-118">Or</span></span>

    <span data-ttu-id="40cca-119">Retorna um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (implementação nativa).</span><span class="sxs-lookup"><span data-stu-id="40cca-119">Returns an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object (native implementation).</span></span> <span data-ttu-id="40cca-120">Para fazer isso, ele:</span><span class="sxs-lookup"><span data-stu-id="40cca-120">To do this, it:</span></span>

    -   <span data-ttu-id="40cca-121">Constrói um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para o elemento.</span><span class="sxs-lookup"><span data-stu-id="40cca-121">Constructs an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for the element.</span></span>
    -   <span data-ttu-id="40cca-122">Chama [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) para realizar marshaling do ponteiro do objeto.</span><span class="sxs-lookup"><span data-stu-id="40cca-122">Calls [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) to marshal the object's pointer.</span></span>
    -   <span data-ttu-id="40cca-123">Retorna o LRESULT para Oleacc.dll.</span><span class="sxs-lookup"><span data-stu-id="40cca-123">Returns the LRESULT to Oleacc.dll.</span></span>

5.  <span data-ttu-id="40cca-124">Oleacc.dll examina o valor de retorno do [**WM \_ GetObject**](wm-getobject.md).</span><span class="sxs-lookup"><span data-stu-id="40cca-124">Oleacc.dll examines the return value from [**WM\_GETOBJECT**](wm-getobject.md).</span></span>

    <span data-ttu-id="40cca-125">Se for zero, Oleacc.dll construirá um objeto proxy e o retornará ao cliente.</span><span class="sxs-lookup"><span data-stu-id="40cca-125">If it is zero, Oleacc.dll constructs a proxy object and returns it to the client.</span></span>

    <span data-ttu-id="40cca-126">Ou</span><span class="sxs-lookup"><span data-stu-id="40cca-126">Or</span></span>

    <span data-ttu-id="40cca-127">Se ele for diferente de zero, Oleacc.dll chamará [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult) para desempacotar o ponteiro do objeto do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativo e retorne-o para o cliente.</span><span class="sxs-lookup"><span data-stu-id="40cca-127">If it is nonzero, Oleacc.dll calls [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult) to unmarshal the native [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object pointer and returns it to the client.</span></span>

 

 




