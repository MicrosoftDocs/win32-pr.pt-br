---
description: Função D3DXSHEvalHemisphereLight (D3dx9math. h) – avalia uma luz que é uma interpolação linear entre duas cores na esfera.
ms.assetid: c5815f12-f706-40f6-bf5e-78a211cfbbea
title: Função D3DXSHEvalHemisphereLight (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7bc06dcf866c21cc5dcb96b23dea5a4640293fef
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093955"
---
# <a name="d3dxshevalhemispherelight-function-d3dx9mathh"></a><span data-ttu-id="17c38-103">Função D3DXSHEvalHemisphereLight (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="17c38-103">D3DXSHEvalHemisphereLight function (D3dx9math.h)</span></span>

<span data-ttu-id="17c38-104">Avalia uma luz que é uma interpolação linear entre duas cores na esfera.</span><span class="sxs-lookup"><span data-stu-id="17c38-104">Evaluates a light that is a linear interpolation between two colors over the sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="17c38-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17c38-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="17c38-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17c38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17c38-107">*Ordem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17c38-107">*Order* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17c38-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="17c38-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="17c38-109">Ordem da avaliação harmônica esférica (SH).</span><span class="sxs-lookup"><span data-stu-id="17c38-109">Order of the spherical harmonic (SH) evaluation.</span></span> <span data-ttu-id="17c38-110">Deve estar no intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, inclusive.</span><span class="sxs-lookup"><span data-stu-id="17c38-110">Must be in the range of [D3DXSH\_MINORDER](other-d3dx-constants.md) to D3DXSH\_MAXORDER, inclusive.</span></span> <span data-ttu-id="17c38-111">A avaliação gera coeficientes do Order ².</span><span class="sxs-lookup"><span data-stu-id="17c38-111">The evaluation generates Order² coefficients.</span></span> <span data-ttu-id="17c38-112">O grau da avaliação é a ordem 1.</span><span class="sxs-lookup"><span data-stu-id="17c38-112">The degree of the evaluation is Order - 1.</span></span>

</dd> <dt>

<span data-ttu-id="17c38-113">*pDir* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17c38-113">*pDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17c38-114">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="17c38-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="17c38-115">Ponteiro para o vetor de direção do eixo hemisfério (x, y, z) no qual avaliar as funções de base SH.</span><span class="sxs-lookup"><span data-stu-id="17c38-115">Pointer to the (x, y, z) hemisphere axis direction vector in which to evaluate the SH basis functions.</span></span> <span data-ttu-id="17c38-116">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="17c38-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="17c38-117">*Superior* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17c38-117">*Top* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17c38-118">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="17c38-118">Type: **[**D3DXCOLOR**](d3dxcolor.md)**</span></span>

<span data-ttu-id="17c38-119">A cor do céu.</span><span class="sxs-lookup"><span data-stu-id="17c38-119">The sky color.</span></span>

</dd> <dt>

<span data-ttu-id="17c38-120">*Parte inferior* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17c38-120">*Bottom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17c38-121">Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="17c38-121">Type: **[**D3DXCOLOR**](d3dxcolor.md)**</span></span>

<span data-ttu-id="17c38-122">A cor do solo.</span><span class="sxs-lookup"><span data-stu-id="17c38-122">The ground color.</span></span>

</dd> <dt>

<span data-ttu-id="17c38-123">*pROut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17c38-123">*pROut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17c38-124">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="17c38-124">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="17c38-125">Ponteiro para o vetor SH de saída para o componente vermelho.</span><span class="sxs-lookup"><span data-stu-id="17c38-125">Pointer to the output SH vector for the red component.</span></span>

</dd> <dt>

<span data-ttu-id="17c38-126">*pGOut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17c38-126">*pGOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17c38-127">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="17c38-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="17c38-128">Ponteiro para o vetor SH de saída para o componente verde.</span><span class="sxs-lookup"><span data-stu-id="17c38-128">Pointer to the output SH vector for the green component.</span></span>

</dd> <dt>

<span data-ttu-id="17c38-129">*pBOut* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="17c38-129">*pBOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17c38-130">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="17c38-130">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="17c38-131">Ponteiro para o vetor SH de saída para o componente azul.</span><span class="sxs-lookup"><span data-stu-id="17c38-131">Pointer to the output SH vector for the blue component.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17c38-132">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="17c38-132">Return value</span></span>

<span data-ttu-id="17c38-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="17c38-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="17c38-134">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="17c38-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="17c38-135">Se a função falhar, o valor de retorno poderá ser: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="17c38-135">If the function fails, the return value can be: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="17c38-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="17c38-136">Remarks</span></span>

<span data-ttu-id="17c38-137">A interpolação é feita linearmente entre os dois pontos, e não a superfície da esfera (ou seja, se o eixo fosse (0, 0, 1) ele é linear em Z, não no ângulo de azimuthal).</span><span class="sxs-lookup"><span data-stu-id="17c38-137">The interpolation is done linearly between the two points, not over the surface of the sphere (that is, if the axis was (0,0,1) it is linear in Z, not in the azimuthal angle).</span></span> <span data-ttu-id="17c38-138">A função de iluminação esférica resultante é normalizada para que um ponto em uma superfície perfeitamente difusa sem sombreamento e um apontador normal na direção *pDir* resultem em Exit radiante com um valor de 1 (se a cor superior fosse branca e a cor inferior fosse preta).</span><span class="sxs-lookup"><span data-stu-id="17c38-138">The resulting spherical lighting function is normalized so that a point on a perfectly diffuse surface with no shadowing and a normal pointed in the direction *pDir* would result in exit radiance with a value of 1 (if the top color was white and the bottom color was black).</span></span> <span data-ttu-id="17c38-139">Esse é um modelo muito simples em que *Top* representa a intensidade do "céu" e *inferior* representa a intensidade do "aterramento".</span><span class="sxs-lookup"><span data-stu-id="17c38-139">This is a very simple model where *Top* represents the intensity of the "sky" and *Bottom* represents the intensity of the "ground."</span></span>

<span data-ttu-id="17c38-140">Na esfera com raio de unidade, conforme mostrado na ilustração a seguir, a direção pode ser especificada simplesmente com teta, o ângulo sobre o eixo z na [direção da mão direita](coordinate-systems.md)e Phi, o ângulo de z.</span><span class="sxs-lookup"><span data-stu-id="17c38-140">On the sphere with unit radius, as shown in the following illustration, direction can be specified simply with theta, the angle about the z-axis in the [right-handed direction](coordinate-systems.md), and phi, the angle from z.</span></span>

![ilustração de um Sphere com raio de unidade](images/spherical-coordinates.png)

<span data-ttu-id="17c38-142">As equações a seguir mostram a relação entre as coordenadas cartesianas (x, y, z) e esférico (teta, Phi) na esfera da unidade.</span><span class="sxs-lookup"><span data-stu-id="17c38-142">The following equations show the relationship between Cartesian (x, y, z) and spherical (theta, phi) coordinates on the unit sphere.</span></span> <span data-ttu-id="17c38-143">O ângulo teta varia sobre o intervalo de 0 a 2 PI, enquanto Phi varia de 0 a PI.</span><span class="sxs-lookup"><span data-stu-id="17c38-143">The angle theta varies over the range of 0 to 2 pi, while phi varies from 0 to pi.</span></span>

![equações da relação entre coordenadas cartesianas e esférica](images/spherical-coordinates-equations.png)

## <a name="requirements"></a><span data-ttu-id="17c38-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17c38-145">Requirements</span></span>



| <span data-ttu-id="17c38-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="17c38-146">Requirement</span></span> | <span data-ttu-id="17c38-147">Valor</span><span class="sxs-lookup"><span data-stu-id="17c38-147">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="17c38-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="17c38-148">Header</span></span><br/>  | <dl> <span data-ttu-id="17c38-149"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="17c38-149"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="17c38-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="17c38-150">Library</span></span><br/> | <dl> <span data-ttu-id="17c38-151"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="17c38-151"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="17c38-152">Consulte também</span><span class="sxs-lookup"><span data-stu-id="17c38-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17c38-153">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="17c38-153">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="17c38-154">Transferência radiante de computação (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="17c38-154">Precomputed Radiance Transfer (Direct3D 9)</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
