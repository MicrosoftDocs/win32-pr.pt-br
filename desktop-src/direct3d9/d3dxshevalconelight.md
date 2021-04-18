---
description: Avalia uma luz que é um cone de intensidade constante e retorna dados Spectral esféricos harmônicas (SH).
ms.assetid: 13088e3b-76ae-43ef-886e-686f1f18a31d
title: Função D3DXSHEvalConeLight (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalConeLight
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2400fe0430e008ea1b704ee4daef51eeee7bd7a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104569642"
---
# <a name="d3dxshevalconelight-function-d3dx9mathh"></a><span data-ttu-id="b3479-103">Função D3DXSHEvalConeLight (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="b3479-103">D3DXSHEvalConeLight function (D3dx9math.h)</span></span>

<span data-ttu-id="b3479-104">Avalia uma luz que é um cone de intensidade constante e retorna dados Spectral esféricos harmônicas (SH).</span><span class="sxs-lookup"><span data-stu-id="b3479-104">Evaluates a light that is a cone of constant intensity and returns spectral spherical harmonic (SH) data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3479-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3479-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalConeLight(
  _In_        UINT        Order,
  _In_  const D3DXVECTOR3 *pDir,
  _In_        FLOAT       Radius,
  _In_        FLOAT       RIntensity,
  _In_        FLOAT       GIntensity,
  _In_        FLOAT       BIntensity,
  _Out_       FLOAT       *pROut,
  _Out_       FLOAT       *pGOut,
  _Out_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="b3479-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3479-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3479-107">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3479-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3479-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3479-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3479-109">Ordem da avaliação SH.</span><span class="sxs-lookup"><span data-stu-id="b3479-109">Order of the SH evaluation.</span></span> <span data-ttu-id="b3479-110">Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="b3479-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="b3479-111">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="b3479-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="b3479-112">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="b3479-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="b3479-113">*pDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3479-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3479-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b3479-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b3479-115">Ponteiro para o vetor de direção do eixo hemisfério (x, y, z) no qual avaliar as funções de base SH.</span><span class="sxs-lookup"><span data-stu-id="b3479-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="b3479-116">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="b3479-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b3479-117">*RADIUS* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3479-117">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3479-118">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3479-118">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3479-119">Raio de cone em radianos.</span><span class="sxs-lookup"><span data-stu-id="b3479-119">Radius of cone in radians.</span></span>

</dd> <dt>

<span data-ttu-id="b3479-120">*RIntensity* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3479-120">*RIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3479-121">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3479-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3479-122">A intensidade vermelha da luz.</span><span class="sxs-lookup"><span data-stu-id="b3479-122">The red intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="b3479-123">*GIntensity* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3479-123">*GIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3479-124">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3479-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3479-125">A intensidade verde da luz.</span><span class="sxs-lookup"><span data-stu-id="b3479-125">The green intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="b3479-126">*BIntensity* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b3479-126">*BIntensity* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3479-127">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b3479-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b3479-128">A intensidade azul da luz.</span><span class="sxs-lookup"><span data-stu-id="b3479-128">The blue intensity of the light.</span></span>

</dd> <dt>

<span data-ttu-id="b3479-129">*pROut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b3479-129">*pROut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3479-130">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b3479-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b3479-131">Ponteiro para o vetor SH de saída para o componente vermelho.</span><span class="sxs-lookup"><span data-stu-id="b3479-131">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="b3479-132">*pGOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b3479-132">*pGOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3479-133">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b3479-133">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b3479-134">Ponteiro para o vetor SH de saída para o componente verde.</span><span class="sxs-lookup"><span data-stu-id="b3479-134">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="b3479-135">*pBOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b3479-135">*pBOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3479-136">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b3479-136">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b3479-137">Ponteiro para o vetor SH de saída para o componente azul.</span><span class="sxs-lookup"><span data-stu-id="b3479-137">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3479-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3479-138">Return value</span></span>

<span data-ttu-id="b3479-139">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b3479-139">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b3479-140">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b3479-140">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b3479-141">Se a função falhar, o valor de retorno poderá ser: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b3479-141">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3479-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3479-142">Remarks</span></span>

<span data-ttu-id="b3479-143">Avalia uma luz que é um cone de intensidade constante e retorna dados Spectral SH.</span><span class="sxs-lookup"><span data-stu-id="b3479-143">Evaluates a light that is a cone of constant intensity and returns spectral SH data.</span></span> <span data-ttu-id="b3479-144">O vetor de saída é calculado de forma que, se a taxa de intensidade R/G/B for igual a 1, a saída radiante de um ponto diretamente sob a luz (orientada na direção do cone em um objeto difuso com um albedo de 1) seria 1,0.</span><span class="sxs-lookup"><span data-stu-id="b3479-144">The output vector is computed so that if the intensity ratio R/G/B is equal to 1, the exit radiance of a point directly under the light (oriented in the cone direction on a diffuse object with an albedo of 1) would be 1.0.</span></span> <span data-ttu-id="b3479-145">Isso computará três exemplos de Spectral; *pROut* será retornado, enquanto *pGOut* e *pBOut* podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="b3479-145">This will compute three spectral samples; *pROut* will be returned, while *pGOut* and *pBOut* may be returned.</span></span>

<span data-ttu-id="b3479-146">Na esfera com raio de unidade, conforme mostrado na ilustração a seguir, a direção pode ser especificada simplesmente com teta, o ângulo sobre o eixo z na [direção da mão direita](coordinate-systems.md)e Phi, o ângulo de z.</span><span class="sxs-lookup"><span data-stu-id="b3479-146">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![ilustração de um Sphere com raio de unidade](images/spherical-coordinates.png)

<span data-ttu-id="b3479-148">As equações a seguir mostram a relação entre as coordenadas cartesianas (x, y, z) e esférico (teta, Phi) na esfera da unidade.</span><span class="sxs-lookup"><span data-stu-id="b3479-148">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="b3479-149">O ângulo teta varia sobre o intervalo de 0 a 2 PI, enquanto Phi varia de 0 a PI.</span><span class="sxs-lookup"><span data-stu-id="b3479-149">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![equações da relação entre coordenadas cartesianas e esférica](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="b3479-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3479-151">Requirements</span></span>



| <span data-ttu-id="b3479-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3479-152">Requirement</span></span> | <span data-ttu-id="b3479-153">Valor</span><span class="sxs-lookup"><span data-stu-id="b3479-153">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3479-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3479-154">Header</span></span><br/>  | <dl> <span data-ttu-id="b3479-155"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3479-155"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b3479-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b3479-156">Library</span></span><br/> | <dl> <span data-ttu-id="b3479-157"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3479-157"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b3479-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3479-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3479-159">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="b3479-159">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="b3479-160">Transferência radiante de computação (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b3479-160">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
