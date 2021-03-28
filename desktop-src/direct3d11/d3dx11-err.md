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
# <a name="d3dx11_err-enumeration"></a>\_Enumeração de erro D3DX11

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.

 

Os erros são representados por valores negativos e não podem ser combinados. Veja a seguir uma lista de valores que podem ser retornados por métodos incluídos na biblioteca do utilitário D3DX. Consulte as descrições do método individual para obter listas dos valores que cada um pode retornar. Essas listas não são necessariamente abrangentes.

## <a name="syntax"></a>Syntax


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx11_err_cannot_modify_index_buffer"></span>**D3DX11 \_ Err \_ não pode \_ Modificar o \_ buffer do índice \_**
</dt> <dd>

O buffer de índice não pode ser modificado.

</dd> <dt>

<span id="D3DX11_ERR_INVALID_MESH"></span><span id="d3dx11_err_invalid_mesh"></span>**D3DX11 \_ erro \_ de \_ malha inválido**
</dt> <dd>

A malha é inválida.

</dd> <dt>

<span id="D3DX11_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx11_err_cannot_attr_sort"></span>**D3DX11 \_ Err \_ não \_ pode \_ classificar a classificação**
</dt> <dd>

A classificação de atributo (D3DXMESHOPT \_ ATTRSORT) não tem suporte como uma técnica de otimização.

</dd> <dt>

<span id="D3DX11_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx11_err_skinning_not_supported"></span>**\_ \_ \_ Não \_ há suporte para o D3DX11 de erro de capa**
</dt> <dd>

Não há suporte para a casca de capa.

</dd> <dt>

<span id="D3DX11_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx11_err_too_many_influences"></span>**D3DX11 erro em excesso de \_ \_ \_ \_ influências**
</dt> <dd>

Muitas influências especificadas.

</dd> <dt>

<span id="D3DX11_ERR_INVALID_DATA"></span><span id="d3dx11_err_invalid_data"></span>**\_ \_ Dados inválidos de erro D3DX11 \_**
</dt> <dd>

Os dados são inválidos.

</dd> <dt>

<span id="D3DX11_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx11_err_loaded_mesh_has_no_data"></span>**A \_ malha carregada de erro D3DX11 \_ \_ \_ \_ não tem \_ dados**
</dt> <dd>

A malha não tem dados.

</dd> <dt>

<span id="D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx11_err_duplicate_named_fragment"></span>**\_ \_ Fragmento nomeado duplicado D3DX11 Err \_ \_**
</dt> <dd>

Já existe um fragmento com esse nome.

</dd> <dt>

<span id="D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx11_err_cannot_remove_last_item"></span>**D3DX11 \_ Err \_ não pode \_ remover o \_ último \_ Item**
</dt> <dd>

O último item não pode ser excluído.

</dd> </dl>

## <a name="remarks"></a>Comentários

O código de instalação \_ FACDD é usado para gerar códigos de erro, como nas macros a seguir.


```
#define _FACDD                  0x876
#define MAKE_DDHRESULT( code )  MAKE_HRESULT( 1, _FACDD, code )
enum _D3DXERR {
    D3DXERR_CANNOTMODIFYINDEXBUFFER = MAKE_DDHRESULT(2900),
    D3DXERR_INVALIDMESH             = MAKE_DDHRESULT(2901),
    ...
    };
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX11. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





