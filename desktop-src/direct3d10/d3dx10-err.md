---
description: D3DX10_ERR Enumeração-os erros são representados por valores negativos e não podem ser combinados.
ms.assetid: 4149ce6d-e87a-4003-b123-5555c6b3b086
title: Enumeração de D3DX10_ERR (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ERR
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 520abae0409dd4214106363d7ffde0cfb5c81ff1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094345"
---
# <a name="d3dx10_err-enumeration"></a><span data-ttu-id="77f99-103">\_Enumeração de erro D3DX10</span><span class="sxs-lookup"><span data-stu-id="77f99-103">D3DX10\_ERR enumeration</span></span>

<span data-ttu-id="77f99-104">Os erros são representados por valores negativos e não podem ser combinados.</span><span class="sxs-lookup"><span data-stu-id="77f99-104">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="77f99-105">Veja a seguir uma lista de valores que podem ser retornados por métodos incluídos na biblioteca do utilitário D3DX.</span><span class="sxs-lookup"><span data-stu-id="77f99-105">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="77f99-106">Consulte as descrições do método individual para obter listas dos valores que cada um pode retornar.</span><span class="sxs-lookup"><span data-stu-id="77f99-106">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="77f99-107">Essas listas não são necessariamente abrangentes.</span><span class="sxs-lookup"><span data-stu-id="77f99-107">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="77f99-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="77f99-108">Syntax</span></span>


```C++
typedef enum D3DX10_ERR { 
  D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER  = MAKE_DDHRESULT(2900),
  D3DX10_ERR_INVALID_MESH                = MAKE_DDHRESULT(2901),
  D3DX10_ERR_CANNOT_ATTR_SORT            = MAKE_DDHRESULT(2902),
  D3DX10_ERR_SKINNING_NOT_SUPPORTED      = MAKE_DDHRESULT(2903),
  D3DX10_ERR_TOO_MANY_INFLUENCES         = MAKE_DDHRESULT(2904),
  D3DX10_ERR_INVALID_DATA                = MAKE_DDHRESULT(2905),
  D3DX10_ERR_LOADED_MESH_HAS_NO_DATA     = MAKE_DDHRESULT(2906),
  D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT    = MAKE_DDHRESULT(2907),
  D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM     = MAKE_DDHRESULT(2908)
} D3DX10_ERR, *LPD3DX10_ERR;
```



## <a name="constants"></a><span data-ttu-id="77f99-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="77f99-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="77f99-110"><span id="D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx10_err_cannot_modify_index_buffer"></span>**D3DX10 \_ Err \_ não pode \_ Modificar o \_ buffer do índice \_**</span><span class="sxs-lookup"><span data-stu-id="77f99-110"><span id="D3DX10_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx10_err_cannot_modify_index_buffer"></span>**D3DX10\_ERR\_CANNOT\_MODIFY\_INDEX\_BUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="77f99-111">O buffer de índice não pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="77f99-111">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="77f99-112"><span id="D3DX10_ERR_INVALID_MESH"></span><span id="d3dx10_err_invalid_mesh"></span>**D3DX10 \_ erro \_ de \_ malha inválido**</span><span class="sxs-lookup"><span data-stu-id="77f99-112"><span id="D3DX10_ERR_INVALID_MESH"></span><span id="d3dx10_err_invalid_mesh"></span>**D3DX10\_ERR\_INVALID\_MESH**</span></span>
</dt> <dd>

<span data-ttu-id="77f99-113">A malha é inválida.</span><span class="sxs-lookup"><span data-stu-id="77f99-113">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="77f99-114"><span id="D3DX10_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx10_err_cannot_attr_sort"></span>**D3DX10 \_ Err \_ não \_ pode \_ classificar a classificação**</span><span class="sxs-lookup"><span data-stu-id="77f99-114"><span id="D3DX10_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx10_err_cannot_attr_sort"></span>**D3DX10\_ERR\_CANNOT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="77f99-115">A classificação de atributo (D3DXMESHOPT \_ ATTRSORT) não tem suporte como uma técnica de otimização.</span><span class="sxs-lookup"><span data-stu-id="77f99-115">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="77f99-116"><span id="D3DX10_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx10_err_skinning_not_supported"></span>**\_ \_ \_ Não \_ há suporte para o D3DX10 de erro de capa**</span><span class="sxs-lookup"><span data-stu-id="77f99-116"><span id="D3DX10_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx10_err_skinning_not_supported"></span>**D3DX10\_ERR\_SKINNING\_NOT\_SUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="77f99-117">Não há suporte para a casca de capa.</span><span class="sxs-lookup"><span data-stu-id="77f99-117">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="77f99-118"><span id="D3DX10_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx10_err_too_many_influences"></span>**D3DX10 erro em excesso de \_ \_ \_ \_ influências**</span><span class="sxs-lookup"><span data-stu-id="77f99-118"><span id="D3DX10_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx10_err_too_many_influences"></span>**D3DX10\_ERR\_TOO\_MANY\_INFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="77f99-119">Muitas influências especificadas.</span><span class="sxs-lookup"><span data-stu-id="77f99-119">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="77f99-120"><span id="D3DX10_ERR_INVALID_DATA"></span><span id="d3dx10_err_invalid_data"></span>**\_ \_ Dados inválidos de erro D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="77f99-120"><span id="D3DX10_ERR_INVALID_DATA"></span><span id="d3dx10_err_invalid_data"></span>**D3DX10\_ERR\_INVALID\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="77f99-121">Os dados são inválidos.</span><span class="sxs-lookup"><span data-stu-id="77f99-121">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="77f99-122"><span id="D3DX10_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx10_err_loaded_mesh_has_no_data"></span>**A \_ malha carregada de erro D3DX10 \_ \_ \_ \_ não tem \_ dados**</span><span class="sxs-lookup"><span data-stu-id="77f99-122"><span id="D3DX10_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx10_err_loaded_mesh_has_no_data"></span>**D3DX10\_ERR\_LOADED\_MESH\_HAS\_NO\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="77f99-123">A malha não tem dados.</span><span class="sxs-lookup"><span data-stu-id="77f99-123">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="77f99-124"><span id="D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx10_err_duplicate_named_fragment"></span>**\_ \_ Fragmento nomeado duplicado D3DX10 Err \_ \_**</span><span class="sxs-lookup"><span data-stu-id="77f99-124"><span id="D3DX10_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx10_err_duplicate_named_fragment"></span>**D3DX10\_ERR\_DUPLICATE\_NAMED\_FRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="77f99-125">Já existe um fragmento com esse nome.</span><span class="sxs-lookup"><span data-stu-id="77f99-125">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="77f99-126"><span id="D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx10_err_cannot_remove_last_item"></span>**D3DX10 \_ Err \_ não pode \_ remover o \_ último \_ Item**</span><span class="sxs-lookup"><span data-stu-id="77f99-126"><span id="D3DX10_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx10_err_cannot_remove_last_item"></span>**D3DX10\_ERR\_CANNOT\_REMOVE\_LAST\_ITEM**</span></span>
</dt> <dd>

<span data-ttu-id="77f99-127">O último item não pode ser excluído.</span><span class="sxs-lookup"><span data-stu-id="77f99-127">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77f99-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="77f99-128">Remarks</span></span>

<span data-ttu-id="77f99-129">O código de instalação \_ FACDD é usado para gerar códigos de erro, como nas macros a seguir.</span><span class="sxs-lookup"><span data-stu-id="77f99-129">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="77f99-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77f99-130">Requirements</span></span>



| <span data-ttu-id="77f99-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="77f99-131">Requirement</span></span> | <span data-ttu-id="77f99-132">Valor</span><span class="sxs-lookup"><span data-stu-id="77f99-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="77f99-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77f99-133">Header</span></span><br/> | <dl> <span data-ttu-id="77f99-134"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="77f99-134"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77f99-135">Consulte também</span><span class="sxs-lookup"><span data-stu-id="77f99-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77f99-136">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="77f99-136">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




