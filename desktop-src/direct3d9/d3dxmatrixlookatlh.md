---
description: Cria uma matriz de visão à esquerda.
ms.assetid: bf34d3d8-725d-4fc1-b4c8-6c98f9dac329
title: Função D3DXMatrixLookAtLH (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97fa7acdf467761bd3b3cfbc023662e9b3368b98
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791546"
---
# <a name="d3dxmatrixlookatlh-function-d3dx9mathh"></a><span data-ttu-id="b14e9-103">Função D3DXMatrixLookAtLH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="b14e9-103">D3DXMatrixLookAtLH function (D3dx9math.h)</span></span>

<span data-ttu-id="b14e9-104">Cria uma matriz de visão à esquerda.</span><span class="sxs-lookup"><span data-stu-id="b14e9-104">Builds a left-handed, look-at matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="b14e9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b14e9-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixLookAtLH(
  _Inout_       D3DXMATRIX  *pOut,
  _In_    const D3DXVECTOR3 *pEye,
  _In_    const D3DXVECTOR3 *pAt,
  _In_    const D3DXVECTOR3 *pUp
);
```



## <a name="parameters"></a><span data-ttu-id="b14e9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b14e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b14e9-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="b14e9-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b14e9-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b14e9-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b14e9-109">Ponteiro para a estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="b14e9-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b14e9-110">*pEye* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b14e9-110">*pEye* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b14e9-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b14e9-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b14e9-112">Ponteiro para a estrutura [**D3DXVECTOR3**](d3dxvector3.md) que define o ponto de olho.</span><span class="sxs-lookup"><span data-stu-id="b14e9-112">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the eye point.</span></span> <span data-ttu-id="b14e9-113">Esse valor é usado na tradução.</span><span class="sxs-lookup"><span data-stu-id="b14e9-113">This value is used in translation.</span></span>

</dd> <dt>

<span data-ttu-id="b14e9-114">*pAt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b14e9-114">*pAt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b14e9-115">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b14e9-115">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b14e9-116">Ponteiro para a estrutura [**D3DXVECTOR3**](d3dxvector3.md) que define o destino da aparência da câmera.</span><span class="sxs-lookup"><span data-stu-id="b14e9-116">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the camera look-at target.</span></span>

</dd> <dt>

<span data-ttu-id="b14e9-117">*pUp* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b14e9-117">*pUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b14e9-118">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="b14e9-118">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="b14e9-119">Ponteiro para a estrutura [**D3DXVECTOR3**](d3dxvector3.md) que define o mundo atual, geralmente \[ 0, 1, 0 \] .</span><span class="sxs-lookup"><span data-stu-id="b14e9-119">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) structure that defines the current world's up, usually \[0, 1, 0\].</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b14e9-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b14e9-120">Return value</span></span>

<span data-ttu-id="b14e9-121">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="b14e9-121">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="b14e9-122">Ponteiro para uma estrutura [**D3DXMATRIX**](d3dxmatrix.md) que é uma matriz de aparência da esquerda.</span><span class="sxs-lookup"><span data-stu-id="b14e9-122">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a left-handed, look-at matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="b14e9-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="b14e9-123">Remarks</span></span>

<span data-ttu-id="b14e9-124">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="b14e9-124">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="b14e9-125">Dessa forma, a função **D3DXMatrixLookAtLH** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="b14e9-125">In this way, the **D3DXMatrixLookAtLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="b14e9-126">Essa função usa a fórmula a seguir para calcular a matriz retornada.</span><span class="sxs-lookup"><span data-stu-id="b14e9-126">This function uses the following formula to compute the returned matrix.</span></span>


```
zaxis = normal(At - Eye)
xaxis = normal(cross(Up, zaxis))
yaxis = cross(zaxis, xaxis)
    
 xaxis.x           yaxis.x           zaxis.x          0
 xaxis.y           yaxis.y           zaxis.y          0
 xaxis.z           yaxis.z           zaxis.z          0
-dot(xaxis, eye)  -dot(yaxis, eye)  -dot(zaxis, eye)  1
```



## <a name="requirements"></a><span data-ttu-id="b14e9-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b14e9-127">Requirements</span></span>



| <span data-ttu-id="b14e9-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b14e9-128">Requirement</span></span> | <span data-ttu-id="b14e9-129">Valor</span><span class="sxs-lookup"><span data-stu-id="b14e9-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b14e9-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b14e9-130">Header</span></span><br/>  | <dl> <span data-ttu-id="b14e9-131"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="b14e9-131"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="b14e9-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b14e9-132">Library</span></span><br/> | <dl> <span data-ttu-id="b14e9-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b14e9-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b14e9-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="b14e9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b14e9-135">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="b14e9-135">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="b14e9-136">**D3DXMatrixLookAtRH**</span><span class="sxs-lookup"><span data-stu-id="b14e9-136">**D3DXMatrixLookAtRH**</span></span>](d3dxmatrixlookatrh.md)
</dt> </dl>

 

 




