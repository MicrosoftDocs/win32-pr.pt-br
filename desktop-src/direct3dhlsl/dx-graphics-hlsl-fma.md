---
title: FMA (Corecrt \_ Math. h)
description: Retorna a adição de multiplicação cruzada de precisão dupla de a \ b + c.
ms.assetid: C4EF2552-7388-4CA8-B78F-6B2D4C8FC5F6
keywords:
- FMA HLSL
topic_type:
- apiref
api_name:
- fma
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 287f07881a00ca53a3f1fe702cf4d95b64bf14c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369591"
---
# <a name="fma"></a><span data-ttu-id="f20d7-104">fma</span><span class="sxs-lookup"><span data-stu-id="f20d7-104">fma</span></span>

<span data-ttu-id="f20d7-105">Retorna a adição de multiplicação de precisão dupla de um \* b + c.</span><span class="sxs-lookup"><span data-stu-id="f20d7-105">Returns the double-precision fused multiply-addition of a \* b + c.</span></span>



| <span data-ttu-id="f20d7-106">*RET* FMA (duplo *a*, *b*, *c*);</span><span class="sxs-lookup"><span data-stu-id="f20d7-106">*ret* fma(double *a*, *b*, *c*);</span></span> |
|----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="f20d7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f20d7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f20d7-108"><span id="a"></span><span id="A"></span>*um*</span><span class="sxs-lookup"><span data-stu-id="f20d7-108"><span id="a"></span><span id="A"></span>*a*</span></span>
</dt> <dd>

<span data-ttu-id="f20d7-109">\[no \] primeiro valor da adição de multiplicação com fusível.</span><span class="sxs-lookup"><span data-stu-id="f20d7-109">\[in\] The first value in the fused multiply-addition.</span></span>

</dd> <dt>

<span data-ttu-id="f20d7-110"><span id="b"></span><span id="B"></span>*b*</span><span class="sxs-lookup"><span data-stu-id="f20d7-110"><span id="b"></span><span id="B"></span>*b*</span></span>
</dt> <dd>

<span data-ttu-id="f20d7-111">\[no \] segundo valor da adição de multiplicação com fusível.</span><span class="sxs-lookup"><span data-stu-id="f20d7-111">\[in\] The second value in the fused multiply-addition.</span></span>

</dd> <dt>

<span data-ttu-id="f20d7-112"><span id="c"></span><span id="C"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="f20d7-112"><span id="c"></span><span id="C"></span>*c*</span></span>
</dt> <dd>

<span data-ttu-id="f20d7-113">\[no \] terceiro valor da adição de multiplicação com fusível.</span><span class="sxs-lookup"><span data-stu-id="f20d7-113">\[in\] The third value in the fused multiply-addition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f20d7-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="f20d7-114">Return Value</span></span>

<span data-ttu-id="f20d7-115">A adição de precisão dupla combinada de parâmetros *a* \* *b*  +  *c*.</span><span class="sxs-lookup"><span data-stu-id="f20d7-115">The double-precision fused multiply-addition of parameters *a* \* *b* + *c*.</span></span> <span data-ttu-id="f20d7-116">O valor retornado deve ser preciso para 0,5 unidades de menos precisão (ULP).</span><span class="sxs-lookup"><span data-stu-id="f20d7-116">The returned value must be accurate to 0.5 units of least precision (ULP).</span></span>

## <a name="remarks"></a><span data-ttu-id="f20d7-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f20d7-117">Remarks</span></span>

<span data-ttu-id="f20d7-118">O **FMA** intrínseco deve dar suporte a Nans, INFs e normas.</span><span class="sxs-lookup"><span data-stu-id="f20d7-118">The **fma** intrinsic must support NaNs, INFs, and Denorms.</span></span>

