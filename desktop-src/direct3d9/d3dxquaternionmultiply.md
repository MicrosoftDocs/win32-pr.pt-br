---
description: Função D3DXQuaternionMultiply (D3dx9math. h) – Multiplica dois quaternions.
ms.assetid: 11072fc9-dae8-4f63-b07d-b709eed381df
title: Função D3DXQuaternionMultiply (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7250484e4943e8b077a63e35951c17a44eaf2de3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118034"
---
# <a name="d3dxquaternionmultiply-function-d3dx9mathh"></a><span data-ttu-id="8fc1c-103">Função D3DXQuaternionMultiply (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="8fc1c-103">D3DXQuaternionMultiply function (D3dx9math.h)</span></span>

<span data-ttu-id="8fc1c-104">Multiplica dois quaternions.</span><span class="sxs-lookup"><span data-stu-id="8fc1c-104">Multiplies two quaternions.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fc1c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8fc1c-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionMultiply(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2
);
```



## <a name="parameters"></a><span data-ttu-id="8fc1c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8fc1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fc1c-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="8fc1c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fc1c-108">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="8fc1c-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="8fc1c-109">Ponteiro para a estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="8fc1c-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8fc1c-110">*pQ1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8fc1c-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fc1c-111">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="8fc1c-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="8fc1c-112">Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="8fc1c-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8fc1c-113">*pQ2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8fc1c-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fc1c-114">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="8fc1c-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="8fc1c-115">Ponteiro para uma estrutura de [**D3DXQUATERNION**](d3dxquaternion.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="8fc1c-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fc1c-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8fc1c-116">Return value</span></span>

<span data-ttu-id="8fc1c-117">Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="8fc1c-117">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="8fc1c-118">Ponteiro para uma estrutura [**D3DXQUATERNION**](d3dxquaternion.md) que é o produto de dois quaternions.</span><span class="sxs-lookup"><span data-stu-id="8fc1c-118">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the product of two quaternions.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fc1c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="8fc1c-119">Remarks</span></span>

<span data-ttu-id="8fc1c-120">O resultado representa a rotação Q1 seguida da rotação Q2 (out = T2 \* Q1).</span><span class="sxs-lookup"><span data-stu-id="8fc1c-120">The result represents the rotation Q1 followed by the rotation Q2 (Out = Q2 \* Q1).</span></span> <span data-ttu-id="8fc1c-121">Isso é feito para que **D3DXQuaternionMultiply** mantenha a mesma semântica que [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) porque a unidade quaternions pode ser considerada como outra maneira de representar matrizes de rotação.</span><span class="sxs-lookup"><span data-stu-id="8fc1c-121">This is done so that **D3DXQuaternionMultiply** maintain the same semantics as [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) because unit quaternions can be considered as another way to represent rotation matrices.</span></span>

<span data-ttu-id="8fc1c-122">As transformações são concatenadas na mesma ordem para as funções **D3DXQuaternionMultiply** e [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) .</span><span class="sxs-lookup"><span data-stu-id="8fc1c-122">Transformations are concatenated in the same order for both the **D3DXQuaternionMultiply** and [**D3DXMatrixMultiply**](d3dxmatrixmultiply.md) functions.</span></span> <span data-ttu-id="8fc1c-123">Por exemplo, supondo que mX e mY representem as mesmas rotações que qX e qY, m e q representarão as mesmas rotações.</span><span class="sxs-lookup"><span data-stu-id="8fc1c-123">For example, assuming mX and mY represent the same rotations as qX and qY, both m and q will represent the same rotations.</span></span>


```
D3DXMatrixMultiply(&m, &mX, &mY);
D3DXQuaternionMultiply(&q, &qX, &qY);
```



<span data-ttu-id="8fc1c-124">A multiplicação de quaternions não é comutada.</span><span class="sxs-lookup"><span data-stu-id="8fc1c-124">The multiplication of quaternions is not commutative.</span></span>

<span data-ttu-id="8fc1c-125">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="8fc1c-125">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="8fc1c-126">Dessa forma, a função **D3DXQuaternionMultiply** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="8fc1c-126">In this way, the **D3DXQuaternionMultiply** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="8fc1c-127">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) para qualquer entrada de Quaternion que ainda não esteja normalizada.</span><span class="sxs-lookup"><span data-stu-id="8fc1c-127">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fc1c-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fc1c-128">Requirements</span></span>



| <span data-ttu-id="8fc1c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fc1c-129">Requirement</span></span> | <span data-ttu-id="8fc1c-130">Valor</span><span class="sxs-lookup"><span data-stu-id="8fc1c-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc1c-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8fc1c-131">Header</span></span><br/>  | <dl> <span data-ttu-id="8fc1c-132"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fc1c-132"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="8fc1c-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8fc1c-133">Library</span></span><br/> | <dl> <span data-ttu-id="8fc1c-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8fc1c-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8fc1c-135">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8fc1c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fc1c-136">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="8fc1c-136">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="8fc1c-137">**D3DXMatrixMultiply**</span><span class="sxs-lookup"><span data-stu-id="8fc1c-137">**D3DXMatrixMultiply**</span></span>](d3dxmatrixmultiply.md)
</dt> </dl>

 

 




