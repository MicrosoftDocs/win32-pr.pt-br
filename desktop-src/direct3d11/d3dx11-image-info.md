---
title: Estrutura de D3DX11_IMAGE_INFO (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Opcionalmente, forneça informações para APIs do carregador de textura para controlar como as texturas são carregadas. | Estrutura de D3DX11_IMAGE_INFO (D3DX11tex. h)
ms.assetid: 981f4f1d-7609-416a-8f92-c7223d8b2773
keywords:
- Estrutura D3DX11_IMAGE_INFO Direct3D 11
- Ponteiro de estrutura LPD3DX11_IMAGE_INFO Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 927967f8e76d0147ccc264bcbdd773191a170ae7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968693"
---
# <a name="d3dx11_image_info-structure"></a>Estrutura de informações de \_ imagem D3DX11 \_

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.

 

Opcionalmente, forneça informações para APIs do carregador de textura para controlar como as texturas são carregadas. Um valor de D3DX11 \_ padrão para qualquer um desses parâmetros fará com que o D3DX use automaticamente o valor do arquivo de origem.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DX11_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D11_RESOURCE_DIMENSION ResourceDimension;
  D3DX11_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX11_IMAGE_INFO, *LPD3DX11_IMAGE_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**Largura**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

A largura de destino da textura. Se a largura real da textura for maior ou menor que esse valor, a textura será dimensionada para cima ou para baixo para se ajustar a essa largura de destino.

</dd> <dt>

**Altura**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

A altura de destino da textura. Se a altura real da textura for maior ou menor que esse valor, a textura será dimensionada para cima ou para baixo para se ajustar a essa altura de destino.

</dd> <dt>

**Profundidade**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

A profundidade da textura. Isso se aplica somente a texturas de volume.

</dd> <dt>

**ArraySize**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

O número de elementos na matriz.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

O número máximo de níveis de mipmap na textura. Consulte os comentários em [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv). Usar 0 ou D3DX11 \_ padrão fará com que uma cadeia de mipmap completa seja criada.

</dd> <dt>

**MiscFlags**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Diversas propriedades de recurso especificadas com um sinalizador de [**\_ \_ \_ sinalizador variado de recurso D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) .

</dd> <dt>

**Formato**
</dt> <dd>

Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Uma enumeração de [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) especificando o formato em que a textura estará depois de ser carregada.

</dd> <dt>

**ResourceDimension**
</dt> <dd>

Tipo: **[ **D3D11 \_ \_ dimensão de recurso**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**

</dd> <dd>

Um valor de [**\_ \_ dimensão de recurso D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) , que identifica o tipo de recurso.

</dd> <dt>

**ImageFileFormat**
</dt> <dd>

Tipo: **[ **\_ formato de \_ arquivo \_ de imagem D3DX11**](d3dx11-image-file-format.md)**

</dd> <dd>

Um valor de [**\_ formato de \_ arquivo \_ de imagem D3DX11**](d3dx11-image-file-format.md) , que identifica o formato de imagem.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é usada por métodos como: [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)ou [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

