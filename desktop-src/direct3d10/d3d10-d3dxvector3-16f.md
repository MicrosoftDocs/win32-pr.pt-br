---
description: O mesmo que um D3DXVECTOR3, mas usa valores de ponto flutuante de 16 bits para x, y e z.
ms.assetid: b21676f1-5cff-4eef-bd60-5c09882283dc
title: Estrutura de D3DXVECTOR3_16F (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR3_16F
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: b7143e864eddf37842e19d7554150beaf50c0b53
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930566"
---
# <a name="d3dxvector3_16f-structure"></a><span data-ttu-id="dc936-103">\_Estrutura D3DXVECTOR3 16F</span><span class="sxs-lookup"><span data-stu-id="dc936-103">D3DXVECTOR3\_16F structure</span></span>

<span data-ttu-id="dc936-104">O mesmo que um [**D3DXVECTOR3**](d3d10-d3dxvector3.md), mas usa valores de ponto flutuante de 16 bits para x, y e z.</span><span class="sxs-lookup"><span data-stu-id="dc936-104">Same as a [**D3DXVECTOR3**](d3d10-d3dxvector3.md), but it uses 16-bit floating point values for x, y, and z.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc936-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dc936-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR3_16F {
  FLOAT x;
  FLOAT y;
  FLOAT z;
} D3DXVECTOR3_16F, *LPD3DXVECTOR3_16F;
```



## <a name="members"></a><span data-ttu-id="dc936-106">Membros</span><span class="sxs-lookup"><span data-stu-id="dc936-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="dc936-107">**x**</span><span class="sxs-lookup"><span data-stu-id="dc936-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="dc936-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc936-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dc936-109">O componente x.</span><span class="sxs-lookup"><span data-stu-id="dc936-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="dc936-110">**y**</span><span class="sxs-lookup"><span data-stu-id="dc936-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="dc936-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc936-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dc936-112">O componente y.</span><span class="sxs-lookup"><span data-stu-id="dc936-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="dc936-113">**z**</span><span class="sxs-lookup"><span data-stu-id="dc936-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="dc936-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc936-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="dc936-115">O componente z.</span><span class="sxs-lookup"><span data-stu-id="dc936-115">The z-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc936-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="dc936-116">Remarks</span></span>

<span data-ttu-id="dc936-117">**D3DXVECTOR3 \_ 16F** tem as seguintes extensões de C++.</span><span class="sxs-lookup"><span data-stu-id="dc936-117">**D3DXVECTOR3\_16F** has the following C++ extensions.</span></span>

### <a name="d3dxvector3_16f-extensions"></a><span data-ttu-id="dc936-118">\_Extensões D3DXVECTOR3 16F</span><span class="sxs-lookup"><span data-stu-id="dc936-118">D3DXVECTOR3\_16F Extensions</span></span>


```

typedef struct D3DXVECTOR3_16F
{
#ifdef __cplusplus
public:
    D3DXVECTOR3_16F() {};
    D3DXVECTOR3_16F( CONST FLOAT * );
    D3DXVECTOR3_16F( CONST D3DVECTOR& );
    D3DXVECTOR3_16F( CONST D3DXFLOAT16 * );
    D3DXVECTOR3_16F( CONST D3DXFLOAT16 &x, CONST D3DXFLOAT16 &y, CONST D3DXFLOAT16 &z );

    // casting
    operator D3DXFLOAT16* ();
    operator CONST D3DXFLOAT16* () const;

    // binary operators
    BOOL operator == ( CONST D3DXVECTOR3_16F& ) const;
    BOOL operator != ( CONST D3DXVECTOR3_16F& ) const;

public:
#endif //__cplusplus
    D3DXFLOAT16 x, y, z;

} D3DXVECTOR3_16F, *LPD3DXVECTOR3_16F;
```



## <a name="requirements"></a><span data-ttu-id="dc936-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc936-119">Requirements</span></span>



| <span data-ttu-id="dc936-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc936-120">Requirement</span></span> | <span data-ttu-id="dc936-121">Valor</span><span class="sxs-lookup"><span data-stu-id="dc936-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc936-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dc936-122">Header</span></span><br/> | <dl> <span data-ttu-id="dc936-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc936-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc936-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="dc936-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc936-125">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="dc936-125">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
