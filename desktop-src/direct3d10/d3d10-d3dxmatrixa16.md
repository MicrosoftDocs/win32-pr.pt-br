---
description: Estrutura D3DXMATRIXA16 (D3DX10Math. h) – um 4x4, matriz alinhada com 16 bytes que contém métodos e sobrecargas de operador.
ms.assetid: d9e9c1cc-7555-4011-a4b4-8cce20404841
title: Estrutura D3DXMATRIXA16 (D3DX10Math. h)
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
- D3DX10Math.h
ms.openlocfilehash: e81071d44340ef7a4b874633e736e21016c697a6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113184"
---
# <a name="d3dxmatrixa16-structure-d3dx10mathh"></a><span data-ttu-id="985b1-103">Estrutura D3DXMATRIXA16 (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="985b1-103">D3DXMATRIXA16 structure (D3DX10Math.h)</span></span>

<span data-ttu-id="985b1-104">Um 4x4, matriz alinhada em 16 bytes que contém métodos e sobrecargas de operador.</span><span class="sxs-lookup"><span data-stu-id="985b1-104">A 4x4, 16-byte-aligned matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="985b1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="985b1-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIXA16 {
  FLOAT _ij;
} D3DXMATRIXA16, *LPD3DXMATRIXA16;
```



## <a name="members"></a><span data-ttu-id="985b1-106">Membros</span><span class="sxs-lookup"><span data-stu-id="985b1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="985b1-107">**\_Ligatura**</span><span class="sxs-lookup"><span data-stu-id="985b1-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="985b1-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="985b1-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="985b1-109">O componente (i, j) da matriz, onde é o número da linha e j é o número da coluna.</span><span class="sxs-lookup"><span data-stu-id="985b1-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="985b1-110">Por exemplo, \_ 34 significa o mesmo que \[ um ₃ ₄ \] , o componente na terceira linha e a quarta coluna.</span><span class="sxs-lookup"><span data-stu-id="985b1-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="985b1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="985b1-111">Remarks</span></span>

<span data-ttu-id="985b1-112">Uma matriz alinhada de 16 bytes, quando usada pelas funções matemáticas do D3DX, foi otimizada para melhorar o desempenho em processadores Intel Pentium 4.</span><span class="sxs-lookup"><span data-stu-id="985b1-112">A 16-byte aligned matrix, when used by D3DX math functions, has been optimized for improved performance on Intel Pentium 4 processors.</span></span> <span data-ttu-id="985b1-113">As matrizes são alinhadas independentemente de onde são criadas: na pilha de programas, no heap ou no escopo global.</span><span class="sxs-lookup"><span data-stu-id="985b1-113">Matrices are aligned independent of where they are created: on the program stack, in the heap, or in global scope.</span></span> <span data-ttu-id="985b1-114">O alinhamento é feito usando \_ \_ declspec (align (16)), que funciona com Visual C++ .net e com Visual C++ 6,0 somente quando o pacote de processador é instalado.</span><span class="sxs-lookup"><span data-stu-id="985b1-114">Alignment is accomplished using \_\_declspec(align(16)), which works with Visual C++ .NET and with Visual C++ 6.0 only when the processor pack is installed.</span></span> <span data-ttu-id="985b1-115">Infelizmente, não há como detectar o pacote do processador, portanto, o alinhamento de bytes é ativado por padrão somente com o Visual C++ .NET.</span><span class="sxs-lookup"><span data-stu-id="985b1-115">Unfortunately, there is no way to detect the processor pack, so byte alignment is turned on by default only with Visual C++ .NET.</span></span>

<span data-ttu-id="985b1-116">Vetores e quaternions não são alinhados em byte em D3DX.</span><span class="sxs-lookup"><span data-stu-id="985b1-116">Vectors and quaternions are not byte aligned in D3DX.</span></span> <span data-ttu-id="985b1-117">Ao usar vetores e quaternions com funções matemáticas de D3DX, use \_ declspec (align (16)) para gerar vetores alinhados em bytes e quaternions, pois eles serão executados significativamente melhor.</span><span class="sxs-lookup"><span data-stu-id="985b1-117">When using vectors and quaternions with D3DX math functions, use \_declspec(align(16)) to generate byte aligned vectors and quaternions, because they will perform significantly better.</span></span> <span data-ttu-id="985b1-118">A definição de \_ declspec é mostrada aqui.</span><span class="sxs-lookup"><span data-stu-id="985b1-118">The definition of \_declspec is shown here.</span></span>


```
#define D3DX_ALIGN16 __declspec(align(16))
```



<span data-ttu-id="985b1-119">Outros compiladores interpretam **D3DXMATRIXA16** como [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="985b1-119">Other compilers interpret **D3DXMATRIXA16** as [**D3DXMATRIX**](d3d10-d3dxmatrix.md).</span></span> <span data-ttu-id="985b1-120">Usar essa estrutura em um compilador que não alinha de fato a matriz pode ser problemática porque não expõe bugs que ignoram o alinhamento.</span><span class="sxs-lookup"><span data-stu-id="985b1-120">Using this structure on a compiler that does not actually align the matrix can be problematic because it will not expose bugs that ignore alignment.</span></span> <span data-ttu-id="985b1-121">Por exemplo, se um objeto **D3DXMATRIXA16** estiver dentro de uma estrutura ou classe, um [memcpy](https://msdn2.microsoft.com/library/dswaw1wk(vs.71).aspx) poderá ser feito com uma embalagem justa (ignorando limites de 16 bytes).</span><span class="sxs-lookup"><span data-stu-id="985b1-121">For example, if a **D3DXMATRIXA16** object is inside a structure or class, a [memcpy](https://msdn2.microsoft.com/library/dswaw1wk(vs.71).aspx) might be done with tight packing (ignoring 16-byte boundaries).</span></span> <span data-ttu-id="985b1-122">Isso causaria quebras de compilação se o compilador fosse ao mesmo tempo em que adicionava o alinhamento da matriz.</span><span class="sxs-lookup"><span data-stu-id="985b1-122">This would cause build breaks if the compiler were to sometime add matrix aligning.</span></span>

### <a name="d3dxmatrixa16-extensions"></a><span data-ttu-id="985b1-123">Extensões D3DXMATRIXA16</span><span class="sxs-lookup"><span data-stu-id="985b1-123">D3DXMATRIXA16 Extensions</span></span>

<span data-ttu-id="985b1-124">O **D3DXMATRIXA16** tem as seguintes extensões C++.</span><span class="sxs-lookup"><span data-stu-id="985b1-124">**D3DXMATRIXA16** has the following C++ extensions.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="985b1-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="985b1-125">Requirements</span></span>



| <span data-ttu-id="985b1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="985b1-126">Requirement</span></span> | <span data-ttu-id="985b1-127">Valor</span><span class="sxs-lookup"><span data-stu-id="985b1-127">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="985b1-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="985b1-128">Header</span></span><br/> | <dl> <span data-ttu-id="985b1-129"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="985b1-129"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="985b1-130">Consulte também</span><span class="sxs-lookup"><span data-stu-id="985b1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="985b1-131">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="985b1-131">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
