---
description: Define as configurações usadas para computações de quadro tangente de malha.
ms.assetid: b525b4cc-9a2d-4569-bae8-7cc7f7832cbc
title: Enumeração D3DXTANGENT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTANGENT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 43e3c5ced0eee3366b85070ce89d19154d048ab4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798458"
---
# <a name="d3dxtangent-enumeration"></a><span data-ttu-id="54e8d-103">Enumeração D3DXTANGENT</span><span class="sxs-lookup"><span data-stu-id="54e8d-103">D3DXTANGENT enumeration</span></span>

<span data-ttu-id="54e8d-104">Define as configurações usadas para computações de quadro tangente de malha.</span><span class="sxs-lookup"><span data-stu-id="54e8d-104">Defines settings used for mesh tangent frame computations.</span></span>

## <a name="syntax"></a><span data-ttu-id="54e8d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="54e8d-105">Syntax</span></span>


```C++
typedef enum D3DXTANGENT { 
  D3DXTANGENT_WRAP_U                   = 0x01,
  D3DXTANGENT_WRAP_V                   = 0x02,
  D3DXTANGENT_WRAP_UV                  = 0x03,
  D3DXTANGENT_DONT_NORMALIZE_PARTIALS  = 0x04,
  D3DXTANGENT_DONT_ORTHOGONALIZE       = 0x08,
  D3DXTANGENT_ORTHOGONALIZE_FROM_V     = 0x010,
  D3DXTANGENT_ORTHOGONALIZE_FROM_U     = 0x020,
  D3DXTANGENT_WEIGHT_BY_AREA           = 0x040,
  D3DXTANGENT_WEIGHT_EQUAL             = 0x080,
  D3DXTANGENT_WIND_CW                  = 0x0100,
  D3DXTANGENT_CALCULATE_NORMALS        = 0x0200,
  D3DXTANGENT_GENERATE_IN_PLACE        = 0x0400
} D3DXTANGENT, *LPD3DXTANGENT;
```



## <a name="constants"></a><span data-ttu-id="54e8d-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="54e8d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="54e8d-107"><span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT \_ Wrap \_ U**</span><span class="sxs-lookup"><span data-stu-id="54e8d-107"><span id="D3DXTANGENT_WRAP_U"></span><span id="d3dxtangent_wrap_u"></span>**D3DXTANGENT\_WRAP\_U**</span></span>
</dt> <dd>

<span data-ttu-id="54e8d-108">Os valores de coordenadas de textura na direção u estão entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="54e8d-108">Texture coordinate values in the u direction are between 0 and 1.</span></span> <span data-ttu-id="54e8d-109">Nesse caso, um conjunto de coordenadas de textura será escolhido para minimizar o perímetro do triângulo.</span><span class="sxs-lookup"><span data-stu-id="54e8d-109">In this case a texture coordinate set will be chosen that minimizes the perimeter of the triangle.</span></span> <span data-ttu-id="54e8d-110">Consulte [quebra de textura (Direct3D 9)](texture-wrapping.md).</span><span class="sxs-lookup"><span data-stu-id="54e8d-110">See [Texture Wrapping (Direct3D 9)](texture-wrapping.md).</span></span>

</dd> <dt>

<span data-ttu-id="54e8d-111"><span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT \_ Wrap \_ V**</span><span class="sxs-lookup"><span data-stu-id="54e8d-111"><span id="D3DXTANGENT_WRAP_V"></span><span id="d3dxtangent_wrap_v"></span>**D3DXTANGENT\_WRAP\_V**</span></span>
</dt> <dd>

<span data-ttu-id="54e8d-112">Os valores de coordenadas de textura na direção v estão entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="54e8d-112">Texture coordinate values in the v direction are between 0 and 1.</span></span> <span data-ttu-id="54e8d-113">Nesse caso, um conjunto de coordenadas de textura será escolhido para minimizar o perímetro do triângulo.</span><span class="sxs-lookup"><span data-stu-id="54e8d-113">In this case a texture coordinate set will be chosen that minimizes the perimeter of the triangle.</span></span> <span data-ttu-id="54e8d-114">Consulte [quebra de textura (Direct3D 9)](texture-wrapping.md).</span><span class="sxs-lookup"><span data-stu-id="54e8d-114">See [Texture Wrapping (Direct3D 9)](texture-wrapping.md).</span></span>

