---
description: Função D3DXMatrixLookAtRH (D3DX10Math. h) – compila uma matriz de aparência à direita.
ms.assetid: 98c8932f-f179-42ed-a361-a89065b71876
title: Função D3DXMatrixLookAtRH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixLookAtRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0380207124e4a446b6303dbb377d116b8ae058ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103444"
---
# <a name="d3dxmatrixlookatrh-function-d3dx10mathh"></a><span data-ttu-id="b47b5-103">Função D3DXMatrixLookAtRH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="b47b5-103">D3DXMatrixLookAtRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="b47b5-104">Cria uma matriz de aparência à direita.</span><span class="sxs-lookup"><span data-stu-id="b47b5-104">Builds a right-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b47b5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b47b5-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtRH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="b47b5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b47b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b47b5-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="b47b5-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b47b5-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b47b5-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b47b5-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="b47b5-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b47b5-110">*pEye* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b47b5-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b47b5-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b47b5-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b47b5-112">Ponteiro para o [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que define o ponto de olho.</span><span class="sxs-lookup"><span data-stu-id="b47b5-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that defines the eye point.</span></span> <span data-ttu-id="b47b5-113">Esse valor é usado na tradução.</span><span class="sxs-lookup"><span data-stu-id="b47b5-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="b47b5-114">*pAt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b47b5-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b47b5-115">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b47b5-115">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b47b5-116">Ponteiro para a estrutura D3DXVECTOR3 que define o destino da aparência da câmera.</span><span class="sxs-lookup"><span data-stu-id="b47b5-116">Pointer to the D3DXVECTOR3 structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="b47b5-117">*pUp* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b47b5-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b47b5-118">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b47b5-118">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="b47b5-119">Ponteiro para a estrutura D3DXVECTOR3 que define o mundo atual, geralmente \[ 0, 1, 0 \] .</span><span class="sxs-lookup"><span data-stu-id="b47b5-119">Pointer to the D3DXVECTOR3 structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b47b5-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b47b5-120">Return value</span></span>

<span data-ttu-id="b47b5-121">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b47b5-121">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b47b5-122">Ponteiro para uma estrutura D3DXMATRIX que é uma matriz de aparência da mão direita.</span><span class="sxs-lookup"><span data-stu-id="b47b5-122">Pointer to a D3DXMATRIX structure that is a right-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="b47b5-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="b47b5-123">Remarks</span></span>

<span data-ttu-id="b47b5-124">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="b47b5-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="b47b5-125">Dessa forma, a função D3DXMatrixLookAtRH pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="b47b5-125">In this way, the D3DXMatrixLookAtRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b47b5-126">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="b47b5-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(Eye - At)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 -xaxis.x           yaxis.x           -zaxis.x          0
 -xaxis.y           yaxis.y           -zaxis.y          0
 -xaxis.z           yaxis.z           -zaxis.z          0
dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="b47b5-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b47b5-127">Requirements</span></span>



| <span data-ttu-id="b47b5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b47b5-128">Requirement</span></span> | <span data-ttu-id="b47b5-129">Valor</span><span class="sxs-lookup"><span data-stu-id="b47b5-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b47b5-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b47b5-130">Header</span></span><br/>  | <dl> <span data-ttu-id="b47b5-131"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b47b5-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="b47b5-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b47b5-132">Library</span></span><br/> | <dl> <span data-ttu-id="b47b5-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b47b5-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b47b5-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b47b5-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b47b5-135">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="b47b5-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
