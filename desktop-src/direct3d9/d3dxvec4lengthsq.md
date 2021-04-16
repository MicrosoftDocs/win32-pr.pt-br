---
description: Retorna o quadrado do comprimento de um vetor 4D.
ms.assetid: 73091179-4acb-408b-8c91-766052999f26
title: Função D3DXVec4LengthSq (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4LengthSq
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6348d4c42039c5aff47998721119c16317e22791
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105768348"
---
# <a name="d3dxvec4lengthsq-function"></a><span data-ttu-id="6fa43-103">Função D3DXVec4LengthSq</span><span class="sxs-lookup"><span data-stu-id="6fa43-103">D3DXVec4LengthSq function</span></span>

<span data-ttu-id="6fa43-104">Retorna o quadrado do comprimento de um vetor 4D.</span><span class="sxs-lookup"><span data-stu-id="6fa43-104">Returns the square of the length of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fa43-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fa43-105">Syntax</span></span>


```C++
FLOAT D3DXVec4LengthSq(
  _In_ const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="6fa43-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fa43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fa43-107">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6fa43-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6fa43-108">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="6fa43-108">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="6fa43-109">Ponteiro para a estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="6fa43-109">Pointer to the source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fa43-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6fa43-110">Return value</span></span>

<span data-ttu-id="6fa43-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6fa43-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6fa43-112">O comprimento quadrado do vetor.</span><span class="sxs-lookup"><span data-stu-id="6fa43-112">The vector's squared length.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fa43-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fa43-113">Requirements</span></span>



| <span data-ttu-id="6fa43-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fa43-114">Requirement</span></span> | <span data-ttu-id="6fa43-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6fa43-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fa43-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6fa43-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6fa43-117"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fa43-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="6fa43-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6fa43-118">Library</span></span><br/> | <dl> <span data-ttu-id="6fa43-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6fa43-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6fa43-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6fa43-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fa43-121">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="6fa43-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="6fa43-122">**D3DXVec4Length**</span><span class="sxs-lookup"><span data-stu-id="6fa43-122">**D3DXVec4Length**</span></span>](d3dxvec4length.md)
</dt> </dl>

 

 