</dd> <dt>

<span data-ttu-id="54e8d-115"><span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**\_UV de encapsulamento D3DXTANGENT \_**</span><span class="sxs-lookup"><span data-stu-id="54e8d-115"><span id="D3DXTANGENT_WRAP_UV"></span><span id="d3dxtangent_wrap_uv"></span>**D3DXTANGENT\_WRAP\_UV**</span></span>
</dt> <dd>

<span data-ttu-id="54e8d-116">Os valores de coordenadas de textura nas direções você e v estão entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="54e8d-116">Texture coordinate values in both u and v directions are between 0 and 1.</span></span> <span data-ttu-id="54e8d-117">Nesse caso, um conjunto de coordenadas de textura será escolhido para minimizar o perímetro do triângulo.</span><span class="sxs-lookup"><span data-stu-id="54e8d-117">In this case a texture coordinate set will be chosen that minimizes the perimeter of the triangle.</span></span> <span data-ttu-id="54e8d-118">Consulte [quebra de textura (Direct3D 9)](texture-wrapping.md).</span><span class="sxs-lookup"><span data-stu-id="54e8d-118">See [Texture Wrapping (Direct3D 9)](texture-wrapping.md).</span></span>

</dd> <dt>

<span data-ttu-id="54e8d-119"><span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT \_ não \_ normalizar \_ parciais**</span><span class="sxs-lookup"><span data-stu-id="54e8d-119"><span id="D3DXTANGENT_DONT_NORMALIZE_PARTIALS"></span><span id="d3dxtangent_dont_normalize_partials"></span>**D3DXTANGENT\_DONT\_NORMALIZE\_PARTIALS**</span></span>
</dt> <dd>

<span data-ttu-id="54e8d-120">Não normalizar derivações parciais em relação às coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="54e8d-120">Do not normalize partial derivatives with respect to texture coordinates.</span></span> <span data-ttu-id="54e8d-121">Se não for normalizado, a escala dos derivativos parciais será proporcional à escala do modelo 3D dividido pela escala do triângulo no espaço (u, v).</span><span class="sxs-lookup"><span data-stu-id="54e8d-121">If not normalized, the scale of the partial derivatives is proportional to the scale of the 3D model divided by the scale of the triangle in (u, v) space.</span></span> <span data-ttu-id="54e8d-122">Esse valor de escala fornece uma medida de quanto a textura é ampliada em uma determinada direção.</span><span class="sxs-lookup"><span data-stu-id="54e8d-122">This scale value provides a measure of how much the texture is stretched in a given direction.</span></span> <span data-ttu-id="54e8d-123">O comprimento de vetor resultante é uma soma ponderada dos comprimentos dos derivativos parciais.</span><span class="sxs-lookup"><span data-stu-id="54e8d-123">The resulting vector length is a weighted sum of the lengths of the partial derivatives.</span></span>

</dd> <dt>

<span data-ttu-id="54e8d-124"><span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT \_ não \_ ortogonalize**</span><span class="sxs-lookup"><span data-stu-id="54e8d-124"><span id="D3DXTANGENT_DONT_ORTHOGONALIZE"></span><span id="d3dxtangent_dont_orthogonalize"></span>**D3DXTANGENT\_DONT\_ORTHOGONALIZE**</span></span>
</dt> <dd>

<span data-ttu-id="54e8d-125">Não transforme coordenadas de textura em coordenadas cartesianas ortogonal.</span><span class="sxs-lookup"><span data-stu-id="54e8d-125">Do not transform texture coordinates to orthogonal Cartesian coordinates.</span></span> <span data-ttu-id="54e8d-126">Mutuamente exclusivo com D3DXTANGENT \_ ortogonale \_ de \_ você e D3DXTANGENT \_ ortogonalize \_ da \_ V.</span><span class="sxs-lookup"><span data-stu-id="54e8d-126">Mutually exclusive with D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V.</span></span>

