---
description: Transforma um plano por uma matriz. A matriz de entrada é a transpoção inversa da transformação real.
ms.assetid: 3581b397-cbd8-4aed-80dd-1841f331a367
title: Função D3DXPlaneTransform (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneTransform
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fd82478d9fb1f08bb0320a8c84357efcdf20be26
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105757582"
---
# <a name="d3dxplanetransform-function-d3dx9mathh"></a><span data-ttu-id="e4e5c-104">Função D3DXPlaneTransform (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="e4e5c-104">D3DXPlaneTransform function (D3dx9math.h)</span></span>

<span data-ttu-id="e4e5c-105">Transforma um plano por uma matriz.</span><span class="sxs-lookup"><span data-stu-id="e4e5c-105">Transforms a plane by a matrix.</span></span> <span data-ttu-id="e4e5c-106">A matriz de entrada é a transpoção inversa da transformação real.</span><span class="sxs-lookup"><span data-stu-id="e4e5c-106">The input matrix is the inverse transpose of the actual transformation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4e5c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4e5c-107">Syntax</span></span>


```C++
D3DXPLANE* D3DXPlaneTransform(
  _Inout_       D3DXPLANE  *pOut,
  _In_    const D3DXPLANE  *pP,
  _In_    const D3DXMATRIX *pM
);
```



## <a name="parameters"></a><span data-ttu-id="e4e5c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4e5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4e5c-109">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="e4e5c-109">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e5c-110">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4e5c-110">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="e4e5c-111">Ponteiro para a estrutura [**D3DXPLANE**](d3dxplane.md) que contém o plano transformado resultante.</span><span class="sxs-lookup"><span data-stu-id="e4e5c-111">Pointer to the [**D3DXPLANE**](d3dxplane.md) structure that contains the resulting transformed plane.</span></span> <span data-ttu-id="e4e5c-112">Confira o exemplo.</span><span class="sxs-lookup"><span data-stu-id="e4e5c-112">See example.</span></span>

</dd> <dt>

<span data-ttu-id="e4e5c-113">*PP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4e5c-113">*pP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e5c-114">Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4e5c-114">Type: **const [**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="e4e5c-115">Ponteiro para a estrutura [**D3DXPLANE**](d3dxplane.md) de entrada, que contém o plano que será transformado.</span><span class="sxs-lookup"><span data-stu-id="e4e5c-115">Pointer to the input [**D3DXPLANE**](d3dxplane.md) structure, which contains the plane that will be transformed.</span></span> <span data-ttu-id="e4e5c-116">O vetor (a, b, c) que descreve o plano deve ser normalizado antes que essa função seja chamada.</span><span class="sxs-lookup"><span data-stu-id="e4e5c-116">The vector (a,b,c) that describes the plane must be normalized before this function is called.</span></span> <span data-ttu-id="e4e5c-117">Confira o exemplo.</span><span class="sxs-lookup"><span data-stu-id="e4e5c-117">See example.</span></span>

</dd> <dt>

<span data-ttu-id="e4e5c-118">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4e5c-118">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e5c-119">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e4e5c-119">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e4e5c-120">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) de origem, que contém os valores de transformação.</span><span class="sxs-lookup"><span data-stu-id="e4e5c-120">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure, which contains the transformation values.</span></span> <span data-ttu-id="e4e5c-121">Essa matriz deve conter a transpoção inversa dos valores de transformação.</span><span class="sxs-lookup"><span data-stu-id="e4e5c-121">This matrix must contain the inverse transpose of the transformation values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4e5c-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4e5c-122">Return value</span></span>

<span data-ttu-id="e4e5c-123">Tipo: **[ **D3DXPLANE**](d3dxplane.md)\***</span><span class="sxs-lookup"><span data-stu-id="e4e5c-123">Type: **[**D3DXPLANE**](d3dxplane.md)\***</span></span>

<span data-ttu-id="e4e5c-124">Ponteiro para uma estrutura [**D3DXPLANE**](d3dxplane.md) , representando o plano transformado.</span><span class="sxs-lookup"><span data-stu-id="e4e5c-124">Pointer to a [**D3DXPLANE**](d3dxplane.md) structure, representing the transformed plane.</span></span> <span data-ttu-id="e4e5c-125">Esse é o mesmo valor retornado no parâmetro pOut para que essa função possa ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="e4e5c-125">This is the same value returned in the pOut parameter so that this function can be used as a parameter for another function.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4e5c-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4e5c-126">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="e4e5c-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e4e5c-127">Examples</span></span>

