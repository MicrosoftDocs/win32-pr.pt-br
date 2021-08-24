---
title: D3DX11_ERR enumeração (D3DX11.h)
description: Observação A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store. Os erros são representados por valores negativos e não podem ser combinados.
ms.assetid: d042621d-a20b-4945-b6aa-714a451aa88a
keywords:
- D3DX11_ERR enumeração Direct3D 11
- LPD3DX11_ERR ponteiro de enumeração Direct3D 11
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
ms.openlocfilehash: d80b906b5b95693458eeea353f40fe446a22e8e33a6011b7851cf6d9663b3ed4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729316"
---
# <a name="d3dx11_err-enumeration"></a>Enumeração ERR D3DX11 \_

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store.

 

Os erros são representados por valores negativos e não podem ser combinados. Veja a seguir uma lista de valores que podem ser retornados por métodos incluídos na biblioteca do utilitário D3DX. Confira as descrições de método individuais para ver as listas dos valores que cada um pode retornar. Essas listas não são necessariamente abrangentes.

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

<span id="D3DX11_ERR_CANNOT_MODIFY_INDEX_BUFFER"></span><span id="d3dx11_err_cannot_modify_index_buffer"></span>**D3DX11 \_ ERR NÃO PODE MODIFICAR O BUFFER DE \_ \_ \_ \_ ÍNDICE**
</dt> <dd>

O buffer de índice não pode ser modificado.

</dd> <dt>

<span id="D3DX11_ERR_INVALID_MESH"></span><span id="d3dx11_err_invalid_mesh"></span>**D3DX11 \_ ERRO DE MALHA \_ \_ INVÁLIDA**
</dt> <dd>

A malha é inválida.

</dd> <dt>

<span id="D3DX11_ERR_CANNOT_ATTR_SORT"></span><span id="d3dx11_err_cannot_attr_sort"></span>**D3DX11 \_ ERR NÃO PODE CLASSIFICAR \_ \_ \_ ATTR**
</dt> <dd>

A classificação de atributo (D3DXMESHOPT \_ ATTRSORT) não tem suporte como uma técnica de otimização.

</dd> <dt>

<span id="D3DX11_ERR_SKINNING_NOT_SUPPORTED"></span><span id="d3dx11_err_skinning_not_supported"></span>**D3DX11 \_ NÃO \_ HÁ \_ SUPORTE PARA A REAÇÃO DE ERRO \_**
</dt> <dd>

Não há suporte para a reação de dados.

</dd> <dt>

<span id="D3DX11_ERR_TOO_MANY_INFLUENCES"></span><span id="d3dx11_err_too_many_influences"></span>**D3DX11 \_ ERR \_ MUITAS \_ \_ INFLUÊNCIAS**
</dt> <dd>

Muitas influências especificadas.

</dd> <dt>

<span id="D3DX11_ERR_INVALID_DATA"></span><span id="d3dx11_err_invalid_data"></span>**D3DX11 \_ ERRO DE DADOS \_ \_ INVÁLIDOS**
</dt> <dd>

Os dados são inválidos.

</dd> <dt>

<span id="D3DX11_ERR_LOADED_MESH_HAS_NO_DATA"></span><span id="d3dx11_err_loaded_mesh_has_no_data"></span>**D3DX11 \_ ERR \_ LOADED \_ MESH \_ HAS \_ NO \_ DATA**
</dt> <dd>

A malha não tem dados.

</dd> <dt>

<span id="D3DX11_ERR_DUPLICATE_NAMED_FRAGMENT"></span><span id="d3dx11_err_duplicate_named_fragment"></span>**D3DX11 \_ ERRO \_ DUPLICADO CHAMADO \_ \_ FRAGMENTO**
</dt> <dd>

Já existe um fragmento com esse nome.

</dd> <dt>

<span id="D3DX11_ERR_CANNOT_REMOVE_LAST_ITEM"></span><span id="d3dx11_err_cannot_remove_last_item"></span>**D3DX11 \_ ERR NÃO PODE REMOVER O ÚLTIMO \_ \_ \_ \_ ITEM**
</dt> <dd>

O último item não pode ser excluído.

</dd> </dl>

## <a name="remarks"></a>Comentários

O código \_ de instalação FACDD é usado para gerar códigos de erro, como nas macros a seguir.


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
| parâmetro<br/> | <dl> <dt>D3DX11.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





