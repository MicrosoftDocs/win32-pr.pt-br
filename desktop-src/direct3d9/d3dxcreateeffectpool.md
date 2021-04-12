---
description: Crie um pool de efeitos. Um pool é usado para compartilhar parâmetros entre efeitos.
ms.assetid: 5b202f85-b32b-4041-8873-0de535c2f59f
title: Função D3DXCreateEffectPool (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectPool
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 14753500ac15fb0ed30d46b1121431af78e1fe93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173156"
---
# <a name="d3dxcreateeffectpool-function"></a>Função D3DXCreateEffectPool

Crie um pool de efeitos. Um pool é usado para compartilhar parâmetros entre efeitos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DXCreateEffectPool(
  _Out_ LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppPool* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***

Retorna um ponteiro para o pool criado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK.

Se os argumentos forem inválidos, o método retornará D3DERR \_ INVALIDCALL.

Se o método falhar, o valor de retorno será E \_ falhará.

## <a name="remarks"></a>Comentários

Para efeitos em um pool, os parâmetros compartilhados com o mesmo nome compartilham valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de efeito](dx9-graphics-reference-effects-functions.md)
</dt> </dl>

 

 