<span data-ttu-id="e4e5c-128">Este exemplo transforma um plano aplicando uma escala não uniforme.</span><span class="sxs-lookup"><span data-stu-id="e4e5c-128">This example transforms a plane by applying a non-uniform scale.</span></span>


```
D3DXPLANE   planeNew;
D3DXPLANE   plane(0,1,1,0);
D3DXPlaneNormalize(&plane, &plane);

D3DXMATRIX  matrix;
D3DXMatrixScaling(&matrix, 1.0f,2.0f,3.0f); 
D3DXMatrixInverse(&matrix, NULL, &matrix);
D3DXMatrixTranspose(&matrix, &matrix);
D3DXPlaneTransform(&planeNew, &plane, &matrix);
```



<span data-ttu-id="e4e5c-129">Um plano é descrito por ax + by + cz + DW = 0.</span><span class="sxs-lookup"><span data-stu-id="e4e5c-129">A plane is described by ax + by + cz + dw = 0.</span></span> <span data-ttu-id="e4e5c-130">O primeiro plano é criado com (a, b, c, d) = (0, 1, 1, 0), que é um plano descrito por y + z = 0.</span><span class="sxs-lookup"><span data-stu-id="e4e5c-130">The first plane is created with (a,b,c,d) = (0,1,1,0), which is a plane described by y + z = 0.</span></span> <span data-ttu-id="e4e5c-131">Após o dimensionamento, o novo plano contém (a, b, c, d) = (0, 0.353 f, 0.235 f, 0), que mostra o novo plano a ser descrito por 0.353 y + 0.235 z = 0.</span><span class="sxs-lookup"><span data-stu-id="e4e5c-131">After scaling, the new plane contains (a,b,c,d) = (0, 0.353f, 0.235f, 0), which shows the new plane to be described by 0.353y + 0.235z = 0.</span></span>

<span data-ttu-id="e4e5c-132">O parâmetro pM contém a transpoção inversa da matriz de transformação.</span><span class="sxs-lookup"><span data-stu-id="e4e5c-132">The parameter pM contains the inverse transpose of the transformation matrix.</span></span> <span data-ttu-id="e4e5c-133">A Transpose inversa é exigida por esse método para que o vetor normal do plano transformado também possa ser transformado corretamente.</span><span class="sxs-lookup"><span data-stu-id="e4e5c-133">The inverse transpose is required by this method so that the normal vector of the transformed plane can be correctly transformed as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4e5c-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4e5c-134">Requirements</span></span>



| <span data-ttu-id="e4e5c-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4e5c-135">Requirement</span></span> | <span data-ttu-id="e4e5c-136">Valor</span><span class="sxs-lookup"><span data-stu-id="e4e5c-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4e5c-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4e5c-137">Header</span></span><br/>  | <dl> <span data-ttu-id="e4e5c-138"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4e5c-138"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="e4e5c-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e4e5c-139">Library</span></span><br/> | <dl> <span data-ttu-id="e4e5c-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4e5c-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e4e5c-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4e5c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4e5c-142">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="e4e5c-142">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="e4e5c-143">**D3DXPlaneNormalize**</span><span class="sxs-lookup"><span data-stu-id="e4e5c-143">**D3DXPlaneNormalize**</span></span>](d3dxplanenormalize.md)
</dt> <dt>

[<span data-ttu-id="e4e5c-144">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="e4e5c-144">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="e4e5c-145">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="e4e5c-145">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="e4e5c-146">**D3DXMatrixRotationZ**</span><span class="sxs-lookup"><span data-stu-id="e4e5c-146">**D3DXMatrixRotationZ**</span></span>](d3dxmatrixrotationz.md)
</dt> <dt>

[<span data-ttu-id="e4e5c-147">**D3DXMatrixInverse**</span><span class="sxs-lookup"><span data-stu-id="e4e5c-147">**D3DXMatrixInverse**</span></span>](d3dxmatrixinverse.md)
</dt> <dt>

[<span data-ttu-id="e4e5c-148">**D3DXMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="e4e5c-148">**D3DXMatrixTranspose**</span></span>](d3dxmatrixtranspose.md)
</dt> </dl>

 

 




