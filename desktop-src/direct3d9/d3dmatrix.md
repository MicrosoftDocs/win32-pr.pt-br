---
description: Descreve uma matriz.
ms.assetid: d6b98a32-e745-4724-b8ce-a81a3f5416f3
title: D3DMATRIX (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATRIX
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6b4339d2e44e1add46103bae58ad3e02c8a6509b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812225"
---
# <a name="d3dmatrix"></a><span data-ttu-id="5b5cd-103">D3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="5b5cd-103">D3DMATRIX</span></span>

<span data-ttu-id="5b5cd-104">Descreve uma matriz.</span><span class="sxs-lookup"><span data-stu-id="5b5cd-104">Describes a matrix.</span></span>

``` syntax
typedef struct _D3DMATRIX {
    union {
        struct {
            float        _11, _12, _13, _14;
            float        _21, _22, _23, _24;
            float        _31, _32, _33, _34;
            float        _41, _42, _43, _44;

        };
        float m[4][4];
    };
} D3DMATRIX;
```

<span data-ttu-id="5b5cd-105">Tipos derivados: \* LPD3DMATRIX</span><span class="sxs-lookup"><span data-stu-id="5b5cd-105">Derived types: \*LPD3DMATRIX</span></span>

## <a name="members"></a><span data-ttu-id="5b5cd-106">Membros</span><span class="sxs-lookup"><span data-stu-id="5b5cd-106">Members</span></span>



| <span data-ttu-id="5b5cd-107">Item</span><span class="sxs-lookup"><span data-stu-id="5b5cd-107">Item</span></span>                                                        | <span data-ttu-id="5b5cd-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b5cd-108">Description</span></span>                                                                                                                                                                                                     |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b5cd-109"><span id="_ij"></span><span id="_IJ"></span>\_Ligatura</span><span class="sxs-lookup"><span data-stu-id="5b5cd-109"><span id="_ij"></span><span id="_IJ"></span>\_ij</span></span><br/> | <span data-ttu-id="5b5cd-110">Uma matriz de floats que representa uma matriz 4x4, onde é o número da linha e j é o número da coluna.</span><span class="sxs-lookup"><span data-stu-id="5b5cd-110">An array of floats that represent a 4x4 matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="5b5cd-111">Por exemplo, \_ 34 significa o mesmo que \[ um ₃ ₄ \] , o componente na terceira linha e a quarta coluna.</span><span class="sxs-lookup"><span data-stu-id="5b5cd-111">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5b5cd-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b5cd-112">Remarks</span></span>

<span data-ttu-id="5b5cd-113">No Direct3D, o \_ elemento 34 de uma matriz de projeção não pode ser um número negativo.</span><span class="sxs-lookup"><span data-stu-id="5b5cd-113">In Direct3D, the \_34 element of a projection matrix cannot be a negative number.</span></span> <span data-ttu-id="5b5cd-114">Se seu aplicativo precisar usar um valor negativo nesse local, ele deverá dimensionar toda a matriz de projeção em-1 em vez disso.</span><span class="sxs-lookup"><span data-stu-id="5b5cd-114">If your application needs to use a negative value in this location, it should scale the entire projection matrix by -1 instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b5cd-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b5cd-115">Requirements</span></span>



| <span data-ttu-id="5b5cd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b5cd-116">Requirement</span></span> | <span data-ttu-id="5b5cd-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5b5cd-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b5cd-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b5cd-118">Header</span></span><br/> | <dl> <span data-ttu-id="5b5cd-119"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b5cd-119"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b5cd-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b5cd-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b5cd-121">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="5b5cd-121">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="5b5cd-122">**GetTransform**</span><span class="sxs-lookup"><span data-stu-id="5b5cd-122">**GetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[<span data-ttu-id="5b5cd-123">**MultiplyTransform**</span><span class="sxs-lookup"><span data-stu-id="5b5cd-123">**MultiplyTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[<span data-ttu-id="5b5cd-124">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="5b5cd-124">**SetTransform**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

<span data-ttu-id="5b5cd-125">**SetTransform**</span><span class="sxs-lookup"><span data-stu-id="5b5cd-125">**SetTransform**</span></span>
</dt> <dt>

[<span data-ttu-id="5b5cd-126">**D3DXMATRIX**</span><span class="sxs-lookup"><span data-stu-id="5b5cd-126">**D3DXMATRIX**</span></span>](d3dxmatrix.md)
</dt> <dt>

[<span data-ttu-id="5b5cd-127">Transformações (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5b5cd-127">Transforms (Direct3D 9)</span></span>](transforms.md)
</dt> </dl>

 

 
