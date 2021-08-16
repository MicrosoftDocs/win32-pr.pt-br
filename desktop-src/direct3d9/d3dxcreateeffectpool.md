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
ms.openlocfilehash: 55df5e579b724a26e30223a0a0df7ffa815bda5a64b6f7d7e7e2c2c7f02f2fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804572"
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

## <a name="return-value"></a>Valor retornado

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

 

 




