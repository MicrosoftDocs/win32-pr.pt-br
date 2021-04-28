---
description: Função D3DXPlaneTransformArray (D3DX10Math. h) – transforma uma matriz de planos por uma matriz. Os vetores que descrevem cada plano devem ser normalizados.
ms.assetid: 9529b06a-0575-4115-8d35-fc35a7bfb0bd
title: Função D3DXPlaneTransformArray (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransformArray
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d8b02b64fd13e7466980340056fceccc1da784cf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103254"
---
# <a name="d3dxplanetransformarray-function-d3dx10mathh"></a><span data-ttu-id="2d54f-104">Função D3DXPlaneTransformArray (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="2d54f-104">D3DXPlaneTransformArray function (D3DX10Math.h)</span></span>

<span data-ttu-id="2d54f-105">Transforma uma matriz de planos por uma matriz.</span><span class="sxs-lookup"><span data-stu-id="2d54f-105">Transforms an array of planes by a matrix.</span></span> <span data-ttu-id="2d54f-106">Os vetores que descrevem cada plano devem ser normalizados.</span><span class="sxs-lookup"><span data-stu-id="2d54f-106">The vectors that describe each plane must be normalized.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d54f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d54f-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransformArray(
  _Inout_       D3DXPLANE  *pOut,
  _In_          UINT       OutStride,
  _In_    const D3DXPLANE  *pP,
  _In_          UINT       PStride,
  _In_    const D3DXMATRIX *pM,
  _In_          UINT       n
);
```



## <a name="parameters"></a><span data-ttu-id="2d54f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d54f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d54f-109">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="2d54f-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d54f-110">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="2d54f-110">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="2d54f-111">Ponteiro para a estrutura [**D3DXPLANE**](d3d10-d3dxplane.md) que contém o plano transformado resultante.</span><span class="sxs-lookup"><span data-stu-id="2d54f-111">Pointer to the [**D3DXPLANE**](d3d10-d3dxplane.md) structure that contains the resulting transformed plane.</span></span> <span data-ttu-id="2d54f-112">Consulte o exemplo.</span><span class="sxs-lookup"><span data-stu-id="2d54f-112">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="2d54f-113">*Didistância* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d54f-113">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d54f-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d54f-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2d54f-115">O stride de cada plano transformado.</span><span class="sxs-lookup"><span data-stu-id="2d54f-115">The stride of each transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="2d54f-116">*PP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d54f-116">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d54f-117">Tipo: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="2d54f-117">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="2d54f-118">Ponteiro para a estrutura D3DXPLANE de entrada, que contém a matriz de planos para transformar.</span><span class="sxs-lookup"><span data-stu-id="2d54f-118">Pointer to the input D3DXPLANE structure, which contains the array of planes to transform.</span></span> <span data-ttu-id="2d54f-119">O vetor (a, b, c) que descreve o plano deve ser normalizado antes que essa função seja chamada.</span><span class="sxs-lookup"><span data-stu-id="2d54f-119">The vector (a, b, c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="2d54f-120">Consulte o exemplo.</span><span class="sxs-lookup"><span data-stu-id="2d54f-120">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="2d54f-121">*PStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d54f-121">*PStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d54f-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d54f-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2d54f-123">O stride de cada plano não transformado.</span><span class="sxs-lookup"><span data-stu-id="2d54f-123">The stride of each non-transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="2d54f-124">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2d54f-124">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d54f-125">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="2d54f-125">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2d54f-126">Ponteiro para a estrutura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origem, que contém a transpoção inversa dos valores de transformação.</span><span class="sxs-lookup"><span data-stu-id="2d54f-126">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure, which contains the inverse transpose of the transformation values.</span></span>

</dd> <dt>

<span data-ttu-id="2d54f-127">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="2d54f-127">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d54f-128">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d54f-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2d54f-129">O número de planos para transformar.</span><span class="sxs-lookup"><span data-stu-id="2d54f-129">The number of planes to transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d54f-130">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2d54f-130">Return value</span></span>

<span data-ttu-id="2d54f-131">Tipo: **[ **D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="2d54f-131">Type: **[**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="2d54f-132">Ponteiro para uma estrutura D3DXPLANE, representando o plano transformado.</span><span class="sxs-lookup"><span data-stu-id="2d54f-132">Pointer to a D3DXPLANE structure, representing the transformed plane.</span></span> <span data-ttu-id="2d54f-133">Esse é o mesmo valor retornado no parâmetro pOut para que essa função possa ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="2d54f-133">This is the same value returned in the pOut parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d54f-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d54f-134">Remarks</span></span>

<span data-ttu-id="2d54f-135">Este exemplo transforma um plano aplicando uma escala não uniforme.</span><span class="sxs-lookup"><span data-stu-id="2d54f-135">This example transforms one plane by applying a non-uniform scale.</span></span>


```
#define ARRAYSIZE 4
D3DXPLANE planeNew[ARRAYSIZE];
D3DXPLANE plane[ARRAYSIZE];

for(int i = 0; i < ARRAYSIZE; i++)
{
    plane = D3DXPLANE( 0.0f, 1.0f, 1.0f, 0.0f );
    D3DXPlaneNormalize( &plane[i], &plane[i] );
}

D3DXMATRIX  matrix;
D3DXMatrixScaling( &matrix, 1.0f, 2.0f, 3.0f ); 
D3DXMatrixInverse( &matrix, NULL, &matrix );
D3DXMatrixTranspose( &matrix, &matrix );
D3DXPlaneTransformArray( &planeNew, sizeof (D3DXPLANE), &plane, 
                         sizeof (D3DXPLANE), &matrix, ARRAYSIZE );
```



<span data-ttu-id="2d54f-136">Um plano é descrito por ax + by + cz + DW = 0.</span><span class="sxs-lookup"><span data-stu-id="2d54f-136">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="2d54f-137">O primeiro plano é criado com (a, b, c, d) = (0, 1, 1, 0), que é um plano descrito por y + z = 0.</span><span class="sxs-lookup"><span data-stu-id="2d54f-137">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="2d54f-138">Após o dimensionamento, o novo plano contém (a, b, c, d) = (0, 0.353 f, 0.235 f, 0), que mostra o novo plano a ser descrito por 0.353 y + 0.235 z = 0.</span><span class="sxs-lookup"><span data-stu-id="2d54f-138">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="2d54f-139">O parâmetro pM contém a transpoção inversa da matriz de transformação.</span><span class="sxs-lookup"><span data-stu-id="2d54f-139">The parameter pM, contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="2d54f-140">A Transpose inversa é exigida por esse método para que o vetor normal do plano transformado também possa ser transformado corretamente.</span><span class="sxs-lookup"><span data-stu-id="2d54f-140">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d54f-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d54f-141">Requirements</span></span>



| <span data-ttu-id="2d54f-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d54f-142">Requirement</span></span> | <span data-ttu-id="2d54f-143">Valor</span><span class="sxs-lookup"><span data-stu-id="2d54f-143">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d54f-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d54f-144">Header</span></span><br/>  | <dl> <span data-ttu-id="2d54f-145"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d54f-145"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="2d54f-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d54f-146">Library</span></span><br/> | <dl> <span data-ttu-id="2d54f-147"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d54f-147"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2d54f-148">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2d54f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d54f-149">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="2d54f-149">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