</dd> <dt>

<span data-ttu-id="54e8d-127"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**D3DXTANGENT \_ ortogonalize \_ da \_ V**</span><span class="sxs-lookup"><span data-stu-id="54e8d-127"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_V"></span><span id="d3dxtangent_orthogonalize_from_v"></span>**D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V**</span></span>
</dt> <dd>

<span data-ttu-id="54e8d-128">Compute a derivada parcial em relação à coordenada de textura v de forma independente para cada vértice e, em seguida, computar a derivada parcial com relação a você como o produto cruzado da derivada parcial em relação ao v e ao vetor normal.</span><span class="sxs-lookup"><span data-stu-id="54e8d-128">Compute the partial derivative with respect to texture coordinate v independently for each vertex, and then compute the partial derivative with respect to u as the cross product of the partial derivative with respect to v and the normal vector.</span></span> <span data-ttu-id="54e8d-129">Mutuamente exclusivo com D3DXTANGENT não \_ é \_ ortogonalize e D3DXTANGENT \_ ortogonalize a \_ partir de \_ U.</span><span class="sxs-lookup"><span data-stu-id="54e8d-129">Mutually exclusive with D3DXTANGENT\_DONT\_ORTHOGONALIZE and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U.</span></span>

</dd> <dt>

<span data-ttu-id="54e8d-130"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**D3DXTANGENT \_ ortogonale \_ de \_ U**</span><span class="sxs-lookup"><span data-stu-id="54e8d-130"><span id="D3DXTANGENT_ORTHOGONALIZE_FROM_U"></span><span id="d3dxtangent_orthogonalize_from_u"></span>**D3DXTANGENT\_ORTHOGONALIZE\_FROM\_U**</span></span>
</dt> <dd>

<span data-ttu-id="54e8d-131">Compute a derivada parcial em relação à coordenada de textura u independentemente para cada vértice e, em seguida, computar a derivada parcial com relação a v como o produto cruzado do vetor normal e o derivativo parcial em relação a você.</span><span class="sxs-lookup"><span data-stu-id="54e8d-131">Compute the partial derivative with respect to texture coordinate u independently for each vertex, and then compute the partial derivative with respect to v as the cross product of the normal vector and the partial derivative with respect to u.</span></span> <span data-ttu-id="54e8d-132">Mutuamente exclusivo com D3DXTANGENT não \_ é \_ ortogonalize e D3DXTANGENT \_ ortogonalize \_ da \_ V.</span><span class="sxs-lookup"><span data-stu-id="54e8d-132">Mutually exclusive with D3DXTANGENT\_DONT\_ORTHOGONALIZE and D3DXTANGENT\_ORTHOGONALIZE\_FROM\_V.</span></span>

</dd> <dt>

<span data-ttu-id="54e8d-133"><span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**\_Peso D3DXTANGENT \_ por \_ área**</span><span class="sxs-lookup"><span data-stu-id="54e8d-133"><span id="D3DXTANGENT_WEIGHT_BY_AREA"></span><span id="d3dxtangent_weight_by_area"></span>**D3DXTANGENT\_WEIGHT\_BY\_AREA**</span></span>
</dt> <dd>

<span data-ttu-id="54e8d-134">Peso a direção do vetor derivado normal ou parcial por vértice de acordo com as áreas de triângulos anexadas a esse vértice.</span><span class="sxs-lookup"><span data-stu-id="54e8d-134">Weight the direction of the computed per-vertex normal or partial derivative vector according to the areas of triangles attached to that vertex.</span></span> <span data-ttu-id="54e8d-135">Mutuamente exclusivo com peso D3DXTANGENT \_ \_ igual.</span><span class="sxs-lookup"><span data-stu-id="54e8d-135">Mutually exclusive with D3DXTANGENT\_WEIGHT\_EQUAL.</span></span>

</dd> <dt>

