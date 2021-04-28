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
# <a name="d3dxerr-enumeration"></a>Enumeração D3DXERR

Os erros são representados por valores negativos e não podem ser combinados. Veja a seguir uma lista de valores que podem ser retornados por métodos incluídos na biblioteca do utilitário D3DX. Consulte as descrições do método individual para obter listas dos valores que cada um pode retornar. Essas listas não são necessariamente abrangentes.

## <a name="syntax"></a>Sintaxe


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**D3DXERR \_ CANNOTMODIFYINDEXBUFFER**
</dt> <dd>

O buffer de índice não pode ser modificado.

</dd> <dt>

<span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**D3DXERR \_ INVALIDMESH**
</dt> <dd>

A malha é inválida.

</dd> <dt>

<span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**D3DXERR \_ CANNOTATTRSORT**
</dt> <dd>

A classificação de atributo (D3DXMESHOPT \_ ATTRSORT) não tem suporte como uma técnica de otimização.

</dd> <dt>

<span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**D3DXERR \_ SKINNINGNOTSUPPORTED**
</dt> <dd>

Não há suporte para a casca de capa.

</dd> <dt>

<span id="D3DXERR_TOOMANYINFLUENCES"></span><span id="d3dxerr_toomanyinfluences"></span>**D3DXERR \_ TOOMANYINFLUENCES**
</dt> <dd>

Muitas influências especificadas.

</dd> <dt>

<span id="D3DXERR_INVALIDDATA"></span><span id="d3dxerr_invaliddata"></span>**D3DXERR \_ INVALIDDATA**
</dt> <dd>

Os dados são inválidos.

</dd> <dt>

<span id="D3DXERR_LOADEDMESHASNODATA"></span><span id="d3dxerr_loadedmeshasnodata"></span>**D3DXERR \_ LOADEDMESHASNODATA**
</dt> <dd>

A malha não tem dados.

</dd> <dt>

<span id="D3DXERR_DUPLICATENAMEDFRAGMENT"></span><span id="d3dxerr_duplicatenamedfragment"></span>**D3DXERR \_ DUPLICATENAMEDFRAGMENT**
</dt> <dd>

Já existe um fragmento com esse nome.

</dd> <dt>

<span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**D3DXERR \_ CANNOTREMOVELASTITEM**
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
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Enumerações D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




