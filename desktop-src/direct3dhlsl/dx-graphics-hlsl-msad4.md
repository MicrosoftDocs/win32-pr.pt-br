---
title: msad4
description: Compara um valor de referência de 4 bytes e um valor de origem de 8 bytes e acumula um vetor de quatro somas. Cada soma corresponde à soma mascarada de diferenças absolutas de um alinhamento de byte diferente entre o valor de referência e o valor de origem.
ms.assetid: 6497F9AE-4524-44C2-A1C6-2A4ACB30FA9C
keywords:
- msad4 HLSL
topic_type:
- apiref
api_name:
- msad4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 552db3afd07677777b47e939d659c0f6e333e496
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104967254"
---
# <a name="msad4"></a><span data-ttu-id="b30cc-105">msad4</span><span class="sxs-lookup"><span data-stu-id="b30cc-105">msad4</span></span>

<span data-ttu-id="b30cc-106">Compara um valor de referência de 4 bytes e um valor de origem de 8 bytes e acumula um vetor de quatro somas.</span><span class="sxs-lookup"><span data-stu-id="b30cc-106">Compares a 4-byte reference value and an 8-byte source value and accumulates a vector of 4 sums.</span></span> <span data-ttu-id="b30cc-107">Cada soma corresponde à soma mascarada de diferenças absolutas de um alinhamento de byte diferente entre o valor de referência e o valor de origem.</span><span class="sxs-lookup"><span data-stu-id="b30cc-107">Each sum corresponds to the masked sum of absolute differences of a different byte alignment between the reference value and the source value.</span></span>



| <span data-ttu-id="b30cc-108">uint4 Result = msad4 (referência uint, fonte uint2, uint4 Accum);</span><span class="sxs-lookup"><span data-stu-id="b30cc-108">uint4 result = msad4(uint reference, uint2 source, uint4 accum);</span></span> |
|------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="b30cc-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b30cc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b30cc-110"><span id="reference"></span><span id="REFERENCE"></span>*referência*</span><span class="sxs-lookup"><span data-stu-id="b30cc-110"><span id="reference"></span><span id="REFERENCE"></span>*reference*</span></span>
</dt> <dd>

<span data-ttu-id="b30cc-111">\[na \] matriz de referência de 4 bytes em um valor **uint** .</span><span class="sxs-lookup"><span data-stu-id="b30cc-111">\[in\] The reference array of 4 bytes in one **uint** value.</span></span>

</dd> <dt>

<span data-ttu-id="b30cc-112"><span id="source"></span><span id="SOURCE"></span>*original*</span><span class="sxs-lookup"><span data-stu-id="b30cc-112"><span id="source"></span><span id="SOURCE"></span>*source*</span></span>
</dt> <dd>

<span data-ttu-id="b30cc-113">\[na \] matriz de origem de 8 bytes em dois valores de **uint2** .</span><span class="sxs-lookup"><span data-stu-id="b30cc-113">\[in\] The source array of 8 bytes in two **uint2** values.</span></span>

</dd> <dt>

<span data-ttu-id="b30cc-114"><span id="accum"></span><span id="ACCUM"></span>*Accum*</span><span class="sxs-lookup"><span data-stu-id="b30cc-114"><span id="accum"></span><span id="ACCUM"></span>*accum*</span></span>
</dt> <dd>

<span data-ttu-id="b30cc-115">\[em \] um vetor de quatro valores.</span><span class="sxs-lookup"><span data-stu-id="b30cc-115">\[in\] A vector of 4 values.</span></span> <span data-ttu-id="b30cc-116">**msad4** adiciona esse vetor à soma mascarada de diferenças absolutas dos diferentes alinhamentos de byte entre o valor de referência e o valor de origem.</span><span class="sxs-lookup"><span data-stu-id="b30cc-116">**msad4** adds this vector to the masked sum of absolute differences of the different byte alignments between the reference value and the source value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b30cc-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b30cc-117">Return Value</span></span>

<span data-ttu-id="b30cc-118">Um vetor de quatro somas.</span><span class="sxs-lookup"><span data-stu-id="b30cc-118">A vector of 4 sums.</span></span> <span data-ttu-id="b30cc-119">Cada soma corresponde à soma mascarada de diferenças absolutas de diferentes alinhamentos de bytes entre o valor de referência e o valor de origem.</span><span class="sxs-lookup"><span data-stu-id="b30cc-119">Each sum corresponds to the masked sum of absolute differences of different byte alignments between the reference value and the source value.</span></span> <span data-ttu-id="b30cc-120">**msad4** não inclui uma diferença na soma se essa diferença for mascarada (ou seja, o byte de referência é 0).</span><span class="sxs-lookup"><span data-stu-id="b30cc-120">**msad4** doesn't include a difference in the sum if that difference is masked (that is, the reference byte is 0).</span></span>

## <a name="remarks"></a><span data-ttu-id="b30cc-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="b30cc-121">Remarks</span></span>

