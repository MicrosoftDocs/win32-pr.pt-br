---
description: Descreve um Quaternion.
ms.assetid: 3d88ed17-5b0a-46d5-8fe6-d66e1fa26c13
title: Estrutura D3DXQUATERNION (D3dx9math. h)
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
- d3dx9math.h
ms.openlocfilehash: 59d3f147e8eb233b9197394bad738d19d9ceba5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105798414"
---
# <a name="d3dxquaternion-structure-d3dx9mathh"></a><span data-ttu-id="7c5ac-103">Estrutura D3DXQUATERNION (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="7c5ac-103">D3DXQUATERNION structure (D3dx9math.h)</span></span>

<span data-ttu-id="7c5ac-104">Descreve um Quaternion.</span><span class="sxs-lookup"><span data-stu-id="7c5ac-104">Describes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c5ac-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7c5ac-105">Syntax</span></span>


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a><span data-ttu-id="7c5ac-106">Membros</span><span class="sxs-lookup"><span data-stu-id="7c5ac-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7c5ac-107">**x**</span><span class="sxs-lookup"><span data-stu-id="7c5ac-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="7c5ac-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c5ac-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7c5ac-109">O componente x.</span><span class="sxs-lookup"><span data-stu-id="7c5ac-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="7c5ac-110">**y**</span><span class="sxs-lookup"><span data-stu-id="7c5ac-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="7c5ac-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c5ac-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7c5ac-112">O componente y.</span><span class="sxs-lookup"><span data-stu-id="7c5ac-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="7c5ac-113">**z**</span><span class="sxs-lookup"><span data-stu-id="7c5ac-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="7c5ac-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c5ac-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7c5ac-115">O componente z.</span><span class="sxs-lookup"><span data-stu-id="7c5ac-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="7c5ac-116">**w**</span><span class="sxs-lookup"><span data-stu-id="7c5ac-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="7c5ac-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c5ac-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7c5ac-118">O componente w-.</span><span class="sxs-lookup"><span data-stu-id="7c5ac-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7c5ac-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c5ac-119">Remarks</span></span>

<span data-ttu-id="7c5ac-120">Os quaternions adicionam um quarto elemento aos \[ valores x, y, z \] que definem um vetor, resultando em vetores de 4D arbitrários.</span><span class="sxs-lookup"><span data-stu-id="7c5ac-120">Quaternions add a fourth element to the \[ x, y, z\] values that define a vector, resulting in arbitrary 4D vectors.</span></span> <span data-ttu-id="7c5ac-121">No entanto, o seguinte ilustra como cada elemento de uma unidade Quaternion está relacionado a uma rotação de ângulo angular (em que q representa uma unidade Quaternion (x, y, z, w), o eixo é normalizado e teta é a rotação do CCW desejada sobre o eixo):</span><span class="sxs-lookup"><span data-stu-id="7c5ac-121">However, the following illustrates how each element of a unit quaternion relates to an axis-angle rotation (where q represents a unit quaternion (x, y, z, w), axis is normalized, and theta is the desired CCW rotation about the axis):</span></span>


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



<span data-ttu-id="7c5ac-122">Os programadores de C++ podem aproveitar a sobrecarga de operador e a conversão de tipos com as [**extensões D3DXQUATERNION**](d3dxquaternion-extensions.md), que implementam construtores sobrecarregados e operadores de atribuição, unários e binários (incluindo igualdade).</span><span class="sxs-lookup"><span data-stu-id="7c5ac-122">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXQUATERNION Extensions**](d3dxquaternion-extensions.md), which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c5ac-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c5ac-123">Requirements</span></span>



| <span data-ttu-id="7c5ac-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c5ac-124">Requirement</span></span> | <span data-ttu-id="7c5ac-125">Valor</span><span class="sxs-lookup"><span data-stu-id="7c5ac-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c5ac-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7c5ac-126">Header</span></span><br/> | <dl> <span data-ttu-id="7c5ac-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c5ac-127"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c5ac-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c5ac-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c5ac-129">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="7c5ac-129">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="7c5ac-130">Vetores, vértices e quaternions (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7c5ac-130">Vectors, Vertices, and Quaternions (Direct3D 9)</span></span>](vectors--vertices--and-quaternions.md)
</dt> </dl>

 

 
