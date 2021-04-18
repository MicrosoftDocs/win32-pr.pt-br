---
description: Crie um sprite para desenhar uma textura 2D. Observação em vez de usar essa função, recomendamos que você use Direct2D e a biblioteca DirectXTK, SpriteBatch Class.
ms.assetid: 64efb8e4-da0b-4e67-874a-e0bb0083961c
title: Função D3DX10CreateSprite (D3DX10. h)
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
ms.openlocfilehash: cf40e303cb616f35ea5cd3526c263e3bd12ae428
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105789342"
---
# <a name="d3dx10createsprite-function"></a>Função D3DX10CreateSprite

Crie um sprite para desenhar uma textura 2D.

> [!Note]  
> Em vez de usar essa função, recomendamos que você use [Direct2D](../direct2d/direct2d-portal.md) e a biblioteca [DirectXTK](https://github.com/Microsoft/DirectXTK) , **SpriteBatch** Class.

 

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

*pDevice* \[ no\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Um ponteiro para o dispositivo (consulte a [**interface ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) que irá desenhar o sprite.

</dd> <dt>

*cDeviceBufferSize* \[ no\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

O tamanho do buffer de vértice, em número de sprites, que será enviado ao dispositivo quando [**ID3DX10Sprite:: flush**](id3dx10sprite-flush.md) ou [**ID3DX10Sprite::D rawspritesimmediate**](id3dx10sprite-drawspritesimmediate.md) for chamado. Isso deve ser um pequeno número se você souber que estará renderizando um pequeno número de sprites por vez (para economizar memória) e um grande número se você souber que será renderizado um grande número de sprites por vez. O valor máximo é 4096. Se 0 for especificado, o tamanho do buffer de vértice será definido automaticamente como 4096.

</dd> <dt>

*ppSprite* \[ fora\]
</dt> <dd>

Tipo: **[ **LPD3DX10SPRITE**](id3dx10sprite.md)\***

O endereço de um ponteiro para uma interface Sprite (consulte a [**interface ID3DX10Sprite**](id3dx10sprite.md)).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se a função for bem sucedido, o valor de retorno será S \_ OK. Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções de Uso Geral](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
