---
description: Opcionalmente, forneça informações para APIs do carregador de textura para controlar como as texturas são carregadas. Um valor de D3DX10 \_ padrão para qualquer um desses parâmetros fará com que o D3DX use automaticamente o valor do arquivo de origem.
ms.assetid: 8325d50e-a8a9-4ee2-87e2-e60fb3699af6
title: Estrutura de D3DX10_IMAGE_LOAD_INFO (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 89e819e81c11842feaa6996e047f3cac3587792c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812374"
---
# <a name="d3dx10_image_load_info-structure"></a>\_Estrutura de \_ informações de carregamento de imagem D3DX10 \_

Opcionalmente, forneça informações para APIs do carregador de textura para controlar como as texturas são carregadas. Um valor de D3DX10 \_ padrão para qualquer um desses parâmetros fará com que o D3DX use automaticamente o valor do arquivo de origem.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DX10_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D10_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX10_IMAGE_INFO *pSrcInfo;
} D3DX10_IMAGE_LOAD_INFO, *LPD3DX10_IMAGE_LOAD_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**Largura**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

A largura de destino da textura. Se a largura real da textura for maior ou menor que esse valor, a textura será dimensionada para cima ou para baixo para se ajustar a essa largura de destino.

</dd> <dt>

**Altura**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

A altura de destino da textura. Se a altura real da textura for maior ou menor que esse valor, a textura será dimensionada para cima ou para baixo para se ajustar a essa altura de destino.

</dd> <dt>

**Profundidade**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

A profundidade da textura. Isso se aplica somente a texturas de volume.

</dd> <dt>

**FirstMipLevel**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

O nível de mipmap de resolução mais alto da textura. Se for maior que 0, depois que a textura for carregada, FirstMipLevel será mapeado para o nível de mipmap 0.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

O número máximo de níveis de mipmap que a textura terá. Usar 0 ou D3DX10 \_ padrão fará com que uma cadeia de mipmap completa seja criada.

</dd> <dt>

**Usage**
</dt> <dd>

Tipo: **[ **\_ uso de d3d10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)**

</dd> <dd>

A maneira como o recurso de textura deve ser usado. Consulte [**\_ uso de d3d10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).

</dd> <dt>

**BindFlags**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Os estágios de pipeline aos quais a textura terá permissão de associação. Consulte [**\_ \_ sinalizador de ligação d3d10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag).

</dd> <dt>

**CpuAccessFlags**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

As permissões de acesso que a CPU terá para o recurso de textura. Consulte [**\_ sinalizador de \_ acesso \_ de CPU d3d10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag).

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

O formato em que a textura estará depois de ser carregada. Consulte [**o \_ formato dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).

</dd> <dt>

**Filter**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Filtre a textura usando o filtro especificado (somente ao reamostrar). Consulte [**\_ \_ sinalizador de filtro D3DX10**](d3dx10-filter-flag.md).

</dd> <dt>

**MipFilter**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Filtre os níveis de MIP de textura usando o filtro especificado (somente se estiver gerando mipmaps). Os valores válidos são \_ filtro D3DX10 \_ nenhum, \_ ponto de filtro D3DX10 \_ , filtro de D3DX10 \_ \_ linear ou triângulo de filtro de D3DX10 \_ \_ . Consulte [**\_ \_ sinalizador de filtro D3DX10**](d3dx10-filter-flag.md).

</dd> <dt>

**pSrcInfo**
</dt> <dd>

Tipo: **[ **D3DX10 \_ Image \_ info**](d3dx10-image-info.md)\***

</dd> <dd>

Informações sobre a imagem original. Consulte [**D3DX10 \_ Image \_ info**](d3dx10-image-info.md). Pode ser obtido com [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md), [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)ou [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao inicializar a estrutura, você pode definir qualquer membro como D3DX10 \_ padrão e D3DX irá inicializá-lo com um valor padrão da textura de origem quando a textura for carregada.

Essa estrutura pode ser usada por APIs que:

-   Crie recursos, como [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) e [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md).
-   Crie processadores de dados, como [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) ou [**D3DX10CreateAsyncShaderResourceViewProcessor**](d3dx10createasyncshaderresourceviewprocessor.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
