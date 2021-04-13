---
description: O mesmo que um D3DXVECTOR4, mas usa valores de ponto flutuante de 16 bits para x, y e z.
ms.assetid: 2db5fb3e-ffe0-4bcf-8894-a8bc7eefaf82
title: Estrutura de D3DXVECTOR4_16F (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR4_16F
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: d3d46e6bc5423260e550fd026ca52420b1c392ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298539"
---
# <a name="d3dxvector4_16f-structure"></a><span data-ttu-id="96325-103">\_Estrutura D3DXVECTOR4 16F</span><span class="sxs-lookup"><span data-stu-id="96325-103">D3DXVECTOR4\_16F structure</span></span>

<span data-ttu-id="96325-104">O mesmo que um [**D3DXVECTOR4**](d3d10-d3dxvector4.md), mas usa valores de ponto flutuante de 16 bits para x, y e z.</span><span class="sxs-lookup"><span data-stu-id="96325-104">Same as a [**D3DXVECTOR4**](d3d10-d3dxvector4.md), but it uses 16-bit floating point values for x, y, and z.</span></span>

## <a name="syntax"></a><span data-ttu-id="96325-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96325-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR4_16F {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXVECTOR4_16F, *LPD3DXVECTOR4_16F;
```



## <a name="members"></a><span data-ttu-id="96325-106">Membros</span><span class="sxs-lookup"><span data-stu-id="96325-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="96325-107">**x**</span><span class="sxs-lookup"><span data-stu-id="96325-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="96325-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="96325-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="96325-109">O componente x.</span><span class="sxs-lookup"><span data-stu-id="96325-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="96325-110">**y**</span><span class="sxs-lookup"><span data-stu-id="96325-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="96325-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="96325-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="96325-112">O componente y.</span><span class="sxs-lookup"><span data-stu-id="96325-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="96325-113">**z**</span><span class="sxs-lookup"><span data-stu-id="96325-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="96325-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="96325-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="96325-115">O componente z.</span><span class="sxs-lookup"><span data-stu-id="96325-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="96325-116">**w**</span><span class="sxs-lookup"><span data-stu-id="96325-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="96325-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="96325-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="96325-118">O componente w-.</span><span class="sxs-lookup"><span data-stu-id="96325-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96325-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="96325-119">Remarks</span></span>

<span data-ttu-id="96325-120">**D3DXVECTOR4 \_ 16F** tem as seguintes extensões de C++.</span><span class="sxs-lookup"><span data-stu-id="96325-120">**D3DXVECTOR4\_16F** has the following C++ extensions.</span></span>

### <a name="d3dxvector4_16f-extensions"></a><span data-ttu-id="96325-121">\_Extensões D3DXVECTOR4 16F</span><span class="sxs-lookup"><span data-stu-id="96325-121">D3DXVECTOR4\_16F Extensions</span></span>


```
typedef struct D3DXVECTOR4_16F
{
#ifdef __cplusplus
public:
    D3DXVECTOR4_16F() {};
    D3DXVECTOR4_16F( CONST FLOAT * );
    D3DXVECTOR4_16F( CONST D3DXFLOAT16 * );
    D3DXVECTOR4_16F( CONST D3DXVECTOR3_16F& xyz, CONST D3DXFLOAT16& w );
    D3DXVECTOR4_16F( CONST D3DXFLOAT16& x, CONST D3DXFLOAT16& y, CONST D3DXFLOAT16& z, CONST D3DXFLOAT16& w );

    // casting
    operator D3DXFLOAT16* ();
    operator CONST D3DXFLOAT16* () const;

    // binary operators
    BOOL operator == ( CONST D3DXVECTOR4_16F& ) const;
    BOOL operator != ( CONST D3DXVECTOR4_16F& ) const;

public:
#endif //__cplusplus
    D3DXFLOAT16 x, y, z, w;

} D3DXVECTOR4_16F, *LPD3DXVECTOR4_16F;
```



## <a name="requirements"></a><span data-ttu-id="96325-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96325-122">Requirements</span></span>



| <span data-ttu-id="96325-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="96325-123">Requirement</span></span> | <span data-ttu-id="96325-124">Valor</span><span class="sxs-lookup"><span data-stu-id="96325-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96325-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="96325-125">Header</span></span><br/> | <dl> <span data-ttu-id="96325-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="96325-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96325-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="96325-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96325-128">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="96325-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
