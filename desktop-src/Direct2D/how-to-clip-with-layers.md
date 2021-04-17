---
title: Como recortar para uma máscara geométrica
description: Mostra como recortar uma região com camadas.
ms.assetid: eaeb6cfd-de62-46f1-972d-a11e0ccc11d9
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 979281fb7fa6e034894bffaecbd6246fe8a9aa94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454217"
---
# <a name="how-to-clip-to-a-geometric-mask"></a><span data-ttu-id="26723-103">Como recortar para uma máscara geométrica</span><span class="sxs-lookup"><span data-stu-id="26723-103">How to Clip to a Geometric Mask</span></span>

<span data-ttu-id="26723-104">Este tópico descreve como usar uma máscara geométrica para recortar uma região de uma camada.</span><span class="sxs-lookup"><span data-stu-id="26723-104">This topic describes how to use a geometric mask to clip a region of a layer.</span></span>

<span data-ttu-id="26723-105">**Para recortar uma região com uma máscara geométrica**</span><span class="sxs-lookup"><span data-stu-id="26723-105">**To clip a region with a geometric mask**</span></span>

1.  <span data-ttu-id="26723-106">Crie o [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) que será usado para recortar a região.</span><span class="sxs-lookup"><span data-stu-id="26723-106">Create the [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) that will be used to clip the region.</span></span>
2.  <span data-ttu-id="26723-107">Chame [**ID2D1RenderTarget:: CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) para criar uma camada.</span><span class="sxs-lookup"><span data-stu-id="26723-107">Call [**ID2D1RenderTarget::CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) to create a layer.</span></span>
3.  <span data-ttu-id="26723-108">Chame [**ID2D1RenderTarget::P ushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) e passe a máscara geométrica que você definiu na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="26723-108">Call [**ID2D1RenderTarget::PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) and pass the geometric mask you defined in step 1.</span></span>
4.  <span data-ttu-id="26723-109">Desenhe o conteúdo para o clipe.</span><span class="sxs-lookup"><span data-stu-id="26723-109">Draw the content to clip.</span></span>
5.  <span data-ttu-id="26723-110">Chame [**ID2D1RenderTarget::P oplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) para remover a camada do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="26723-110">Call [**ID2D1RenderTarget::PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) to remove the layer from the render target.</span></span>

<span data-ttu-id="26723-111">O exemplo a seguir usa uma máscara geométrica para recortar uma imagem e vários retângulos.</span><span class="sxs-lookup"><span data-stu-id="26723-111">The example that follows uses a geometric mask to clip an image and several rectangles.</span></span> <span data-ttu-id="26723-112">A ilustração a seguir mostra o bitmap original à esquerda e o bitmap recortado na máscara geométrica à direita.</span><span class="sxs-lookup"><span data-stu-id="26723-112">The following illustration shows the original bitmap on the left, and the bitmap clipped to the geometric mask on the right.</span></span>

![ilustração de um bitmap Goldfish antes e depois que o bitmap é recortado para uma máscara em formato estrela](images/cliparegion-layers.png)

<span data-ttu-id="26723-114">Para recortar o desenho conforme mostrado na ilustração anterior, você cria um [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) e o usa para definir uma estrela.</span><span class="sxs-lookup"><span data-stu-id="26723-114">To clip the drawing as shown in the preceding illustration, you create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and use it to define a star.</span></span> <span data-ttu-id="26723-115">O código a seguir mostra como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="26723-115">The following code shows how to do this.</span></span>


```C++
// Create the path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);
}

// Write to the path geometry using the geometry sink to create a star.
if (SUCCEEDED(hr))
{
    hr = m_pPathGeometry->Open(&pSink);
}
if (SUCCEEDED(hr))
{
    pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
    pSink->BeginFigure(D2D1::Point2F(20, 50), D2D1_FIGURE_BEGIN_FILLED);
    pSink->AddLine(D2D1::Point2F(130, 50));
    pSink->AddLine(D2D1::Point2F(20, 130));
    pSink->AddLine(D2D1::Point2F(80, 0));
    pSink->AddLine(D2D1::Point2F(130, 130));
    pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

    hr = pSink->Close();
}

SafeRelease(&pSink);
```



<span data-ttu-id="26723-116">Chame [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) para criar uma camada.</span><span class="sxs-lookup"><span data-stu-id="26723-116">Call [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) to create a layer.</span></span>

> [!Note]  
> <span data-ttu-id="26723-117">A partir do Windows 8, você não precisa chamar [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)).</span><span class="sxs-lookup"><span data-stu-id="26723-117">Starting with Windows 8, you don't need to call [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)).</span></span> <span data-ttu-id="26723-118">Na maioria das vezes, o desempenho será melhor se você não chamar esse método e Direct2D gerenciar os recursos de camada.</span><span class="sxs-lookup"><span data-stu-id="26723-118">In most situations performance is better if you don't call this method and Direct2D manages the layer resources.</span></span>

 

<span data-ttu-id="26723-119">Chame [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) com a máscara de geometria para enviar por push a camada.</span><span class="sxs-lookup"><span data-stu-id="26723-119">Call [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) with the geometry mask to push the layer.</span></span> <span data-ttu-id="26723-120">Desenhe o conteúdo para o clipe e, em seguida, chame [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) para exibir a camada.</span><span class="sxs-lookup"><span data-stu-id="26723-120">Draw the content to clip, then call [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) to pop the layer.</span></span> <span data-ttu-id="26723-121">Isso produz o desenho em forma de estrela.</span><span class="sxs-lookup"><span data-stu-id="26723-121">This produces the star-shaped drawing.</span></span> <span data-ttu-id="26723-122">O código a seguir mostra como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="26723-122">The following code shows how to do this.</span></span>


```C++
HRESULT DemoApp::RenderWithLayer(ID2D1RenderTarget *pRT)
{
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

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

    SafeRelease(&pLayer);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="26723-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="26723-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26723-124">Visão geral de camadas</span><span class="sxs-lookup"><span data-stu-id="26723-124">Layers Overview</span></span>](direct2d-layers-overview.md)
</dt> <dt>

[<span data-ttu-id="26723-125">Referência de Direct2D</span><span class="sxs-lookup"><span data-stu-id="26723-125">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 