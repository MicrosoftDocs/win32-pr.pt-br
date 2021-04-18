---
description: Determina o produto de ponto de dois vetores 2D.
ms.assetid: ae77ff29-44be-4b67-9c63-aaffa4fe8d59
title: Função D3DXVec2Dot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Dot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 79b65127c415695b3df9f927b6edff8fcdd5c58d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764539"
---
# <a name="d3dxvec2dot-function"></a><span data-ttu-id="28747-103">Função D3DXVec2Dot</span><span class="sxs-lookup"><span data-stu-id="28747-103">D3DXVec2Dot function</span></span>

<span data-ttu-id="28747-104">Determina o produto de ponto de dois vetores 2D.</span><span class="sxs-lookup"><span data-stu-id="28747-104">Determines the dot product of two 2D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="28747-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28747-105">Syntax</span></span>


```C++
FLOAT D3DXVec2Dot(
  _In_ const D3DXVECTOR2 *pV1,
  _In_ const D3DXVECTOR2 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="28747-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28747-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28747-107">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="28747-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28747-108">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="28747-108">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="28747-109">Ponteiro para uma estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="28747-109">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="28747-110">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="28747-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28747-111">Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="28747-111">Type: **const [**D3DXVECTOR2**](d3dxvector2.md)\***</span></span>

<span data-ttu-id="28747-112">Ponteiro para uma estrutura de [**D3DXVECTOR2**](d3dxvector2.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="28747-112">Pointer to a source [**D3DXVECTOR2**](d3dxvector2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28747-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="28747-113">Return value</span></span>

<span data-ttu-id="28747-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28747-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="28747-115">O produto escalar.</span><span class="sxs-lookup"><span data-stu-id="28747-115">The dot product.</span></span>

## <a name="requirements"></a><span data-ttu-id="28747-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28747-116">Requirements</span></span>



| <span data-ttu-id="28747-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="28747-117">Requirement</span></span> | <span data-ttu-id="28747-118">Valor</span><span class="sxs-lookup"><span data-stu-id="28747-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28747-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="28747-119">Header</span></span><br/>  | <dl> <span data-ttu-id="28747-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="28747-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="28747-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="28747-121">Library</span></span><br/> | <dl> <span data-ttu-id="28747-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="28747-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="28747-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="28747-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28747-124">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="28747-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="28747-125">**D3DXVec2CCW**</span><span class="sxs-lookup"><span data-stu-id="28747-125">**D3DXVec2CCW**</span></span>](d3dxvec2ccw.md)
</dt> </dl>

 

 