<span data-ttu-id="54e8d-136"><span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**\_Peso D3DXTANGENT \_ igual**</span><span class="sxs-lookup"><span data-stu-id="54e8d-136"><span id="D3DXTANGENT_WEIGHT_EQUAL"></span><span id="d3dxtangent_weight_equal"></span>**D3DXTANGENT\_WEIGHT\_EQUAL**</span></span>
</dt> <dd>

<span data-ttu-id="54e8d-137">Compute um vetor normal de comprimento de unidade para cada triângulo da malha de entrada.</span><span class="sxs-lookup"><span data-stu-id="54e8d-137">Compute a unit-length normal vector for each triangle of the input mesh.</span></span> <span data-ttu-id="54e8d-138">Mutuamente exclusivo com peso D3DXTANGENT \_ \_ por \_ área.</span><span class="sxs-lookup"><span data-stu-id="54e8d-138">Mutually exclusive with D3DXTANGENT\_WEIGHT\_BY\_AREA.</span></span>

</dd> <dt>

<span data-ttu-id="54e8d-139"><span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**\_PV de vento D3DXTANGENT \_**</span><span class="sxs-lookup"><span data-stu-id="54e8d-139"><span id="D3DXTANGENT_WIND_CW"></span><span id="d3dxtangent_wind_cw"></span>**D3DXTANGENT\_WIND\_CW**</span></span>
</dt> <dd>

<span data-ttu-id="54e8d-140">Os vértices são ordenados em uma direção horária em volta de cada triângulo.</span><span class="sxs-lookup"><span data-stu-id="54e8d-140">Vertices are ordered in a clockwise direction around each triangle.</span></span> <span data-ttu-id="54e8d-141">Portanto, a direção de vetor normal calculada é invertida 180 graus a partir da direção calculada usando a ordenação de vértices no sentido anti-horário.</span><span class="sxs-lookup"><span data-stu-id="54e8d-141">The computed normal vector direction is therefore inverted 180 degrees from the direction computed using counterclockwise vertex ordering.</span></span>

</dd> <dt>

<span data-ttu-id="54e8d-142"><span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT \_ calcular \_ Normals**</span><span class="sxs-lookup"><span data-stu-id="54e8d-142"><span id="D3DXTANGENT_CALCULATE_NORMALS"></span><span id="d3dxtangent_calculate_normals"></span>**D3DXTANGENT\_CALCULATE\_NORMALS**</span></span>
</dt> <dd>

<span data-ttu-id="54e8d-143">Calcule o vetor normal por vértice para cada triângulo da malha de entrada e ignore todos os vetores normais já existentes na malha de entrada.</span><span class="sxs-lookup"><span data-stu-id="54e8d-143">Compute the per-vertex normal vector for each triangle of the input mesh, and ignore any normal vectors already in the input mesh.</span></span>

</dd> <dt>

<span data-ttu-id="54e8d-144"><span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT \_ gerar \_ no \_ local**</span><span class="sxs-lookup"><span data-stu-id="54e8d-144"><span id="D3DXTANGENT_GENERATE_IN_PLACE"></span><span id="d3dxtangent_generate_in_place"></span>**D3DXTANGENT\_GENERATE\_IN\_PLACE**</span></span>
</dt> <dd>

<span data-ttu-id="54e8d-145">Os resultados são armazenados na malha de entrada original e a malha de saída não é usada.</span><span class="sxs-lookup"><span data-stu-id="54e8d-145">The results are stored in the original input mesh, and the output mesh is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="54e8d-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54e8d-146">Requirements</span></span>



| <span data-ttu-id="54e8d-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="54e8d-147">Requirement</span></span> | <span data-ttu-id="54e8d-148">Valor</span><span class="sxs-lookup"><span data-stu-id="54e8d-148">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54e8d-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="54e8d-149">Header</span></span><br/> | <dl> <span data-ttu-id="54e8d-150"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="54e8d-150"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54e8d-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="54e8d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54e8d-152">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="54e8d-152">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="54e8d-153">**D3DXComputeTangentFrameEx**</span><span class="sxs-lookup"><span data-stu-id="54e8d-153">**D3DXComputeTangentFrameEx**</span></span>](d3dxcomputetangentframeex.md)
</dt> </dl>

 

 




