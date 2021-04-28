---
description: Enumeração D3DXERR-os erros são representados por valores negativos e não podem ser combinados.
ms.assetid: 2318278e-e1e1-4cd8-a5ce-5c99f3bc47ba
title: Enumeração D3DXERR (D3dx9. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXERR
api_type:
- HeaderDef
api_location:
- d3dx9.h
ms.openlocfilehash: 1c1dd03500a493b30d7c1d3bfdfdf800b65a6d82
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094295"
---
# <a name="d3dxerr-enumeration"></a><span data-ttu-id="26eff-103">Enumeração D3DXERR</span><span class="sxs-lookup"><span data-stu-id="26eff-103">D3DXERR enumeration</span></span>

<span data-ttu-id="26eff-104">Os erros são representados por valores negativos e não podem ser combinados.</span><span class="sxs-lookup"><span data-stu-id="26eff-104">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="26eff-105">Veja a seguir uma lista de valores que podem ser retornados por métodos incluídos na biblioteca do utilitário D3DX.</span><span class="sxs-lookup"><span data-stu-id="26eff-105">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="26eff-106">Consulte as descrições do método individual para obter listas dos valores que cada um pode retornar.</span><span class="sxs-lookup"><span data-stu-id="26eff-106">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="26eff-107">Essas listas não são necessariamente abrangentes.</span><span class="sxs-lookup"><span data-stu-id="26eff-107">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="26eff-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="26eff-108">Syntax</span></span>


```C++
enum _D3DXERR {
  D3DXERR_CANNOTMODIFYINDEXBUFFER, 
  D3DXERR_INVALIDMESH, 
  D3DXERR_CANNOTATTRSORT, 
  D3DXERR_SKINNINGNOTSUPPORTED, 
  D3DXERR_TOOMANYINFLUENCES, 
  D3DXERR_INVALIDDATA, 
  D3DXERR_LOADEDMESHASNODATA, 
  D3DXERR_DUPLICATENAMEDFRAGMENT, 
  D3DXERR_CANNOTREMOVELASTITEM 

};
```



## <a name="constants"></a><span data-ttu-id="26eff-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="26eff-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="26eff-110"><span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**D3DXERR \_ CANNOTMODIFYINDEXBUFFER**</span><span class="sxs-lookup"><span data-stu-id="26eff-110"><span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**D3DXERR\_CANNOTMODIFYINDEXBUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="26eff-111">O buffer de índice não pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="26eff-111">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="26eff-112"><span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**D3DXERR \_ INVALIDMESH**</span><span class="sxs-lookup"><span data-stu-id="26eff-112"><span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**D3DXERR\_INVALIDMESH**</span></span>
</dt> <dd>

<span data-ttu-id="26eff-113">A malha é inválida.</span><span class="sxs-lookup"><span data-stu-id="26eff-113">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="26eff-114"><span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**D3DXERR \_ CANNOTATTRSORT**</span><span class="sxs-lookup"><span data-stu-id="26eff-114"><span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**D3DXERR\_CANNOTATTRSORT**</span></span>
</dt> <dd>

<span data-ttu-id="26eff-115">A classificação de atributo (D3DXMESHOPT \_ ATTRSORT) não tem suporte como uma técnica de otimização.</span><span class="sxs-lookup"><span data-stu-id="26eff-115">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="26eff-116"><span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**D3DXERR \_ SKINNINGNOTSUPPORTED**</span><span class="sxs-lookup"><span data-stu-id="26eff-116"><span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**D3DXERR\_SKINNINGNOTSUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="26eff-117">Não há suporte para a casca de capa.</span><span class="sxs-lookup"><span data-stu-id="26eff-117">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="26eff-118"><span id="D3DXERR_TOOMANYINFLUENCES"></span><span id="d3dxerr_toomanyinfluences"></span>**D3DXERR \_ TOOMANYINFLUENCES**</span><span class="sxs-lookup"><span data-stu-id="26eff-118"><span id="D3DXERR_TOOMANYINFLUENCES"></span><span id="d3dxerr_toomanyinfluences"></span>**D3DXERR\_TOOMANYINFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="26eff-119">Muitas influências especificadas.</span><span class="sxs-lookup"><span data-stu-id="26eff-119">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="26eff-120"><span id="D3DXERR_INVALIDDATA"></span><span id="d3dxerr_invaliddata"></span>**D3DXERR \_ INVALIDDATA**</span><span class="sxs-lookup"><span data-stu-id="26eff-120"><span id="D3DXERR_INVALIDDATA"></span><span id="d3dxerr_invaliddata"></span>**D3DXERR\_INVALIDDATA**</span></span>
</dt> <dd>

<span data-ttu-id="26eff-121">Os dados são inválidos.</span><span class="sxs-lookup"><span data-stu-id="26eff-121">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="26eff-122"><span id="D3DXERR_LOADEDMESHASNODATA"></span><span id="d3dxerr_loadedmeshasnodata"></span>**D3DXERR \_ LOADEDMESHASNODATA**</span><span class="sxs-lookup"><span data-stu-id="26eff-122"><span id="D3DXERR_LOADEDMESHASNODATA"></span><span id="d3dxerr_loadedmeshasnodata"></span>**D3DXERR\_LOADEDMESHASNODATA**</span></span>
</dt> <dd>

<span data-ttu-id="26eff-123">A malha não tem dados.</span><span class="sxs-lookup"><span data-stu-id="26eff-123">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="26eff-124"><span id="D3DXERR_DUPLICATENAMEDFRAGMENT"></span><span id="d3dxerr_duplicatenamedfragment"></span>**D3DXERR \_ DUPLICATENAMEDFRAGMENT**</span><span class="sxs-lookup"><span data-stu-id="26eff-124"><span id="D3DXERR_DUPLICATENAMEDFRAGMENT"></span><span id="d3dxerr_duplicatenamedfragment"></span>**D3DXERR\_DUPLICATENAMEDFRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="26eff-125">Já existe um fragmento com esse nome.</span><span class="sxs-lookup"><span data-stu-id="26eff-125">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="26eff-126"><span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**D3DXERR \_ CANNOTREMOVELASTITEM**</span><span class="sxs-lookup"><span data-stu-id="26eff-126"><span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**D3DXERR\_CANNOTREMOVELASTITEM**</span></span>
</dt> <dd>

<span data-ttu-id="26eff-127">O último item não pode ser excluído.</span><span class="sxs-lookup"><span data-stu-id="26eff-127">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26eff-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="26eff-128">Remarks</span></span>

<span data-ttu-id="26eff-129">O código de instalação \_ FACDD é usado para gerar códigos de erro, como nas macros a seguir.</span><span class="sxs-lookup"><span data-stu-id="26eff-129">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="26eff-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26eff-130">Requirements</span></span>



| <span data-ttu-id="26eff-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="26eff-131">Requirement</span></span> | <span data-ttu-id="26eff-132">Valor</span><span class="sxs-lookup"><span data-stu-id="26eff-132">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="26eff-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="26eff-133">Header</span></span><br/> | <dl> <span data-ttu-id="26eff-134"><dt>D3dx9. h</dt></span><span class="sxs-lookup"><span data-stu-id="26eff-134"><dt>D3dx9.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26eff-135">Consulte também</span><span class="sxs-lookup"><span data-stu-id="26eff-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26eff-136">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="26eff-136">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




