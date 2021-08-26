---
title: Estrutura de CD3DX12_RESOURCE_DESC (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura desc de recurso D3D12 \_ .
ms.assetid: F18D41BE-8AEF-444E-AC8B-EC57C63BF083
keywords:
- Estrutura de CD3DX12_RESOURCE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c9d92953abdb0cf77a7a55f7b64341b857a111baaef0d84d4d44855b02efb2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028296"
---
# <a name="cd3dx12_resource_desc-structure"></a>\_Estrutura desc de recurso CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ \_ desc de recurso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_RESOURCE_DESC  : public D3D12_RESOURCE_DESC{
                        CD3DX12_RESOURCE_DESC();
                        explicit CD3DX12_RESOURCE_DESC(const D3D12_RESOURCE_DESC& o);
                        CD3DX12_RESOURCE_DESC(D3D12_RESOURCE_DIMENSION dimension, UINT64 alignment, UINT64 width, UINT height, UINT16 depthOrArraySize, UINT16 mipLevels, DXGI_FORMAT format, UINT sampleCount, UINT sampleQuality, D3D12_TEXTURE_LAYOUT layout, D3D12_RESOURCE_FLAGS flags);
  CD3DX12_RESOURCE_DESC static inline Buffer(const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE);
  CD3DX12_RESOURCE_DESC static inline Buffer(UINT64 width, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex1D(DXGI_FORMAT format, UINT64 width, UINT16 arraySize = 1, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex2D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 arraySize = 1, UINT16 mipLevels = 0, UINT sampleCount = 1, UINT sampleQuality = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  CD3DX12_RESOURCE_DESC static inline Tex3D(DXGI_FORMAT format, UINT64 width, UINT height, UINT16 depth, UINT16 mipLevels = 0, D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 alignment = 0);
  UINT16                inline Depth() const;
  UINT16                inline ArraySize() const;
  UINT8                 inline PlaneCount(ID3D12Device* pDevice) const;
  UINT                  inline Subresources(ID3D12Device* pDevice) const;
  UINT                  inline CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice);
                        operator const D3D12_RESOURCE_DESC&() const;
                        operator == (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
                        operator !=  (const D3D12_RESOURCE_DESC& l, const D3D12_RESOURCE_DESC& r);
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Recurso CD3DX12 \_ DESC ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de um \_ recurso CD3DX12 \_ desc.

</dd> <dt>

**recurso CD3DX12 \_ explícito \_ DESC (const D3D12 \_ recurso \_ desc& o)**
</dt> <dd>

Cria uma nova instância de um \_ recurso CD3DX12 \_ DESC, inicializada com o conteúdo de outra estrutura [**\_ \_ desc de recurso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) .

</dd> <dt>

**\_Recurso CD3DX12 \_ DESC ( \_ \_ dimensão de dimensão de recurso D3D12, alinhamento de UINT64, largura de UInt64, altura uint, UInt16 depthOrArraySize, UInt16 mipLevels, \_ formato de formato dxgi, uint SAMPLECOUNT, uint sampleQuality, D3D12 \_ \_ layout de layout de textura, D3D12 \_ flags de sinalizadores de recurso \_ )**
</dt> <dd>

Cria uma nova instância de um \_ recurso CD3DX12 \_ DESC, inicializando os seguintes parâmetros:

[**D3D12 \_ Dimensão de \_ dimensão de recurso**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)

Alinhamento de UINT64

Largura de UINT64

Altura UINT

UINT16 depthOrArraySize

UINT16 mipLevels

[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato

SampleCount UINT

SampleQuality UINT

[**D3D12 \_ Layout de \_ layout de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)

[**D3D12 \_ Sinalizadores de \_ sinalizadores de recurso**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags)

</dd> <dt>

**Buffer embutido estático (const \_ D3D12 \_ informações de alocação de recursos \_& resAllocInfo, \_ sinalizadores de sinalizadores de recursos D3D12 \_ = D3D12 \_ sinalizador de recurso \_ \_ nenhum)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**D3D12 \_ \_ \_ Informações de alocação de recursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)& resAllocInfo

opt [**D3D12 \_ Sinalizadores de \_ sinalizadores de recurso**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = sinalizador de recurso D3D12 \_ \_ \_ nenhum

</dd> <dt>

**Buffer embutido estático (largura de UINT64, sinalizadores de \_ sinalizadores de recurso D3D12 \_ = \_ \_ sinalizador de recurso D3D12 \_ nenhum, alinhamento de UInt64 = 0)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

Largura de UINT64

opt [**D3D12 \_ Sinalizadores de \_ sinalizadores de recurso**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = sinalizador de recurso D3D12 \_ \_ \_ nenhum

opt Alinhamento de UINT64 = 0

</dd> <dt>

**Tex1D embutido estático ( \_ formato de formato dxgi, largura de UINT64, UINT16-matrizes = 1, UINT16 mipLevels = 0, D3D12 sinalizadores de \_ sinalizadores de recursos \_ = D3D12 \_ \_ sinalizador \_ de recurso nenhum, D3D12 de layout de textura de vetor \_ \_ = D3D12 \_ \_ layout de textura \_ desconhecido, alinhamento de UINT64 = 0)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato

Largura de UINT64

opt UINT16 matrizes = 1

opt UINT16 mipLevels = 0

opt [**D3D12 \_ Sinalizadores de \_ sinalizadores de recurso**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = sinalizador de recurso D3D12 \_ \_ \_ nenhum

opt [**D3D12 \_ Layout do \_ layout de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = layout de textura D3D12 \_ \_ \_ desconhecido

opt Alinhamento de UINT64 = 0

</dd> <dt>

**estático embutido Tex2D ( \_ formato de formato dxgi, largura de UINT64, altura uint, UINT16 matrizes = 1, UINT16 mipLevels = 0, uint sampleCount = 1, uint sampleQuality = 0, sinalizadores de sinalizadores de recursos de D3D12 \_ \_ = D3D12 \_ \_ sinalizador de recurso \_ nenhum, D3D12 layout de \_ layout de textura \_ = D3D12 \_ \_ layout de textura \_ desconhecido, alinhamento de UINT64 = 0)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato

Largura de UINT64

Altura UINT

opt UINT16 matrizes = 1

opt UINT16 mipLevels = 0

opt UINT sampleCount = 1

opt UINT sampleQuality = 0

opt [**D3D12 \_ Sinalizadores de \_ sinalizadores de recurso**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = sinalizador de recurso D3D12 \_ \_ \_ nenhum

opt [**D3D12 \_ Layout do \_ layout de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = layout de textura D3D12 \_ \_ \_ desconhecido

opt Alinhamento de UINT64 = 0

</dd> <dt>

**estático embutido Tex3D ( \_ formato de formato dxgi, largura UINT64, altura uint, intensidade de UInt16, UInt16 mipLevels = 0, D3D12 sinalizadores de \_ recurso \_ sinalizadores = D3D12 \_ sinalizador de recurso \_ \_ nenhum, D3D12 layout de \_ layout de textura \_ = D3D12 de \_ \_ layout de textura \_ desconhecido, alinhamento de UINT64 = 0)**
</dt> <dd>

Especifica uma função que inicializa os seguintes parâmetros:

[**Dxgi \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato

Largura de UINT64

Altura UINT

Profundidade de UINT16

opt UINT16 mipLevels = 0

opt [**D3D12 \_ Sinalizadores de \_ sinalizadores de recurso**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_flags) = sinalizador de recurso D3D12 \_ \_ \_ nenhum

opt [**D3D12 \_ Layout do \_ layout de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout) = layout de textura D3D12 \_ \_ \_ desconhecido

opt Alinhamento de UINT64 = 0

</dd> <dt>

**constante embutida () const**
</dt> <dd>

Se Dimension = = [**D3D12 \_ Resource \_ Dimension**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D, retornará DepthOrArraySize. Se Dimension! = D3D12 \_ Resource \_ Dimension \_ TEXTURE3D, retornará 1.

</dd> <dt>

**constante de matrizes embutidas () const**
</dt> <dd>

Se Dimension! = D3D12 \_ Resource \_ Dimension \_ TEXTURE3D, retornará DepthOrArraySize. Se Dimension = = D3D12 \_ Resource \_ Dimension \_ TEXTURE3D, retornará 1. Consulte [**D3D12 \_ Resource \_ Dimension**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension) \_ TEXTURE3D.

</dd> <dt>

**PlaneCount embutida (ID3D12Device \* pDevice) const**
</dt> <dd>

Retorna D3D12GetFormatPlaneCount (pDevice, Format). Consulte [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) e [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device).

</dd> <dt>

**ID3D12Device de subrecursos embutidos ( \* pDevice) const**
</dt> <dd>

Retorna o número de subrecursos, calculado como MipLevels de \* matrizize () \* PlaneCount (pDevice).

</dd> <dt>

**CalcSubresource embutido (UINT MipSlice, UINT ArraySlice, UINT PlaneSlice)**
</dt> <dd>

Calcula um índice de subrecurso usando [**D3D12CalcSubresource**](d3d12calcsubresource.md).

</dd> <dt>

**\_ \_ constante de& de recurso const D3D12 () const**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> <dt>

**Operator = = (const D3D12 \_ recurso \_ desc& l, const D3D12 \_ recurso \_ desc& r)**
</dt> <dd>

Retornará true se todos os membros de cada estrutura forem idênticos.

</dd> <dt>

**Operator! = (const D3D12 \_ Resource \_ desc& l, const D3D12 \_ Resource \_ desc& r)**
</dt> <dd>

Retornará false se todos os membros de cada estrutura forem idênticos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3D12 de \_ recurso \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

