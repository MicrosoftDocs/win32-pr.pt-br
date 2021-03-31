---
description: Um 4x4, matriz alinhada em 16 bytes que contém métodos e sobrecargas de operador.
ms.assetid: c7082fe5-f98b-4ab7-b8c2-7cdbab4848ad
title: Estrutura D3DXMATRIXA16 (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATRIXA16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 57d2e5e796b929c87d4724d298758f26088918c4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103663991"
---
# <a name="d3dxmatrixa16-structure-d3dx9mathh"></a><span data-ttu-id="12791-103">Estrutura D3DXMATRIXA16 (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="12791-103">D3DXMATRIXA16 structure (D3dx9math.h)</span></span>

<span data-ttu-id="12791-104">Um 4x4, matriz alinhada em 16 bytes que contém métodos e sobrecargas de operador.</span><span class="sxs-lookup"><span data-stu-id="12791-104">A 4x4, 16-byte-aligned matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="12791-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12791-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIXA16 {
  FLOAT _ij;
} D3DXMATRIXA16, *LPD3DXMATRIXA16;
```



## <a name="members"></a><span data-ttu-id="12791-106">Membros</span><span class="sxs-lookup"><span data-stu-id="12791-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="12791-107">**\_Ligatura**</span><span class="sxs-lookup"><span data-stu-id="12791-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="12791-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="12791-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="12791-109">O componente (i, j) da matriz, onde é o número da linha e j é o número da coluna.</span><span class="sxs-lookup"><span data-stu-id="12791-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="12791-110">Por exemplo, \_ 34 significa o mesmo que \[ um ₃ ₄ \] , o componente na terceira linha e a quarta coluna.</span><span class="sxs-lookup"><span data-stu-id="12791-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12791-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="12791-111">Remarks</span></span>

<span data-ttu-id="12791-112">Uma matriz alinhada de 16 bytes, quando usada pelas funções matemáticas do D3DX, foi otimizada para melhorar o desempenho em processadores Intel Pentium 4.</span><span class="sxs-lookup"><span data-stu-id="12791-112">A 16-byte aligned matrix, when used by D3DX math functions, has been optimized for improved performance on Intel Pentium 4 processors.</span></span> <span data-ttu-id="12791-113">As matrizes são alinhadas independentemente de onde são criadas: na pilha de programas, no heap ou no escopo global.</span><span class="sxs-lookup"><span data-stu-id="12791-113">Matrices are aligned independent of where they are created: on the program stack, in the heap, or in global scope.</span></span> <span data-ttu-id="12791-114">O alinhamento é feito usando \_ \_ declspec (align (16)), que funciona com Visual C++ .net e com Visual C++ 6,0 somente quando o pacote de processador é instalado.</span><span class="sxs-lookup"><span data-stu-id="12791-114">Alignment is accomplished using \_\_declspec(align(16)), which works with Visual C++ .NET and with Visual C++ 6.0 only when the processor pack is installed.</span></span> <span data-ttu-id="12791-115">Infelizmente, não há como detectar o pacote do processador, portanto, o alinhamento de bytes é ativado por padrão somente com o Visual C++ .NET.</span><span class="sxs-lookup"><span data-stu-id="12791-115">Unfortunately, there is no way to detect the processor pack, so byte alignment is turned on by default only with Visual C++ .NET.</span></span>

<span data-ttu-id="12791-116">Vetores e quaternions não são alinhados em byte em D3DX.</span><span class="sxs-lookup"><span data-stu-id="12791-116">Vectors and quaternions are not byte aligned in D3DX.</span></span> <span data-ttu-id="12791-117">Ao usar vetores e quaternions com funções matemáticas de D3DX, use \_ declspec (align (16)) para gerar vetores alinhados em bytes e quaternions, pois eles serão executados significativamente melhor.</span><span class="sxs-lookup"><span data-stu-id="12791-117">When using vectors and quaternions with D3DX math functions, use \_declspec(align(16)) to generate byte aligned vectors and quaternions, because they will perform significantly better.</span></span> <span data-ttu-id="12791-118">A definição de \_ declspec é mostrada aqui.</span><span class="sxs-lookup"><span data-stu-id="12791-118">The definition of \_declspec is shown here.</span></span>


```
#define D3DX_ALIGN16 __declspec(align(16))
```



<span data-ttu-id="12791-119">Outros compiladores interpretam D3DXMATRIXA16 como D3DXMATRIX.</span><span class="sxs-lookup"><span data-stu-id="12791-119">Other compilers interpret D3DXMATRIXA16 as D3DXMATRIX.</span></span> <span data-ttu-id="12791-120">Usar essa estrutura em um compilador que não alinha de fato a matriz pode ser problemática porque não expõe bugs que ignoram o alinhamento.</span><span class="sxs-lookup"><span data-stu-id="12791-120">Using this structure on a compiler that does not actually align the matrix can be problematic because it will not expose bugs that ignore alignment.</span></span> <span data-ttu-id="12791-121">Por exemplo, se um objeto D3DXMATRIXA16 estiver dentro de uma estrutura ou classe, um [**memcpy**](https://msdn.microsoft.com/library/dswaw1wk(v=VS.71).aspx) poderá ser feito com uma embalagem justa (ignorando limites de 16 bytes).</span><span class="sxs-lookup"><span data-stu-id="12791-121">For example, if a D3DXMATRIXA16 object is inside a structure or class, a [**memcpy**](https://msdn.microsoft.com/library/dswaw1wk(v=VS.71).aspx) might be done with tight packing (ignoring 16-byte boundaries).</span></span> <span data-ttu-id="12791-122">Isso causaria quebras de compilação se o compilador fosse ao mesmo tempo em que adicionava o alinhamento da matriz.</span><span class="sxs-lookup"><span data-stu-id="12791-122">This would cause build breaks if the compiler were to sometime add matrix aligning.</span></span>

### <a name="d3dxmatrixa16"></a><span data-ttu-id="12791-123">D3DXMATRIXA16</span><span class="sxs-lookup"><span data-stu-id="12791-123">D3DXMATRIXA16</span></span>

<span data-ttu-id="12791-124">O **D3DXMATRIXA16** tem as seguintes extensões C++.</span><span class="sxs-lookup"><span data-stu-id="12791-124">**D3DXMATRIXA16** has the following C++ extensions.</span></span>


```
typedef struct _D3DXMATRIXA16 : public D3DXMATRIX
{
    _D3DXMATRIXA16();
    _D3DXMATRIXA16( CONST FLOAT * f);
    _D3DXMATRIXA16( CONST D3DMATRIX& m);
    _D3DXMATRIXA16( FLOAT _11, FLOAT _12, FLOAT _13, FLOAT _14,
                    FLOAT _21, FLOAT _22, FLOAT _23, FLOAT _24,
                    FLOAT _31, FLOAT _32, FLOAT _33, FLOAT _34,
                    FLOAT _41, FLOAT _42, FLOAT _43, FLOAT _44 );
    void* operator new(size_t s);
    void* operator new[](size_t s);

    // The two operators below are not virtual operators. If you cast
    //   to D3DXMATRIX, do not delete using them
    void operator delete(void* p);
    void operator delete[](void* p);

    struct _D3DXMATRIXA16& operator=(CONST D3DXMATRIX& rhs);
} _D3DXMATRIXA16;

typedef D3DX_ALIGN16 _D3DXMATRIXA16 D3DXMATRIXA16, *LPD3DXMATRIXA16;
        
```



## <a name="requirements"></a><span data-ttu-id="12791-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12791-125">Requirements</span></span>



| <span data-ttu-id="12791-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="12791-126">Requirement</span></span> | <span data-ttu-id="12791-127">Valor</span><span class="sxs-lookup"><span data-stu-id="12791-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="12791-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12791-128">Header</span></span><br/> | <dl> <span data-ttu-id="12791-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="12791-129"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12791-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="12791-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12791-131">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="12791-131">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="12791-132">**D3DXMATRIX**</span><span class="sxs-lookup"><span data-stu-id="12791-132">**D3DXMATRIX**</span></span>](d3dxmatrix.md)
</dt> </dl>

 

 
