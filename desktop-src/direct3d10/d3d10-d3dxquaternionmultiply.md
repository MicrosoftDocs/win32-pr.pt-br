---
description: Multiplica dois quaternions.
ms.assetid: f549e383-9c39-47a9-84e4-82365bdf1155
title: Função D3DXQuaternionMultiply (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionMultiply
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 74e10117bf27d922480418e5aa0b8ea60a13528c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105778460"
---
# <a name="d3dxquaternionmultiply-function-d3dx10mathh"></a><span data-ttu-id="fe15c-103">Função D3DXQuaternionMultiply (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="fe15c-103">D3DXQuaternionMultiply function (D3DX10Math.h)</span></span>

<span data-ttu-id="fe15c-104">Multiplica dois quaternions.</span><span class="sxs-lookup"><span data-stu-id="fe15c-104">Multiplies two quaternions.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe15c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe15c-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionMultiply(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a><span data-ttu-id="fe15c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe15c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe15c-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="fe15c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe15c-108">Tipo: **[ **D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="fe15c-108">Type: **[**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fe15c-109">Ponteiro para o [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="fe15c-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="fe15c-110">*pQ1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fe15c-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe15c-111">Tipo: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="fe15c-111">Type: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fe15c-112">Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="fe15c-112">Pointer to a source [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="fe15c-113">*pQ2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fe15c-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe15c-114">Tipo: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="fe15c-114">Type: **const [**D3DXQUATERNION**](d3d10-d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fe15c-115">Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="fe15c-115">Pointer to a source [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe15c-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fe15c-116">Return value</span></span>

<span data-ttu-id="fe15c-117">Tipo: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="fe15c-117">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="fe15c-118">Ponteiro para uma estrutura [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) que é o produto de dois quaternions.</span><span class="sxs-lookup"><span data-stu-id="fe15c-118">Pointer to a [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) structure that is the product of two quaternions.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe15c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe15c-119">Remarks</span></span>

<span data-ttu-id="fe15c-120">O resultado representa a rotação Q1 seguida da rotação Q2 (out = T2 \* Q1).</span><span class="sxs-lookup"><span data-stu-id="fe15c-120">The result represents the rotation Q1 followed by the rotation Q2 (Out = Q2 \* Q1).</span></span> <span data-ttu-id="fe15c-121">Isso é feito para que **D3DXQuaternionMultiply** mantenha a mesma semântica que [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) porque a unidade quaternions pode ser considerada como outra maneira de representar matrizes de rotação.</span><span class="sxs-lookup"><span data-stu-id="fe15c-121">This is done so that **D3DXQuaternionMultiply** maintain the same semantics as [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) because unit quaternions can be considered as another way to represent rotation matrices.</span></span>

<span data-ttu-id="fe15c-122">As transformações são concatenadas na mesma ordem para as funções **D3DXQuaternionMultiply** e [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) .</span><span class="sxs-lookup"><span data-stu-id="fe15c-122">Transformations are concatenated in the same order for both the **D3DXQuaternionMultiply** and [**D3DXMatrixMultiply**](d3d10-d3dxmatrixmultiply.md) Functions.</span></span> <span data-ttu-id="fe15c-123">Por exemplo, supondo que mX e mY representem as mesmas rotações que qX e qY, m e q representarão as mesmas rotações.</span><span class="sxs-lookup"><span data-stu-id="fe15c-123">For example, assuming mX and mY represent the same rotations as qX and qY, both m and q will represent the same rotations.</span></span>


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



<span data-ttu-id="fe15c-124">A multiplicação de quaternions não é comutada.</span><span class="sxs-lookup"><span data-stu-id="fe15c-124">The multiplication of quaternions is not commutative.</span></span>

<span data-ttu-id="fe15c-125">O valor de retorno para essa função é o mesmo valor retornado no parâmetro pOut.</span><span class="sxs-lookup"><span data-stu-id="fe15c-125">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="fe15c-126">Dessa forma, a função **D3DXQuaternionMultiply** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="fe15c-126">In this way, the **D3DXQuaternionMultiply** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="fe15c-127">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="fe15c-127">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe15c-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe15c-128">Requirements</span></span>



| <span data-ttu-id="fe15c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe15c-129">Requirement</span></span> | <span data-ttu-id="fe15c-130">Valor</span><span class="sxs-lookup"><span data-stu-id="fe15c-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe15c-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe15c-131">Header</span></span><br/>  | <dl> <span data-ttu-id="fe15c-132"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe15c-132"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="fe15c-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fe15c-133">Library</span></span><br/> | <dl> <span data-ttu-id="fe15c-134"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe15c-134"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fe15c-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe15c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe15c-136">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="fe15c-136">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
