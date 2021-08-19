---
description: Desenhar uma matriz de sprites.
ms.assetid: 3fcc7705-0d59-450e-b137-c9cb7ec6b1ea
title: Método ID3DX10Sprite::D rawSpritesImmediate (D3DX10.h)
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
ms.openlocfilehash: 0a3295d64efc3f3ff05b39e0866a15fb7eed9ba2d8c580fe2c7b219d36708e02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046894"
---
# <a name="id3dx10spritedrawspritesimmediate-method"></a>Método ID3DX10Sprite::D rawSpritesImmediate

Desenhar uma matriz de sprites. Isso enviará imediatamente os sprites para o dispositivo para renderização, que é diferente de [**ID3DX10Sprite::D rawSpritesBuffered,**](id3dx10sprite-drawspritesbuffered.md) que adiciona apenas uma matriz de sprites a um lote de sprites a serem renderizados quando [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) é chamado. Esse método de desenho é mais útil ao desenhar um grande número de sprites que já foram classificação na CPU (ou não precisam ser classificação), como em um sistema de partículas. Isso deve ser chamado entre chamadas para [**ID3DX10Sprite::Begin**](id3dx10sprite-begin.md) e [**ID3DX10Sprite::End.**](id3dx10sprite-end.md)

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

*pSprites* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DX10 \_ SPRITE**](d3dx10-sprite.md)\***

A matriz de sprites a ser desenhada. Consulte [**D3DX10 \_ SPRITE**](d3dx10-sprite.md).

</dd> <dt>

*cSprites* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

O número de sprites em pSprites.

</dd> <dt>

*cbSprite* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

O tamanho da estrutura de sprite que você está passando para pSprites. Passar 0 é o equivalente a passar sizeof(D3DX10 \_ SPRITE).

</dd> <dt>

*sinalizadores* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Reservado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

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

 

 
