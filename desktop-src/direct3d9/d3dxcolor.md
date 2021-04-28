---
description: Estrutura D3DXCOLOR (D3dx9math. h) – descreve os valores de cor.
ms.assetid: 53d3176a-f727-498e-8bea-0e30e0a1c66e
title: Estrutura D3DXCOLOR (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOLOR
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 58b02abc49b695169674a2579b73dc2359801a73
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115924"
---
# <a name="d3dxcolor-structure-d3dx9mathh"></a><span data-ttu-id="fc1e8-103">Estrutura D3DXCOLOR (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="fc1e8-103">D3DXCOLOR structure (D3dx9math.h)</span></span>

<span data-ttu-id="fc1e8-104">Descreve os valores de cor.</span><span class="sxs-lookup"><span data-stu-id="fc1e8-104">Describes color values.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc1e8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc1e8-105">Syntax</span></span>


```C++
typedef struct D3DXCOLOR {
  FLOAT r;
  FLOAT g;
  FLOAT b;
  FLOAT a;
} D3DXCOLOR, *LPD3DXCOLOR;
```



## <a name="members"></a><span data-ttu-id="fc1e8-106">Membros</span><span class="sxs-lookup"><span data-stu-id="fc1e8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fc1e8-107">**r**</span><span class="sxs-lookup"><span data-stu-id="fc1e8-107">**r**</span></span>
</dt> <dd>

<span data-ttu-id="fc1e8-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc1e8-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fc1e8-109">Componente vermelho da cor.</span><span class="sxs-lookup"><span data-stu-id="fc1e8-109">Red component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="fc1e8-110">**m**</span><span class="sxs-lookup"><span data-stu-id="fc1e8-110">**g**</span></span>
</dt> <dd>

<span data-ttu-id="fc1e8-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc1e8-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fc1e8-112">Componente verde da cor.</span><span class="sxs-lookup"><span data-stu-id="fc1e8-112">Green component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="fc1e8-113">**b**</span><span class="sxs-lookup"><span data-stu-id="fc1e8-113">**b**</span></span>
</dt> <dd>

<span data-ttu-id="fc1e8-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc1e8-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fc1e8-115">Componente azul da cor.</span><span class="sxs-lookup"><span data-stu-id="fc1e8-115">Blue component of the color.</span></span>

</dd> <dt>

<span data-ttu-id="fc1e8-116">**um**</span><span class="sxs-lookup"><span data-stu-id="fc1e8-116">**a**</span></span>
</dt> <dd>

<span data-ttu-id="fc1e8-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fc1e8-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="fc1e8-118">Componente alfa da cor.</span><span class="sxs-lookup"><span data-stu-id="fc1e8-118">Alpha component of the color.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc1e8-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc1e8-119">Remarks</span></span>

<span data-ttu-id="fc1e8-120">Os programadores de C++ podem aproveitar a sobrecarga de operador e a conversão de tipos com as [**extensões D3DXCOLOR**](d3dxcolor-extensions.md), que implementam construtores sobrecarregados, bem como operadores de atribuição, unários e binários (incluindo igualdade).</span><span class="sxs-lookup"><span data-stu-id="fc1e8-120">C++ programmers can take advantage of operator overloading and type casting with the [**D3DXCOLOR Extensions**](d3dxcolor-extensions.md), which implement overloaded constructors, as well as assignment, unary, and binary (including equality) operators.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc1e8-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc1e8-121">Requirements</span></span>



| <span data-ttu-id="fc1e8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc1e8-122">Requirement</span></span> | <span data-ttu-id="fc1e8-123">Valor</span><span class="sxs-lookup"><span data-stu-id="fc1e8-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc1e8-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fc1e8-124">Header</span></span><br/> | <dl> <span data-ttu-id="fc1e8-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc1e8-125"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc1e8-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fc1e8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc1e8-127">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="fc1e8-127">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
