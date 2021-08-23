---
description: Define informações de posição, textura e cor sobre um Sprite.
ms.assetid: 4b8d1ed1-75d5-418c-b809-410c6a44d425
title: Estrutura de D3DX10_SPRITE (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SPRITE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: ec8b220d55d3ac55d2a8b68fa3b95398a395611da150235d03314114055214e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753506"
---
# <a name="d3dx10_sprite-structure"></a>\_Estrutura de Sprite D3DX10

Define informações de posição, textura e cor sobre um Sprite.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DX10_SPRITE {
  D3DXMATRIX               matWorld;
  D3DXVECTOR2              TexCoord;
  D3DXVECTOR2              TexSize;
  D3DXCOLOR                ColorModulate;
  ID3D10ShaderResourceView *pTexture;
  UINT                     TextureIndex;
} D3DX10_SPRITE;
```



## <a name="members"></a>Membros

<dl> <dt>

**matWorld**
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)**

</dd> <dd>

A transformação modelo-mundo do Sprite. Isso define a posição e a orientação do sprite no espaço do mundo.

</dd> <dt>

**TexCoord**
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**

</dd> <dd>

Deslocamento do canto superior esquerdo da textura que indica onde a imagem Sprite deve começar na textura. **TexCoord** está em coordenadas de textura.

</dd> <dt>

**TexSize**
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)**

</dd> <dd>

Um vetor que contém a largura e a altura do sprite em coordenadas de textura.

</dd> <dt>

**ColorModulate**
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](../direct3d9/d3dxcolor.md)**

</dd> <dd>

Uma cor que será multiplicada pela cor do pixel antes da renderização.

</dd> <dt>

**pTexture**
</dt> <dd>

Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\***

</dd> <dd>

Ponteiro para uma exibição de recurso de sombreador que representa a textura de Sprite. Consulte a [**interface ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview).

</dd> <dt>

**TextureIndex**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

O índice da textura. Se pTexture não representar uma matriz de textura, isso deverá ser 0.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
