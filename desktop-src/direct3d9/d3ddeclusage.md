---
description: Identifica o uso pretendido de dados de vértice.
ms.assetid: ee9b46c2-b779-480c-9b5c-6d189d2af014
title: Enumeração D3DDECLUSAGE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLUSAGE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f3997aa38a7a97455b9f36d8afbee896ca9ae937
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105802149"
---
# <a name="d3ddeclusage-enumeration"></a><span data-ttu-id="fd71a-103">Enumeração D3DDECLUSAGE</span><span class="sxs-lookup"><span data-stu-id="fd71a-103">D3DDECLUSAGE enumeration</span></span>

<span data-ttu-id="fd71a-104">Identifica o uso pretendido de dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="fd71a-104">Identifies the intended use of vertex data.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd71a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd71a-105">Syntax</span></span>


```C++
typedef enum D3DDECLUSAGE { 
  D3DDECLUSAGE_POSITION      = 0,
  D3DDECLUSAGE_BLENDWEIGHT   = 1,
  D3DDECLUSAGE_BLENDINDICES  = 2,
  D3DDECLUSAGE_NORMAL        = 3,
  D3DDECLUSAGE_PSIZE         = 4,
  D3DDECLUSAGE_TEXCOORD      = 5,
  D3DDECLUSAGE_TANGENT       = 6,
  D3DDECLUSAGE_BINORMAL      = 7,
  D3DDECLUSAGE_TESSFACTOR    = 8,
  D3DDECLUSAGE_POSITIONT     = 9,
  D3DDECLUSAGE_COLOR         = 10,
  D3DDECLUSAGE_FOG           = 11,
  D3DDECLUSAGE_DEPTH         = 12,
  D3DDECLUSAGE_SAMPLE        = 13
} D3DDECLUSAGE, *LPD3DDECLUSAGE;
```



## <a name="constants"></a><span data-ttu-id="fd71a-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="fd71a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fd71a-107"><span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**\_Posição D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="fd71a-107"><span id="D3DDECLUSAGE_POSITION"></span><span id="d3ddeclusage_position"></span>**D3DDECLUSAGE\_POSITION**</span></span>
</dt> <dd>

<span data-ttu-id="fd71a-108">Posicionar dados variando de (-1,-1) a (1, 1).</span><span class="sxs-lookup"><span data-stu-id="fd71a-108">Position data ranging from (-1,-1) to (1,1).</span></span> <span data-ttu-id="fd71a-109">Use a \_ posição D3DDECLUSAGE com um índice de uso de 0 para especificar a posição não transformada para o processamento de vértice de função fixa e o n-patch Tessellator.</span><span class="sxs-lookup"><span data-stu-id="fd71a-109">Use D3DDECLUSAGE\_POSITION with a usage index of 0 to specify untransformed position for fixed function vertex processing and the n-patch tessellator.</span></span> <span data-ttu-id="fd71a-110">Use a \_ posição D3DDECLUSAGE com um índice de uso de 1 para especificar a posição não transformada no sombreador de vértice de função fixa para a interpolação de vértice.</span><span class="sxs-lookup"><span data-stu-id="fd71a-110">Use D3DDECLUSAGE\_POSITION with a usage index of 1 to specify untransformed position in the fixed function vertex shader for vertex tweening.</span></span>

</dd> <dt>

<span data-ttu-id="fd71a-111"><span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**D3DDECLUSAGE \_ BLENDWEIGHT**</span><span class="sxs-lookup"><span data-stu-id="fd71a-111"><span id="D3DDECLUSAGE_BLENDWEIGHT"></span><span id="d3ddeclusage_blendweight"></span>**D3DDECLUSAGE\_BLENDWEIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="fd71a-112">Mesclagem de dados de peso.</span><span class="sxs-lookup"><span data-stu-id="fd71a-112">Blending weight data.</span></span> <span data-ttu-id="fd71a-113">Use D3DDECLUSAGE \_ BLENDWEIGHT com um índice de uso de 0 para especificar os pesos de mistura usados em mistura de vértice indexada e não indexada.</span><span class="sxs-lookup"><span data-stu-id="fd71a-113">Use D3DDECLUSAGE\_BLENDWEIGHT with a usage index of 0 to specify the blend weights used in indexed and nonindexed vertex blending.</span></span>

</dd> <dt>

<span data-ttu-id="fd71a-114"><span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**D3DDECLUSAGE \_ BLENDINDICES**</span><span class="sxs-lookup"><span data-stu-id="fd71a-114"><span id="D3DDECLUSAGE_BLENDINDICES"></span><span id="d3ddeclusage_blendindices"></span>**D3DDECLUSAGE\_BLENDINDICES**</span></span>
</dt> <dd>

