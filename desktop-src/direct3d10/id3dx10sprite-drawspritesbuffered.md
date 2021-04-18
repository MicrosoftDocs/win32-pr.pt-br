---
description: Adicione uma matriz de sprites ao lote de sprites a serem renderizados.
ms.assetid: e6a9f806-7244-4139-b47e-c46dfab38a31
title: 'ID3DX10Sprite: método rawSpritesBuffered de:D (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesBuffered
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72893f6a8c3cf82c67f014b4bdbb9a92453de319
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764258"
---
# <a name="id3dx10spritedrawspritesbuffered-method"></a>ID3DX10Sprite: método rawSpritesBuffered de:D

Adicione uma matriz de sprites ao lote de sprites a serem renderizados. Isso deve ser chamado entre chamadas para [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) e [**ID3DX10Sprite:: End**](id3dx10sprite-end.md)e [**ID3DX10Sprite:: flush**](id3dx10sprite-flush.md) deve ser chamado antes de end enviar todos os sprites em lote para o dispositivo para renderização. Esse método Draw é mais útil ao desenhar um pequeno número de sprites que você deseja armazenar em buffer em um lote grande, como fontes.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DrawSpritesBuffered(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites
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

 

 
