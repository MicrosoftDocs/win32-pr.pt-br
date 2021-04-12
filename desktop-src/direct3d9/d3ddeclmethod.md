---
description: Define o método de declaração de vértice que é uma operação predefinida executada pelo Tessellator (ou qualquer rotina de geometria de procedimento nos dados de vértice durante o mosaico).
ms.assetid: 030e04a6-4e2d-4756-80ef-e4a6a0103fd1
title: Enumeração D3DDECLMETHOD (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLMETHOD
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 534fef5a4eaf9d22d502097124dcecdb91433f73
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298526"
---
# <a name="d3ddeclmethod-enumeration"></a><span data-ttu-id="d1812-103">Enumeração D3DDECLMETHOD</span><span class="sxs-lookup"><span data-stu-id="d1812-103">D3DDECLMETHOD enumeration</span></span>

<span data-ttu-id="d1812-104">Define o método de declaração de vértice que é uma operação predefinida executada pelo Tessellator (ou qualquer rotina de geometria de procedimento nos dados de vértice durante o mosaico).</span><span class="sxs-lookup"><span data-stu-id="d1812-104">Defines the vertex declaration method which is a predefined operation performed by the tessellator (or any procedural geometry routine on the vertex data during tessellation).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1812-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1812-105">Syntax</span></span>


```C++
typedef enum D3DDECLMETHOD { 
  D3DDECLMETHOD_DEFAULT           = 0,
  D3DDECLMETHOD_PARTIALU          = 1,
  D3DDECLMETHOD_PARTIALV          = 2,
  D3DDECLMETHOD_CROSSUV           = 3,
  D3DDECLMETHOD_UV                = 4,
  D3DDECLMETHOD_LOOKUP            = 5,
  D3DDECLMETHOD_LOOKUPPRESAMPLED  = 6
} D3DDECLMETHOD, *LPD3DDECLMETHOD;
```



## <a name="constants"></a><span data-ttu-id="d1812-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="d1812-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d1812-107"><span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**D3DDECLMETHOD \_ padrão**</span><span class="sxs-lookup"><span data-stu-id="d1812-107"><span id="D3DDECLMETHOD_DEFAULT"></span><span id="d3ddeclmethod_default"></span>**D3DDECLMETHOD\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="d1812-108">Valor padrão.</span><span class="sxs-lookup"><span data-stu-id="d1812-108">Default value.</span></span> <span data-ttu-id="d1812-109">O Tessellator copia os dados de vértice (dados de spline para patches) como estão, sem cálculos adicionais.</span><span class="sxs-lookup"><span data-stu-id="d1812-109">The tessellator copies the vertex data (spline data for patches) as is, with no additional calculations.</span></span> <span data-ttu-id="d1812-110">Quando o Tessellator é usado, esse elemento é interpolado.</span><span class="sxs-lookup"><span data-stu-id="d1812-110">When the tessellator is used, this element is interpolated.</span></span> <span data-ttu-id="d1812-111">Caso contrário, os dados de vértice serão copiados para o registro de entrada.</span><span class="sxs-lookup"><span data-stu-id="d1812-111">Otherwise vertex data is copied into the input register.</span></span> <span data-ttu-id="d1812-112">O tipo de entrada e saída pode ser qualquer valor, mas sempre são do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="d1812-112">The input and output type can be any value, but are always the same type.</span></span>

</dd> <dt>

<span data-ttu-id="d1812-113"><span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD \_ parcialu**</span><span class="sxs-lookup"><span data-stu-id="d1812-113"><span id="D3DDECLMETHOD_PARTIALU"></span><span id="d3ddeclmethod_partialu"></span>**D3DDECLMETHOD\_PARTIALU**</span></span>
</dt> <dd>

<span data-ttu-id="d1812-114">Computa a tangente em um ponto no caminho do retângulo ou do triângulo na direção do U.</span><span class="sxs-lookup"><span data-stu-id="d1812-114">Computes the tangent at a point on the rectangle or triangle patch in the U direction.</span></span> <span data-ttu-id="d1812-115">O tipo de entrada pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="d1812-115">The input type can be one of the following:</span></span>

-   <span data-ttu-id="d1812-116">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="d1812-116">D3DDECLTYPE\_D3DCOLOR</span></span>
-   <span data-ttu-id="d1812-117">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="d1812-117">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="d1812-118">D3DDECLTYPE \_ FLOAT4</span><span class="sxs-lookup"><span data-stu-id="d1812-118">D3DDECLTYPE\_FLOAT4</span></span>
-   <span data-ttu-id="d1812-119">D3DDECLTYPE \_ SHORT4</span><span class="sxs-lookup"><span data-stu-id="d1812-119">D3DDECLTYPE\_SHORT4</span></span>
-   <span data-ttu-id="d1812-120">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="d1812-120">D3DDECLTYPE\_UBYTE4</span></span>

<span data-ttu-id="d1812-121">O tipo de saída é sempre D3DDECLTYPE \_ FLOAT3.</span><span class="sxs-lookup"><span data-stu-id="d1812-121">The output type is always D3DDECLTYPE\_FLOAT3.</span></span>

</dd> <dt>

<span data-ttu-id="d1812-122"><span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**D3DDECLMETHOD \_ PARTIALV**</span><span class="sxs-lookup"><span data-stu-id="d1812-122"><span id="D3DDECLMETHOD_PARTIALV"></span><span id="d3ddeclmethod_partialv"></span>**D3DDECLMETHOD\_PARTIALV**</span></span>
</dt> <dd>

<span data-ttu-id="d1812-123">Computa a tangente em um ponto no caminho do retângulo ou do triângulo na direção V.</span><span class="sxs-lookup"><span data-stu-id="d1812-123">Computes the tangent at a point on the rectangle or triangle patch in the V direction.</span></span> <span data-ttu-id="d1812-124">O tipo de entrada pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="d1812-124">The input type can be one of the following:</span></span>

-   <span data-ttu-id="d1812-125">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="d1812-125">D3DDECLTYPE\_D3DCOLOR</span></span>
-   <span data-ttu-id="d1812-126">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="d1812-126">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="d1812-127">D3DDECLTYPE \_ FLOAT4</span><span class="sxs-lookup"><span data-stu-id="d1812-127">D3DDECLTYPE\_FLOAT4</span></span>
-   <span data-ttu-id="d1812-128">D3DDECLTYPE \_ SHORT4</span><span class="sxs-lookup"><span data-stu-id="d1812-128">D3DDECLTYPE\_SHORT4</span></span>
-   <span data-ttu-id="d1812-129">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="d1812-129">D3DDECLTYPE\_UBYTE4</span></span>

<span data-ttu-id="d1812-130">O tipo de saída é sempre D3DDECLTYPE \_ FLOAT3.</span><span class="sxs-lookup"><span data-stu-id="d1812-130">The output type is always D3DDECLTYPE\_FLOAT3.</span></span>

</dd> <dt>

<span data-ttu-id="d1812-131"><span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**D3DDECLMETHOD \_ CROSSUV**</span><span class="sxs-lookup"><span data-stu-id="d1812-131"><span id="D3DDECLMETHOD_CROSSUV"></span><span id="d3ddeclmethod_crossuv"></span>**D3DDECLMETHOD\_CROSSUV**</span></span>
</dt> <dd>

<span data-ttu-id="d1812-132">Computa o normal em um ponto no caminho do retângulo ou do triângulo ao pegar o produto cruzado de duas tangentes.</span><span class="sxs-lookup"><span data-stu-id="d1812-132">Computes the normal at a point on the rectangle or triangle patch by taking the cross product of two tangents.</span></span> <span data-ttu-id="d1812-133">O tipo de entrada pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="d1812-133">The input type can be one of the following:</span></span>

-   <span data-ttu-id="d1812-134">D3DDECLTYPE \_ D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="d1812-134">D3DDECLTYPE\_D3DCOLOR</span></span>
-   <span data-ttu-id="d1812-135">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="d1812-135">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="d1812-136">D3DDECLTYPE \_ FLOAT4</span><span class="sxs-lookup"><span data-stu-id="d1812-136">D3DDECLTYPE\_FLOAT4</span></span>
-   <span data-ttu-id="d1812-137">D3DDECLTYPE \_ SHORT4</span><span class="sxs-lookup"><span data-stu-id="d1812-137">D3DDECLTYPE\_SHORT4</span></span>
-   <span data-ttu-id="d1812-138">D3DDECLTYPE \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="d1812-138">D3DDECLTYPE\_UBYTE4</span></span>

<span data-ttu-id="d1812-139">O tipo de saída é sempre D3DDECLTYPE \_ FLOAT3.</span><span class="sxs-lookup"><span data-stu-id="d1812-139">The output type is always D3DDECLTYPE\_FLOAT3.</span></span>

</dd> <dt>

<span data-ttu-id="d1812-140"><span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**\_UV D3DDECLMETHOD**</span><span class="sxs-lookup"><span data-stu-id="d1812-140"><span id="D3DDECLMETHOD_UV"></span><span id="d3ddeclmethod_uv"></span>**D3DDECLMETHOD\_UV**</span></span>
</dt> <dd>

<span data-ttu-id="d1812-141">Copie os valores de U, V em um ponto no patch de retângulo ou triângulo.</span><span class="sxs-lookup"><span data-stu-id="d1812-141">Copy out the U, V values at a point on the rectangle or triangle patch.</span></span> <span data-ttu-id="d1812-142">Isso resulta em um float 2D.</span><span class="sxs-lookup"><span data-stu-id="d1812-142">This results in a 2D float.</span></span> <span data-ttu-id="d1812-143">O tipo de entrada deve ser definido como D3DDECLTYPE \_ não utilizado.</span><span class="sxs-lookup"><span data-stu-id="d1812-143">The input type must be set to D3DDECLTYPE\_UNUSED.</span></span> <span data-ttu-id="d1812-144">O tipo de dados de saída é sempre D3DDECLTYPE \_ FLOAT2.</span><span class="sxs-lookup"><span data-stu-id="d1812-144">The output data type is always D3DDECLTYPE\_FLOAT2.</span></span> <span data-ttu-id="d1812-145">O fluxo de entrada e o deslocamento também são não utilizados (mas devem ser definidos como 0).</span><span class="sxs-lookup"><span data-stu-id="d1812-145">The input stream and offset are also unused (but must be set to 0).</span></span>

</dd> <dt>

<span data-ttu-id="d1812-146"><span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**Pesquisa de D3DDECLMETHOD \_**</span><span class="sxs-lookup"><span data-stu-id="d1812-146"><span id="D3DDECLMETHOD_LOOKUP"></span><span id="d3ddeclmethod_lookup"></span>**D3DDECLMETHOD\_LOOKUP**</span></span>
</dt> <dd>

<span data-ttu-id="d1812-147">Pesquisar um mapa de deslocamento.</span><span class="sxs-lookup"><span data-stu-id="d1812-147">Look up a displacement map.</span></span> <span data-ttu-id="d1812-148">O tipo de entrada pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="d1812-148">The input type can be one of the following:</span></span>

-   <span data-ttu-id="d1812-149">D3DDECLTYPE \_ FLOAT2</span><span class="sxs-lookup"><span data-stu-id="d1812-149">D3DDECLTYPE\_FLOAT2</span></span>
-   <span data-ttu-id="d1812-150">D3DDECLTYPE \_ FLOAT3</span><span class="sxs-lookup"><span data-stu-id="d1812-150">D3DDECLTYPE\_FLOAT3</span></span>
-   <span data-ttu-id="d1812-151">D3DDECLTYPE \_ FLOAT4</span><span class="sxs-lookup"><span data-stu-id="d1812-151">D3DDECLTYPE\_FLOAT4</span></span>

<span data-ttu-id="d1812-152">Somente os componentes. x e. y são usados para a pesquisa de mapa de textura.</span><span class="sxs-lookup"><span data-stu-id="d1812-152">Only the .x and .y components are used for the texture map lookup.</span></span> <span data-ttu-id="d1812-153">O tipo de saída é sempre D3DDECLTYPE \_ FLOAT1.</span><span class="sxs-lookup"><span data-stu-id="d1812-153">The output type is always D3DDECLTYPE\_FLOAT1.</span></span> <span data-ttu-id="d1812-154">O dispositivo deve oferecer suporte ao mapeamento de deslocamento.</span><span class="sxs-lookup"><span data-stu-id="d1812-154">The device must support displacement mapping.</span></span> <span data-ttu-id="d1812-155">Para obter mais informações sobre mapeamento de deslocamento, consulte [mapeamento de deslocamento (Direct3D 9)](displacement-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="d1812-155">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span> <span data-ttu-id="d1812-156">Essa constante é suportada apenas pelo pipeline programável em dados de N-patch, se N-patches estiverem habilitados.</span><span class="sxs-lookup"><span data-stu-id="d1812-156">This constant is supported only by the programmable pipeline on N-patch data, if N-patches are enabled.</span></span>

</dd> <dt>

<span data-ttu-id="d1812-157"><span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**D3DDECLMETHOD \_ LOOKUPPRESAMPLED**</span><span class="sxs-lookup"><span data-stu-id="d1812-157"><span id="D3DDECLMETHOD_LOOKUPPRESAMPLED"></span><span id="d3ddeclmethod_lookuppresampled"></span>**D3DDECLMETHOD\_LOOKUPPRESAMPLED**</span></span>
</dt> <dd>

<span data-ttu-id="d1812-158">Pesquisar um mapa de deslocamento de amostra.</span><span class="sxs-lookup"><span data-stu-id="d1812-158">Look up a presampled displacement map.</span></span> <span data-ttu-id="d1812-159">O tipo de entrada deve ser definido como D3DDECLTYPE \_ não utilizado; o índice de fluxo e o deslocamento do fluxo devem ser definidos como 0.</span><span class="sxs-lookup"><span data-stu-id="d1812-159">The input type must be set to D3DDECLTYPE\_UNUSED; the stream index and the stream offset must be set to 0.</span></span> <span data-ttu-id="d1812-160">O tipo de saída para essa operação é sempre D3DDECLTYPE \_ FLOAT1.</span><span class="sxs-lookup"><span data-stu-id="d1812-160">The output type for this operation is always D3DDECLTYPE\_FLOAT1.</span></span> <span data-ttu-id="d1812-161">O dispositivo deve oferecer suporte ao mapeamento de deslocamento.</span><span class="sxs-lookup"><span data-stu-id="d1812-161">The device must support displacement mapping.</span></span> <span data-ttu-id="d1812-162">Para obter mais informações sobre mapeamento de deslocamento, consulte [mapeamento de deslocamento (Direct3D 9)](displacement-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="d1812-162">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span> <span data-ttu-id="d1812-163">Essa constante é suportada apenas pelo pipeline programável em dados de N-patch, se N-patches estiverem habilitados.</span><span class="sxs-lookup"><span data-stu-id="d1812-163">This constant is supported only by the programmable pipeline on N-patch data, if N-patches are enabled.</span></span> <span data-ttu-id="d1812-164">Esse método pode ser usado somente com o \_ exemplo D3DDECLUSAGE.</span><span class="sxs-lookup"><span data-stu-id="d1812-164">This method can be used only with D3DDECLUSAGE\_SAMPLE.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1812-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1812-165">Remarks</span></span>

<span data-ttu-id="d1812-166">O Tessellator examina o método para determinar quais dados calcular dos dados de vértice durante o mosaico.</span><span class="sxs-lookup"><span data-stu-id="d1812-166">The tessellator looks at the method to determine what data to calculate from the vertex data during tessellation.</span></span> <span data-ttu-id="d1812-167">Os dados de malha devem usar o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="d1812-167">Mesh data should use the default value.</span></span> <span data-ttu-id="d1812-168">Os patches podem usar qualquer um dos outros tipos implementados.</span><span class="sxs-lookup"><span data-stu-id="d1812-168">Patches can use any of the other implemented types.</span></span>

<span data-ttu-id="d1812-169">Os dados de vértice são declarados com uma matriz de estruturas [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) .</span><span class="sxs-lookup"><span data-stu-id="d1812-169">Vertex data is declared with an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures.</span></span> <span data-ttu-id="d1812-170">Cada elemento na matriz contém um método de declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="d1812-170">Each element in the array contains a vertex declaration method.</span></span>

<span data-ttu-id="d1812-171">Além de usar \_ o padrão D3DDECLMETHOD, uma malha normal pode usar os \_ métodos D3DDECLMETHOD Lookup e D3DDECLMETHOD \_ LOOKUPPRESAMPLED quando N-patches estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="d1812-171">In addition to using D3DDECLMETHOD\_DEFAULT, a normal mesh can use D3DDECLMETHOD\_LOOKUP and D3DDECLMETHOD\_LOOKUPPRESAMPLED methods when N-patches are enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1812-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1812-172">Requirements</span></span>



| <span data-ttu-id="d1812-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1812-173">Requirement</span></span> | <span data-ttu-id="d1812-174">Valor</span><span class="sxs-lookup"><span data-stu-id="d1812-174">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1812-175">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1812-175">Header</span></span><br/> | <dl> <span data-ttu-id="d1812-176"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1812-176"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1812-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1812-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1812-178">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="d1812-178">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




