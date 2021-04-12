---
description: Prepare um dispositivo para desenhar sprites.
ms.assetid: cffe5ac3-eeee-4ece-afcc-04a476b75863
title: 'Método ID3DX10Sprite:: Begin (D3DX10. h)'
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
ms.openlocfilehash: ede2995f72eb1200e68f035119643a362e15701e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173094"
---
# <a name="id3dx10spritebegin-method"></a>Método ID3DX10Sprite:: Begin

Prepare um dispositivo para desenhar sprites.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Begin(
  [in] UINT flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sinalizadores* \[ de no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Sinalizadores que controlam como os sprites serão desenhados. Consulte [**\_ \_ sinalizador de Sprite D3DX10**](d3dx10-sprite-flag.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentários

Cada chamada para BEGIN deve ser correspondida com uma chamada para [**ID3DX10Sprite:: End**](id3dx10sprite-end.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