<span data-ttu-id="fd71a-115">Mesclando dados de índices.</span><span class="sxs-lookup"><span data-stu-id="fd71a-115">Blending indices data.</span></span> <span data-ttu-id="fd71a-116">Use D3DDECLUSAGE \_ BLENDINDICES com um índice de uso de 0 para especificar índices de matrizes para a dicapação da paleta indexada.</span><span class="sxs-lookup"><span data-stu-id="fd71a-116">Use D3DDECLUSAGE\_BLENDINDICES with a usage index of 0 to specify matrix indices for indexed paletted skinning.</span></span>

</dd> <dt>

<span data-ttu-id="fd71a-117"><span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**D3DDECLUSAGE \_ normal**</span><span class="sxs-lookup"><span data-stu-id="fd71a-117"><span id="D3DDECLUSAGE_NORMAL"></span><span id="d3ddeclusage_normal"></span>**D3DDECLUSAGE\_NORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="fd71a-118">Dados normais de vértice.</span><span class="sxs-lookup"><span data-stu-id="fd71a-118">Vertex normal data.</span></span> <span data-ttu-id="fd71a-119">Use D3DDECLUSAGE \_ normal com um índice de uso de 0 para especificar Normals de vértice para processamento de vértice de função fixa e o n-patch Tessellator.</span><span class="sxs-lookup"><span data-stu-id="fd71a-119">Use D3DDECLUSAGE\_NORMAL with a usage index of 0 to specify vertex normals for fixed function vertex processing and the n-patch tessellator.</span></span> <span data-ttu-id="fd71a-120">Use D3DDECLUSAGE \_ normal com um índice de uso de 1 para especificar os Normals de vértice para o processamento de vértice de função fixa para a interpolação de vértice.</span><span class="sxs-lookup"><span data-stu-id="fd71a-120">Use D3DDECLUSAGE\_NORMAL with a usage index of 1 to specify vertex normals for fixed function vertex processing for vertex tweening.</span></span>

</dd> <dt>

<span data-ttu-id="fd71a-121"><span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**D3DDECLUSAGE \_ PSIZE**</span><span class="sxs-lookup"><span data-stu-id="fd71a-121"><span id="D3DDECLUSAGE_PSIZE"></span><span id="d3ddeclusage_psize"></span>**D3DDECLUSAGE\_PSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="fd71a-122">Dados de tamanho do ponto.</span><span class="sxs-lookup"><span data-stu-id="fd71a-122">Point size data.</span></span> <span data-ttu-id="fd71a-123">Use D3DDECLUSAGE \_ PSIZE com um índice de uso de 0 para especificar o atributo de tamanho de ponto usado pelo mecanismo de instalação do rasterizador para expandir um ponto em um Quad para a funcionalidade Point-Sprite.</span><span class="sxs-lookup"><span data-stu-id="fd71a-123">Use D3DDECLUSAGE\_PSIZE with a usage index of 0 to specify the point-size attribute used by the setup engine of the rasterizer to expand a point into a quad for the point-sprite functionality.</span></span>

</dd> <dt>

<span data-ttu-id="fd71a-124"><span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**D3DDECLUSAGE \_ TEXCOORD**</span><span class="sxs-lookup"><span data-stu-id="fd71a-124"><span id="D3DDECLUSAGE_TEXCOORD"></span><span id="d3ddeclusage_texcoord"></span>**D3DDECLUSAGE\_TEXCOORD**</span></span>
</dt> <dd>

<span data-ttu-id="fd71a-125">Dados de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="fd71a-125">Texture coordinate data.</span></span> <span data-ttu-id="fd71a-126">Use D3DDECLUSAGE \_ TEXCOORD, n para especificar coordenadas de textura no processamento de vértice de função fixa e em sombreadores de pixel antes do PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="fd71a-126">Use D3DDECLUSAGE\_TEXCOORD, n to specify texture coordinates in fixed function vertex processing and in pixel shaders prior to ps\_3\_0.</span></span> <span data-ttu-id="fd71a-127">Eles podem ser usados para passar dados definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="fd71a-127">These can be used to pass user defined data.</span></span>

</dd> <dt>

<span data-ttu-id="fd71a-128"><span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**\_TANGENTE D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="fd71a-128"><span id="D3DDECLUSAGE_TANGENT"></span><span id="d3ddeclusage_tangent"></span>**D3DDECLUSAGE\_TANGENT**</span></span>
</dt> <dd>

<span data-ttu-id="fd71a-129">Dados da tangente do vértice.</span><span class="sxs-lookup"><span data-stu-id="fd71a-129">Vertex tangent data.</span></span>

