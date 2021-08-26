---
description: D3DX10_IMAGE_INFO estrutura - retorna uma descrição do conteúdo original de um arquivo de imagem.
ms.assetid: 40d89166-cc11-490d-867c-ae5db23a0784
title: D3DX10_IMAGE_INFO (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_INFO
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: bf3aa2eeb3e908a76e05588940927fff53dd1583c937d95a1c862f6021bd630f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989516"
---
# <a name="d3dx10_image_info-structure"></a>Estrutura D3DX10 \_ IMAGE \_ INFO

Retorna uma descrição do conteúdo original de um arquivo de imagem.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DX10_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D10_RESOURCE_DIMENSION ResourceDimension;
  D3DX10_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX10_IMAGE_INFO, *LPD3DX10_IMAGE_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**Largura**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Largura da imagem original em pixels.

</dd> <dt>

**Altura**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Altura da imagem original em pixels.

</dd> <dt>

**Profundidade**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Profundidade da imagem original em pixels.

</dd> <dt>

**ArraySize**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamanho da matriz de textura. *ArraySize* será 1 para uma única imagem.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de níveis de mipmap na imagem original.

</dd> <dt>

**MiscFlags**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Propriedades de recursos diversos (consulte [**D3D10 \_ RESOURCE \_ MISC \_ FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).

</dd> <dt>

**Formato**
</dt> <dd>

Tipo: **[ **FORMATO \_ DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Um valor do tipo enumerado [**DXGI \_ FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) que descreve mais de perto os dados na imagem original.

</dd> <dt>

**ResourceDimension**
</dt> <dd>

Tipo: **[ **D3D10 \_ RESOURCE \_ DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**

</dd> <dd>

Representa o tipo da textura armazenada no arquivo. Consulte [**D3D10 \_ RESOURCE \_ DIMENSION**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).

</dd> <dt>

**ImageFileFormat**
</dt> <dd>

Tipo: **[ **FORMATO DE ARQUIVO DE IMAGEM D3DX10 \_ \_ \_**](d3dx10-image-file-format.md)**

</dd> <dd>

Representa o formato do arquivo de imagem. Consulte [**FORMATO DE ARQUIVO DE IMAGEM D3DX10 \_ \_ \_**](d3dx10-image-file-format.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
