---
description: Descreve um Quaternion.
ms.assetid: e6cb45b2-3132-4315-b02d-a3dfc444f8cc
title: Estrutura D3DXQUATERNION (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQUATERNION
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 405e48c99d7298708af193016930a8defdf9d600
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298715"
---
# <a name="d3dxquaternion-structure-d3dx10mathh"></a><span data-ttu-id="87834-103">Estrutura D3DXQUATERNION (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="87834-103">D3DXQUATERNION structure (D3DX10Math.h)</span></span>

<span data-ttu-id="87834-104">Descreve um Quaternion.</span><span class="sxs-lookup"><span data-stu-id="87834-104">Describes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="87834-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87834-105">Syntax</span></span>


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a><span data-ttu-id="87834-106">Membros</span><span class="sxs-lookup"><span data-stu-id="87834-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="87834-107">**x**</span><span class="sxs-lookup"><span data-stu-id="87834-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="87834-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87834-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87834-109">O componente x.</span><span class="sxs-lookup"><span data-stu-id="87834-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="87834-110">**y**</span><span class="sxs-lookup"><span data-stu-id="87834-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="87834-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87834-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87834-112">O componente y.</span><span class="sxs-lookup"><span data-stu-id="87834-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="87834-113">**z**</span><span class="sxs-lookup"><span data-stu-id="87834-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="87834-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87834-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87834-115">O componente z.</span><span class="sxs-lookup"><span data-stu-id="87834-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="87834-116">**w**</span><span class="sxs-lookup"><span data-stu-id="87834-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="87834-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87834-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="87834-118">O componente w-.</span><span class="sxs-lookup"><span data-stu-id="87834-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87834-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="87834-119">Remarks</span></span>

<span data-ttu-id="87834-120">Os quaternions adicionam um quarto elemento aos \[ valores x, y, z \] que definem um vetor, resultando em vetores de 4D arbitrários.</span><span class="sxs-lookup"><span data-stu-id="87834-120">Quaternions add a fourth element to the \[ x, y, z\] values that define a vector, resulting in arbitrary 4D vectors.</span></span> <span data-ttu-id="87834-121">No entanto, o seguinte ilustra como cada elemento de uma unidade Quaternion está relacionado a uma rotação de ângulo angular (em que q representa uma unidade Quaternion (x, y, z, w), o eixo é normalizado e teta é a rotação do CCW desejada sobre o eixo):</span><span class="sxs-lookup"><span data-stu-id="87834-121">However, the following illustrates how each element of a unit quaternion relates to an axis-angle rotation (where q represents a unit quaternion (x, y, z, w), axis is normalized, and theta is the desired CCW rotation about the axis):</span></span>


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



## <a name="requirements"></a><span data-ttu-id="87834-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87834-122">Requirements</span></span>



| <span data-ttu-id="87834-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="87834-123">Requirement</span></span> | <span data-ttu-id="87834-124">Valor</span><span class="sxs-lookup"><span data-stu-id="87834-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87834-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="87834-125">Header</span></span><br/> | <dl> <span data-ttu-id="87834-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="87834-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87834-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="87834-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87834-128">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="87834-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
