---
title: Métodos ID2D1RenderTarget PushLayer (D2d1 \_ 1. h)
description: Adiciona a camada especificada ao destino de renderização para que ele receba todas as operações de desenho subsequentes até que PopLayer seja chamado.
ms.assetid: 9336662c-e94e-40ba-adbe-066d704958bc
keywords:
- Métodos PushLayer Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 6a5609192162ae0b0c0e2af8f1b84429d8710509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796278"
---
# <a name="id2d1rendertargetpushlayer-methods"></a><span data-ttu-id="683c6-104">ID2D1RenderTarget: métodos de ushLayer de:P</span><span class="sxs-lookup"><span data-stu-id="683c6-104">ID2D1RenderTarget::PushLayer methods</span></span>

<span data-ttu-id="683c6-105">Adiciona a camada especificada ao destino de renderização para que ele receba todas as operações de desenho subsequentes até que [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="683c6-105">Adds the specified layer to the render target so that it receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span>

### <a name="overload-list"></a><span data-ttu-id="683c6-106">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="683c6-106">Overload list</span></span>



| <span data-ttu-id="683c6-107">Método</span><span class="sxs-lookup"><span data-stu-id="683c6-107">Method</span></span>                                                                                                                            | <span data-ttu-id="683c6-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="683c6-108">Description</span></span>                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="683c6-109">[**PushLayer ( \_ parâmetros de camada D2D1 \_&, ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="683c6-109">[**PushLayer(D2D1\_LAYER\_PARAMETERS&,ID2D1Layer\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))</span></span>  | <span data-ttu-id="683c6-110">Adiciona a camada especificada ao destino de renderização para que ele receba todas as operações de desenho subsequentes até que [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="683c6-110">Adds the specified layer to the render target so that it receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span> <br/> |
| <span data-ttu-id="683c6-111">[**PushLayer ( \_ parâmetros da camada d2d1 \_ \* , ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="683c6-111">[**PushLayer(D2D1\_LAYER\_PARAMETERS\*,ID2D1Layer\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer))</span></span> | <span data-ttu-id="683c6-112">Adiciona a camada especificada ao destino de renderização para que ele receba todas as operações de desenho subsequentes até que [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="683c6-112">Adds the specified layer to the render target so that it receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="683c6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="683c6-113">Remarks</span></span>

<span data-ttu-id="683c6-114">O método [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) permite que um chamador comece a redirecionar a renderização para uma camada.</span><span class="sxs-lookup"><span data-stu-id="683c6-114">The [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method enables a caller to begin redirecting rendering to a layer.</span></span> <span data-ttu-id="683c6-115">Todas as operações de renderização são válidas em uma camada.</span><span class="sxs-lookup"><span data-stu-id="683c6-115">All rendering operations are valid in a layer.</span></span> <span data-ttu-id="683c6-116">O local da camada é afetado pelo conjunto de transformação mundial no destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="683c6-116">The location of the layer is affected by the world transform set on the render target.</span></span>

<span data-ttu-id="683c6-117">Cada **PushLayer** deve ter uma chamada [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) correspondente.</span><span class="sxs-lookup"><span data-stu-id="683c6-117">Each **PushLayer** must have a matching [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) call.</span></span> <span data-ttu-id="683c6-118">Se houver mais chamadas **PopLayer** que chamadas **PushLayer** , o destino de renderização será colocado em um estado de erro.</span><span class="sxs-lookup"><span data-stu-id="683c6-118">If there are more **PopLayer** calls than **PushLayer** calls, the render target is placed into an error state.</span></span> <span data-ttu-id="683c6-119">Se a [**liberação**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) for chamada antes que todas as camadas pendentes sejam retiradas, o destino de renderização será colocado em um estado de erro e um erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="683c6-119">If [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called before all outstanding layers are popped, the render target is placed into an error state, and an error is returned.</span></span> <span data-ttu-id="683c6-120">O estado de erro pode ser limpo por uma chamada para [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span><span class="sxs-lookup"><span data-stu-id="683c6-120">The error state can be cleared by a call to [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span>

<span data-ttu-id="683c6-121">Um recurso [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) específico pode estar ativo apenas uma vez.</span><span class="sxs-lookup"><span data-stu-id="683c6-121">A particular [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) resource can be active only at one time.</span></span> <span data-ttu-id="683c6-122">Em outras palavras, você não pode chamar um método [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) e, em seguida, seguir imediatamente com outro método **PushLayer** com o mesmo recurso de camada.</span><span class="sxs-lookup"><span data-stu-id="683c6-122">In other words, you cannot call a [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method, and then immediately follow with another **PushLayer** method with the same layer resource.</span></span> <span data-ttu-id="683c6-123">Em vez disso, você deve chamar o segundo método **PushLayer** com recursos de camada diferentes.</span><span class="sxs-lookup"><span data-stu-id="683c6-123">Instead, you must call the second **PushLayer** method with different layer resources.</span></span>

<span data-ttu-id="683c6-124">Para obter um exemplo, consulte [como cortar uma região com camadas](how-to-clip-with-layers.md).</span><span class="sxs-lookup"><span data-stu-id="683c6-124">For an example, see [How to Clip a Region with Layers](how-to-clip-with-layers.md).</span></span>

<span data-ttu-id="683c6-125">Esse método não retornará um código de erro se ele falhar.</span><span class="sxs-lookup"><span data-stu-id="683c6-125">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="683c6-126">Para determinar se uma operação de desenho (como **PushLayer**) falhou, verifique o resultado retornado pelos métodos [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget:: flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .</span><span class="sxs-lookup"><span data-stu-id="683c6-126">To determine whether a drawing operation (such as **PushLayer**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="683c6-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="683c6-127">Examples</span></span>

<span data-ttu-id="683c6-128">O exemplo a seguir usa uma camada para recortar um bitmap para uma máscara geométrica.</span><span class="sxs-lookup"><span data-stu-id="683c6-128">The following example uses a layer to clip a bitmap to a geometric mask.</span></span> <span data-ttu-id="683c6-129">Para obter o exemplo completo, consulte [como recortar para uma máscara geométrica](how-to-clip-with-layers.md).</span><span class="sxs-lookup"><span data-stu-id="683c6-129">For the complete example, see [How to Clip to a Geometric Mask](how-to-clip-with-layers.md).</span></span>


```C++
HRESULT DemoApp::RenderWithLayer(ID2D1RenderTarget *pRT)
{
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &amp;pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(350, 50));

        // Push the layer with the geometric mask.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );
            
  
        pRT->DrawBitmap(m_pOrigBitmap, D2D1::RectF(0, 0, 200, 133));
        pRT->FillRectangle(D2D1::RectF(0.f, 0.f, 25.f, 25.f), m_pSolidColorBrush);  
        pRT->FillRectangle(D2D1::RectF(25.f, 25.f, 50.f, 50.f), m_pSolidColorBrush);
        pRT->FillRectangle(D2D1::RectF(50.f, 50.f, 75.f, 75.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(75.f, 75.f, 100.f, 100.f), m_pSolidColorBrush);    
        pRT->FillRectangle(D2D1::RectF(100.f, 100.f, 125.f, 125.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(125.f, 125.f, 150.f, 150.f), m_pSolidColorBrush);    
        

        pRT->PopLayer();
    }

    SafeRelease(&amp;pLayer);

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="683c6-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="683c6-130">Requirements</span></span>



| <span data-ttu-id="683c6-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="683c6-131">Requirement</span></span> | <span data-ttu-id="683c6-132">Valor</span><span class="sxs-lookup"><span data-stu-id="683c6-132">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="683c6-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="683c6-133">Header</span></span><br/>  | <dl> <span data-ttu-id="683c6-134"><dt>D2d1 \_ 1. h (inclui D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="683c6-134"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="683c6-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="683c6-135">Library</span></span><br/> | <dl> <span data-ttu-id="683c6-136"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="683c6-136"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="683c6-137">DLL</span><span class="sxs-lookup"><span data-stu-id="683c6-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="683c6-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="683c6-138"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="683c6-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="683c6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="683c6-140">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="683c6-140">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="683c6-141">Visão geral de camadas</span><span class="sxs-lookup"><span data-stu-id="683c6-141">Layers Overview</span></span>](direct2d-layers-overview.md)
</dt> </dl>

<span data-ttu-id="683c6-142">�</span><span class="sxs-lookup"><span data-stu-id="683c6-142">�</span></span>

<span data-ttu-id="683c6-143">�</span><span class="sxs-lookup"><span data-stu-id="683c6-143">�</span></span>
