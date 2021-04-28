---
description: Função D3DXQuaternionRotationMatrix (D3DX10Math. h) – compila um Quaternion a partir de uma matriz de rotação.
ms.assetid: 316bf3e0-32ff-4e5e-b771-99f7eea2e27c
title: Função D3DXQuaternionRotationMatrix (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionRotationMatrix
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: cb923c135d436b36fe032d344366fdee687d27a0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103144"
---
# <a name="d3dxquaternionrotationmatrix-function-d3dx10mathh"></a><span data-ttu-id="12abe-103">Função D3DXQuaternionRotationMatrix (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="12abe-103">D3DXQuaternionRotationMatrix function (D3DX10Math.h)</span></span>

<span data-ttu-id="12abe-104">Cria um Quaternion a partir de uma matriz de rotação.</span><span class="sxs-lookup"><span data-stu-id="12abe-104">Builds a quaternion from a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="12abe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12abe-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionRotationMatrix(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXMATRIX     *pM
);
```



## <a name="parameters"></a><span data-ttu-id="12abe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12abe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12abe-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="12abe-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="12abe-108">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="12abe-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="12abe-109">Ponteiro para o [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="12abe-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="12abe-110">*PM* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12abe-110">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12abe-111">Tipo: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="12abe-111">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="12abe-112">Ponteiro para a estrutura de [**D3DXMATRIX**](d3d10-d3dxmatrix.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="12abe-112">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12abe-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="12abe-113">Return value</span></span>

<span data-ttu-id="12abe-114">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="12abe-114">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="12abe-115">Ponteiro para a estrutura D3DXQUATERNION criada a partir de uma matriz de rotação.</span><span class="sxs-lookup"><span data-stu-id="12abe-115">Pointer to the D3DXQUATERNION structure built from a rotation matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="12abe-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="12abe-116">Remarks</span></span>

<span data-ttu-id="12abe-117">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="12abe-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="12abe-118">Dessa forma, a função D3DXQuaternionRotationMatrix pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="12abe-118">In this way, the D3DXQuaternionRotationMatrix function can be used as a parameter for another function.</span></span>

<span data-ttu-id="12abe-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="12abe-119">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="12abe-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12abe-120">Requirements</span></span>



| <span data-ttu-id="12abe-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="12abe-121">Requirement</span></span> | <span data-ttu-id="12abe-122">Valor</span><span class="sxs-lookup"><span data-stu-id="12abe-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12abe-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12abe-123">Header</span></span><br/>  | <dl> <span data-ttu-id="12abe-124"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="12abe-124"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="12abe-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="12abe-125">Library</span></span><br/> | <dl> <span data-ttu-id="12abe-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12abe-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="12abe-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="12abe-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12abe-128">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="12abe-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