<span data-ttu-id="b30cc-122">Para usar o **msad4** intrínseco no código do sombreador, chame o método [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) com [**\_ \_ \_ as opções D3D11 Feature D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) para verificar se o dispositivo Direct3D dá suporte à opção de recurso [**SAD4ShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) .</span><span class="sxs-lookup"><span data-stu-id="b30cc-122">To use the **msad4** intrinsic in your shader code, call the [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) method with [**D3D11\_FEATURE\_D3D11\_OPTIONS**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature) to verify that the Direct3D device supports the [**SAD4ShaderInstructions**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) feature option.</span></span> <span data-ttu-id="b30cc-123">O **msad4** intrínseco requer um driver de vídeo WDDM 1,2 e todos os drivers de exibição do WDDM 1,2 devem dar suporte a **msad4**.</span><span class="sxs-lookup"><span data-stu-id="b30cc-123">The **msad4** intrinsic requires a WDDM 1.2 display driver, and all WDDM 1.2 display drivers must support **msad4**.</span></span> <span data-ttu-id="b30cc-124">Se seu aplicativo cria um dispositivo de renderização com [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0 ou 11,1 e o destino de compilação é o modelo de sombreador 5 ou posterior, o código-fonte HLSL pode usar o intrínseco **msad4** .</span><span class="sxs-lookup"><span data-stu-id="b30cc-124">If your app creates a rendering device with [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.0 or 11.1 and the compilation target is shader model 5 or later, the HLSL source code can use the **msad4** intrinsic.</span></span>

<span data-ttu-id="b30cc-125">Os valores de retorno só são precisos até 65535.</span><span class="sxs-lookup"><span data-stu-id="b30cc-125">Return values are only accurate up to 65535.</span></span> <span data-ttu-id="b30cc-126">Se você chamar o **msad4** intrínseco com entradas que podem resultar em valores de retorno maiores que 65535, **msad4** produzirá resultados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="b30cc-126">If you call the **msad4** intrinsic with inputs that might result in return values greater than 65535, **msad4** produces undefined results.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="b30cc-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="b30cc-127">Minimum Shader Model</span></span>

<span data-ttu-id="b30cc-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b30cc-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b30cc-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="b30cc-129">Shader Model</span></span>                                                | <span data-ttu-id="b30cc-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="b30cc-130">Supported</span></span> |
|-------------------------------------------------------------|-----------|
| [<span data-ttu-id="b30cc-131">Modelo do sombreador 5 ou posterior</span><span class="sxs-lookup"><span data-stu-id="b30cc-131">Shader model 5 or later</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="b30cc-132">sim</span><span class="sxs-lookup"><span data-stu-id="b30cc-132">yes</span></span>       |



 

## <a name="examples"></a><span data-ttu-id="b30cc-133">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b30cc-133">Examples</span></span>

<span data-ttu-id="b30cc-134">Aqui está um exemplo de cálculo de resultado para **msad4**:</span><span class="sxs-lookup"><span data-stu-id="b30cc-134">Here is an example result calculation for **msad4**:</span></span>


```
reference = 0xA100B2C3;
source.x = 0xD7B0C372
source.y = 0x4F57C2A3
accum = {1,2,3,4}
result.x alignment source: 0xD7B0C372
result.x = accum.x + |0xD7   0xA1| + 0 (masked) + |0xC3   0xB2| + |0x72   0xC3| = 1 + 54 + 0 + 17 + 81 = 153
result.y alignment source: 0xA3D7B0C3
result.y = accum.y + |0xA3   0xA1| + 0 (masked) + |0xB0   0xB2| + |0xC3   0xC3| = 2 + 2 + 0 + 2 + 0 = 6
result.z alignment source: 0xC2A3D7B0
result.z = accum.z + |0xC2   0xA1| + 0 (masked) + |0xD7   0xB2| + |0xB0   0xC3| = 3 + 33 + 0 + 37 + 19 = 92
result.w alignment source: 0x57C2A3D7
result.w = accum.w + |0x57   0xA1| + 0 (masked) + |0xA3   0xB2| + |0xD7   0xC3| = 4 + 74 + 0 + 15 + 20 = 113
result = {153,6,92,113}
```



<span data-ttu-id="b30cc-135">Aqui está um exemplo de como você pode usar **msad4** para pesquisar um padrão de referência dentro de um buffer:</span><span class="sxs-lookup"><span data-stu-id="b30cc-135">Here is an example of how you can use **msad4** to search for a reference pattern within a buffer:</span></span>


```
uint4 accum = {0,0,0,0};
for(uint i=0;i<REF_SIZE;i++)
    accum = msad4(
        buf_ref[i], 
        uint2(buf_src[DTid.x+i], buf_src[DTid.x+i+1]), 
        accum);
buf_accum[DTid.x] = accum;
```



## <a name="requirements"></a><span data-ttu-id="b30cc-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b30cc-136">Requirements</span></span>



| <span data-ttu-id="b30cc-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="b30cc-137">Requirement</span></span> | <span data-ttu-id="b30cc-138">Valor</span><span class="sxs-lookup"><span data-stu-id="b30cc-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="b30cc-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b30cc-139">Minimum supported client</span></span><br/> | <span data-ttu-id="b30cc-140">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b30cc-140">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>           |
| <span data-ttu-id="b30cc-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b30cc-141">Minimum supported server</span></span><br/> | <span data-ttu-id="b30cc-142">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b30cc-142">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b30cc-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="b30cc-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b30cc-144">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="b30cc-144">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

