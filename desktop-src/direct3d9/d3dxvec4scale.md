---
description: Dimensiona um vetor 4D.
ms.assetid: b185a9b9-f768-4b50-aa6c-667c71eac39a
title: Função D3DXVec4Scale (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Scale
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a29ee7b8519c802deb0542b6b7ba3ea22692f36d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807820"
---
# <a name="d3dxvec4scale-function"></a><span data-ttu-id="18928-103">Função D3DXVec4Scale</span><span class="sxs-lookup"><span data-stu-id="18928-103">D3DXVec4Scale function</span></span>

<span data-ttu-id="18928-104">Dimensiona um vetor 4D.</span><span class="sxs-lookup"><span data-stu-id="18928-104">Scales a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="18928-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18928-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Scale(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_          FLOAT       s
);
```



## <a name="parameters"></a><span data-ttu-id="18928-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18928-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18928-107">*pout* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="18928-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="18928-108">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="18928-108">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="18928-109">Ponteiro para a estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="18928-109">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="18928-110">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="18928-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18928-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="18928-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="18928-112">Ponteiro para a estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="18928-112">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="18928-113">*s* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="18928-113">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18928-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18928-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18928-115">Valor de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="18928-115">Scaling value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18928-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="18928-116">Return value</span></span>

<span data-ttu-id="18928-117">Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="18928-117">Type: **[**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="18928-118">Ponteiro para a estrutura [**D3DXVECTOR4**](d3dxvector4.md) que é o vetor dimensionado.</span><span class="sxs-lookup"><span data-stu-id="18928-118">Pointer to the [**D3DXVECTOR4**](d3dxvector4.md) structure that is the scaled vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="18928-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="18928-119">Remarks</span></span>

<span data-ttu-id="18928-120">O valor de retorno para essa função é o mesmo valor retornado no parâmetro *pout* .</span><span class="sxs-lookup"><span data-stu-id="18928-120">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="18928-121">Dessa forma, a função **D3DXVec4Scale** pode ser usada como um parâmetro para outra função.</span><span class="sxs-lookup"><span data-stu-id="18928-121">In this way, the **D3DXVec4Scale** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="18928-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18928-122">Requirements</span></span>



| <span data-ttu-id="18928-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="18928-123">Requirement</span></span> | <span data-ttu-id="18928-124">Valor</span><span class="sxs-lookup"><span data-stu-id="18928-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18928-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="18928-125">Header</span></span><br/>  | <dl> <span data-ttu-id="18928-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="18928-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="18928-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="18928-127">Library</span></span><br/> | <dl> <span data-ttu-id="18928-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18928-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="18928-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="18928-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18928-130">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="18928-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="18928-131">**D3DXVec4Add**</span><span class="sxs-lookup"><span data-stu-id="18928-131">**D3DXVec4Add**</span></span>](d3dxvec4add.md)
</dt> <dt>

[<span data-ttu-id="18928-132">**D3DXVec4Subtract**</span><span class="sxs-lookup"><span data-stu-id="18928-132">**D3DXVec4Subtract**</span></span>](d3dxvec4subtract.md)
</dt> </dl>

 

 
