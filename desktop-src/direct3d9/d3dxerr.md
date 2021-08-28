---
description: Enumeração D3DXERR – os erros são representados por valores negativos e não podem ser combinados.
ms.assetid: 2318278e-e1e1-4cd8-a5ce-5c99f3bc47ba
title: Enumeração D3DXERR (D3dx9.h)
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
ms.openlocfilehash: 2fc6f72ab88a3c85eff592e289364a1f67eb9c220a7592397eda14b8bf4aace6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988506"
---
# <a name="d3dxerr-enumeration"></a>Enumeração D3DXERR

Os erros são representados por valores negativos e não podem ser combinados. Veja a seguir uma lista de valores que podem ser retornados por métodos incluídos na biblioteca do utilitário D3DX. Confira as descrições de método individuais para ver as listas dos valores que cada um pode retornar. Essas listas não são necessariamente abrangentes.

## <a name="syntax"></a>Syntax


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

<span id="D3DXERR_CANNOTMODIFYINDEXBUFFER"></span><span id="d3dxerr_cannotmodifyindexbuffer"></span>**D3DXERR \_ NÃO PODEMODIFYINDEXBUFFER**
</dt> <dd>

O buffer de índice não pode ser modificado.

</dd> <dt>

<span id="D3DXERR_INVALIDMESH"></span><span id="d3dxerr_invalidmesh"></span>**D3DXERR \_ INVALIDMESH**
</dt> <dd>

A malha é inválida.

</dd> <dt>

<span id="D3DXERR_CANNOTATTRSORT"></span><span id="d3dxerr_cannotattrsort"></span>**D3DXERR \_ NÃO PODEATTRSORT**
</dt> <dd>

A classificação de atributo (D3DXMESHOPT \_ ATTRSORT) não tem suporte como uma técnica de otimização.

</dd> <dt>

<span id="D3DXERR_SKINNINGNOTSUPPORTED"></span><span id="d3dxerr_skinningnotsupported"></span>**D3DXERR \_ NÃO COMPATÍVEL**
</dt> <dd>

Não há suporte para a reação de dados.

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

<span id="D3DXERR_CANNOTREMOVELASTITEM"></span><span id="d3dxerr_cannotremovelastitem"></span>**D3DXERR \_ NÃO PODEREMOVELASTITEM**
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
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