</dd> <dt>

<span data-ttu-id="fd71a-130"><span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**D3DDECLUSAGE \_ BInormal**</span><span class="sxs-lookup"><span data-stu-id="fd71a-130"><span id="D3DDECLUSAGE_BINORMAL"></span><span id="d3ddeclusage_binormal"></span>**D3DDECLUSAGE\_BINORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="fd71a-131">Dados binormal do vértice.</span><span class="sxs-lookup"><span data-stu-id="fd71a-131">Vertex binormal data.</span></span>

</dd> <dt>

<span data-ttu-id="fd71a-132"><span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**D3DDECLUSAGE \_ TESSFACTOR**</span><span class="sxs-lookup"><span data-stu-id="fd71a-132"><span id="D3DDECLUSAGE_TESSFACTOR"></span><span id="d3ddeclusage_tessfactor"></span>**D3DDECLUSAGE\_TESSFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="fd71a-133">Valor de ponto flutuante único positivo.</span><span class="sxs-lookup"><span data-stu-id="fd71a-133">Single positive floating point value.</span></span> <span data-ttu-id="fd71a-134">Use D3DDECLUSAGE \_ TESSFACTOR com um índice de uso de 0 para especificar um fator de mosaico usado na unidade de mosaico para controlar a taxa de mosaico.</span><span class="sxs-lookup"><span data-stu-id="fd71a-134">Use D3DDECLUSAGE\_TESSFACTOR with a usage index of 0 to specify a tessellation factor used in the tessellation unit to control the rate of tessellation.</span></span> <span data-ttu-id="fd71a-135">Para obter mais informações sobre o tipo de dados, consulte D3DDECLTYPE \_ FLOAT1.</span><span class="sxs-lookup"><span data-stu-id="fd71a-135">For more information about the data type, see D3DDECLTYPE\_FLOAT1.</span></span>

</dd> <dt>

<span data-ttu-id="fd71a-136"><span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**Posição de D3DDECLUSAGE \_**</span><span class="sxs-lookup"><span data-stu-id="fd71a-136"><span id="D3DDECLUSAGE_POSITIONT"></span><span id="d3ddeclusage_positiont"></span>**D3DDECLUSAGE\_POSITIONT**</span></span>
</dt> <dd>

<span data-ttu-id="fd71a-137">Os dados de vértice contêm dados de posição transformados que variam de (0, 0) a (largura do visor, altura do visor).</span><span class="sxs-lookup"><span data-stu-id="fd71a-137">Vertex data contains transformed position data ranging from (0,0) to (viewport width, viewport height).</span></span> <span data-ttu-id="fd71a-138">Use D3DDECLUSAGE \_ positionout com um índice de uso de 0 para especificar a posição transformada.</span><span class="sxs-lookup"><span data-stu-id="fd71a-138">Use D3DDECLUSAGE\_POSITIONT with a usage index of 0 to specify transformed position.</span></span> <span data-ttu-id="fd71a-139">Quando uma declaração que contém isso é definida, o pipeline não executa o processamento de vértice.</span><span class="sxs-lookup"><span data-stu-id="fd71a-139">When a declaration containing this is set, the pipeline does not perform vertex processing.</span></span>

</dd> <dt>

<span data-ttu-id="fd71a-140"><span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**\_Cor D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="fd71a-140"><span id="D3DDECLUSAGE_COLOR"></span><span id="d3ddeclusage_color"></span>**D3DDECLUSAGE\_COLOR**</span></span>
</dt> <dd>

<span data-ttu-id="fd71a-141">Os dados de vértice contêm a cor difusa ou especular.</span><span class="sxs-lookup"><span data-stu-id="fd71a-141">Vertex data contains diffuse or specular color.</span></span> <span data-ttu-id="fd71a-142">Use a \_ cor de D3DDECLUSAGE com um índice de uso de 0 para especificar a cor difusa no sombreador de vértices da função fixa e sombreadores de pixel antes do PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="fd71a-142">Use D3DDECLUSAGE\_COLOR with a usage index of 0 to specify the diffuse color in the fixed function vertex shader and pixel shaders prior to ps\_3\_0.</span></span> <span data-ttu-id="fd71a-143">Use a \_ cor de D3DDECLUSAGE com um índice de uso de 1 para especificar a cor especular no sombreador de vértices da função fixa e sombreadores de pixel antes do PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="fd71a-143">Use D3DDECLUSAGE\_COLOR with a usage index of 1 to specify the specular color in the fixed function vertex shader and pixel shaders prior to ps\_3\_0.</span></span>

