---
title: Enumeração de D3DX11_ERR (D3DX11. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Os erros são representados por valores negativos e não podem ser combinados.
ms.assetid: d042621d-a20b-4945-b6aa-714a451aa88a
keywords:
- Enumeração D3DX11_ERR Direct3D 11
- Ponteiro de enumeração LPD3DX11_ERR Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_ERR
api_location:
- D3DX11.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0607bd495bad4bdeacf66ae593670dbe3ad0d2e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989396"
---
# <a name="d3dx11_err-enumeration"></a><span data-ttu-id="c7381-106">\_Enumeração de erro D3DX11</span><span class="sxs-lookup"><span data-stu-id="c7381-106">D3DX11\_ERR enumeration</span></span>

> [!Note]  
> <span data-ttu-id="c7381-107">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="c7381-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="c7381-108">Os erros são representados por valores negativos e não podem ser combinados.</span><span class="sxs-lookup"><span data-stu-id="c7381-108">Errors are represented by negative values and cannot be combined.</span></span> <span data-ttu-id="c7381-109">Veja a seguir uma lista de valores que podem ser retornados por métodos incluídos na biblioteca do utilitário D3DX.</span><span class="sxs-lookup"><span data-stu-id="c7381-109">The following is a list of values that can be returned by methods included with the D3DX utility library.</span></span> <span data-ttu-id="c7381-110">Consulte as descrições do método individual para obter listas dos valores que cada um pode retornar.</span><span class="sxs-lookup"><span data-stu-id="c7381-110">See the individual method descriptions for lists of the values that each can return.</span></span> <span data-ttu-id="c7381-111">Essas listas não são necessariamente abrangentes.</span><span class="sxs-lookup"><span data-stu-id="c7381-111">These lists are not necessarily comprehensive.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7381-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7381-112">Syntax</span></span>


```C++
typedef enum D3DX11_ERR { 
  D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER  = MAKE_DDHRESULT(2900),
  D3DX11_ERR_INVALID_MESH                = MAKE_DDHRESULT(2901),
  D3DX11_ERR_CANNOT_ATTR_SORT            = MAKE_DDHRESULT(2902),
  D3DX11_ERR_SKINNING_NOT_SUPPORTED      = MAKE_DDHRESULT(2903),
  D3DX11_ERR_TOO_MANY_INFLUENCES         = MAKE_DDHRESULT(2904),
  D3DX11_ERR_INVALID_DATA                = MAKE_DDHRESULT(2905),
  D3DX11_ERR_LOADED_MESH_HAS_NO_DATA     = MAKE_DDHRESULT(2906),
  D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT    = MAKE_DDHRESULT(2907),
  D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM     = MAKE_DDHRESULT(2908)
} D3DX11_ERR, *LPD3DX11_ERR;
```



## <a name="constants"></a><span data-ttu-id="c7381-113">Constantes</span><span class="sxs-lookup"><span data-stu-id="c7381-113">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c7381-114"><span id="D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx11_err_cannot_modify_index_buffer"></span>**D3DX11 \_ Err \_ não pode \_ Modificar o \_ buffer do índice \_**</span><span class="sxs-lookup"><span data-stu-id="c7381-114"><span id="D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx11_err_cannot_modify_index_buffer"></span>**D3DX11\_ERR\_CANNOT\_MODIFY\_INDEX\_BUFFER**</span></span>
</dt> <dd>

<span data-ttu-id="c7381-115">O buffer de índice não pode ser modificado.</span><span class="sxs-lookup"><span data-stu-id="c7381-115">The index buffer cannot be modified.</span></span>

</dd> <dt>

<span data-ttu-id="c7381-116"><span id="D3DX11_ERR_INVALID_MESH"></span><span id="d3dx11_err_invalid_mesh"></span>**D3DX11 \_ erro \_ de \_ malha inválido**</span><span class="sxs-lookup"><span data-stu-id="c7381-116"><span id="D3DX11_ERR_INVALID_MESH"></span><span id="d3dx11_err_invalid_mesh"></span>**D3DX11\_ERR\_INVALID\_MESH**</span></span>
</dt> <dd>

<span data-ttu-id="c7381-117">A malha é inválida.</span><span class="sxs-lookup"><span data-stu-id="c7381-117">The mesh is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="c7381-118"><span id="D3DX11_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx11_err_cannot_attr_sort"></span>**D3DX11 \_ Err \_ não \_ pode \_ classificar a classificação**</span><span class="sxs-lookup"><span data-stu-id="c7381-118"><span id="D3DX11_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx11_err_cannot_attr_sort"></span>**D3DX11\_ERR\_CANNOT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="c7381-119">A classificação de atributo (D3DXMESHOPT \_ ATTRSORT) não tem suporte como uma técnica de otimização.</span><span class="sxs-lookup"><span data-stu-id="c7381-119">Attribute sort (D3DXMESHOPT\_ATTRSORT) is not supported as an optimization technique.</span></span>

</dd> <dt>

<span data-ttu-id="c7381-120"><span id="D3DX11_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx11_err_skinning_not_supported"></span>**\_ \_ \_ Não \_ há suporte para o D3DX11 de erro de capa**</span><span class="sxs-lookup"><span data-stu-id="c7381-120"><span id="D3DX11_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx11_err_skinning_not_supported"></span>**D3DX11\_ERR\_SKINNING\_NOT\_SUPPORTED**</span></span>
</dt> <dd>

<span data-ttu-id="c7381-121">Não há suporte para a casca de capa.</span><span class="sxs-lookup"><span data-stu-id="c7381-121">Skinning is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c7381-122"><span id="D3DX11_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx11_err_too_many_influences"></span>**D3DX11 erro em excesso de \_ \_ \_ \_ influências**</span><span class="sxs-lookup"><span data-stu-id="c7381-122"><span id="D3DX11_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx11_err_too_many_influences"></span>**D3DX11\_ERR\_TOO\_MANY\_INFLUENCES**</span></span>
</dt> <dd>

<span data-ttu-id="c7381-123">Muitas influências especificadas.</span><span class="sxs-lookup"><span data-stu-id="c7381-123">Too many influences specified.</span></span>

</dd> <dt>

<span data-ttu-id="c7381-124"><span id="D3DX11_ERR_INVALID_DATA"></span><span id="d3dx11_err_invalid_data"></span>**\_ \_ Dados inválidos de erro D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="c7381-124"><span id="D3DX11_ERR_INVALID_DATA"></span><span id="d3dx11_err_invalid_data"></span>**D3DX11\_ERR\_INVALID\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="c7381-125">Os dados são inválidos.</span><span class="sxs-lookup"><span data-stu-id="c7381-125">The data is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="c7381-126"><span id="D3DX11_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx11_err_loaded_mesh_has_no_data"></span>**A \_ malha carregada de erro D3DX11 \_ \_ \_ \_ não tem \_ dados**</span><span class="sxs-lookup"><span data-stu-id="c7381-126"><span id="D3DX11_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx11_err_loaded_mesh_has_no_data"></span>**D3DX11\_ERR\_LOADED\_MESH\_HAS\_NO\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="c7381-127">A malha não tem dados.</span><span class="sxs-lookup"><span data-stu-id="c7381-127">The mesh has no data.</span></span>

</dd> <dt>

<span data-ttu-id="c7381-128"><span id="D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx11_err_duplicate_named_fragment"></span>**\_ \_ Fragmento nomeado duplicado D3DX11 Err \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c7381-128"><span id="D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx11_err_duplicate_named_fragment"></span>**D3DX11\_ERR\_DUPLICATE\_NAMED\_FRAGMENT**</span></span>
</dt> <dd>

<span data-ttu-id="c7381-129">Já existe um fragmento com esse nome.</span><span class="sxs-lookup"><span data-stu-id="c7381-129">A fragment with that name already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c7381-130"><span id="D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx11_err_cannot_remove_last_item"></span>**D3DX11 \_ Err \_ não pode \_ remover o \_ último \_ Item**</span><span class="sxs-lookup"><span data-stu-id="c7381-130"><span id="D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx11_err_cannot_remove_last_item"></span>**D3DX11\_ERR\_CANNOT\_REMOVE\_LAST\_ITEM**</span></span>
</dt> <dd>

<span data-ttu-id="c7381-131">O último item não pode ser excluído.</span><span class="sxs-lookup"><span data-stu-id="c7381-131">The last item cannot be deleted.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7381-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7381-132">Remarks</span></span>

<span data-ttu-id="c7381-133">O código de instalação \_ FACDD é usado para gerar códigos de erro, como nas macros a seguir.</span><span class="sxs-lookup"><span data-stu-id="c7381-133">The facility code \_FACDD is used to generate error codes, as in the following macros.</span></span>


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a><span data-ttu-id="c7381-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7381-134">Requirements</span></span>



| <span data-ttu-id="c7381-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7381-135">Requirement</span></span> | <span data-ttu-id="c7381-136">Valor</span><span class="sxs-lookup"><span data-stu-id="c7381-136">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c7381-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c7381-137">Header</span></span><br/> | <dl> <span data-ttu-id="c7381-138"><dt>D3DX11. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7381-138"><dt>D3DX11.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7381-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7381-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7381-140">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="c7381-140">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





