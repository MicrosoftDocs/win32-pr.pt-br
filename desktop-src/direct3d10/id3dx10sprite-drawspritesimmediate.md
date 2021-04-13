---
description: Desenhe uma matriz de sprites.
ms.assetid: 3fcc7705-0d59-450e-b137-c9cb7ec6b1ea
title: 'ID3DX10Sprite: método rawSpritesImmediate de:D (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesImmediate
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7fa4012f5f589c7bc0d1f789599da142194f6e08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298873"
---
# <a name="id3dx10spritedrawspritesimmediate-method"></a>ID3DX10Sprite: método rawSpritesImmediate de:D

Desenhe uma matriz de sprites. Isso enviará imediatamente os sprites para o dispositivo para renderização, que é diferente de [**ID3DX10Sprite::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md) , que adiciona apenas uma matriz de sprites a um lote de sprites a serem renderizados quando [**ID3DX10Sprite:: flush**](id3dx10sprite-flush.md) é chamado. Esse método Draw é mais útil ao desenhar um grande número de sprites que já foram classificados na CPU (ou não precisam ser classificados), como em um sistema de partículas. Isso deve ser chamado entre chamadas para [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) e [**ID3DX10Sprite:: End**](id3dx10sprite-end.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DrawSpritesImmediate(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites,
  [in] UINT          cbSprite,
  [in] UINT          flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSprites* \[ no\]
</dt> <dd>

Tipo: **[ **D3DX10 \_ Sprite**](d3dx10-sprite.md)\***

A matriz de sprites a ser desenhada. Confira [**D3DX10 \_ Sprite**](d3dx10-sprite.md).

</dd> <dt>

*cSprites* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O número de sprites em pSprites.

</dd> <dt>

*cbSprite* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O tamanho da estrutura Sprite que você está passando para pSprites. Passar em 0 é o equivalente a passar em sizeof (D3DX10 \_ Sprite).

</dd> <dt>

*sinalizadores* \[ de no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Reservado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

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

 

 
