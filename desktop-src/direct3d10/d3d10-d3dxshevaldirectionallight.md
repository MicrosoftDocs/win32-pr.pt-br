---
description: Avalia uma luz direcional e retorna dados Spectral esféricos (SH).
ms.assetid: b5c657f5-d291-4e53-908c-670b29a1888a
title: Função D3DXSHEvalDirectionalLight (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalDirectionalLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9c6b5c9590132d9fe3d0fc07ae419d442144079a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104567126"
---
# <a name="d3dxshevaldirectionallight-function-d3dx10h"></a><span data-ttu-id="8e8b8-103">Função D3DXSHEvalDirectionalLight (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="8e8b8-103">D3DXSHEvalDirectionalLight function (D3DX10.h)</span></span>

<span data-ttu-id="8e8b8-104">Avalia uma luz direcional e retorna dados Spectral esféricos (SH).</span><span class="sxs-lookup"><span data-stu-id="8e8b8-104">Evaluates a directional light and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e8b8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e8b8-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalDirectionalLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       FLOAT       RIntensity,
  _In_       FLOAT       GIntensity,
  _In_       FLOAT       BIntensity,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="8e8b8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e8b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e8b8-107">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8e8b8-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e8b8-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e8b8-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e8b8-109">Ordem da avaliação SH.</span><span class="sxs-lookup"><span data-stu-id="8e8b8-109">Order of the SH evaluation.</span></span> <span data-ttu-id="8e8b8-110">Deve estar no intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="8e8b8-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="8e8b8-111">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="8e8b8-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="8e8b8-112">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="8e8b8-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="8e8b8-113">*pDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8e8b8-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e8b8-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="8e8b8-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="8e8b8-115">Ponteiro para o vetor de direção do eixo hemisfério (x, y, z) no qual avaliar as funções de base SH.</span><span class="sxs-lookup"><span data-stu-id="8e8b8-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="8e8b8-116">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="8e8b8-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="8e8b8-117">*RIntensity* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8e8b8-117">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e8b8-118">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e8b8-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e8b8-119">A intensidade vermelha da luz.</span><span class="sxs-lookup"><span data-stu-id="8e8b8-119">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="8e8b8-120">*GIntensity* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8e8b8-120">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e8b8-121">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e8b8-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e8b8-122">A intensidade verde da luz.</span><span class="sxs-lookup"><span data-stu-id="8e8b8-122">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="8e8b8-123">*BIntensity* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8e8b8-123">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e8b8-124">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e8b8-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e8b8-125">A intensidade azul da luz.</span><span class="sxs-lookup"><span data-stu-id="8e8b8-125">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="8e8b8-126">*pROut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8e8b8-126">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e8b8-127">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8e8b8-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8e8b8-128">Ponteiro para o vetor SH de saída para o componente vermelho.</span><span class="sxs-lookup"><span data-stu-id="8e8b8-128">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="8e8b8-129">*pGOut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8e8b8-129">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e8b8-130">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8e8b8-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8e8b8-131">Ponteiro opcional para o vetor de saída SH para o componente verde.</span><span class="sxs-lookup"><span data-stu-id="8e8b8-131">Optional pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="8e8b8-132">*pBOut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8e8b8-132">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e8b8-133">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="8e8b8-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="8e8b8-134">Ponteiro opcional para o vetor de saída SH para o componente azul.</span><span class="sxs-lookup"><span data-stu-id="8e8b8-134">Optional pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e8b8-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8e8b8-135">Return value</span></span>

<span data-ttu-id="8e8b8-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8e8b8-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8e8b8-137">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8e8b8-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8e8b8-138">Se a função falhar, o valor de retorno poderá ser: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="8e8b8-138">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e8b8-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e8b8-139">Remarks</span></span>

<span data-ttu-id="8e8b8-140">O vetor de saída é calculado de forma que, se a taxa de intensidade R/G/B for igual a 1, o radiante de saída resultante de um ponto diretamente sob a luz em um objeto difuso com um albedo de 1 seria 1,0.</span><span class="sxs-lookup"><span data-stu-id="8e8b8-140">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the resulting exit radiance of a point directly under the light on a diffuse object with an albedo of 1 would be 1.0.</span></span> <span data-ttu-id="8e8b8-141">Isso computará três exemplos de Spectral; pROut será retornado, enquanto pGOut e pBOut podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="8e8b8-141">This will compute three spectral samples; pROut will be returned, while pGOut and pBOut may be returned.</span></span>

<span data-ttu-id="8e8b8-142">Na esfera com raio de unidade, conforme mostrado na ilustração a seguir, a direção pode ser especificada simplesmente com teta, o ângulo sobre o eixo z na direção da mão direita e Phi, o ângulo de z.</span><span class="sxs-lookup"><span data-stu-id="8e8b8-142">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![ilustração de um Sphere com raio de unidade](images/spherical-coordinates.png)

<span data-ttu-id="8e8b8-144">As equações a seguir mostram a relação entre as coordenadas cartesianas (x, y, z) e esférico (teta, Phi) na esfera da unidade.</span><span class="sxs-lookup"><span data-stu-id="8e8b8-144">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="8e8b8-145">O ângulo teta varia sobre o intervalo de 0 a 2 PI, enquanto Phi varia de 0 a PI.</span><span class="sxs-lookup"><span data-stu-id="8e8b8-145">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![equações da relação entre coordenadas cartesianas e esférica](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="8e8b8-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e8b8-147">Requirements</span></span>



| <span data-ttu-id="8e8b8-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e8b8-148">Requirement</span></span> | <span data-ttu-id="8e8b8-149">Valor</span><span class="sxs-lookup"><span data-stu-id="8e8b8-149">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e8b8-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8e8b8-150">Header</span></span><br/>  | <dl> <span data-ttu-id="8e8b8-151"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e8b8-151"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8e8b8-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8e8b8-152">Library</span></span><br/> | <dl> <span data-ttu-id="8e8b8-153"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e8b8-153"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e8b8-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e8b8-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e8b8-155">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="8e8b8-155">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
