---
description: Determina o produto de ponto de dois vetores 3D.
ms.assetid: 61aa7751-cc06-4673-929b-d7c1e691e395
title: Função D3DXVec3Dot (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3Dot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 22d6930a44f129154482f9b1aab24337e8bcdc83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813994"
---
# <a name="d3dxvec3dot-function"></a><span data-ttu-id="948e6-103">Função D3DXVec3Dot</span><span class="sxs-lookup"><span data-stu-id="948e6-103">D3DXVec3Dot function</span></span>

<span data-ttu-id="948e6-104">Determina o produto de ponto de dois vetores 3D.</span><span class="sxs-lookup"><span data-stu-id="948e6-104">Determines the dot product of two 3D vectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="948e6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="948e6-105">Syntax</span></span>


```C++
FLOAT D3DXVec3Dot(
  _In_ const D3DXVECTOR3 *pV1,
  _In_ const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a><span data-ttu-id="948e6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="948e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="948e6-107">*pV1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="948e6-107">*pV1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="948e6-108">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="948e6-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="948e6-109">Ponteiro para uma estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="948e6-109">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="948e6-110">*pV2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="948e6-110">*pV2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="948e6-111">Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="948e6-111">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="948e6-112">Ponteiro para uma estrutura de [**D3DXVECTOR3**](d3dxvector3.md) de origem.</span><span class="sxs-lookup"><span data-stu-id="948e6-112">Pointer to a source [**D3DXVECTOR3**](d3dxvector3.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="948e6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="948e6-113">Return value</span></span>

<span data-ttu-id="948e6-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="948e6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="948e6-115">O ponto-produto.</span><span class="sxs-lookup"><span data-stu-id="948e6-115">The dot-product.</span></span>

## <a name="requirements"></a><span data-ttu-id="948e6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="948e6-116">Requirements</span></span>



| <span data-ttu-id="948e6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="948e6-117">Requirement</span></span> | <span data-ttu-id="948e6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="948e6-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="948e6-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="948e6-119">Header</span></span><br/>  | <dl> <span data-ttu-id="948e6-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="948e6-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="948e6-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="948e6-121">Library</span></span><br/> | <dl> <span data-ttu-id="948e6-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="948e6-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="948e6-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="948e6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="948e6-124">Funções matemáticas</span><span class="sxs-lookup"><span data-stu-id="948e6-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="948e6-125">**D3DXVec3Cross**</span><span class="sxs-lookup"><span data-stu-id="948e6-125">**D3DXVec3Cross**</span></span>](d3dxvec3cross.md)
</dt> </dl>

 

 
