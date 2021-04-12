---
description: A semântica mapeia um parâmetro para os registros de vértice ou de sombreador de pixel. Eles também podem ser cadeias de caracteres descritivas opcionais anexadas a parâmetros que não são de registro.
ms.assetid: 547a6ff3-be24-4299-9119-6719ad09b4ef
title: Estrutura D3DXSEMANTIC (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSEMANTIC
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 08a30ac4d669beb5b93f2823219cb167d9e8d67f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370943"
---
# <a name="d3dxsemantic-structure"></a><span data-ttu-id="d35bd-104">Estrutura D3DXSEMANTIC</span><span class="sxs-lookup"><span data-stu-id="d35bd-104">D3DXSEMANTIC structure</span></span>

<span data-ttu-id="d35bd-105">A semântica mapeia um parâmetro para os registros de vértice ou de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="d35bd-105">Semantics map a parameter to vertex or pixel shader registers.</span></span> <span data-ttu-id="d35bd-106">Eles também podem ser cadeias de caracteres descritivas opcionais anexadas a parâmetros que não são de registro.</span><span class="sxs-lookup"><span data-stu-id="d35bd-106">They can also be optional descriptive strings attached to non-register parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="d35bd-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d35bd-107">Syntax</span></span>


```C++
typedef struct D3DXSEMANTIC {
  UINT Usage;
  UINT UsageIndex;
} D3DXSEMANTIC, *LPD3DXSEMANTIC;
```



## <a name="members"></a><span data-ttu-id="d35bd-108">Membros</span><span class="sxs-lookup"><span data-stu-id="d35bd-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d35bd-109">**Usage**</span><span class="sxs-lookup"><span data-stu-id="d35bd-109">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="d35bd-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d35bd-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d35bd-111">Opções que identificam como os recursos são usados.</span><span class="sxs-lookup"><span data-stu-id="d35bd-111">Options that identify how resources are used.</span></span> <span data-ttu-id="d35bd-112">Consulte [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="d35bd-112">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

</dd> <dt>

<span data-ttu-id="d35bd-113">**UsageIndex**</span><span class="sxs-lookup"><span data-stu-id="d35bd-113">**UsageIndex**</span></span>
</dt> <dd>

<span data-ttu-id="d35bd-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d35bd-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d35bd-115">Opções que modificam como o uso é interpretado.</span><span class="sxs-lookup"><span data-stu-id="d35bd-115">Options that modify how the usage is interpreted.</span></span> <span data-ttu-id="d35bd-116">O índice de uso e uso compõem uma declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="d35bd-116">The usage and usage index make up a vertex declaration.</span></span> <span data-ttu-id="d35bd-117">Consulte [declaração de vértice (Direct3D 9)](vertex-declaration.md).</span><span class="sxs-lookup"><span data-stu-id="d35bd-117">See [Vertex Declaration (Direct3D 9)](vertex-declaration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d35bd-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="d35bd-118">Remarks</span></span>

<span data-ttu-id="d35bd-119">A semântica é necessária para os registros de vértice e sombreador de pixel, entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="d35bd-119">Semantics are required for vertex and pixel shader, input and output registers.</span></span>

## <a name="requirements"></a><span data-ttu-id="d35bd-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d35bd-120">Requirements</span></span>



| <span data-ttu-id="d35bd-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d35bd-121">Requirement</span></span> | <span data-ttu-id="d35bd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d35bd-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d35bd-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d35bd-123">Header</span></span><br/> | <dl> <span data-ttu-id="d35bd-124"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="d35bd-124"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d35bd-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="d35bd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d35bd-126">Estruturas de efeito</span><span class="sxs-lookup"><span data-stu-id="d35bd-126">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
