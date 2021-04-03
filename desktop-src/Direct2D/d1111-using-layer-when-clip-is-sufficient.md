---
title: D1111 usando camada quando o clipe é suficiente
ms.assetid: 07fe3c66-15be-408b-a30b-a7f52919c058
description: Uma camada está sendo usada com uma máscara de opacidade nula, 1,0 de opacidade e uma máscara geométrica retangular alinhada ao eixo. A API de clipe Push/pop deve obter os mesmos resultados com melhor desempenho.
keywords:
- D1111 usando camada quando o clipe é suficiente Direct2D
topic_type:
- apiref
api_name:
- D1111 Using Layer When Clip Is Sufficient
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: a30bbfd7b8ca448928249018a28bc4d6a8a2f57f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641792"
---
# <a name="d1111-using-layer-when-clip-is-sufficient"></a><span data-ttu-id="7177e-105">D1111: usando a camada quando o clipe é suficiente</span><span class="sxs-lookup"><span data-stu-id="7177e-105">D1111: Using Layer When Clip Is Sufficient</span></span>

<span data-ttu-id="7177e-106">PERF-uma camada está sendo usada com uma máscara de opacidade **nula** , 1,0 de opacidade e uma máscara geométrica retangular alinhada ao eixo.</span><span class="sxs-lookup"><span data-stu-id="7177e-106">PERF - A layer is being used with a **NULL** opacity mask, 1.0 opacity, and an axis aligned rectangular geometric mask.</span></span> <span data-ttu-id="7177e-107">A API de clipe Push/pop deve obter os mesmos resultados com melhor desempenho.</span><span class="sxs-lookup"><span data-stu-id="7177e-107">The Push/Pop Clip API should achieve the same results with higher performance.</span></span>

## <a name="placeholders"></a><span data-ttu-id="7177e-108">Espaços reservados</span><span class="sxs-lookup"><span data-stu-id="7177e-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="7177e-109"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span><span class="sxs-lookup"><span data-stu-id="7177e-109"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="7177e-110">O endereço da interface.</span><span class="sxs-lookup"><span data-stu-id="7177e-110">The address of the interface.</span></span>

</dd> </dl> 

|             |             |
|-------------|-------------|
| <span data-ttu-id="7177e-111">Nível de erro</span><span class="sxs-lookup"><span data-stu-id="7177e-111">Error Level</span></span> | <span data-ttu-id="7177e-112">Informações do</span><span class="sxs-lookup"><span data-stu-id="7177e-112">Information</span></span> |



 

## <a name="examples"></a><span data-ttu-id="7177e-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7177e-113">Examples</span></span>

<span data-ttu-id="7177e-114">O código a seguir usa [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) e [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) quando a camada contém apenas um primitivo (um retângulo) e os campos da estrutura [**de \_ \_ parâmetros da camada d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) são definidos como padrões.</span><span class="sxs-lookup"><span data-stu-id="7177e-114">The following code uses the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) when the layer contains only one primitive (a rectangle) and the fields of the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure are set to defaults.</span></span> <span data-ttu-id="7177e-115">Para obter os valores padrão da estrutura de **\_ \_ parâmetros de camada d2d1** , consulte [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).</span><span class="sxs-lookup"><span data-stu-id="7177e-115">For the default values of the **D2D1\_LAYER\_PARAMETERS** structure, see [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).</span></span>


```C++
        ID2D1Layer *m_pLayer;

        hr = m_pRenderTarget->CreateLayer(D2D1::SizeF(100, 100), &m_pLayer);
        m_pRenderTarget->PushLayer(D2D1::LayerParameters(), m_pLayer);
        m_pRenderTarget->FillRectangle(D2D1::RectF(100, 50, 400, 160), m_pBlackBrush);
        m_pRenderTarget->PopLayer();
```



<span data-ttu-id="7177e-116">Este exemplo produz a seguinte mensagem de depuração:</span><span class="sxs-lookup"><span data-stu-id="7177e-116">This example produces the following debug message:</span></span>

``` syntax
DEBUG INFO - PERF - A layer is being used with a NULL opacity mask, 1.0 opacity, 
            and an axis aligned rectangular geometric mask.  
            The Push/Pop Clip API should achieve the same results with higher performance.
```

## <a name="possible-causes"></a><span data-ttu-id="7177e-117">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="7177e-117">Possible Causes</span></span>

<span data-ttu-id="7177e-118">Uma camada foi usada quando os métodos [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) e [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) seriam suficientes.</span><span class="sxs-lookup"><span data-stu-id="7177e-118">A layer was used when the [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) methods would have sufficed.</span></span>

 

 