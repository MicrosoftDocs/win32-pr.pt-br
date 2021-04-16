---
description: Uma matriz 4x4 que contém métodos e sobrecargas de operador.
ms.assetid: 0911088b-50cf-4c4a-996e-351386fc359b
title: Estrutura D3DXMATRIX (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATRIX
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 2b09691ff27307e041a79b57e9d32c7e74e5eef1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765720"
---
# <a name="d3dxmatrix-structure-d3dx9mathh"></a><span data-ttu-id="c084a-103">Estrutura D3DXMATRIX (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c084a-103">D3DXMATRIX structure (D3dx9math.h)</span></span>

<span data-ttu-id="c084a-104">Uma matriz 4x4 que contém métodos e sobrecargas de operador.</span><span class="sxs-lookup"><span data-stu-id="c084a-104">A 4x4 matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="c084a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c084a-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIX {
  FLOAT _ij;
} D3DXMATRIX, *LPD3DXMATRIX;
```



## <a name="members"></a><span data-ttu-id="c084a-106">Membros</span><span class="sxs-lookup"><span data-stu-id="c084a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c084a-107">**\_Ligatura**</span><span class="sxs-lookup"><span data-stu-id="c084a-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="c084a-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c084a-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c084a-109">O componente (i, j) da matriz, onde é o número da linha e j é o número da coluna.</span><span class="sxs-lookup"><span data-stu-id="c084a-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="c084a-110">Por exemplo, \_ 34 significa o mesmo que \[ um ₃ ₄ \] , o componente na terceira linha e a quarta coluna.</span><span class="sxs-lookup"><span data-stu-id="c084a-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c084a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c084a-111">Remarks</span></span>

<span data-ttu-id="c084a-112">Os programadores C não podem usar a estrutura D3DXMATRIX, eles devem usar a estrutura [**D3DMATRIX**](d3dmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="c084a-112">C programmers cannot use the D3DXMATRIX structure, they must use the [**D3DMATRIX**](d3dmatrix.md) structure.</span></span> <span data-ttu-id="c084a-113">Os programadores do C++ podem aproveitar os construtores sobrecarregados e os operadores de atribuição, unário e binário (incluindo igualdade).</span><span class="sxs-lookup"><span data-stu-id="c084a-113">C++ programmers can take advantage of overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

<span data-ttu-id="c084a-114">No D3DX, o \_ elemento 34 de uma matriz de projeção não pode ser um número negativo.</span><span class="sxs-lookup"><span data-stu-id="c084a-114">In D3DX, the \_34 element of a projection matrix cannot be a negative number.</span></span> <span data-ttu-id="c084a-115">Se seu aplicativo precisar usar um valor negativo nesse local, ele deverá dimensionar toda a matriz de projeção em-1 em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c084a-115">If your application needs to use a negative value in this location, it should scale the entire projection matrix by -1 instead.</span></span>

### <a name="d3dxmatrix-extensions"></a><span data-ttu-id="c084a-116">Extensões D3DXMATRIX</span><span class="sxs-lookup"><span data-stu-id="c084a-116">D3DXMATRIX Extensions</span></span>

<span data-ttu-id="c084a-117">O **D3DXMATRIX** tem as seguintes extensões C++.</span><span class="sxs-lookup"><span data-stu-id="c084a-117">**D3DXMATRIX** has the following C++ extensions.</span></span>


```
#ifdef __cplusplus
typedef struct D3DXMATRIX : public D3DMATRIX
{
public:
    D3DXMATRIX() {};
    D3DXMATRIX( CONST FLOAT * );
    D3DXMATRIX( CONST D3DMATRIX& );
    D3DXMATRIX( CONST D3DXFLOAT16 * );
    D3DXMATRIX( FLOAT _11, FLOAT _12, FLOAT _13, FLOAT _14,
                FLOAT _21, FLOAT _22, FLOAT _23, FLOAT _24,
                FLOAT _31, FLOAT _32, FLOAT _33, FLOAT _34,
                FLOAT _41, FLOAT _42, FLOAT _43, FLOAT _44 );


    // access grants
    FLOAT& operator () ( UINT Row, UINT Col );
    FLOAT  operator () ( UINT Row, UINT Col ) const;

    // casting operators
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXMATRIX& operator *= ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator += ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator -= ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator *= ( FLOAT );
    D3DXMATRIX& operator /= ( FLOAT );

    // unary operators
    D3DXMATRIX operator + () const;
    D3DXMATRIX operator - () const;

    // binary operators
    D3DXMATRIX operator * ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator + ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator - ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator * ( FLOAT ) const;
    D3DXMATRIX operator / ( FLOAT ) const;

    friend D3DXMATRIX operator * ( FLOAT, CONST D3DXMATRIX& );

    BOOL operator == ( CONST D3DXMATRIX& ) const;
    BOOL operator != ( CONST D3DXMATRIX& ) const;

} D3DXMATRIX, *LPD3DXMATRIX;

#else //!__cplusplus
typedef struct _D3DMATRIX D3DXMATRIX, *LPD3DXMATRIX;
#endif //!__cplusplus
```



## <a name="requirements"></a><span data-ttu-id="c084a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c084a-118">Requirements</span></span>



| <span data-ttu-id="c084a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c084a-119">Requirement</span></span> | <span data-ttu-id="c084a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c084a-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c084a-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c084a-121">Header</span></span><br/> | <dl> <span data-ttu-id="c084a-122"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c084a-122"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c084a-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c084a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c084a-124">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="c084a-124">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="c084a-125">**D3DMATRIX**</span><span class="sxs-lookup"><span data-stu-id="c084a-125">**D3DMATRIX**</span></span>](d3dmatrix.md)
</dt> </dl>

 

 
