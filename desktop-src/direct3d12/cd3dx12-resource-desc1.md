---
title: Estrutura de CD3DX12_RESOURCE_DESC1 (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**D3DX12_RESOURCE_DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc) .
keywords:
- Estrutura de CD3DX12_RESOURCE_DESC1
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_DESC1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2021
ms.openlocfilehash: 87fe62c475e1d961258671355c4c9be133bf0a41
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813229"
---
# <a name="cd3dx12_resource_desc1-structure"></a>Estrutura de CD3DX12_RESOURCE_DESC1

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**D3DX12_RESOURCE_DESC1**](/windows/win32/api/d3d12/D3DX12_RESOURCE_DESC1/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1) .

## <a name="syntax"></a>Sintaxe

```cpp
struct CD3DX12_RESOURCE_DESC1 : public D3D12_RESOURCE_DESC1
{
    CD3DX12_RESOURCE_DESC1();
    explicit CD3DX12_RESOURCE_DESC1(const D3D12_RESOURCE_DESC1& o) noexcept;
    CD3DX12_RESOURCE_DESC1(
        D3D12_RESOURCE_DIMENSION dimension,
        UINT64 alignment,
        UINT64 width,
        UINT height,
        UINT16 depthOrArraySize,
        UINT16 mipLevels,
        DXGI_FORMAT format,
        UINT sampleCount,
        UINT sampleQuality,
        D3D12_TEXTURE_LAYOUT layout,
        D3D12_RESOURCE_FLAGS flags,
        UINT samplerFeedbackMipRegionWidth = 0,
        UINT samplerFeedbackMipRegionHeight = 0,
        UINT samplerFeedbackMipRegionDepth = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Buffer(
        const D3D12_RESOURCE_ALLOCATION_INFO& resAllocInfo,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Buffer(
        UINT64 width,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        UINT64 alignment = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Tex1D(
        DXGI_FORMAT format,
        UINT64 width,
        UINT16 arraySize = 1,
        UINT16 mipLevels = 0,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN,
        UINT64 alignment = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Tex2D(
        DXGI_FORMAT format,
        UINT64 width,
        UINT height,
        UINT16 arraySize = 1,
        UINT16 mipLevels = 0,
        UINT sampleCount = 1,
        UINT sampleQuality = 0,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN,
        UINT64 alignment = 0,
        UINT samplerFeedbackMipRegionWidth = 0,
        UINT samplerFeedbackMipRegionHeight = 0,
        UINT samplerFeedbackMipRegionDepth = 0) noexcept;
    static inline CD3DX12_RESOURCE_DESC1 Tex3D(
        DXGI_FORMAT format,
        UINT64 width,
        UINT height,
        UINT16 depth,
        UINT16 mipLevels = 0,
        D3D12_RESOURCE_FLAGS flags = D3D12_RESOURCE_FLAG_NONE,
        D3D12_TEXTURE_LAYOUT layout = D3D12_TEXTURE_LAYOUT_UNKNOWN,
        UINT64 alignment = 0) noexcept;
    inline UINT16 Depth() const noexcept;
    inline UINT16 ArraySize() const noexcept;
    inline UINT8 PlaneCount(_In_ ID3D12Device* pDevice) const noexcept;
    inline UINT Subresources(_In_ ID3D12Device* pDevice) const noexcept;
    inline UINT CalcSubresource(UINT MipSlice, UINT ArraySlice, UINT PlaneSlice) noexcept;
};
inline bool operator==(const D3D12_RESOURCE_DESC1& l, const D3D12_RESOURCE_DESC1& r) noexcept;
inline bool operator!=(const D3D12_RESOURCE_DESC1& l, const D3D12_RESOURCE_DESC1& r) noexcept;
```

## <a name="members"></a>Membros

`CD3DX12_RESOURCE_DESC1`

Construtor padrão. Cria uma nova instância, não inicializada, de um **CD3DX12_RESOURCE_DESC1**.

`CD3DX12_RESOURCE_DESC1(const D3D12_RESOURCE_DESC1&)`

Construtor que cria uma nova instância de um **CD3DX12_RESOURCE_DESC1** inicializado com o conteúdo de uma estrutura de [**D3DX12_RESOURCE_DESC1**](/windows/win32/api/d3d12/D3DX12_RESOURCE_DESC1/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1) .

`CD3DX12_RESOURCE_DESC1(D3D12_RESOURCE_DIMENSION, UINT64, UINT64, UINT, UINT16, UINT16, DXGI_FORMAT, UINT, UINT, D3D12_TEXTURE_LAYOUT, D3D12_RESOURCE_FLAGS, UINT = 0, UINT = 0, UINT = 0)`

Construtor que cria uma nova instância de um **CD3DX12_RESOURCE_DESC1** inicializado com os parâmetros passados a ele.

`Buffer(const D3D12_RESOURCE_ALLOCATION_INFO&, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE)`

Uma função estática que constrói e retorna uma nova instância de uma **CD3DX12_RESOURCE_DESC1** inicializada com esses valores.

|Membro de dados|valor|
|-|-|
|Dimensão|D3D12_RESOURCE_DIMENSION_BUFFER|
|Alinhamento|*resAllocInfo*. Sintonia|
|Largura|*resAllocInfo*. SizeInBytes|
|Altura|1|
|DepthOrArraySize|1|
|MipLevels|1|
|Formatar|DXGI_FORMAT_UNKNOWN|
|Contagem de SampleDesc.|1|
|SampleDesc. Quality|0|
|Layout|D3D12_TEXTURE_LAYOUT_ROW_MAJOR|
|Flags|*sinalizadores*|
|SamplerFeedbackMipRegion. Width|0|
|SamplerFeedbackMipRegion. Height|0|
|SamplerFeedbackMipRegion. Depth|0|

