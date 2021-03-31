---
description: Retorna uma descrição do conteúdo original de um arquivo de imagem.
ms.assetid: d6cbd5b7-642e-43ce-a2ed-11a400c5bdc1
title: Estrutura de D3DXIMAGE_INFO (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMAGE_INFO
api_type:
- HeaderDef
api_location:
- d3dx9tex.h
ms.openlocfilehash: 6ec152dc56dcea3a718cf5cd42fb351d4fddf852
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664001"
---
# <a name="d3dximage_info-structure"></a>Estrutura de informações do D3DXIMAGE \_

Retorna uma descrição do conteúdo original de um arquivo de imagem.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DXIMAGE_INFO {
  UINT                 Width;
  UINT                 Height;
  UINT                 Depth;
  UINT                 MipLevels;
  D3DFORMAT            Format;
  D3DRESOURCETYPE      ResourceType;
  D3DXIMAGE_FILEFORMAT ImageFileFormat;
} D3DXIMAGE_INFO, *LPD3DXIMAGE_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**Largura**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Largura da imagem original em pixels.

</dd> <dt>

**Altura**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Altura da imagem original em pixels.

</dd> <dt>

**Profundidade**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Profundidade da imagem original em pixels.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de níveis de MIP na imagem original.

</dd> <dt>

**Formato**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Um valor do tipo enumerado [D3DFORMAT](d3dformat.md) que melhor descreve os dados na imagem original.

</dd> <dt>

**ResourceType**
</dt> <dd>

Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Representa o tipo da textura armazenada no arquivo. Ele é D3DRTYPE \_ Texture, D3DRTYPE \_ VOLUMETEXTURE ou D3DRTYPE \_ CubeTexture.

</dd> <dt>

**ImageFileFormat**
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ FileFormat**](./d3dximage-fileformat.md)**

</dd> <dd>

Representa o formato do arquivo de imagem.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx9tex. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
