---
description: Transforma uma matriz de planos por uma matriz. Os vetores que descrevem cada plano devem ser normalizados.
ms.assetid: e82e830b-efbb-4bdc-b370-7bfa4326a669
title: Função D3DXPlaneTransformArray (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a9a213b17aca9999ef0028fdceb4bb4321d47660
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105750890"
---
# <a name="d3dxplanetransformarray-function-d3dx9mathh"></a><span data-ttu-id="fd488-104">Função D3DXPlaneTransformArray (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="fd488-104">D3DXPlaneTransformArray function (D3dx9math.h)</span></span>

<span data-ttu-id="fd488-105">Transforma uma matriz de planos por uma matriz.</span><span class="sxs-lookup"><span data-stu-id="fd488-105">Transforms an array of planes by a matrix.</span></span> <span data-ttu-id="fd488-106">Os vetores que descrevem cada plano devem ser normalizados.</span><span class="sxs-lookup"><span data-stu-id="fd488-106">The vectors that describe each plane must be normalized.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd488-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd488-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransformArray(
  _Inout_       D3DXPLANE  *pOut,
  _Out_         UINT       OutStride,
  _In_    const D3DXPLANE  *pP,
  _In_          UINT       PStride,
  _In_    const D3DXMATRIX *pM,
  _In_          UINT       n
);
```



## <a name="parameters"></a><span data-ttu-id="fd488-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd488-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd488-109">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="fd488-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd488-110">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="fd488-110">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="fd488-111">Ponteiro para a estrutura [**D3DXPLANE**](d3dxplane.md) que contém o plano transformado resultante.</span><span class="sxs-lookup"><span data-stu-id="fd488-111">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that contains the resulting transformed plane.</span></span> <span data-ttu-id="fd488-112">Consulte o exemplo.</span><span class="sxs-lookup"><span data-stu-id="fd488-112">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="fd488-113">*Didistância* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fd488-113">*OutStride* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd488-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd488-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fd488-115">O stride de cada plano transformado.</span><span class="sxs-lookup"><span data-stu-id="fd488-115">The stride of each transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="fd488-116">*PP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd488-116">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd488-117">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="fd488-117">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="fd488-118">Ponteiro para a estrutura [**D3DXPLANE**](d3dxplane.md) de entrada, que contém a matriz de planos para transformar.</span><span class="sxs-lookup"><span data-stu-id="fd488-118">Pointer to the input [**D3DXPLANE**](d3dxplane.md) structure, which contains the array of planes to transform.</span></span> <span data-ttu-id="fd488-119">O vetor (a, b, c) que descreve o plano deve ser normalizado antes que essa função seja chamada.</span><span class="sxs-lookup"><span data-stu-id="fd488-119">The vector (a,b,c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="fd488-120">Consulte o exemplo.</span><span class="sxs-lookup"><span data-stu-id="fd488-120">See Example.</span></span>

</dd> <dt>

<span data-ttu-id="fd488-121">*PStride* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd488-121">*PStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd488-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd488-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fd488-123">O stride de cada plano não transformado.</span><span class="sxs-lookup"><span data-stu-id="fd488-123">The stride of each non-transformed plane.</span></span>

</dd> <dt>

<span data-ttu-id="fd488-124">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fd488-124">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd488-125">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="fd488-125">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="fd488-126">Ponteiro para a estrutura de [**D3DXMATRIX**](d3dxmatrix.md) de origem, que contém a transpoção inversa dos valores de transformação.</span><span class="sxs-lookup"><span data-stu-id="fd488-126">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure, which contains the inverse transpose of the transformation values.</span></span>

</dd> <dt>

<span data-ttu-id="fd488-127">*n* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="fd488-127">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd488-128">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fd488-128">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fd488-129">O número de planos para transformar.</span><span class="sxs-lookup"><span data-stu-id="fd488-129">The number of planes to transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd488-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fd488-130">Return value</span></span>

<span data-ttu-id="fd488-131">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="fd488-131">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="fd488-132">Ponteiro para uma estrutura [**D3DXPLANE**](d3dxplane.md) , representando o plano transformado.</span><span class="sxs-lookup"><span data-stu-id="fd488-132">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure, representing the transformed plane.</span></span> <span data-ttu-id="fd488-133">Esse é o mesmo valor retornado no parâmetro *pout* para que essa função possa ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="fd488-133">This is the same value returned in the *pOut* parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd488-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd488-134">Remarks</span></span>

<span data-ttu-id="fd488-135">Este exemplo transforma um plano aplicando uma escala não uniforme.</span><span class="sxs-lookup"><span data-stu-id="fd488-135">This example transforms one plane by applying a non-uniform scale.</span></span>


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



<span data-ttu-id="fd488-136">Um plano é descrito por ax + by + cz + DW = 0.</span><span class="sxs-lookup"><span data-stu-id="fd488-136">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="fd488-137">O primeiro plano é criado com (a, b, c, d) = (0, 1, 1, 0), que é um plano descrito por y + z = 0.</span><span class="sxs-lookup"><span data-stu-id="fd488-137">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="fd488-138">Após o dimensionamento, o novo plano contém (a, b, c, d) = (0, 0.353 f, 0.235 f, 0), que mostra o novo plano a ser descrito por 0.353 y + 0.235 z = 0.</span><span class="sxs-lookup"><span data-stu-id="fd488-138">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="fd488-139">O parâmetro *PM* contém a transpoção inversa da matriz de transformação.</span><span class="sxs-lookup"><span data-stu-id="fd488-139">The parameter *pM* contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="fd488-140">A Transpose inversa é exigida por esse método para que o vetor normal do plano transformado também possa ser transformado corretamente.</span><span class="sxs-lookup"><span data-stu-id="fd488-140">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd488-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd488-141">Requirements</span></span>



| <span data-ttu-id="fd488-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd488-142">Requirement</span></span> | <span data-ttu-id="fd488-143">Valor</span><span class="sxs-lookup"><span data-stu-id="fd488-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd488-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fd488-144">Header</span></span><br/>  | <dl> <span data-ttu-id="fd488-145"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd488-145"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="fd488-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fd488-146">Library</span></span><br/> | <dl> <span data-ttu-id="fd488-147"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd488-147"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fd488-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd488-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd488-149">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="fd488-149">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="fd488-150">**D3DXPlaneNormalize**</span><span class="sxs-lookup"><span data-stu-id="fd488-150">**D3DXPlaneNormalize**</span></span>](d3dxplanenormalize.md)
</dt> <dt>

[<span data-ttu-id="fd488-151">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="fd488-151">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="fd488-152">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="fd488-152">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="fd488-153">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="fd488-153">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> <dt>

[<span data-ttu-id="fd488-154">**D3DXMatrixInverse**</span><span class="sxs-lookup"><span data-stu-id="fd488-154">**D3DXMatrixInverse**</span></span>](d3dxmatrixinverse.md)
</dt> <dt>

[<span data-ttu-id="fd488-155">**D3DXMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="fd488-155">**D3DXMatrixTranspose**</span></span>](d3dxmatrixtranspose.md)
</dt> </dl>

 

 
