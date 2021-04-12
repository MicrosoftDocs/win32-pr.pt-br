---
description: Retorna uma descrição do conteúdo original de um arquivo de imagem.
ms.assetid: 40d89166-cc11-490d-867c-ae5db23a0784
title: Estrutura de D3DX10_IMAGE_INFO (D3DX10. h)
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
ms.openlocfilehash: bf240296610c083e0d042d187ae29054461193a8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298537"
---
# <a name="d3dx10_image_info-structure"></a>Estrutura de informações de \_ imagem D3DX10 \_

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

**ArraySize**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Tamanho da matriz de textura. As *matrizes* serão 1 para uma única imagem.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número de níveis de mipmap na imagem original.

</dd> <dt>

**MiscFlags**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Propriedades de recurso diversas ( [**consulte \_ \_ \_ sinalizador d3d10 do recurso**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).

</dd> <dt>

**Formato**
</dt> <dd>

Tipo: **[ **\_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Um valor do tipo enumerado de [**\_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) que melhor descreve os dados na imagem original.

</dd> <dt>

**ResourceDimension**
</dt> <dd>

Tipo: **[ **d3d10 \_ \_ dimensão de recurso**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension)**

</dd> <dd>

Representa o tipo da textura armazenada no arquivo. Consulte [**d3d10 \_ Resource \_ Dimension**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_dimension).

</dd> <dt>

**ImageFileFormat**
</dt> <dd>

Tipo: **[ **\_ formato de \_ arquivo \_ de imagem D3DX10**](d3dx10-image-file-format.md)**

</dd> <dd>

Representa o formato do arquivo de imagem. Consulte [**\_ formato de \_ arquivo \_ de imagem D3DX10**](d3dx10-image-file-format.md).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
