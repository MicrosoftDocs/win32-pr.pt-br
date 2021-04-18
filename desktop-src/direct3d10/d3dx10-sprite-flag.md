---
description: 'Sinalizadores de Sprite que dizem ao comportamento da API de desenho de Sprite. Eles são passados em ID3DX10Sprite:: Begin.'
ms.assetid: 734096e6-1482-479c-b287-a77a4695487c
title: Enumeração de D3DX10_SPRITE_FLAG (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SPRITE_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 21ba4f035b43b1a002b014909fb4d0a02a64d1e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105790424"
---
# <a name="d3dx10_sprite_flag-enumeration"></a>\_Enumeração de \_ sinalizador Sprite D3DX10

Sinalizadores de Sprite que dizem ao comportamento da API de desenho de Sprite. Eles são passados em [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md).

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX10_SPRITE_FLAG { 
  D3DX10_SPRITE_SORT_TEXTURE              = 0x01,
  D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT  = 0x02,
  D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK  = 0x04,
  D3DX10_SPRITE_SAVE_STATE                = 0x08,
  D3DX10_SPRITE_ADDREF_TEXTURES           = 0x10
} D3DX10_SPRITE_FLAG, *LPD3DX10_SPRITE_FLAG;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_SPRITE_SORT_TEXTURE"></span><span id="d3dx10_sprite_sort_texture"></span>**\_Textura de \_ classificação de Sprite D3DX10 \_**
</dt> <dd>

Classifique os sprites por textura antes da renderização para que, quando houver muitos sprites com a mesma textura que textura de todos os sprites sejam renderizados ao mesmo tempo, melhorando o desempenho.

</dd> <dt>

<span id="D3DX10_SPRITE_SORT_DEPTH_BACK_TO_FRONT"></span><span id="d3dx10_sprite_sort_depth_back_to_front"></span>**D3DX10 \_ Sprite \_ classificar \_ profundidade \_ \_ de volta para \_ frente**
</dt> <dd>

Classifique os sprites de volta para frente para que os mais distantes da câmera sejam desenhados primeiro.

</dd> <dt>

<span id="D3DX10_SPRITE_SORT_DEPTH_FRONT_TO_BACK"></span><span id="d3dx10_sprite_sort_depth_front_to_back"></span>**D3DX10 \_ Sprite \_ classificar \_ profundidade \_ \_ de \_ fundo para trás**
</dt> <dd>

Classifique os sprites de frente para trás para que os mais próximos da câmera sejam desenhados primeiro.

</dd> <dt>

<span id="D3DX10_SPRITE_SAVE_STATE"></span><span id="d3dx10_sprite_save_state"></span>**D3DX10 \_ Sprite \_ Salvar \_ estado**
</dt> <dd>

Salva o estado para que quando [**ID3DX10Sprite:: End**](id3dx10sprite-end.md) for chamado, ele irá restaurar o estado para o caminho anterior a [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) foi chamado.

</dd> <dt>

<span id="D3DX10_SPRITE_ADDREF_TEXTURES"></span><span id="d3dx10_sprite_addref_textures"></span>**\_Texturas do D3DX10 Sprite \_ ADDREF \_**
</dt> <dd>

Chama AddRef em todas as texturas quando elas são passadas para [**ID3DX10Sprite::D rawspritesbuffered**](id3dx10sprite-drawspritesbuffered.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Após a conclusão de uma classificação de front-to-back ou de trás para frente, ela fará automaticamente uma classificação secundária por textura. Isso é útil quando há muitos sprites com a mesma textura no mesmo plano, como ao desenhar a interface do usuário em um jogo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




