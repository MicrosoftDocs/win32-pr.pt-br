---
description: Avalia uma luz que é uma interpolação linear entre duas cores na esfera.
ms.assetid: 7523ff42-c81d-4857-a50d-7efa213214b8
title: Função D3DXSHEvalHemisphereLight (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHEvalHemisphereLight
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c6ff3359ce0629eec472e4da24a31c24196c7f15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298714"
---
# <a name="d3dxshevalhemispherelight-function-d3dx10h"></a><span data-ttu-id="1cbb1-103">Função D3DXSHEvalHemisphereLight (D3DX10. h)</span><span class="sxs-lookup"><span data-stu-id="1cbb1-103">D3DXSHEvalHemisphereLight function (D3DX10.h)</span></span>

<span data-ttu-id="1cbb1-104">Avalia uma luz que é uma interpolação linear entre duas cores na esfera.</span><span class="sxs-lookup"><span data-stu-id="1cbb1-104">Evaluates a light that is a linear interpolation between two colors over the sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cbb1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1cbb1-105">Syntax</span></span>


```C++
HRESULT D3DXSHEvalHemisphereLight(
  _In_       UINT        Order,
  _In_ const D3DXVECTOR3 *pDir,
  _In_       D3DXCOLOR   Top,
  _In_       D3DXCOLOR   Bottom,
  _In_       FLOAT       *pROut,
  _In_       FLOAT       *pGOut,
  _In_       FLOAT       *pBOut
);
```



## <a name="parameters"></a><span data-ttu-id="1cbb1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1cbb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cbb1-107">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1cbb1-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cbb1-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1cbb1-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1cbb1-109">Ordem da avaliação harmônica esférica (SH).</span><span class="sxs-lookup"><span data-stu-id="1cbb1-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="1cbb1-110">Deve estar no intervalo de D3DXSH \_ MINORDER a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="1cbb1-110">Must be in the range of D3DXSH\_MINORDER to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="1cbb1-111">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="1cbb1-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="1cbb1-112">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="1cbb1-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="1cbb1-113">*pDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1cbb1-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cbb1-114">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1cbb1-114">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="1cbb1-115">Ponteiro para o vetor de direção do eixo hemisfério (x, y, z) no qual avaliar as funções de base SH.</span><span class="sxs-lookup"><span data-stu-id="1cbb1-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="1cbb1-116">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="1cbb1-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1cbb1-117">*Superior* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1cbb1-117">*Top* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cbb1-118">Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="1cbb1-118">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

<span data-ttu-id="1cbb1-119">A cor do céu.</span><span class="sxs-lookup"><span data-stu-id="1cbb1-119">The sky color.</span></span>

</dd> <dt>

<span data-ttu-id="1cbb1-120">*Parte inferior* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1cbb1-120">*Bottom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cbb1-121">Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="1cbb1-121">Type: **[**D3DXCOLOR**](../direct3d9/d3dxcolor.md)**</span></span>

<span data-ttu-id="1cbb1-122">A cor do solo.</span><span class="sxs-lookup"><span data-stu-id="1cbb1-122">The ground color.</span></span>

</dd> <dt>

<span data-ttu-id="1cbb1-123">*pROut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1cbb1-123">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cbb1-124">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1cbb1-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1cbb1-125">Ponteiro para o vetor SH de saída para o componente vermelho.</span><span class="sxs-lookup"><span data-stu-id="1cbb1-125">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="1cbb1-126">*pGOut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1cbb1-126">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cbb1-127">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1cbb1-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1cbb1-128">Ponteiro para o vetor SH de saída para o componente verde.</span><span class="sxs-lookup"><span data-stu-id="1cbb1-128">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="1cbb1-129">*pBOut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1cbb1-129">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cbb1-130">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1cbb1-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1cbb1-131">Ponteiro para o vetor SH de saída para o componente azul.</span><span class="sxs-lookup"><span data-stu-id="1cbb1-131">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cbb1-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1cbb1-132">Return value</span></span>

<span data-ttu-id="1cbb1-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1cbb1-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1cbb1-134">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1cbb1-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1cbb1-135">Se a função falhar, o valor de retorno poderá ser: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="1cbb1-135">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cbb1-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="1cbb1-136">Remarks</span></span>

<span data-ttu-id="1cbb1-137">A interpolação é feita linearmente entre os dois pontos, e não a superfície da esfera (ou seja, se o eixo fosse (0, 0, 1) ele é linear em Z, não no ângulo de azimuthal).</span><span class="sxs-lookup"><span data-stu-id="1cbb1-137">The interpolation is done linearly between the two points, not over the surface of the sphere (that is, if the axis was (0,0,1) it is linear in Z, not in the azimuthal angle).</span></span> <span data-ttu-id="1cbb1-138">A função de iluminação esférica resultante é normalizada para que um ponto em uma superfície perfeitamente difusa sem sombreamento e um apontador normal na direção pDir resultem em Exit radiante com um valor de 1 (se a cor superior fosse branca e a cor inferior fosse preta).</span><span class="sxs-lookup"><span data-stu-id="1cbb1-138">The resulting spherical lighting function is normalized so that a point on a perfectly diffuse surface with no shadowing and a normal pointed in the direction pDir would result in exit radiance with a value of 1 (if the top color was white and the bottom color was black).</span></span> <span data-ttu-id="1cbb1-139">Esse é um modelo muito simples em que Top representa a intensidade do "céu" e inferior representa a intensidade do "aterramento".</span><span class="sxs-lookup"><span data-stu-id="1cbb1-139">This is a very simple model where Top represents the intensity of the "sky" and Bottom represents the intensity of the "ground."</span></span>

<span data-ttu-id="1cbb1-140">Na esfera com raio de unidade, conforme mostrado na ilustração a seguir, a direção pode ser especificada simplesmente com teta, o ângulo sobre o eixo z na direção da mão direita e Phi, o ângulo de z.</span><span class="sxs-lookup"><span data-stu-id="1cbb1-140">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the right-handed direction, and phi, the angle from z.</span></span>

![ilustração de um Sphere com raio de unidade](images/spherical-coordinates.png)

<span data-ttu-id="1cbb1-142">As equações a seguir mostram a relação entre as coordenadas cartesianas (x, y, z) e esférico (teta, Phi) na esfera da unidade.</span><span class="sxs-lookup"><span data-stu-id="1cbb1-142">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="1cbb1-143">O ângulo teta varia sobre o intervalo de 0 a 2 PI, enquanto Phi varia de 0 a PI.</span><span class="sxs-lookup"><span data-stu-id="1cbb1-143">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![equações da relação entre coordenadas cartesianas e esférica](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="1cbb1-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cbb1-145">Requirements</span></span>



| <span data-ttu-id="1cbb1-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cbb1-146">Requirement</span></span> | <span data-ttu-id="1cbb1-147">Valor</span><span class="sxs-lookup"><span data-stu-id="1cbb1-147">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1cbb1-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1cbb1-148">Header</span></span><br/>  | <dl> <span data-ttu-id="1cbb1-149"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cbb1-149"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="1cbb1-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1cbb1-150">Library</span></span><br/> | <dl> <span data-ttu-id="1cbb1-151"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cbb1-151"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cbb1-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="1cbb1-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cbb1-153">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="1cbb1-153">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
