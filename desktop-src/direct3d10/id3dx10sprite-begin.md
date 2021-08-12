---
description: Prepare um dispositivo para desenhar sprites.
ms.assetid: cffe5ac3-eeee-4ece-afcc-04a476b75863
title: Método ID3DX10Sprite::Begin (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Begin
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e23ff3e4b8be62ac97f2874aa398770936bd84ab1c330c94efb87146046db847
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302401"
---
# <a name="id3dx10spritebegin-method"></a>Método ID3DX10Sprite::Begin

Prepare um dispositivo para desenhar sprites.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Begin(
  [in] UINT flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sinalizadores* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Sinalizadores que controlam como os sprites serão desenhados. Consulte [**D3DX10 \_ SPRITE \_ FLAG**](d3dx10-sprite-flag.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Cada chamada para Begin deve ser corresponder a uma chamada para [**ID3DX10Sprite::End.**](id3dx10sprite-end.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
