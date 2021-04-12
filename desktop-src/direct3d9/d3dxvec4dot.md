---
description: Determina o produto de ponto de dois vetores de 4D.
ms.assetid: 565dede8-6cc8-4313-9480-2f252cac94f2
title: Função D3DXVec4Dot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Dot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a0ef075a768fe9b70a38a4bc3d88b094359bd546
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370965"
---
# <a name="d3dxvec4dot-function"></a><span data-ttu-id="5e87b-103">Função D3DXVec4Dot</span><span class="sxs-lookup"><span data-stu-id="5e87b-103">D3DXVec4Dot function</span></span>

<span data-ttu-id="5e87b-104">Determina o produto de ponto de dois vetores de 4D.</span><span class="sxs-lookup"><span data-stu-id="5e87b-104">Determines the dot product of two 4D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e87b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5e87b-105">Syntax</span></span>


```C++
FLOAT D3DXVec4Dot(
  _In_ const D3DXVECTOR4 *pV1,
  _In_ const D3DXVECTOR4 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="5e87b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e87b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e87b-107">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e87b-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e87b-108">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="5e87b-108">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="5e87b-109">Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="5e87b-109">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5e87b-110">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5e87b-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e87b-111">Tipo: **const [**D3DXVECTOR4**](d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="5e87b-111">Type: **const [**D3DXVECTOR4**](d3dxvector4.md)\***</span></span>

<span data-ttu-id="5e87b-112">Ponteiro para uma estrutura de [**D3DXVECTOR4**](d3dxvector4.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="5e87b-112">Pointer to a source [**D3DXVECTOR4**](d3dxvector4.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e87b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e87b-113">Return value</span></span>

<span data-ttu-id="5e87b-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5e87b-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5e87b-115">O produto escalar.</span><span class="sxs-lookup"><span data-stu-id="5e87b-115">The dot product.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e87b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e87b-116">Requirements</span></span>



| <span data-ttu-id="5e87b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e87b-117">Requirement</span></span> | <span data-ttu-id="5e87b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="5e87b-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e87b-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e87b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="5e87b-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e87b-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="5e87b-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5e87b-121">Library</span></span><br/> | <dl> <span data-ttu-id="5e87b-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e87b-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5e87b-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e87b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e87b-124">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="5e87b-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="5e87b-125">**D3DXVec4Cross**</span><span class="sxs-lookup"><span data-stu-id="5e87b-125">**D3DXVec4Cross**</span></span>](d3dxvec4cross.md)
</dt> </dl>

 

 
