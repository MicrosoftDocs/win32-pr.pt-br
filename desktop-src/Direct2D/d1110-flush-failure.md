---
title: Falha de liberação de D1110
ms.assetid: 44f122b0-08e3-4f63-a575-0f3619144823
description: Uma chamada de liberação por um destino de renderização falhou
keywords:
- D1110 de falha de liberação de Direct2D
topic_type:
- apiref
api_name:
- D1110 Flush Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 4821ba291f3adc8d22d1d1298a88c74b47dc648b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366684"
---
# <a name="d1110-flush-failure"></a><span data-ttu-id="027f3-104">D1110: falha de liberação</span><span class="sxs-lookup"><span data-stu-id="027f3-104">D1110: Flush Failure</span></span>

<span data-ttu-id="027f3-105">Uma chamada de liberação por um recurso com falha de destino de renderização \[  \] .</span><span class="sxs-lookup"><span data-stu-id="027f3-105">A Flush call by a render target failed \[*resource*\].</span></span> <span data-ttu-id="027f3-106">Marcas \[ *da tag1*, *tag2* \] .</span><span class="sxs-lookup"><span data-stu-id="027f3-106">Tags \[*tag1*, *tag2*\].</span></span>

## <a name="placeholders"></a><span data-ttu-id="027f3-107">Espaços reservados</span><span class="sxs-lookup"><span data-stu-id="027f3-107">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="027f3-108"><span id="resource"></span><span id="RESOURCE"></span>*Kit*</span><span class="sxs-lookup"><span data-stu-id="027f3-108"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="027f3-109">O endereço do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="027f3-109">The address of the render target.</span></span>

</dd> <dt>

<span data-ttu-id="027f3-110"><span id="tag1"></span><span id="TAG1"></span>*da tag1*</span><span class="sxs-lookup"><span data-stu-id="027f3-110"><span id="tag1"></span><span id="TAG1"></span>*tag1*</span></span>
</dt> <dd>

<span data-ttu-id="027f3-111">O primeiro valor de marca.</span><span class="sxs-lookup"><span data-stu-id="027f3-111">The first tag value.</span></span> <span data-ttu-id="027f3-112">Consulte [**settags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="027f3-112">See [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="027f3-113"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span><span class="sxs-lookup"><span data-stu-id="027f3-113"><span id="tag2"></span><span id="TAG2"></span>*tag2*</span></span>
</dt> <dd>

<span data-ttu-id="027f3-114">O valor da segunda marca.</span><span class="sxs-lookup"><span data-stu-id="027f3-114">The second tag value.</span></span> <span data-ttu-id="027f3-115">Consulte [**settags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="027f3-115">See [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) for more information.</span></span>

</dd> </dl> 

|             |         |
|-------------|---------|
| <span data-ttu-id="027f3-116">Nível de erro</span><span class="sxs-lookup"><span data-stu-id="027f3-116">Error Level</span></span> | <span data-ttu-id="027f3-117">Aviso</span><span class="sxs-lookup"><span data-stu-id="027f3-117">Warning</span></span> |



 

## <a name="examples"></a><span data-ttu-id="027f3-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="027f3-118">Examples</span></span>

<span data-ttu-id="027f3-119">**Exemplo 1:** O código a seguir mostra que uma chamada de desenho está em um estado inválido.</span><span class="sxs-lookup"><span data-stu-id="027f3-119">**Example 1:** The following code shows that a draw call is in an invalid state.</span></span> <span data-ttu-id="027f3-120">Para evitar a mensagem de aviso, use [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) para definir o modo AntiAlias de d2d1 \_ \_ \_ AntiAlias antes de uma chamada [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) .</span><span class="sxs-lookup"><span data-stu-id="027f3-120">To avoid the warning message, use [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) to set D2D1\_ANTIALIAS\_MODE\_ANTIALIASED before a [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) call.</span></span>


```C++
       
        if(SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->CreateBitmap(
                D2D1::SizeU(1,1),
                NULL,
                0,
                D2D1::BitmapProperties(D2D1::PixelFormat(
                    DXGI_FORMAT_A8_UNORM, 
                    D2D1_ALPHA_MODE_PREMULTIPLIED
                    )),
                &m_pBitmap
                );                    
        }


        m_pRenderTarget->FillOpacityMask(
            m_pBitmapMask,
            m_pFernBitmapBrush,
            D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
            &rcBrushRect
            );

        hr = m_pRenderTarget->Flush();

        hr = m_pRenderTarget->EndDraw();
```





<span data-ttu-id="027f3-121">Este exemplo produz a seguinte mensagem de depuração:</span><span class="sxs-lookup"><span data-stu-id="027f3-121">This example produces the following debug message:</span></span>

``` syntax
D2D DEBUG WARNING - Flush call on render target failed [88990001]. Tags [0, 0].
```

<span data-ttu-id="027f3-122">**Exemplo 2:** O código a seguir mostra que a [**liberação**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) é chamada após a chamada [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="027f3-122">**Example 2:** The following code shows that the [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called after the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) call.</span></span>


```C++
        // Calling Flush after EndDraw generates a
        // flush error message from the debug layer.
       hr = m_pRenderTarget->EndDraw();       
       
       hr = m_pRenderTarget->Flush();
```



<span data-ttu-id="027f3-123">Este exemplo produz a seguinte mensagem de depuração:</span><span class="sxs-lookup"><span data-stu-id="027f3-123">This example produces the following debug message:</span></span>

``` syntax
DEBUG WARNING - A Flush call by a render target failed [88990001]. Tags [0, 0].
```

## <a name="possible-causes"></a><span data-ttu-id="027f3-124">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="027f3-124">Possible Causes</span></span>

<span data-ttu-id="027f3-125">A chamada de [**liberação**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) pode falhar por uma das duas razões.</span><span class="sxs-lookup"><span data-stu-id="027f3-125">The [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) call can fail for one of two reasons.</span></span> <span data-ttu-id="027f3-126">Ele pode falhar porque o método foi chamado fora da chamada [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) / [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) , ou pode falhar porque houve um erro produzido por uma das operações de destino render que foram processadas desde a última chamada **flush** ou **EndDraw** .</span><span class="sxs-lookup"><span data-stu-id="027f3-126">It may fail because the method was called outside of the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)/[**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) call, or it may fail because there was an error produced by one of the render target operations that have been processed since the last **Flush** call or **EndDraw** call.</span></span> <span data-ttu-id="027f3-127">Para corrigir o problema, o aplicativo deve determinar a causa do erro e executar a ação apropriada.</span><span class="sxs-lookup"><span data-stu-id="027f3-127">To fix the issue, the application should determine the cause of the error and take the appropriate action.</span></span>

## <a name="fixes"></a><span data-ttu-id="027f3-128">Correções</span><span class="sxs-lookup"><span data-stu-id="027f3-128">Fixes</span></span>

<span data-ttu-id="027f3-129">Há muitas razões pelas quais uma chamada de [**liberação**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) pode falhar.</span><span class="sxs-lookup"><span data-stu-id="027f3-129">There are many reasons that a [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) call might fail.</span></span> <span data-ttu-id="027f3-130">O aplicativo deve determinar a causa do erro e executar a ação apropriada.</span><span class="sxs-lookup"><span data-stu-id="027f3-130">The application should determine the cause of the error and take the appropriate action.</span></span>

 

 