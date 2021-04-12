---
title: Usar OBJID \_ NATIVEOM para expor uma interface nativa para uma janela
description: Essa técnica permite que os clientes obtenham um objeto personalizado para uma janela. Os servidores podem usar isso para expor um ponteiro para um objeto de documento personalizado para uma janela.
ms.assetid: 91713fe5-f03f-464e-88ee-9d8d66d5b19d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c2c5c6ec194ca643475444feb5839c02d3fa890
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/12/2019
ms.locfileid: "104365162"
---
# <a name="use-objid_nativeom-to-expose-a-native-interface-for-a-window"></a><span data-ttu-id="5cc88-104">Usar OBJID \_ NATIVEOM para expor uma interface nativa para uma janela</span><span class="sxs-lookup"><span data-stu-id="5cc88-104">Use OBJID\_NATIVEOM to expose a native interface for a window</span></span>

<span data-ttu-id="5cc88-105">Essa técnica permite que os clientes obtenham um objeto personalizado para uma janela.</span><span class="sxs-lookup"><span data-stu-id="5cc88-105">This technique allows clients to get a custom object for a window.</span></span> <span data-ttu-id="5cc88-106">Os servidores podem usar isso para expor um ponteiro para um objeto de documento personalizado para uma janela.</span><span class="sxs-lookup"><span data-stu-id="5cc88-106">Servers can use this to expose a pointer to a custom document object for a window.</span></span>

<span data-ttu-id="5cc88-107">**Para expor uma interface de modelo de objeto nativo para uma janela (servidores)**</span><span class="sxs-lookup"><span data-stu-id="5cc88-107">**To expose a native object model interface for a window (servers)**</span></span>

1.  <span data-ttu-id="5cc88-108">Manipule a mensagem do [**WM \_ GetObject**](wm-getobject.md) no procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="5cc88-108">Handle the [**WM\_GETOBJECT**](wm-getobject.md) message in the window procedure.</span></span> <span data-ttu-id="5cc88-109">Quando o valor de *lParam* é [**OBJID \_ NATIVEOM**](object-identifiers.md), retorna um ponteiro de interface para o objeto personalizado usando [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span><span class="sxs-lookup"><span data-stu-id="5cc88-109">When the *lParam* value is [**OBJID\_NATIVEOM**](object-identifiers.md), return an interface pointer to the custom object using [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span></span>
2.  <span data-ttu-id="5cc88-110">Libere o ponteiro de interface depois de chamar [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), se apropriado.</span><span class="sxs-lookup"><span data-stu-id="5cc88-110">Release your interface pointer after calling [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), if appropriate.</span></span> <span data-ttu-id="5cc88-111">Para obter mais informações, consulte **LresultFromObject**.</span><span class="sxs-lookup"><span data-stu-id="5cc88-111">For more information, see **LresultFromObject**.</span></span>

<span data-ttu-id="5cc88-112">Os clientes podem obter um ponteiro para esse objeto personalizado.</span><span class="sxs-lookup"><span data-stu-id="5cc88-112">Clients can obtain a pointer to this custom object.</span></span>

<span data-ttu-id="5cc88-113">**Para obter um ponteiro para um objeto personalizado para uma janela (clientes)**</span><span class="sxs-lookup"><span data-stu-id="5cc88-113">**To obtain a pointer for a custom object for a window (clients)**</span></span>

-   <span data-ttu-id="5cc88-114">Chame [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) e passe [**OBJID \_ NATIVEOM**](object-identifiers.md) como o segundo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5cc88-114">Call [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) and pass [**OBJID\_NATIVEOM**](object-identifiers.md) as the second parameter.</span></span>

<span data-ttu-id="5cc88-115">Observe os seguintes problemas para essa técnica:</span><span class="sxs-lookup"><span data-stu-id="5cc88-115">Note the following issues for this technique:</span></span>

-   <span data-ttu-id="5cc88-116">Essa técnica é semelhante a retornar um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , exceto para a ID de objeto usada e o fato de que [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) retorna um objeto personalizado em vez de **IAccessible**.</span><span class="sxs-lookup"><span data-stu-id="5cc88-116">This technique is similar to returning an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer except for the object ID used and the fact that [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) returns a custom object instead of **IAccessible**.</span></span>
-   <span data-ttu-id="5cc88-117">Os desenvolvedores de servidor podem precisar publicar informações que permitam aos clientes identificar exclusivamente o **HWND** para que possam encontrá-lo antes de chamar [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) em seu identificador de janela.</span><span class="sxs-lookup"><span data-stu-id="5cc88-117">Server developers may need to publish information that allows clients to uniquely identify the **HWND** so that they can find it before calling [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) on its window handle.</span></span>
-   <span data-ttu-id="5cc88-118">Não implemente a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) no objeto personalizado que é retornado.</span><span class="sxs-lookup"><span data-stu-id="5cc88-118">Do not implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface on the custom object that is returned.</span></span> <span data-ttu-id="5cc88-119">Se você fizer isso, o OLEACC tratará como uma **IAccessible** padrão e poderá impedir que as interfaces personalizadas sejam usadas.</span><span class="sxs-lookup"><span data-stu-id="5cc88-119">If you do, OLEACC will treat it is as a standard **IAccessible** and may prevent the custom interfaces from being used.</span></span>
-   <span data-ttu-id="5cc88-120">Para ser usado em vários processos, as interfaces no objeto retornado podem precisar ser registradas com Component Object Model (COM).</span><span class="sxs-lookup"><span data-stu-id="5cc88-120">In order to be used across processes, the interfaces on the returned object may need to be registered with Component Object Model (COM).</span></span>

<span data-ttu-id="5cc88-121">Essa técnica é compatível com vários componentes Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="5cc88-121">This technique is supported by several Microsoft Office components.</span></span> <span data-ttu-id="5cc88-122">Para obter mais informações, consulte [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span><span class="sxs-lookup"><span data-stu-id="5cc88-122">For more information, see [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span></span>

 

 




