---
description: Adiciona um Sprite à lista de sprites em lote.
ms.assetid: 8f5c43a2-68dd-44a9-be2f-f76d9fa2d900
title: 'ID3DXSprite: método RAW de:D (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9cba7b12c55e7ab9f5f939347a8b500ec4965f75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761629"
---
# <a name="id3dxspritedraw-method"></a>ID3DXSprite: método RAW de:D

Adiciona um Sprite à lista de sprites em lote.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Draw(
  [in]       LPDIRECT3DTEXTURE9 pTexture,
  [in] const RECT               *pSrcRect,
  [in] const D3DXVECTOR3        *pCenter,
  [in] const D3DXVECTOR3        *pPosition,
  [in]       D3DCOLOR           Color
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pTexture* \[ no\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa a textura Sprite.

</dd> <dt>

*pSrcRect* \[ no\]
</dt> <dd>

Tipo: **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***

Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que indica a parte da textura de origem a ser usada para o sprite. Se esse parâmetro for **nulo**, a imagem de origem inteira será usada para o sprite.

</dd> <dt>

*pCenter* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para um vetor [**D3DXVECTOR3**](d3dxvector3.md) que identifica o centro do Sprite. Se esse argumento for **nulo**, o ponto (0, 0, 0) será usado, que é o canto superior esquerdo.

</dd> <dt>

*pPosition* \[ no\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para um vetor [**D3DXVECTOR3**](d3dxvector3.md) que identifica a posição do Sprite. Se esse argumento for **nulo**, o ponto (0, 0, 0) será usado, que é o canto superior esquerdo.

</dd> <dt>

*Cor* \[ do no\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

Tipo de [**D3DCOLOR**](d3dcolor.md) . Os canais de cor e alfa são modulados por esse valor. Um valor de 0xFFFFFFFF mantém a cor da fonte original e os dados alfa. Use a [**macro \_ RGBA D3DCOLOR**](d3dcolor-rgba.md) para ajudar a gerar essa cor.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

Para dimensionar, girar ou traduzir um Sprite, chame [**ID3DXSprite:: SetTransform**](id3dxsprite--settransform.md) com uma matriz que contém os valores de SRT (escala, rotação e conversão), antes de chamar ID3DXSprite::D RAW. Para obter informações sobre como definir valores de SRT em uma matriz, consulte [transformações de matriz](transforms.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite:: GetTransform**](id3dxsprite--gettransform.md)
</dt> </dl>

 

 
