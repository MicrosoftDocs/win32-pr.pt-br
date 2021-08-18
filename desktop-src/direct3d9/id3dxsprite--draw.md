---
description: Adiciona um sprite à lista de sprites em lote.
ms.assetid: 8f5c43a2-68dd-44a9-be2f-f76d9fa2d900
title: Método ID3DXSprite::D raw (D3dx9core.h)
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
ms.openlocfilehash: d453a2e03538b7601b5f73033a4749430e8812ef317a90816cac220e61695279
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747366"
---
# <a name="id3dxspritedraw-method"></a>Método ID3DXSprite::D raw

Adiciona um sprite à lista de sprites em lote.

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

*pTexture* \[ Em\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Ponteiro para uma interface [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa a textura de sprite.

</dd> <dt>

*pSrcRect* \[ Em\]
</dt> <dd>

Tipo: **const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

Ponteiro para uma [**estrutura RECT**](/previous-versions//dd162897(v=vs.85)) que indica a parte da textura de origem a ser usada para o sprite. Se esse parâmetro for **NULL,** a imagem de origem inteira será usada para o sprite.

</dd> <dt>

*pCenter* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para um [**vetor D3DXVECTOR3**](d3dxvector3.md) que identifica o centro do sprite. Se esse argumento for **NULL,** o ponto (0,0,0) será usado, que é o canto superior esquerdo.

</dd> <dt>

*pPosition* \[ Em\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Ponteiro para um [**vetor D3DXVECTOR3**](d3dxvector3.md) que identifica a posição do sprite. Se esse argumento for **NULL,** o ponto (0,0,0) será usado, que é o canto superior esquerdo.

</dd> <dt>

*Cor* \[ Em\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

[**Tipo D3DCOLOR.**](d3dcolor.md) A cor e os canais alfa são modulares por esse valor. Um valor de 0xFFFFFFFF mantém a cor de origem original e os dados alfa. Use a [**macro D3DCOLOR \_ RGBA**](d3dcolor-rgba.md) para ajudar a gerar essa cor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se o método for bem-sucedido, o valor de retorno será S \_ OK. Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentários

Para dimensionar, girar ou converter um sprite, chame [**ID3DXSprite::SetTransform**](id3dxsprite--settransform.md) com uma matriz que contém os valores de escala, rotação e tradução (SRT), antes de chamar ID3DXSprite::D raw. Para obter informações sobre como definir valores de SRT em uma matriz, consulte [Matriz Transforms](transforms.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> <dt>

[**ID3DXSprite::GetTransform**](id3dxsprite--gettransform.md)
</dt> </dl>

 

 
