---
description: Função D3DXMatrixLookAtLH (D3DX10Math. h) – compila uma matriz de aparência da esquerda.
ms.assetid: 06888a97-66ef-447f-be8b-ea458ce16b4b
title: Função D3DXMatrixLookAtLH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixLookAtLH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3590d2cbdeead9e1b9b2547b2344163b81f05d11
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109164"
---
# <a name="d3dxmatrixlookatlh-function-d3dx10mathh"></a><span data-ttu-id="d3d1f-103">Função D3DXMatrixLookAtLH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d3d1f-103">D3DXMatrixLookAtLH function (D3DX10Math.h)</span></span>

<span data-ttu-id="d3d1f-104">Cria uma matriz de visão à esquerda.</span><span class="sxs-lookup"><span data-stu-id="d3d1f-104">Builds a left-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3d1f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d3d1f-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtLH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="d3d1f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d3d1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3d1f-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d3d1f-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3d1f-108">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d3d1f-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d3d1f-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3d10-d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="d3d1f-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d3d1f-110">*pEye* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d3d1f-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3d1f-111">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d3d1f-111">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d3d1f-112">Ponteiro para o [**D3DXVECTOR3**](d3d10-d3dxvector3.md) que define o ponto de olho.</span><span class="sxs-lookup"><span data-stu-id="d3d1f-112">Pointer to the [**D3DXVECTOR3**](d3d10-d3dxvector3.md) that defines the eye point.</span></span> <span data-ttu-id="d3d1f-113">Esse valor é usado na tradução.</span><span class="sxs-lookup"><span data-stu-id="d3d1f-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="d3d1f-114">*pAt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d3d1f-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3d1f-115">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d3d1f-115">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d3d1f-116">Ponteiro para a estrutura D3DXVECTOR3 que define o destino da aparência da câmera.</span><span class="sxs-lookup"><span data-stu-id="d3d1f-116">Pointer to the D3DXVECTOR3 structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="d3d1f-117">*pUp* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d3d1f-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3d1f-118">Tipo: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d3d1f-118">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d3d1f-119">Ponteiro para a estrutura D3DXVECTOR3 que define o mundo atual, geralmente \[ 0, 1, 0 \] .</span><span class="sxs-lookup"><span data-stu-id="d3d1f-119">Pointer to the D3DXVECTOR3 structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3d1f-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d3d1f-120">Return value</span></span>

<span data-ttu-id="d3d1f-121">Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="d3d1f-121">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="d3d1f-122">Ponteiro para uma estrutura D3DXMATRIX que é uma matriz de aparência da esquerda.</span><span class="sxs-lookup"><span data-stu-id="d3d1f-122">Pointer to a D3DXMATRIX structure that is a left-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3d1f-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3d1f-123">Remarks</span></span>

<span data-ttu-id="d3d1f-124">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="d3d1f-124">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d3d1f-125">Dessa forma, a função D3DXMatrixLookAtLH pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="d3d1f-125">In this way, the D3DXMatrixLookAtLH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="d3d1f-126">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="d3d1f-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(At - Eye)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
-dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="d3d1f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3d1f-127">Requirements</span></span>



| <span data-ttu-id="d3d1f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3d1f-128">Requirement</span></span> | <span data-ttu-id="d3d1f-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d3d1f-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3d1f-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d3d1f-130">Header</span></span><br/>  | <dl> <span data-ttu-id="d3d1f-131"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3d1f-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="d3d1f-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d3d1f-132">Library</span></span><br/> | <dl> <span data-ttu-id="d3d1f-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3d1f-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d3d1f-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d3d1f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3d1f-135">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="d3d1f-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