<span data-ttu-id="f20d7-119">Para usar o **FMA** intrínseco em seu código de sombreador, chame o método [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) com [**\_ \_ \_ as opções D3D11 Feature D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) para verificar se o dispositivo Direct3D dá suporte à opção de recurso [**ExtendedDoublesShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) .</span><span class="sxs-lookup"><span data-stu-id="f20d7-119">To use the **fma** intrinsic in your shader code, call the [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) method with [**D3D11\_FEATURE\_D3D11\_OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) to verify that the Direct3D device supports the [**ExtendedDoublesShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) feature option.</span></span> <span data-ttu-id="f20d7-120">O **FMA** intrínseco requer um driver de vídeo WDDM 1,2 e todos os drivers de exibição do WDDM 1,2 devem oferecer suporte a **FMA**.</span><span class="sxs-lookup"><span data-stu-id="f20d7-120">The **fma** intrinsic requires a WDDM 1.2 display driver, and all WDDM 1.2 display drivers must support **fma**.</span></span> <span data-ttu-id="f20d7-121">Se seu aplicativo cria um dispositivo de renderização com [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0 ou 11,1 e o destino de compilação é o modelo de sombreador 5 ou posterior, o código-fonte HLSL pode usar o **FMA** intrínseco.</span><span class="sxs-lookup"><span data-stu-id="f20d7-121">If your app creates a rendering device with [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.0 or 11.1 and the compilation target is shader model 5 or later, the HLSL source code can use the **fma** intrinsic.</span></span>

### <a name="type-description"></a><span data-ttu-id="f20d7-122">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="f20d7-122">Type Description</span></span>



| <span data-ttu-id="f20d7-123">Name</span><span class="sxs-lookup"><span data-stu-id="f20d7-123">Name</span></span>  | [<span data-ttu-id="f20d7-124">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="f20d7-124">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="f20d7-125">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="f20d7-125">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="f20d7-126">Tamanho</span><span class="sxs-lookup"><span data-stu-id="f20d7-126">Size</span></span>                         |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| <span data-ttu-id="f20d7-127">*um*</span><span class="sxs-lookup"><span data-stu-id="f20d7-127">*a*</span></span>   | <span data-ttu-id="f20d7-128">[**escalar**](dx-graphics-hlsl-intrinsic-functions.md), **vetor** ou **matriz**</span><span class="sxs-lookup"><span data-stu-id="f20d7-128">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="f20d7-129">**Clique**</span><span class="sxs-lookup"><span data-stu-id="f20d7-129">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="f20d7-130">any</span><span class="sxs-lookup"><span data-stu-id="f20d7-130">any</span></span>                          |
| <span data-ttu-id="f20d7-131">*b*</span><span class="sxs-lookup"><span data-stu-id="f20d7-131">*b*</span></span>   | <span data-ttu-id="f20d7-132">igual à entrada *a*</span><span class="sxs-lookup"><span data-stu-id="f20d7-132">same as input *a*</span></span>                                                                                              | [<span data-ttu-id="f20d7-133">**Clique**</span><span class="sxs-lookup"><span data-stu-id="f20d7-133">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="f20d7-134">mesmas dimensões como entrada *a*</span><span class="sxs-lookup"><span data-stu-id="f20d7-134">same dimensions as input *a*</span></span> |
| <span data-ttu-id="f20d7-135">*c*</span><span class="sxs-lookup"><span data-stu-id="f20d7-135">*c*</span></span>   | <span data-ttu-id="f20d7-136">igual à entrada *a*</span><span class="sxs-lookup"><span data-stu-id="f20d7-136">same as input *a*</span></span>                                                                                              | [<span data-ttu-id="f20d7-137">**Clique**</span><span class="sxs-lookup"><span data-stu-id="f20d7-137">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="f20d7-138">mesmas dimensões como entrada *a*</span><span class="sxs-lookup"><span data-stu-id="f20d7-138">same dimensions as input *a*</span></span> |
| <span data-ttu-id="f20d7-139">*RET*</span><span class="sxs-lookup"><span data-stu-id="f20d7-139">*ret*</span></span> | <span data-ttu-id="f20d7-140">igual à entrada *a*</span><span class="sxs-lookup"><span data-stu-id="f20d7-140">same as input *a*</span></span>                                                                                              | [<span data-ttu-id="f20d7-141">**Clique**</span><span class="sxs-lookup"><span data-stu-id="f20d7-141">**double**</span></span>](/windows/desktop/WinProg/windows-data-types)                       | <span data-ttu-id="f20d7-142">mesmas dimensões como entrada *a*</span><span class="sxs-lookup"><span data-stu-id="f20d7-142">same dimensions as input *a*</span></span> |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="f20d7-143">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="f20d7-143">Minimum Shader Model</span></span>

<span data-ttu-id="f20d7-144">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="f20d7-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f20d7-145">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="f20d7-145">Shader Model</span></span>                                                | <span data-ttu-id="f20d7-146">Com suporte</span><span class="sxs-lookup"><span data-stu-id="f20d7-146">Supported</span></span> |
|-------------------------------------------------------------|-----------|
| [<span data-ttu-id="f20d7-147">Modelo do sombreador 5 ou posterior</span><span class="sxs-lookup"><span data-stu-id="f20d7-147">Shader model 5 or later</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="f20d7-148">sim</span><span class="sxs-lookup"><span data-stu-id="f20d7-148">yes</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="f20d7-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f20d7-149">Requirements</span></span>



| <span data-ttu-id="f20d7-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="f20d7-150">Requirement</span></span> | <span data-ttu-id="f20d7-151">Valor</span><span class="sxs-lookup"><span data-stu-id="f20d7-151">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f20d7-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f20d7-152">Minimum supported client</span></span><br/> | <span data-ttu-id="f20d7-153">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f20d7-153">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="f20d7-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f20d7-154">Minimum supported server</span></span><br/> | <span data-ttu-id="f20d7-155">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f20d7-155">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="f20d7-156">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f20d7-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="f20d7-157"><dt>Corecrt \_ Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f20d7-157"><dt>Corecrt\_math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f20d7-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="f20d7-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f20d7-159">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="f20d7-159">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

