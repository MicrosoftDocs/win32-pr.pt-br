---
title: Estrutura de DDS_HEADER_DXT10 (DDS. h)
description: Extensão de cabeçalho DDS para manipular matrizes de recursos, formatos de pixel DXGI que não mapeiam para as estruturas de formato de pixel do Microsoft DirectDraw herdado e metadados adicionais.
ms.assetid: 502d6943-8f25-446c-b990-8276f862c195
keywords:
- DDS_HEADER_DXT10 de estrutura DDS
topic_type:
- apiref
api_name:
- DDS_HEADER_DXT10
api_location:
- Dds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da95b65739922861002ab134d33f276adabd19c29d14fdea6432616b6c5edc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289783"
---
# <a name="dds_header_dxt10-structure"></a>Estrutura de DXT10 de \_ cabeçalho DDS \_

Extensão de cabeçalho DDS para manipular matrizes de recursos, formatos de pixel DXGI que não mapeiam para as estruturas de formato de pixel do Microsoft DirectDraw herdado e metadados adicionais.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DXGI_FORMAT              dxgiFormat;
  D3D10_RESOURCE_DIMENSION resourceDimension;
  UINT                     miscFlag;
  UINT                     arraySize;
  UINT                     miscFlags2;
} DDS_HEADER_DXT10;
```



## <a name="members"></a>Membros

<dl> <dt>

**dxgiFormat**
</dt> <dd>

Tipo: **[ **\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

O formato de pixel de superfície (consulte o [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).

</dd> <dt>

**resourceDimension**
</dt> <dd>

Tipo: **[ **d3d10 \_ \_ dimensão de recurso**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension)**

</dd> <dd>

Identifica o tipo de recurso. Os valores a seguir para esse membro são um subconjunto dos valores na [**\_ \_ dimensão de recurso d3d10**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_dimension) ou enumeração de [**\_ \_ dimensão de recurso D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_dimension) :



| Type                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                            | Valor |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| DDS \_ Dimension \_ TEXTURE1D ( \_ TEXTURE1D de dimensão de recurso d3d10 \_ \_ ) | O recurso é uma [textura 1D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types). O membro **dwWidth** do [**\_ cabeçalho DDS**](dds-header.md) especifica o tamanho da textura. Normalmente, você define o membro **dwHeight** do **\_ cabeçalho DDS** como 1; você também deve definir o \_ sinalizador de altura DDSD no membro **dwFlags** do **\_ cabeçalho DDS**.                      | 2     |
| DDS \_ Dimension \_ TEXTURE2D ( \_ TEXTURE2D de dimensão de recurso d3d10 \_ \_ ) | O recurso é uma [textura 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) com uma área especificada pelos membros **dwWidth** e **dwHeight** do [**\_ cabeçalho DDS**](dds-header.md). Você também pode usar esse tipo para identificar uma textura de mapa de cubo. Para obter mais informações sobre como identificar uma textura de mapa de cubo, consulte **miscFlag** e **Members** . | 3     |
| DDS \_ Dimension \_ TEXTURE3D ( \_ TEXTURE3D de dimensão de recurso d3d10 \_ \_ ) | Recurso é uma [textura 3D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) com um volume especificado pelos membros **dwWidth**, **DwHeight** e **dwDepth** do [**\_ cabeçalho DDS**](dds-header.md). Você também deve definir o \_ sinalizador de profundidade DDSD no membro **dwFlags** do **\_ cabeçalho do DDS**.                                                                   | 4     |



 

</dd> <dt>

**miscFlag**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Identifica outras opções menos comuns para recursos. O valor a seguir para esse membro é um subconjunto dos valores no [**\_ \_ \_ sinalizador diD3D10 do recurso**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_resource_misc_flag) ou enumeração de [**\_ \_ \_ sinalizador variado do recurso D3D11**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag) :



| Type                             | Descrição                                                                                                  | Valor |
|----------------------------------|--------------------------------------------------------------------------------------------------------------|-------|
| \_TEXTURECUBE de recursos de DDS \_ \_ | Indica que uma [textura 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) é uma textura de mapa de cubo. | 0x4   |



 

</dd> <dt>

**arraySize**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

O número de elementos na matriz.

Para uma [textura 2D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) que também é uma textura de mapa de cubo, esse número representa o número de cubos. Esse número é o mesmo que o número no membro **NumCubes** de [**d3d10 \_ TEXCUBE \_ array \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1) ou [**D3D11 \_ TEXCUBE \_ array \_ SRV**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_texcube_array_srv)). Nesse caso, o arquivo **DDS contém** \* 6 texturas 2D. Para obter mais informações sobre esse caso, consulte a descrição de **miscFlag** .

Para uma [textura 3D](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types), você deve definir esse número como 1.

</dd> <dt>

**miscFlags2**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Contém metadados adicionais (anteriormente reservado). Os três bits inferiores indicam o modo alfa do recurso associado. Os 29 bits superiores são reservados e geralmente são 0.



| Type                            | Descrição                                                                                                                              | Valor |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|-------|
| \_modo alfa do DDS \_ \_ desconhecido       | O conteúdo do canal alfa é desconhecido. Esse é o valor para arquivos herdados, que normalmente é considerado "reto" Alfa.                 | 0x0   |
| \_modo alfa do DDS \_ \_ reto      | Todo o conteúdo do canal alfa é presumido usar alfa reto.                                                                             | 0x1   |
| modo alfa do DDS pré- \_ \_ \_ multiplicado | Qualquer conteúdo de canal alfa está usando alfa precalculado. Os únicos formatos de arquivo herdados que indicam essas informações são ' DX2 ' e ' DX4 '. | 0x2   |
| \_modo alfa do DDS \_ \_ opaco        | Qualquer conteúdo do canal alfa é definido como totalmente opaco.                                                                                    | 0x3   |
| \_modo alfa do DDS \_ \_ personalizado        | Qualquer conteúdo do canal alfa está sendo usado como um 4º Channel e não se destina a representar a transparência (reta ou premultiplicada).      | 0x4   |



 

> [!Note]  
> As bibliotecas de utilitários herdadas D3DX 10 e [D3DX 11](/windows/desktop/direct3d11/d3d11-graphics-reference-d3dx11) falharão ao carregar qualquer. O arquivo DDS com **miscFlags2** não é igual a zero.

 

</dd> </dl>

## <a name="remarks"></a>Comentários

Use essa estrutura junto com um [**\_ cabeçalho DDS**](dds-header.md) para armazenar uma matriz de recursos em um arquivo DDS. Para obter mais informações, consulte [matrizes de textura](dx-graphics-dds-pguide.md).

Esse cabeçalho estará presente se o membro **dwFourCC** da estrutura [**de \_ PIXELFORMAT do DDS**](dds-pixelformat.md) estiver definido como ' DX10 '.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DDS. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência para DDS](dx-graphics-dds-reference.md)
</dt> </dl>

 

