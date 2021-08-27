---
description: Crie um sprite para desenhar uma textura 2D. Observação Em vez de usar essa função, recomendamos que você use Direct2D biblioteca DirectXTK, classe SpriteBatch.
ms.assetid: 64efb8e4-da0b-4e67-874a-e0bb0083961c
title: Função D3DX10CreateSprite (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSprite
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6f67a0a6e0be8a3ea71ff1eef46d72b6cf080d028e7cc32f72a52db6a209cea4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118541050"
---
# <a name="d3dx10createsprite-function"></a>Função D3DX10CreateSprite

Crie um sprite para desenhar uma textura 2D.

> [!Note]  
> Em vez de usar essa função, recomendamos que você [use](../direct2d/direct2d-portal.md) Direct2D biblioteca [DirectXTK,](https://github.com/Microsoft/DirectXTK) **classe SpriteBatch.**

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT D3DX10CreateSprite(
  _In_  ID3D10Device   *pDevice,
  _In_  UINT           cDeviceBufferSize,
  _Out_ LPD3DX10SPRITE *ppSprite
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* \[ Em\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Um ponteiro para o dispositivo (consulte [**Interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) que desenhará o sprite.

</dd> <dt>

*cDeviceBufferSize* \[ Em\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

O tamanho do buffer de vértice, em número de sprites, que será enviado ao dispositivo quando [**ID3DX10Sprite::Flush**](id3dx10sprite-flush.md) ou [**ID3DX10Sprite::D rawSpritesImmediate**](id3dx10sprite-drawspritesimmediate.md) for chamado. Esse deverá ser um número pequeno se você sabe que renderizará um pequeno número de sprites por vez (para economizar memória) e um número grande se você sabe que renderizará um grande número de sprites por vez. O valor máximo é 4096. Se 0 for especificado, o tamanho do buffer de vértice será definido automaticamente como 4096.

</dd> <dt>

*ppSprite* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)\***

O endereço de um ponteiro para uma interface sprite (consulte Interface [**ID3DX10Sprite**](id3dx10sprite.md)).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem-sucedida, o valor de retorno será S \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Uso Geral funções](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
