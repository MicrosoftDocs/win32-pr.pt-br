---
description: Estrutura D3DXVECTOR4 (D3dx9math. h) – descreve um vetor de quatro componentes, incluindo sobrecargas de operador e conversões de tipo.
ms.assetid: fbfe7851-7bec-4fa0-b4dc-52f5cb83d0a4
title: Estrutura D3DXVECTOR4 (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR4
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: d053c6d26df600fdf09d54eb66866014478845be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097564"
---
# <a name="d3dxvector4-structure-d3dx9mathh"></a><span data-ttu-id="43890-103">Estrutura D3DXVECTOR4 (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="43890-103">D3DXVECTOR4 structure (D3dx9math.h)</span></span>

<span data-ttu-id="43890-104">Descreve um vetor de quatro componentes, incluindo sobrecargas de operador e conversões de tipo.</span><span class="sxs-lookup"><span data-stu-id="43890-104">Describes a four-component vector including operator overloads and type casts.</span></span>

## <a name="syntax"></a><span data-ttu-id="43890-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43890-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR4 {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXVECTOR4, *LPD3DXVECTOR4;
```



## <a name="members"></a><span data-ttu-id="43890-106">Membros</span><span class="sxs-lookup"><span data-stu-id="43890-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="43890-107">**x**</span><span class="sxs-lookup"><span data-stu-id="43890-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="43890-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43890-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="43890-109">O componente x.</span><span class="sxs-lookup"><span data-stu-id="43890-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="43890-110">**y**</span><span class="sxs-lookup"><span data-stu-id="43890-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="43890-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43890-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="43890-112">O componente y.</span><span class="sxs-lookup"><span data-stu-id="43890-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="43890-113">**z**</span><span class="sxs-lookup"><span data-stu-id="43890-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="43890-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43890-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="43890-115">O componente z.</span><span class="sxs-lookup"><span data-stu-id="43890-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="43890-116">**w**</span><span class="sxs-lookup"><span data-stu-id="43890-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="43890-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="43890-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="43890-118">O componente w-.</span><span class="sxs-lookup"><span data-stu-id="43890-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43890-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="43890-119">Remarks</span></span>

### <a name="d3dxvector4-extensions"></a><span data-ttu-id="43890-120">Extensões D3DXVECTOR4</span><span class="sxs-lookup"><span data-stu-id="43890-120">D3DXVECTOR4 Extensions</span></span>

<span data-ttu-id="43890-121">O D3DXVECTOR4 tem as seguintes extensões C++.</span><span class="sxs-lookup"><span data-stu-id="43890-121">D3DXVECTOR4 has the following C++ extensions.</span></span>


```
typedef struct D3DXVECTOR4
{
#ifdef __cplusplus
public:
    D3DXVECTOR4() {};
    D3DXVECTOR4( CONST FLOAT* );
    D3DXVECTOR4( CONST D3DXFLOAT16 * );
    D3DXVECTOR4( CONST D3DVECTOR& xyz, FLOAT w );
    D3DXVECTOR4( FLOAT x, FLOAT y, FLOAT z, FLOAT w );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXVECTOR4& operator += ( CONST D3DXVECTOR4& );
    D3DXVECTOR4& operator -= ( CONST D3DXVECTOR4& );
    D3DXVECTOR4& operator *= ( FLOAT );
    D3DXVECTOR4& operator /= ( FLOAT );

    // unary operators
    D3DXVECTOR4 operator + () const;
    D3DXVECTOR4 operator - () const;

    // binary operators
    D3DXVECTOR4 operator + ( CONST D3DXVECTOR4& ) const;
    D3DXVECTOR4 operator - ( CONST D3DXVECTOR4& ) const;
    D3DXVECTOR4 operator * ( FLOAT ) const;
    D3DXVECTOR4 operator / ( FLOAT ) const;

    friend D3DXVECTOR4 operator * ( FLOAT, CONST D3DXVECTOR4& );

    BOOL operator == ( CONST D3DXVECTOR4& ) const;
    BOOL operator != ( CONST D3DXVECTOR4& ) const;

public:
#endif //__cplusplus
    FLOAT x, y, z, w;
} D3DXVECTOR4, *LPD3DXVECTOR4;



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



## <a name="requirements"></a><span data-ttu-id="43890-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43890-122">Requirements</span></span>



| <span data-ttu-id="43890-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="43890-123">Requirement</span></span> | <span data-ttu-id="43890-124">Valor</span><span class="sxs-lookup"><span data-stu-id="43890-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43890-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43890-125">Header</span></span><br/> | <dl> <span data-ttu-id="43890-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="43890-126"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43890-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="43890-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43890-128">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="43890-128">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