`Buffer(UINT64, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE, UINT64 = 0)`

Uma função estática que constrói e retorna uma nova instância de uma **CD3DX12_RESOURCE_DESC1** inicializada com esses valores.

|Membro de dados|valor|
|-|-|
|Dimensão|D3D12_RESOURCE_DIMENSION_BUFFER|
|Alinhamento|*sintonia*|
|Largura|*width*|
|Altura|1|
|DepthOrArraySize|1|
|MipLevels|1|
|Formatar|DXGI_FORMAT_UNKNOWN|
|Contagem de SampleDesc.|1|
|SampleDesc. Quality|0|
|Layout|D3D12_TEXTURE_LAYOUT_ROW_MAJOR|
|Flags|*sinalizadores*|
|SamplerFeedbackMipRegion. Width|0|
|SamplerFeedbackMipRegion. Height|0|
|SamplerFeedbackMipRegion. Depth|0|

`Tex1D(DXGI_FORMAT, UINT64, UINT16 = 1, UINT16 = 0, D3D12_RESOURCE_FLAGS D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 = 0)`

Uma função estática que constrói e retorna uma nova instância de uma **CD3DX12_RESOURCE_DESC1** inicializada com esses valores.

|Membro de dados|valor|
|-|-|
|Dimensão|D3D12_RESOURCE_DIMENSION_TEXTURE1D|
|Alinhamento|*sintonia*|
|Largura|*width*|
|Altura|1|
|DepthOrArraySize|*arraySize*|
|MipLevels|*mipLevels*|
|Formatar|*format*|
|Contagem de SampleDesc.|1|
|SampleDesc. Quality|0|
|Layout|*layout*|
|Flags|*sinalizadores*|
|SamplerFeedbackMipRegion. Width|0|
|SamplerFeedbackMipRegion. Height|0|
|SamplerFeedbackMipRegion. Depth|0|

`Tex2D(DXGI_FORMAT, UINT64, UINT, UINT16 = 1, UINT16 = 0, UINT = 1, UINT = 0, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 = 0, UINT = 0, UINT = 0, UINT = 0)`

Uma função estática que constrói e retorna uma nova instância de uma **CD3DX12_RESOURCE_DESC1** inicializada com esses valores.

|Membro de dados|valor|
|-|-|
|Dimensão|D3D12_RESOURCE_DIMENSION_TEXTURE2D|
|Alinhamento|*sintonia*|
|Largura|*width*|
|Altura|*altura*|
|DepthOrArraySize|*arraySize*|
|MipLevels|*mipLevels*|
|Formatar|*format*|
|Contagem de SampleDesc.|*sampleCount*|
|SampleDesc. Quality|*sampleQuality*|
|Layout|*layout*|
|Flags|*sinalizadores*|
|SamplerFeedbackMipRegion. Width|*samplerFeedbackMipRegionWidth*|
|SamplerFeedbackMipRegion. Height|*samplerFeedbackMipRegionHeight*|
|SamplerFeedbackMipRegion. Depth|*samplerFeedbackMipRegionDepth*|

`Tex3D(DXGI_FORMAT, UINT64, UINT, UINT16, UINT16 = 0, D3D12_RESOURCE_FLAGS = D3D12_RESOURCE_FLAG_NONE, D3D12_TEXTURE_LAYOUT = D3D12_TEXTURE_LAYOUT_UNKNOWN, UINT64 = 0)`

Uma função estática que constrói e retorna uma nova instância de uma **CD3DX12_RESOURCE_DESC1** inicializada com esses valores.

|Membro de dados|valor|
|-|-|
|Dimensão|D3D12_RESOURCE_DIMENSION_TEXTURE3D|
|Alinhamento|*sintonia*|
|Largura|*width*|
|Altura|*altura*|
|DepthOrArraySize|*Detalhado*|
|MipLevels|*mipLevels*|
|Formatar|*format*|
|Contagem de SampleDesc.|1|
|SampleDesc. Quality|0|
|Layout|*layout*|
|Flags|*sinalizadores*|
|SamplerFeedbackMipRegion. Width|0|
|SamplerFeedbackMipRegion. Height|0|
|SamplerFeedbackMipRegion. Depth|0|

`Depth`

Retorna um **UINT16** contendo a profundidade do recurso.

`ArraySize`

Retorna um **UINT16** contendo o tamanho da matriz do recurso.

`PlaneCount(ID3D12Device*)`

Retorna um **UINT8** que contém a contagem de planos para o formato do recurso.

`Subresources(ID3D12Device*)`

Retorna um **uint** que contém o número de subrecursos no recurso.

`CalcSubresource(UINT, UINT, UINT)`

Caculates e retorna um **uint** contendo um índice de subrecurso para o recurso com base nos parâmetros passados para ele.

`operator==(const D3D12_RESOURCE_DESC1&, const D3D12_RESOURCE_DESC1&)`

Uma função gratuita que retorna `true` se os dois parâmetros são equivalentes ao membro; caso contrário, `false` .

`operator!=(const D3D12_RESOURCE_DESC1&, const D3D12_RESOURCE_DESC1&)`

Uma função gratuita que retorna `true` se os dois parâmetros são membros não iguais; caso contrário, `false` .

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Confira também

* [D3DX12_RESOURCE_DESC1](/windows/win32/api/d3d12/D3DX12_RESOURCE_DESC1/windows/win32/api/d3d12/ns-d3d12-d3d12_resource_desc1)
* [Estruturas auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