</dd> <dt>

<span data-ttu-id="fd71a-144"><span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**\_Neblina D3DDECLUSAGE**</span><span class="sxs-lookup"><span data-stu-id="fd71a-144"><span id="D3DDECLUSAGE_FOG"></span><span id="d3ddeclusage_fog"></span>**D3DDECLUSAGE\_FOG**</span></span>
</dt> <dd>

<span data-ttu-id="fd71a-145">Os dados de vértice contêm dados de neblina.</span><span class="sxs-lookup"><span data-stu-id="fd71a-145">Vertex data contains fog data.</span></span> <span data-ttu-id="fd71a-146">Use a \_ neblina D3DDECLUSAGE com um índice de uso de 0 para especificar um valor de mistura de neblina usado após a conclusão do sombreamento de pixel.</span><span class="sxs-lookup"><span data-stu-id="fd71a-146">Use D3DDECLUSAGE\_FOG with a usage index of 0 to specify a fog blend value used after pixel shading finishes.</span></span> <span data-ttu-id="fd71a-147">Isso se aplica a sombreadores de pixel antes da versão PS \_ 3 \_ 0.</span><span class="sxs-lookup"><span data-stu-id="fd71a-147">This applies to pixel shaders prior to version ps\_3\_0.</span></span>

</dd> <dt>

<span data-ttu-id="fd71a-148"><span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**Profundidade de D3DDECLUSAGE \_**</span><span class="sxs-lookup"><span data-stu-id="fd71a-148"><span id="D3DDECLUSAGE_DEPTH"></span><span id="d3ddeclusage_depth"></span>**D3DDECLUSAGE\_DEPTH**</span></span>
</dt> <dd>

<span data-ttu-id="fd71a-149">Os dados de vértice contêm dados de profundidade.</span><span class="sxs-lookup"><span data-stu-id="fd71a-149">Vertex data contains depth data.</span></span>

</dd> <dt>

<span data-ttu-id="fd71a-150"><span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**Exemplo de D3DDECLUSAGE \_**</span><span class="sxs-lookup"><span data-stu-id="fd71a-150"><span id="D3DDECLUSAGE_SAMPLE"></span><span id="d3ddeclusage_sample"></span>**D3DDECLUSAGE\_SAMPLE**</span></span>
</dt> <dd>

<span data-ttu-id="fd71a-151">Os dados de vértice contêm dados de amostra.</span><span class="sxs-lookup"><span data-stu-id="fd71a-151">Vertex data contains sampler data.</span></span> <span data-ttu-id="fd71a-152">Use \_ o exemplo D3DDECLUSAGE com um índice de uso de 0 para especificar o valor de deslocamento a ser pesquisado.</span><span class="sxs-lookup"><span data-stu-id="fd71a-152">Use D3DDECLUSAGE\_SAMPLE with a usage index of 0 to specify the displacement value to look up.</span></span> <span data-ttu-id="fd71a-153">Ele pode ser usado somente com D3DDECLUSAGE \_ LOOKUPPRESAMPLED ou D3DDECLUSAGE \_ Lookup.</span><span class="sxs-lookup"><span data-stu-id="fd71a-153">It can be used only with D3DDECLUSAGE\_LOOKUPPRESAMPLED or D3DDECLUSAGE\_LOOKUP.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fd71a-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd71a-154">Remarks</span></span>

<span data-ttu-id="fd71a-155">Os dados de vértice são declarados com uma matriz de estruturas [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) .</span><span class="sxs-lookup"><span data-stu-id="fd71a-155">Vertex data is declared with an array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) structures.</span></span> <span data-ttu-id="fd71a-156">Cada elemento na matriz contém um tipo de uso.</span><span class="sxs-lookup"><span data-stu-id="fd71a-156">Each element in the array contains a usage type.</span></span>

<span data-ttu-id="fd71a-157">Para obter mais informações sobre declarações de vértice, consulte [declaração de vértice (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="fd71a-157">For more information about vertex declarations, see [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fd71a-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd71a-158">Requirements</span></span>



| <span data-ttu-id="fd71a-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd71a-159">Requirement</span></span> | <span data-ttu-id="fd71a-160">Valor</span><span class="sxs-lookup"><span data-stu-id="fd71a-160">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd71a-161">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fd71a-161">Header</span></span><br/> | <dl> <span data-ttu-id="fd71a-162"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd71a-162"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd71a-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd71a-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd71a-164">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="fd71a-164">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="fd71a-165">Declaração de vértice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fd71a-165">Vertex Declaration (Direct3D 9)</span></span>](vertex-declaration.md)
</dt> </dl>

 

 




