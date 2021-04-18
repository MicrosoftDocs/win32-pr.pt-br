---
description: Retorna o quadrado do comprimento de um vetor 3D.
ms.assetid: 25dc50cc-542b-4989-a858-9b37603393a0
title: Função D3DXVec3LengthSq (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3LengthSq
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7bb7d17d4f1bc06d68a73a2cff9288d159381387
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761229"
---
# <a name="d3dxvec3lengthsq-function"></a><span data-ttu-id="443c2-103">Função D3DXVec3LengthSq</span><span class="sxs-lookup"><span data-stu-id="443c2-103">D3DXVec3LengthSq function</span></span>

<span data-ttu-id="443c2-104">Retorna o quadrado do comprimento de um vetor 3D.</span><span class="sxs-lookup"><span data-stu-id="443c2-104">Returns the square of the length of a 3D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="443c2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="443c2-105">Syntax</span></span>


```C++
FLOAT D3DXVec3LengthSq(
  _In_ const D3DXVECTOR3 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="443c2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="443c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="443c2-107">*VP* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="443c2-107">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="443c2-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="443c2-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="443c2-109">Ponteiro para a estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="443c2-109">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="443c2-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="443c2-110">Return value</span></span>

<span data-ttu-id="443c2-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="443c2-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="443c2-112">O comprimento quadrado do vetor.</span><span class="sxs-lookup"><span data-stu-id="443c2-112">The vector's squared length.</span></span>

## <a name="requirements"></a><span data-ttu-id="443c2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="443c2-113">Requirements</span></span>



| <span data-ttu-id="443c2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="443c2-114">Requirement</span></span> | <span data-ttu-id="443c2-115">Valor</span><span class="sxs-lookup"><span data-stu-id="443c2-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="443c2-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="443c2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="443c2-117"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="443c2-117"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="443c2-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="443c2-118">Library</span></span><br/> | <dl> <span data-ttu-id="443c2-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="443c2-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="443c2-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="443c2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="443c2-121">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="443c2-121">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="443c2-122">**D3DXVec3Length**</span><span class="sxs-lookup"><span data-stu-id="443c2-122">**D3DXVec3Length**</span></span>](d3dxvec3length.md)
</dt> </dl>

 

 
