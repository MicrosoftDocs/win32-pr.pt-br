---
description: Retorna o componente z assumindo o produto cruzado de dois vetores 2D.
ms.assetid: daec19f2-cd0f-4a68-affc-9a42bda8912c
title: Função D3DXVec2CCW (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2CCW
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 71c6e14171a9e7d12d86c30f05885cecf50ce973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105784685"
---
# <a name="d3dxvec2ccw-function"></a><span data-ttu-id="472c1-103">Função D3DXVec2CCW</span><span class="sxs-lookup"><span data-stu-id="472c1-103">D3DXVec2CCW function</span></span>

<span data-ttu-id="472c1-104">Retorna o componente z assumindo o produto cruzado de dois vetores 2D.</span><span class="sxs-lookup"><span data-stu-id="472c1-104">Returns the z-component by taking the cross product of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="472c1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="472c1-105">Syntax</span></span>


```C++
FLOAT D3DXVec2CCW(
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="472c1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="472c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="472c1-107">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="472c1-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="472c1-108">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="472c1-108">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="472c1-109">Ponteiro para uma estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="472c1-109">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="472c1-110">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="472c1-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="472c1-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="472c1-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="472c1-112">Ponteiro para uma estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="472c1-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="472c1-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="472c1-113">Return value</span></span>

<span data-ttu-id="472c1-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="472c1-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="472c1-115">O componente z.</span><span class="sxs-lookup"><span data-stu-id="472c1-115">The z-component.</span></span>

## <a name="remarks"></a><span data-ttu-id="472c1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="472c1-116">Remarks</span></span>

<span data-ttu-id="472c1-117">Essa função determina o componente z determinando o produto cruzado com base na seguinte fórmula: ((x1, y1, 0) Cross (x2, Y2, 0)).</span><span class="sxs-lookup"><span data-stu-id="472c1-117">This function determines the z-component by determining the cross-product based on the following formula: ((x1,y1,0) cross (x2,y2,0)).</span></span> <span data-ttu-id="472c1-118">Ou conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="472c1-118">Or as shown in the following example.</span></span>


```
pV1->x * pV2->y - pV1->y * pV2->x
```



<span data-ttu-id="472c1-119">Se o valor do componente z for positivo, o vetor v2 será no sentido anti-horário do vetor v1.</span><span class="sxs-lookup"><span data-stu-id="472c1-119">If the value of the z-component is positive, the vector V2 is counterclockwise from the vector V1.</span></span> <span data-ttu-id="472c1-120">Essas informações são úteis para a remoção de face para frente.</span><span class="sxs-lookup"><span data-stu-id="472c1-120">This information is useful for back-face culling.</span></span>

## <a name="requirements"></a><span data-ttu-id="472c1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="472c1-121">Requirements</span></span>



| <span data-ttu-id="472c1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="472c1-122">Requirement</span></span> | <span data-ttu-id="472c1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="472c1-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="472c1-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="472c1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="472c1-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="472c1-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="472c1-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="472c1-126">Library</span></span><br/> | <dl> <span data-ttu-id="472c1-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="472c1-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="472c1-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="472c1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="472c1-129">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="472c1-129">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="472c1-130">**D3DXVec2Dot**</span><span class="sxs-lookup"><span data-stu-id="472c1-130">**D3DXVec2Dot**</span></span>](d3dxvec2dot.md)
</dt> </dl>

 

 
