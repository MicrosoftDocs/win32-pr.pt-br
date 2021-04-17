---
description: Fornece as seguintes sobrecargas de operador e conversões de tipo para estruturas D3DXPLANE.
ms.assetid: 05f80b68-fb2b-4fd7-94e9-e5b40968c4aa
title: Extensões D3DXPLANE (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPLANE
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 3ff8f68283cd81e6647fcdea480ac19b48547cab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812075"
---
# <a name="d3dxplane-extensions"></a><span data-ttu-id="0c8a0-103">Extensões D3DXPLANE</span><span class="sxs-lookup"><span data-stu-id="0c8a0-103">D3DXPLANE Extensions</span></span>

<span data-ttu-id="0c8a0-104">Fornece as seguintes sobrecargas de operador e conversões de tipo para estruturas [**D3DXPLANE**](d3dxplane.md) .</span><span class="sxs-lookup"><span data-stu-id="0c8a0-104">Supplies the following operator overloads and type casts for [**D3DXPLANE**](d3dxplane.md) structures.</span></span>

``` syntax
typedef struct D3DXPLANE
{
#ifdef __cplusplus
public:
    D3DXPLANE() {}
    D3DXPLANE( CONST FLOAT* );
    D3DXPLANE( CONST D3DXFLOAT16* );
    D3DXPLANE( FLOAT a, FLOAT b, FLOAT c, FLOAT d );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXPLANE& operator *= ( FLOAT );
    D3DXPLANE& operator /= ( FLOAT );

    // unary operators
    D3DXPLANE operator + () const;
    D3DXPLANE operator - () const;

    // binary operators
    D3DXPLANE operator * ( FLOAT ) const;
    D3DXPLANE operator / ( FLOAT ) const;

    friend D3DXPLANE operator * ( FLOAT, CONST D3DXPLANE& );

    BOOL operator == ( CONST D3DXPLANE& ) const;
    BOOL operator != ( CONST D3DXPLANE& ) const;

#endif //__cplusplus
    FLOAT a, b, c, d;
} D3DXPLANE, *LPD3DXPLANE;
```

<span data-ttu-id="0c8a0-105">Tipos derivados: \* LPD3DXPLANE</span><span class="sxs-lookup"><span data-stu-id="0c8a0-105">Derived types: \*LPD3DXPLANE</span></span>

## <a name="remarks"></a><span data-ttu-id="0c8a0-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c8a0-106">Remarks</span></span>

<span data-ttu-id="0c8a0-107">Para obter mais informações sobre membros de estrutura, consulte [**D3DXPLANE**](d3dxplane.md).</span><span class="sxs-lookup"><span data-stu-id="0c8a0-107">For more information about structure members, refer to [**D3DXPLANE**](d3dxplane.md).</span></span>

<span data-ttu-id="0c8a0-108">As sobrecargas de operador e as conversões de tipo para essa estrutura são implementadas em d3dx9math. inl.</span><span class="sxs-lookup"><span data-stu-id="0c8a0-108">Operator overloads and type casts for this structure are implemented in d3dx9math.inl.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c8a0-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c8a0-109">Requirements</span></span>



| <span data-ttu-id="0c8a0-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c8a0-110">Requirement</span></span> | <span data-ttu-id="0c8a0-111">Valor</span><span class="sxs-lookup"><span data-stu-id="0c8a0-111">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c8a0-112">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c8a0-112">Header</span></span><br/> | <dl> <span data-ttu-id="0c8a0-113"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c8a0-113"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c8a0-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c8a0-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c8a0-115">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="0c8a0-115">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




