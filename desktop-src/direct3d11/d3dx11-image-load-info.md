---
title: D3DX11_IMAGE_LOAD_INFO estrutura (D3DX11tex.h)
description: Observação A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store. Opcionalmente, forneça informações para APIs do carregador de textura para controlar como as texturas são carregadas. | D3DX11_IMAGE_LOAD_INFO estrutura (D3DX11tex.h)
ms.assetid: 6cd2f590-4e15-41e6-9f04-cd91eeb082db
keywords:
- D3DX11_IMAGE_LOAD_INFO estrutura Direct3D 11
- LPD3DX11_IMAGE_LOAD_INFO ponteiro de estrutura Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c45bc3b9ec948c869b121190f52435a257141f1e5a6e9f36c347ab29bafb5522
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536853"
---
# <a name="d3dx11_image_load_info-structure"></a>Estrutura D3DX11 \_ IMAGE \_ LOAD \_ INFO

> [!Note]  
> A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para Windows 8 e não tem suporte para aplicativos da Windows Store.

 

Opcionalmente, forneça informações para APIs do carregador de textura para controlar como as texturas são carregadas. Um valor de D3DX11 DEFAULT para qualquer um desses parâmetros fará com que o D3DX use automaticamente o valor \_ do arquivo de origem.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct D3DX11_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D11_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX11_IMAGE_INFO *pSrcInfo;
} D3DX11_IMAGE_LOAD_INFO, *LPD3DX11_IMAGE_LOAD_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**Largura**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

A largura de destino da textura. Se a largura real da textura for maior ou menor que esse valor, a textura será dimensionada ou reduzida para se ajustar a essa largura de destino.

</dd> <dt>

**Altura**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

A altura de destino da textura. Se a altura real da textura for maior ou menor que esse valor, a textura será dimensionada para cima ou para baixo para se ajustar a essa altura de destino.

</dd> <dt>

**Profundidade**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

A profundidade da textura. Isso se aplica somente a texturas de volume.

</dd> <dt>

**FirstMipLevel**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

O nível de mipmap de resolução mais alta da textura. Se isso for maior que 0, depois que a textura for carregada, FirstMipLevel será mapeado para o nível 0 do mipmap.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

O número máximo de níveis de mipmap na textura. Consulte os comentários em [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv). Usar 0 ou D3DX11 \_ DEFAULT fará com que uma cadeia mipmap completa seja criada.

</dd> <dt>

**Usage**
</dt> <dd>

Tipo: **[ **D3D11 \_ USAGE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**

</dd> <dd>

A maneira como o recurso de textura deve ser usado. Consulte [**D3D11 \_ USAGE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).

</dd> <dt>

**BindFlags**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Os estágios de pipeline aos que a textura terá permissão para se vincular. Consulte [**SINALIZADOR DE \_ VINCULAÇÃO \_ D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag).

</dd> <dt>

**CpuAccessFlags**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

As permissões de acesso que a CPU terá para o recurso de textura. Consulte [**SINALIZADOR DE ACESSO À CPU D3D11 \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).

</dd> <dt>

**MiscFlags**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Propriedades de recursos diversos (consulte [**D3D11 \_ RESOURCE \_ MISC \_ FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)).

</dd> <dt>

**Formato**
</dt> <dd>

Tipo: **[ **FORMATO \_ DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Uma [**enumeração DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) indicando o formato em que a textura estará depois que ela for carregada.

</dd> <dt>

**Filter**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Filtre a textura usando o filtro especificado (somente ao resampling). Consulte [**SINALIZADOR DE FILTRO D3DX11 \_ \_**](d3dx11-filter-flag.md).

</dd> <dt>

**MipFilter**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Filtre os níveis de mip de textura usando o filtro especificado (somente se estiver gerando mipmaps). Os valores válidos são D3DX11 \_ FILTER \_ NONE, D3DX11 \_ FILTER \_ POINT, D3DX11 \_ FILTER LINEAR ou \_ D3DX11 \_ FILTER \_ TRIANGLE. Consulte [**SINALIZADOR DE FILTRO D3DX11 \_ \_**](d3dx11-filter-flag.md).

</dd> <dt>

**pSrcInfo**
</dt> <dd>

Tipo: **[ **D3DX11 \_ IMAGE \_ INFO**](d3dx11-image-info.md)\***

</dd> <dd>

Informações sobre a imagem original. Consulte [**INFORMAÇÕES DE IMAGEM D3DX11 \_ \_**](d3dx11-image-info.md). Pode ser obtido com [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)ou [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao inicializar a estrutura, você pode definir qualquer membro como D3DX11 DEFAULT e D3DX o inicializa com um valor padrão da textura de origem quando a textura \_ é carregada.

Essa estrutura pode ser usada por APIs que:

-   Crie recursos, como [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) e [**D3DX11CreateShaderResourceViewFromFile**](d3dx11createshaderresourceviewfromfile.md).
-   Crie processadores de dados, como [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) ou [**D3DX11CreateAsyncShaderResourceViewProcessor**](d3dx11createasyncshaderresourceviewprocessor.md).

Os valores padrão são:


```
    Width = D3DX11_DEFAULT;
    Height = D3DX11_DEFAULT;
    Depth = D3DX11_DEFAULT;
    FirstMipLevel = D3DX11_DEFAULT;
    MipLevels = D3DX11_DEFAULT;
    Usage = (D3D11_USAGE) D3DX11_DEFAULT;
    BindFlags = D3DX11_DEFAULT;
    CpuAccessFlags = D3DX11_DEFAULT;
    MiscFlags = D3DX11_DEFAULT;
    Format = DXGI_FORMAT_FROM_FILE;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
    pSrcInfo = NULL;
```



Aqui está um breve exemplo que usa essa estrutura para fornecer o formato de pixel ao carregar uma textura. Para ver o código completo, consulte HDRFormats10.cpp no [Exemplo de HDRToneMappingCS11](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx).


```
ID3D11ShaderResourceView* pCubeRV = NULL;
WCHAR strPath[MAX_PATH];
D3DX11_IMAGE_LOAD_INFO LoadInfo;

    DXUTFindDXSDKMediaFileCch( strPath, MAX_PATH, 
        L"Light Probes\\uffizi_cross.dds" );

    LoadInfo.Format = DXGI_FORMAT_R16G16B16A16_FLOAT;

    hr = D3DX11CreateShaderResourceViewFromFile( pd3dDevice, strPath, 
        &LoadInfo, NULL, &pCubeRV, NULL );
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas D3DX](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

