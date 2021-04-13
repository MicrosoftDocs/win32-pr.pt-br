---
description: Avalia uma luz esférica e retorna dados Spectral esféricos (SH).
ms.assetid: e2a2b998-285a-46ef-99fe-ccc923013e9a
title: Função D3DXSHEvalSphericalLight (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalSphericalLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c658480a08360fe8489cfc86319a689e828c0a1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298766"
---
# <a name="d3dxshevalsphericallight-function-d3dx10h"></a><span data-ttu-id="e4cac-103">Função D3DXSHEvalSphericalLight (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="e4cac-103">D3DXSHEvalSphericalLight function (D3DX10.h)</span></span>

<span data-ttu-id="e4cac-104">Avalia uma luz esférica e retorna dados Spectral esféricos (SH).</span><span class="sxs-lookup"><span data-stu-id="e4cac-104">Evaluates a spherical light and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4cac-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4cac-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalSphericalLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pPos,
  _In_       FLOAT       Radius,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="e4cac-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4cac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4cac-107">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4cac-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4cac-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4cac-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4cac-109">Ordem da avaliação SH.</span><span class="sxs-lookup"><span data-stu-id="e4cac-109">Order of the SH evaluation.</span></span> <span data-ttu-id="e4cac-110">Deve estar no intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="e4cac-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="e4cac-111">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="e4cac-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="e4cac-112">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="e4cac-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="e4cac-113">*pPos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4cac-113">*pPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4cac-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4cac-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e4cac-115">Ponteiro para a posição da luz.</span><span class="sxs-lookup"><span data-stu-id="e4cac-115">Pointer to the light position.</span></span>

</dd> <dt>

<span data-ttu-id="e4cac-116">*RADIUS* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4cac-116">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4cac-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4cac-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4cac-118">Raio da fonte de luz esférica.</span><span class="sxs-lookup"><span data-stu-id="e4cac-118">Radius of spherical light source.</span></span>

</dd> <dt>

<span data-ttu-id="e4cac-119">*RIntensity* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4cac-119">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4cac-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4cac-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4cac-121">A intensidade vermelha da luz.</span><span class="sxs-lookup"><span data-stu-id="e4cac-121">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="e4cac-122">*GIntensity* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4cac-122">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4cac-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4cac-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4cac-124">A intensidade verde da luz.</span><span class="sxs-lookup"><span data-stu-id="e4cac-124">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="e4cac-125">*BIntensity* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4cac-125">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4cac-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e4cac-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e4cac-127">A intensidade azul da luz.</span><span class="sxs-lookup"><span data-stu-id="e4cac-127">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="e4cac-128">*pROut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4cac-128">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4cac-129">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4cac-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e4cac-130">Ponteiro para o vetor SH de saída para o componente vermelho.</span><span class="sxs-lookup"><span data-stu-id="e4cac-130">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="e4cac-131">*pGOut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4cac-131">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4cac-132">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4cac-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e4cac-133">Ponteiro para o vetor SH de saída para o componente verde.</span><span class="sxs-lookup"><span data-stu-id="e4cac-133">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="e4cac-134">*pBOut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4cac-134">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4cac-135">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4cac-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e4cac-136">Ponteiro para o vetor SH de saída para o componente azul.</span><span class="sxs-lookup"><span data-stu-id="e4cac-136">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4cac-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4cac-137">Return value</span></span>

<span data-ttu-id="e4cac-138">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e4cac-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e4cac-139">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e4cac-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e4cac-140">Se a função falhar, o valor de retorno poderá ser: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="e4cac-140">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4cac-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4cac-141">Remarks</span></span>

<span data-ttu-id="e4cac-142">Avalia uma luz esférica e retorna dados de Spectral SH.</span><span class="sxs-lookup"><span data-stu-id="e4cac-142">Evaluates a spherical light and returns spectral SH data.</span></span> <span data-ttu-id="e4cac-143">Não há nenhuma normalização da intensidade da luz como há para luzes direcionais, portanto, é preciso tomar cuidado ao especificar as intensidades.</span><span class="sxs-lookup"><span data-stu-id="e4cac-143">There is no normalization of the intensity of the light like there is for directional lights, so care has to be taken when specifying the intensities.</span></span> <span data-ttu-id="e4cac-144">Isso computará três exemplos de Spectral; pROut será retornado, enquanto pGOut e pBOut podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="e4cac-144">This will compute three spectral samples; pROut will be returned, while pGOut and pBOut may be returned.</span></span>

<span data-ttu-id="e4cac-145">Na esfera com raio de unidade, conforme mostrado na ilustração a seguir, a direção pode ser especificada simplesmente com teta, o ângulo sobre o eixo z na direção da mão direita e Phi, o ângulo de z.</span><span class="sxs-lookup"><span data-stu-id="e4cac-145">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![ilustração de um Sphere com raio de unidade](images/spherical-coordinates.png)

<span data-ttu-id="e4cac-147">As equações a seguir mostram a relação entre as coordenadas cartesianas (x, y, z) e esférico (teta, Phi) na esfera da unidade.</span><span class="sxs-lookup"><span data-stu-id="e4cac-147">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="e4cac-148">O ângulo teta varia sobre o intervalo de 0 a 2 PI, enquanto Phi varia de 0 a PI.</span><span class="sxs-lookup"><span data-stu-id="e4cac-148">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![equações da relação entre coordenadas cartesianas e esférica](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="e4cac-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4cac-150">Requirements</span></span>



| <span data-ttu-id="e4cac-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4cac-151">Requirement</span></span> | <span data-ttu-id="e4cac-152">Valor</span><span class="sxs-lookup"><span data-stu-id="e4cac-152">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4cac-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4cac-153">Header</span></span><br/>  | <dl> <span data-ttu-id="e4cac-154"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4cac-154"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="e4cac-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e4cac-155">Library</span></span><br/> | <dl> <span data-ttu-id="e4cac-156"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4cac-156"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4cac-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4cac-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4cac-158">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="e4cac-158">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
