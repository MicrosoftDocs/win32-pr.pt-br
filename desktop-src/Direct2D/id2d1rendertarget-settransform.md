---
title: Métodos SetTransform ID2D1RenderTarget
description: Aplica a transformação especificada ao destino de renderização, substituindo a transformação existente. Todas as operações de desenho subsequentes ocorrem no espaço transformado.
ms.assetid: 04799366-6458-40ff-a2fb-5d227eab041d
keywords:
- Métodos SetTransform Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 8310bf9e5c97beb3ea3cf3b2a9a513f606079a18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756003"
---
# <a name="id2d1rendertargetsettransform-methods"></a><span data-ttu-id="a4e08-105">Métodos ID2D1RenderTarget:: SetTransform</span><span class="sxs-lookup"><span data-stu-id="a4e08-105">ID2D1RenderTarget::SetTransform methods</span></span>

<span data-ttu-id="a4e08-106">Aplica a transformação especificada ao destino de renderização, substituindo a transformação existente.</span><span class="sxs-lookup"><span data-stu-id="a4e08-106">Applies the specified transform to the render target, replacing the existing transformation.</span></span> <span data-ttu-id="a4e08-107">Todas as operações de desenho subsequentes ocorrem no espaço transformado.</span><span class="sxs-lookup"><span data-stu-id="a4e08-107">All subsequent drawing operations occur in the transformed space.</span></span>

### <a name="overload-list"></a><span data-ttu-id="a4e08-108">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="a4e08-108">Overload list</span></span>



| <span data-ttu-id="a4e08-109">Método</span><span class="sxs-lookup"><span data-stu-id="a4e08-109">Method</span></span>                                                                                              | <span data-ttu-id="a4e08-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4e08-110">Description</span></span>                                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4e08-111">[**SetTransform (D2D1 \_ Matrix \_ 3X2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f_))</span><span class="sxs-lookup"><span data-stu-id="a4e08-111">[**SetTransform(D2D1\_MATRIX\_3X2\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f_))</span></span>  | <span data-ttu-id="a4e08-112">Aplica a transformação especificada ao destino de renderização, substituindo a transformação existente.</span><span class="sxs-lookup"><span data-stu-id="a4e08-112">Applies the specified transform to the render target, replacing the existing transformation.</span></span> <span data-ttu-id="a4e08-113">Todas as operações de desenho subsequentes ocorrem no espaço transformado.</span><span class="sxs-lookup"><span data-stu-id="a4e08-113">All subsequent drawing operations occur in the transformed space.</span></span> <br/> |
| <span data-ttu-id="a4e08-114">[**SetTransform ( \_ matriz d2d1 \_ 3x2 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f))</span><span class="sxs-lookup"><span data-stu-id="a4e08-114">[**SetTransform(D2D1\_MATRIX\_3X2\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settransform(constd2d1_matrix_3x2_f))</span></span> | <span data-ttu-id="a4e08-115">Aplica a transformação especificada ao destino de renderização, substituindo a transformação existente.</span><span class="sxs-lookup"><span data-stu-id="a4e08-115">Applies the specified transform to the render target, replacing the existing transformation.</span></span> <span data-ttu-id="a4e08-116">Todas as operações de desenho subsequentes ocorrem no espaço transformado.</span><span class="sxs-lookup"><span data-stu-id="a4e08-116">All subsequent drawing operations occur in the transformed space.</span></span><br/>  |



## <a name="examples"></a><span data-ttu-id="a4e08-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a4e08-117">Examples</span></span>

<span data-ttu-id="a4e08-118">O exemplo a seguir usa o método **SetTransform** para aplicar uma rotação ao destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="a4e08-118">The following example uses the **SetTransform** method to apply a rotation to the render target.</span></span> <span data-ttu-id="a4e08-119">Para obter o exemplo completo, consulte [como girar um objeto](how-to-rotate.md).</span><span class="sxs-lookup"><span data-stu-id="a4e08-119">For the complete example, see [How to Rotate an Object](how-to-rotate.md).</span></span>


```C++
// Apply the rotation transform to the render target.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(
        45.0f,
        D2D1::Point2F(468.0f, 331.5f))
    );
```



<span data-ttu-id="a4e08-120">Para obter exemplos adicionais mostrando como transformar um destino de renderização, consulte [como dimensionar um objeto](how-to-scale.md), [como distorcer um objeto](how-to-skew.md)e [como converter um objeto](how-to-translate.md).</span><span class="sxs-lookup"><span data-stu-id="a4e08-120">For additional examples showing how to transform a render target, see [How to Scale an Object](how-to-scale.md), [How to Skew an Object](how-to-skew.md), and [How to Translate an Object](how-to-translate.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4e08-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4e08-121">Requirements</span></span>



| <span data-ttu-id="a4e08-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4e08-122">Requirement</span></span> | <span data-ttu-id="a4e08-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a4e08-123">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a4e08-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a4e08-124">Library</span></span><br/> | <dl> <span data-ttu-id="a4e08-125"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4e08-125"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="a4e08-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a4e08-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="a4e08-127"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4e08-127"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4e08-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4e08-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4e08-129">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="a4e08-129">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="a4e08-130">Visão geral das transformações</span><span class="sxs-lookup"><span data-stu-id="a4e08-130">Transforms Overview</span></span>](direct2d-transforms-overview.md)
</dt> <dt>

[<span data-ttu-id="a4e08-131">Como girar um objeto</span><span class="sxs-lookup"><span data-stu-id="a4e08-131">How to Rotate an Object</span></span>](how-to-rotate.md)
</dt> <dt>

[<span data-ttu-id="a4e08-132">Como dimensionar um objeto</span><span class="sxs-lookup"><span data-stu-id="a4e08-132">How to Scale an Object</span></span>](how-to-scale.md)
</dt> <dt>

[<span data-ttu-id="a4e08-133">Como distorcer um objeto</span><span class="sxs-lookup"><span data-stu-id="a4e08-133">How to Skew an Object</span></span>](how-to-skew.md)
</dt> <dt>

[<span data-ttu-id="a4e08-134">Como converter um objeto</span><span class="sxs-lookup"><span data-stu-id="a4e08-134">How to Translate an Object</span></span>](how-to-translate.md)
</dt> <dt>

[<span data-ttu-id="a4e08-135">Como aplicar várias transformações a um objeto</span><span class="sxs-lookup"><span data-stu-id="a4e08-135">How to Apply Multiple Transforms to an Object</span></span>](how-to-apply-multiple-transforms.md)
</dt> </dl>

 

