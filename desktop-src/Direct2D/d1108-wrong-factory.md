---
title: Fábrica incorreta D1108
ms.assetid: eb851118-0541-4c9a-a22d-b98f041852bb
description: O recurso foi alocado pela fábrica 1 e usado com a fábrica 2.
keywords:
- D1108 de fábrica incorreta Direct2D
topic_type:
- apiref
api_name:
- D1108 Wrong Factory
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 17c58c72a56af8c480a176259d9fbcb9df586942
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/27/2021
ms.locfileid: "105748682"
---
# <a name="d1108-wrong-factory"></a><span data-ttu-id="3762f-104">D1108: fábrica incorreta</span><span class="sxs-lookup"><span data-stu-id="3762f-104">D1108: Wrong Factory</span></span>

<span data-ttu-id="3762f-105">O recurso \[ *de recurso* \] foi alocado pela \[ *fábrica 1* de fábrica \] e usado com a fábrica de fábrica \[ *2* \] .</span><span class="sxs-lookup"><span data-stu-id="3762f-105">The resource \[*resource*\] was allocated by factory \[*factory 1*\] and used with factory \[*factory 2*\].</span></span>

## <a name="placeholders"></a><span data-ttu-id="3762f-106">Espaços reservados</span><span class="sxs-lookup"><span data-stu-id="3762f-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="3762f-107"><span id="resource"></span><span id="RESOURCE"></span>*Kit*</span><span class="sxs-lookup"><span data-stu-id="3762f-107"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="3762f-108">O endereço da interface.</span><span class="sxs-lookup"><span data-stu-id="3762f-108">The address of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="3762f-109"><span id="factory_1"></span><span id="FACTORY_1"></span>*fábrica 1*</span><span class="sxs-lookup"><span data-stu-id="3762f-109"><span id="factory_1"></span><span id="FACTORY_1"></span>*factory 1*</span></span>
</dt> <dd>

<span data-ttu-id="3762f-110">O endereço da fábrica que alocou o *recurso*.</span><span class="sxs-lookup"><span data-stu-id="3762f-110">The address of the factory that allocated *resource*.</span></span>

</dd> <dt>

<span data-ttu-id="3762f-111"><span id="factory_2"></span><span id="FACTORY_2"></span>*fábrica 2*</span><span class="sxs-lookup"><span data-stu-id="3762f-111"><span id="factory_2"></span><span id="FACTORY_2"></span>*factory 2*</span></span>
</dt> <dd>

<span data-ttu-id="3762f-112">O endereço da fábrica com o qual o *recurso* foi usado.</span><span class="sxs-lookup"><span data-stu-id="3762f-112">The address of the factory with which *resource* was used.</span></span>

</dd> </dl> 




 

## <a name="examples"></a><span data-ttu-id="3762f-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3762f-113">Examples</span></span>

<span data-ttu-id="3762f-114">O exemplo a seguir cria primeiro dois objetos [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) habilitados para depuração; em seguida, ele cria uma geometria da primeira fábrica e um pincel da segunda fábrica.</span><span class="sxs-lookup"><span data-stu-id="3762f-114">The following example first creates two debug-enabled [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) objects; it then creates a geometry from the first factory, and a brush from the second factory.</span></span> <span data-ttu-id="3762f-115">Por fim, ele chama [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry), passando a geometria e o pincel.</span><span class="sxs-lookup"><span data-stu-id="3762f-115">Lastly, it calls [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry), passing in the geometry and the brush.</span></span>


```C++
        // If you set the options.debugLevel to D2D1_DEBUG_LEVEL_NONE,
        // the debug layer is not enabled.
#if defined(DEBUG) || defined(_DEBUG)
        D2D1_FACTORY_OPTIONS options;
        options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;

        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            options,
            &m_pD2DFactory
            );
#else
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            &m_pD2DFactory
            );
#endif


        // Domain violation. Create a second Direct2D factory.
        options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            options,
            &m_pD2DFactory1
            );

        // Create a geometry from the second factory.
        hr = m_pD2DFactory1->CreateRectangleGeometry(
            D2D1::RectF(100, 50, 400, 160),
            &m_pRectangleGeometry
            );
```



<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3762f-116">C++</span><span class="sxs-lookup"><span data-stu-id="3762f-116">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>        // Create a render target from the first factory.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );</code></pre></td>
</tr>
</tbody>
</table>

<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3762f-117">C++</span><span class="sxs-lookup"><span data-stu-id="3762f-117">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>        if (SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->CreateSolidColorBrush(
                D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
                &m_pBlackBrush
                );
        }</code></pre></td>
</tr>
</tbody>
</table>

<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3762f-118">C++</span><span class="sxs-lookup"><span data-stu-id="3762f-118">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>        m_pRenderTarget->FillGeometry(
            m_pRectangleGeometry,   //The rectangle geometry created from the second factory.
            m_pBlackBrush   //The black brush created from the first factory.
            );</code></pre></td>
</tr>
</tbody>
</table>



<span data-ttu-id="3762f-119">Este exemplo produz a seguinte mensagem de depuração:</span><span class="sxs-lookup"><span data-stu-id="3762f-119">This example produces the following debug message:</span></span>


```
 D2D DEBUG ERROR - The resource [003BD628] was allocated 
by factory [002ED698] and used with factory [002ED470].
```



## <a name="possible-causes"></a><span data-ttu-id="3762f-120">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="3762f-120">Possible Causes</span></span>

<span data-ttu-id="3762f-121">Uso de recurso inválido.</span><span class="sxs-lookup"><span data-stu-id="3762f-121">Invalid resource usage.</span></span> <span data-ttu-id="3762f-122">Um recurso alocado por uma fábrica foi usado com outra fábrica.</span><span class="sxs-lookup"><span data-stu-id="3762f-122">A resource allocated by one factory was used with another factory.</span></span>

 

 
