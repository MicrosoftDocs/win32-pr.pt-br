---
description: Esta constante é o número máximo de declaradores de vértice para uma malha.
ms.assetid: 234e99a2-1907-4065-b03b-fb9e8d6812ab
title: Enumeração de MAX_FVF_DECL_SIZE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MAX_FVF_DECL_SIZE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 7204308e6b9355b416218f31af301b5ea6d8fff5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761908"
---
# <a name="max_fvf_decl_size-enumeration"></a><span data-ttu-id="c7fb9-103">Enumeração de tamanho máximo de \_ \_ DECL FVF \_</span><span class="sxs-lookup"><span data-stu-id="c7fb9-103">MAX\_FVF\_DECL\_SIZE enumeration</span></span>

<span data-ttu-id="c7fb9-104">Esta constante é o número máximo de declaradores de vértice para uma malha.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-104">This constant is the maximum number of vertex declarators for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7fb9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7fb9-105">Syntax</span></span>


```C++
typedef enum  { 
  MAX_FVF_DECL_SIZE  = MAXD3DDECLLENGTH + 1
} MAX_FVF_DECL_SIZE;
```



## <a name="constants"></a><span data-ttu-id="c7fb9-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="c7fb9-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c7fb9-107"><span id="MAX_FVF_DECL_SIZE"></span><span id="max_fvf_decl_size"></span>**tamanho máximo de \_ \_ DECL FVF \_**</span><span class="sxs-lookup"><span data-stu-id="c7fb9-107"><span id="MAX_FVF_DECL_SIZE"></span><span id="max_fvf_decl_size"></span>**MAX\_FVF\_DECL\_SIZE**</span></span>
</dt> <dd>

<span data-ttu-id="c7fb9-108">O número máximo de elementos na declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="c7fb9-108">The maximum number of elements in the vertex declaration.</span></span> <span data-ttu-id="c7fb9-109">O adicional (+ 1) é para [**D3DDECL \_ end**](d3ddecl-end.md).</span><span class="sxs-lookup"><span data-stu-id="c7fb9-109">The additional (+1) is for [**D3DDECL\_END**](d3ddecl-end.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7fb9-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7fb9-110">Remarks</span></span>

<span data-ttu-id="c7fb9-111">MAXD3DDECLLENGTH é definido como um máximo de 64 (consulte d3d9types. h).</span><span class="sxs-lookup"><span data-stu-id="c7fb9-111">MAXD3DDECLLENGTH is defined as a maximum of 64 (see d3d9types.h).</span></span> <span data-ttu-id="c7fb9-112">Isso não inclui o elemento vértice do marcador "End".</span><span class="sxs-lookup"><span data-stu-id="c7fb9-112">This does not include the "end" marker vertex element.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7fb9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7fb9-113">Requirements</span></span>



| <span data-ttu-id="c7fb9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7fb9-114">Requirement</span></span> | <span data-ttu-id="c7fb9-115">Valor</span><span class="sxs-lookup"><span data-stu-id="c7fb9-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7fb9-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c7fb9-116">Header</span></span><br/> | <dl> <span data-ttu-id="c7fb9-117"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7fb9-117"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7fb9-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7fb9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7fb9-119">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="c7fb9-119">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="c7fb9-120">**ID3DXBaseMesh**</span><span class="sxs-lookup"><span data-stu-id="c7fb9-120">**ID3DXBaseMesh**</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="c7fb9-121">**Getdeclaration**</span><span class="sxs-lookup"><span data-stu-id="c7fb9-121">**GetDeclaration**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexdeclaration9-getdeclaration)
</dt> <dt>

[<span data-ttu-id="c7fb9-122">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="c7fb9-122">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> <dt>

[<span data-ttu-id="c7fb9-123">**ID3DXSkinInfo**</span><span class="sxs-lookup"><span data-stu-id="c7fb9-123">**ID3DXSkinInfo**</span></span>](id3dxskininfo.md)
</dt> </dl>

 

 
