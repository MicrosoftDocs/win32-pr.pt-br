---
description: Estrutura D3DXFLOAT16 (D3dx9math. h) – descreve um vetor de ponto flutuante de 16 bits.
ms.assetid: f823a327-f07a-44e9-b58a-7865e11e80eb
title: Estrutura D3DXFLOAT16 (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFLOAT16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: dc878575de4338a2a399f329362d79ff2e7654f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094264"
---
# <a name="d3dxfloat16-structure-d3dx9mathh"></a><span data-ttu-id="cbe24-103">Estrutura D3DXFLOAT16 (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="cbe24-103">D3DXFLOAT16 structure (D3dx9math.h)</span></span>

<span data-ttu-id="cbe24-104">Descreve um vetor de ponto flutuante de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="cbe24-104">Describes a 16-bit floating point vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbe24-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cbe24-105">Syntax</span></span>


```C++
typedef struct D3DXFLOAT16 {
  WORD Value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```



## <a name="members"></a><span data-ttu-id="cbe24-106">Membros</span><span class="sxs-lookup"><span data-stu-id="cbe24-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cbe24-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cbe24-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="cbe24-108">Tipo: **[ **Word**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="cbe24-108">Type: **[**WORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cbe24-109">Os dados de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="cbe24-109">The 16-bit data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cbe24-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbe24-110">Remarks</span></span>

<span data-ttu-id="cbe24-111">Os programadores de C++ podem aproveitar a sobrecarga de operador e a conversão de tipos com as [**extensões D3DXFLOAT16**](d3dxfloat16-extensions.md), que implementam construtores sobrecarregados e operadores de atribuição, unários e binários (incluindo igualdade).</span><span class="sxs-lookup"><span data-stu-id="cbe24-111">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXFLOAT16 Extensions**](d3dxfloat16-extensions.md), which implement overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbe24-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbe24-112">Requirements</span></span>



| <span data-ttu-id="cbe24-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbe24-113">Requirement</span></span> | <span data-ttu-id="cbe24-114">Valor</span><span class="sxs-lookup"><span data-stu-id="cbe24-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cbe24-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cbe24-115">Header</span></span><br/> | <dl> <span data-ttu-id="cbe24-116"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbe24-116"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbe24-117">Consulte também</span><span class="sxs-lookup"><span data-stu-id="cbe24-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbe24-118">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="cbe24-118">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
