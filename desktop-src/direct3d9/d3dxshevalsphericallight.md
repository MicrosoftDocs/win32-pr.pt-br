---
description: Função D3DXSHEvalSphericalLight (D3dx9math. h) – avalia uma luz esférica e retorna os dados de Spectral esférico harmônica (SH).
ms.assetid: aa46c162-9c2d-49c0-925c-d0c06456f918
title: Função D3DXSHEvalSphericalLight (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: db671d58806d999e07b1aac1e8e4da2fb38acc6f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117884"
---
# <a name="d3dxshevalsphericallight-function-d3dx9mathh"></a><span data-ttu-id="6b978-103">Função D3DXSHEvalSphericalLight (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="6b978-103">D3DXSHEvalSphericalLight function (D3dx9math.h)</span></span>

<span data-ttu-id="6b978-104">Avalia uma luz esférica e retorna dados Spectral esféricos (SH).</span><span class="sxs-lookup"><span data-stu-id="6b978-104">Evaluates a spherical light and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b978-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6b978-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalSphericalLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pPos,
  _In_        FLOAT       Radius,
  _In_        FLOAT       RIntensity,
  _In_        FLOAT       GIntensity,
  _In_        FLOAT       BIntensity,
  _Out_       FLOAT       *pROut,
  _Out_       FLOAT       *pGOut,
  _Out_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="6b978-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b978-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b978-107">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6b978-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b978-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b978-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b978-109">Ordem da avaliação SH.</span><span class="sxs-lookup"><span data-stu-id="6b978-109">Order of the SH evaluation.</span></span> <span data-ttu-id="6b978-110">Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="6b978-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="6b978-111">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="6b978-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="6b978-112">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="6b978-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="6b978-113">*pPos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6b978-113">*pPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b978-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="6b978-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="6b978-115">Ponteiro para a posição da luz.</span><span class="sxs-lookup"><span data-stu-id="6b978-115">Pointer to the light position.</span></span>

</dd> <dt>

<span data-ttu-id="6b978-116">*RADIUS* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6b978-116">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b978-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b978-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b978-118">Raio da fonte de luz esférica.</span><span class="sxs-lookup"><span data-stu-id="6b978-118">Radius of spherical light source.</span></span>

</dd> <dt>

<span data-ttu-id="6b978-119">*RIntensity* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6b978-119">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b978-120">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b978-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b978-121">A intensidade vermelha da luz.</span><span class="sxs-lookup"><span data-stu-id="6b978-121">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="6b978-122">*GIntensity* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6b978-122">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b978-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b978-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b978-124">A intensidade verde da luz.</span><span class="sxs-lookup"><span data-stu-id="6b978-124">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="6b978-125">*BIntensity* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6b978-125">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b978-126">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b978-126">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b978-127">A intensidade azul da luz.</span><span class="sxs-lookup"><span data-stu-id="6b978-127">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="6b978-128">*pROut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6b978-128">*pROut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b978-129">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6b978-129">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6b978-130">Ponteiro para o vetor SH de saída para o componente vermelho.</span><span class="sxs-lookup"><span data-stu-id="6b978-130">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="6b978-131">*pGOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6b978-131">*pGOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b978-132">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6b978-132">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6b978-133">Ponteiro para o vetor SH de saída para o componente verde.</span><span class="sxs-lookup"><span data-stu-id="6b978-133">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="6b978-134">*pBOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6b978-134">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b978-135">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6b978-135">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6b978-136">Ponteiro para o vetor SH de saída para o componente azul.</span><span class="sxs-lookup"><span data-stu-id="6b978-136">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b978-137">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6b978-137">Return value</span></span>

<span data-ttu-id="6b978-138">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6b978-138">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6b978-139">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6b978-139">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6b978-140">Se a função falhar, o valor de retorno poderá ser: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6b978-140">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b978-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b978-141">Remarks</span></span>

<span data-ttu-id="6b978-142">Avalia uma luz esférica e retorna dados de Spectral SH.</span><span class="sxs-lookup"><span data-stu-id="6b978-142">Evaluates a spherical light and returns spectral SH data.</span></span> <span data-ttu-id="6b978-143">Não há nenhuma normalização da intensidade da luz como há para [luzes direcionais](light-types.md), portanto, é preciso tomar cuidado ao especificar as intensidades.</span><span class="sxs-lookup"><span data-stu-id="6b978-143">There is no normalization of the intensity of the light like there is for [directional lights](light-types.md), so care has to be taken when specifying the intensities.</span></span> <span data-ttu-id="6b978-144">Isso computará três exemplos de Spectral; *pROut* será retornado, enquanto *pGOut* e *pBOut* podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="6b978-144">This will compute three spectral samples; *pROut* will be returned, while *pGOut* and *pBOut* may be returned.</span></span>

<span data-ttu-id="6b978-145">Na esfera com raio de unidade, conforme mostrado na ilustração a seguir, a direção pode ser especificada simplesmente com teta, o ângulo sobre o eixo z na [direção da mão direita](coordinate-systems.md)e Phi, o ângulo de z.</span><span class="sxs-lookup"><span data-stu-id="6b978-145">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![ilustração de um Sphere com raio de unidade](images/spherical-coordinates.png)

<span data-ttu-id="6b978-147">As equações a seguir mostram a relação entre as coordenadas cartesianas (x, y, z) e esférico (teta, Phi) na esfera da unidade.</span><span class="sxs-lookup"><span data-stu-id="6b978-147">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="6b978-148">O ângulo teta varia sobre o intervalo de 0 a 2 PI, enquanto Phi varia de 0 a PI.</span><span class="sxs-lookup"><span data-stu-id="6b978-148">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![equações da relação entre coordenadas cartesianas e esférica](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="6b978-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b978-150">Requirements</span></span>



| <span data-ttu-id="6b978-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b978-151">Requirement</span></span> | <span data-ttu-id="6b978-152">Valor</span><span class="sxs-lookup"><span data-stu-id="6b978-152">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b978-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6b978-153">Header</span></span><br/>  | <dl> <span data-ttu-id="6b978-154"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b978-154"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6b978-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6b978-155">Library</span></span><br/> | <dl> <span data-ttu-id="6b978-156"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b978-156"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6b978-157">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6b978-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b978-158">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="6b978-158">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="6b978-159">Transferência radiante de computação (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6b978-159">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
