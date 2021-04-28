---
description: Função D3DXSHEvalDirectionalLight (D3dx9math. h) – avalia uma luz direcional e retorna dados de Spectral esférica harmônica (SH).
ms.assetid: 6e2e9b02-13bb-4cef-ae9d-343fbf64e5d7
title: Função D3DXSHEvalDirectionalLight (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 488682eca230c8da6cc5048aded4a7a1e7f71bfd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117904"
---
# <a name="d3dxshevaldirectionallight-function-d3dx9mathh"></a><span data-ttu-id="f52f1-103">Função D3DXSHEvalDirectionalLight (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f52f1-103">D3DXSHEvalDirectionalLight function (D3dx9math.h)</span></span>

<span data-ttu-id="f52f1-104">Avalia uma [luz direcional](light-types.md) e retorna dados Spectral esféricos (SH).</span><span class="sxs-lookup"><span data-stu-id="f52f1-104">Evaluates a [directional light](light-types.md) and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f52f1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f52f1-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalDirectionalLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir,
  _In_        FLOAT       RIntensity,
  _In_        FLOAT       GIntensity,
  _In_        FLOAT       BIntensity,
  _Out_       FLOAT       *pROut,
  _Out_       FLOAT       *pGOut,
  _Out_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="f52f1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f52f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f52f1-107">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f52f1-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f52f1-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f52f1-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f52f1-109">Ordem da avaliação SH.</span><span class="sxs-lookup"><span data-stu-id="f52f1-109">Order of the SH evaluation.</span></span> <span data-ttu-id="f52f1-110">Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="f52f1-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="f52f1-111">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="f52f1-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="f52f1-112">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="f52f1-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="f52f1-113">*pDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f52f1-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f52f1-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="f52f1-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="f52f1-115">Ponteiro para o vetor de direção do eixo hemisfério (x, y, z) no qual avaliar as funções de base SH.</span><span class="sxs-lookup"><span data-stu-id="f52f1-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="f52f1-116">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="f52f1-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="f52f1-117">*RIntensity* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f52f1-117">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f52f1-118">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f52f1-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f52f1-119">A intensidade vermelha da luz.</span><span class="sxs-lookup"><span data-stu-id="f52f1-119">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="f52f1-120">*GIntensity* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f52f1-120">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f52f1-121">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f52f1-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f52f1-122">A intensidade verde da luz.</span><span class="sxs-lookup"><span data-stu-id="f52f1-122">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="f52f1-123">*BIntensity* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f52f1-123">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f52f1-124">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f52f1-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f52f1-125">A intensidade azul da luz.</span><span class="sxs-lookup"><span data-stu-id="f52f1-125">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="f52f1-126">*pROut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f52f1-126">*pROut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f52f1-127">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f52f1-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f52f1-128">Ponteiro para o vetor SH de saída para o componente vermelho.</span><span class="sxs-lookup"><span data-stu-id="f52f1-128">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="f52f1-129">*pGOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f52f1-129">*pGOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f52f1-130">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f52f1-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f52f1-131">Ponteiro opcional para o vetor de saída SH para o componente verde.</span><span class="sxs-lookup"><span data-stu-id="f52f1-131">Optional pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="f52f1-132">*pBOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f52f1-132">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f52f1-133">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f52f1-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f52f1-134">Ponteiro opcional para o vetor de saída SH para o componente azul.</span><span class="sxs-lookup"><span data-stu-id="f52f1-134">Optional pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f52f1-135">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f52f1-135">Return value</span></span>

<span data-ttu-id="f52f1-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f52f1-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f52f1-137">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f52f1-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f52f1-138">Se a função falhar, o valor de retorno poderá ser: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="f52f1-138">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f52f1-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="f52f1-139">Remarks</span></span>

<span data-ttu-id="f52f1-140">O vetor de saída é calculado de forma que, se a taxa de intensidade R/G/B for igual a 1, o radiante de saída resultante de um ponto diretamente sob a luz em um objeto difuso com um albedo de 1 seria 1,0.</span><span class="sxs-lookup"><span data-stu-id="f52f1-140">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the resulting exit radiance of a point directly under the light on a diffuse object with an albedo of 1 would be 1.0.</span></span> <span data-ttu-id="f52f1-141">Isso computará três exemplos de Spectral; *pROut* será retornado, enquanto *pGOut* e *pBOut* podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="f52f1-141">This will compute three spectral samples; *pROut* will be returned, while *pGOut* and *pBOut* may be returned.</span></span>

<span data-ttu-id="f52f1-142">Na esfera com raio de unidade, conforme mostrado na ilustração a seguir, a direção pode ser especificada simplesmente com teta, o ângulo sobre o eixo z na [direção da mão direita](coordinate-systems.md)e Phi, o ângulo de z.</span><span class="sxs-lookup"><span data-stu-id="f52f1-142">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![ilustração de um Sphere com raio de unidade](images/spherical-coordinates.png)

<span data-ttu-id="f52f1-144">As equações a seguir mostram a relação entre as coordenadas cartesianas (x, y, z) e esférico (teta, Phi) na esfera da unidade.</span><span class="sxs-lookup"><span data-stu-id="f52f1-144">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="f52f1-145">O ângulo teta varia sobre o intervalo de 0 a 2 PI, enquanto Phi varia de 0 a PI.</span><span class="sxs-lookup"><span data-stu-id="f52f1-145">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![equações da relação entre coordenadas cartesianas e esférica](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="f52f1-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f52f1-147">Requirements</span></span>



| <span data-ttu-id="f52f1-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="f52f1-148">Requirement</span></span> | <span data-ttu-id="f52f1-149">Valor</span><span class="sxs-lookup"><span data-stu-id="f52f1-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f52f1-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f52f1-150">Header</span></span><br/>  | <dl> <span data-ttu-id="f52f1-151"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f52f1-151"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="f52f1-152">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f52f1-152">Library</span></span><br/> | <dl> <span data-ttu-id="f52f1-153"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f52f1-153"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f52f1-154">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f52f1-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f52f1-155">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="f52f1-155">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="f52f1-156">Transferência radiante de computação (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f52f1-156">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
