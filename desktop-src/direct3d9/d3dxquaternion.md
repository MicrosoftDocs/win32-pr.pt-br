---
description: Estrutura D3DXQUATERNION (D3dx9math. h) – descreve um Quaternion.
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
ms.openlocfilehash: f67acc6389ce809c1aa5f4987d9502735fe61e49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115674"
---
# <a name="d3dxquaternion-structure-d3dx9mathh"></a><span data-ttu-id="7e62a-103">Estrutura D3DXQUATERNION (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="7e62a-103">D3DXQUATERNION structure (D3dx9math.h)</span></span>

<span data-ttu-id="7e62a-104">Descreve um Quaternion.</span><span class="sxs-lookup"><span data-stu-id="7e62a-104">Describes a quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e62a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7e62a-105">Syntax</span></span>


```C++
typedef struct D3DXQUATERNION {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXQUATERNION, *LPD3DXQUATERNION;
```



## <a name="members"></a><span data-ttu-id="7e62a-106">Membros</span><span class="sxs-lookup"><span data-stu-id="7e62a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7e62a-107">**x**</span><span class="sxs-lookup"><span data-stu-id="7e62a-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="7e62a-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7e62a-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7e62a-109">O componente x.</span><span class="sxs-lookup"><span data-stu-id="7e62a-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="7e62a-110">**y**</span><span class="sxs-lookup"><span data-stu-id="7e62a-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="7e62a-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7e62a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7e62a-112">O componente y.</span><span class="sxs-lookup"><span data-stu-id="7e62a-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="7e62a-113">**z**</span><span class="sxs-lookup"><span data-stu-id="7e62a-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="7e62a-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7e62a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7e62a-115">O componente z.</span><span class="sxs-lookup"><span data-stu-id="7e62a-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="7e62a-116">**w**</span><span class="sxs-lookup"><span data-stu-id="7e62a-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="7e62a-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7e62a-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="7e62a-118">O componente w-.</span><span class="sxs-lookup"><span data-stu-id="7e62a-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e62a-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e62a-119">Remarks</span></span>

<span data-ttu-id="7e62a-120">Os quaternions adicionam um quarto elemento aos \[ valores x, y, z \] que definem um vetor, resultando em vetores de 4D arbitrários.</span><span class="sxs-lookup"><span data-stu-id="7e62a-120">Quaternions add a fourth element to the \[ x, y, z\] values that define a vector, resulting in arbitrary 4D vectors.</span></span> <span data-ttu-id="7e62a-121">No entanto, o seguinte ilustra como cada elemento de uma unidade Quaternion está relacionado a uma rotação de ângulo angular (em que q representa uma unidade Quaternion (x, y, z, w), o eixo é normalizado e teta é a rotação do CCW desejada sobre o eixo):</span><span class="sxs-lookup"><span data-stu-id="7e62a-121">However, the following illustrates how each element of a unit quaternion relates to an axis-angle rotation (where q represents a unit quaternion (x, y, z, w), axis is normalized, and theta is the desired CCW rotation about the axis):</span></span>


```
q.x = sin(theta/2) * axis.x
q.y = sin(theta/2) * axis.y
q.z = sin(theta/2) * axis.z
q.w = cos(theta/2)
```



<span data-ttu-id="7e62a-122">Os programadores de C++ podem aproveitar a sobrecarga de operador e a conversão de tipos com as [**extensões D3DXQUATERNION**](d3dxquaternion-extensions.md), que implementam construtores sobrecarregados e operadores de atribuição, unários e binários (incluindo igualdade).</span><span class="sxs-lookup"><span data-stu-id="7e62a-122">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXQUATERNION Extensions**](d3dxquaternion-extensions.md), which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e62a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e62a-123">Requirements</span></span>



| <span data-ttu-id="7e62a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e62a-124">Requirement</span></span> | <span data-ttu-id="7e62a-125">Valor</span><span class="sxs-lookup"><span data-stu-id="7e62a-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e62a-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7e62a-126">Header</span></span><br/> | <dl> <span data-ttu-id="7e62a-127"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e62a-127"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e62a-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7e62a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e62a-129">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="7e62a-129">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="7e62a-130">Vetores, vértices e quaternions (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7e62a-130">Vectors, Vertices, and Quaternions (Direct3D 9)</span></span>](vectors--vertices--and-quaternions.md)
</dt> </dl>

 

 
