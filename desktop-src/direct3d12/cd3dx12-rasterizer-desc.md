---
title: Estrutura de CD3DX12_RASTERIZER_DESC (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura Desc do rasterizador D3D12 \_ .
ms.assetid: 28AA8256-1CAF-484F-B219-0F0461BA947C
keywords:
- Estrutura de CD3DX12_RASTERIZER_DESC
topic_type:
- apiref
api_name:
- CD3DX12_RASTERIZER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa95dde87aea8e3c61d0d1fb6de6845f33717f6a46db4df7996a23afd7590b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729426"
---
# <a name="cd3dx12_rasterizer_desc-structure"></a>\_Estrutura Desc do rasterizador CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura [**\_ \_ Desc do rasterizador D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_RASTERIZER_DESC  : public D3D12_RASTERIZER_DESC{
   CD3DX12_RASTERIZER_DESC();
   explicit CD3DX12_RASTERIZER_DESC(const D3D12_RASTERIZER_DESC& o);
   explicit CD3DX12_RASTERIZER_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_RASTERIZER_DESC(D3D12_FILL_MODE fillMode, D3D12_CULL_MODE cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12_CONSERVATIVE_RASTERIZATION_MODE conservativeRaster);
   ~CD3DX12_RASTERIZER_DESC();
   operator const D3D12_RASTERIZER_DESC&() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**CD3DX12 \_ do rasterizador \_ DESC ()**
</dt> <dd>

Cria uma instância nova e não inicializada de uma CD3DX12 do \_ rasterizador \_ desc.

</dd> <dt>

**CD3DX12 \_ de rasterizador explícito \_ (const D3D12 \_ rasterizador \_ desc& o)**
</dt> <dd>

Cria uma nova instância de um \_ rasterizador CD3DX12 \_ DESC, inicializada com o conteúdo de outra estrutura de [**D3D12 do \_ rasterizador \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) .

</dd> <dt>

**CD3DX12 \_ de rasterizador explícito \_ ( \_ padrão CD3DX12)**
</dt> <dd>

Cria uma nova instância de um \_ rasterizador CD3DX12 \_ DESC, inicializada com parâmetros padrão.

``` syntax
        FillMode = D3D12_FILL_MODE_SOLID;  
        CullMode = D3D12_CULL_MODE_BACK;  
        FrontCounterClockwise = FALSE;  
        DepthBias = D3D12_DEFAULT_DEPTH_BIAS;  
        DepthBiasClamp = D3D12_DEFAULT_DEPTH_BIAS_CLAMP;  
        SlopeScaledDepthBias = D3D12_DEFAULT_SLOPE_SCALED_DEPTH_BIAS;  
        DepthClipEnable = TRUE;  
        MultisampleEnable = FALSE;  
        AntialiasedLineEnable = FALSE;  
        ForcedSampleCount = 0;  
        ConservativeRaster = D3D12_CONSERVATIVE_RASTERIZATION_MODE_OFF;  
```

</dd> <dt>

**Explicit CD3DX12 \_ rasterizador \_ DESC (D3D12 \_ modo de preenchimento \_ fillMode, D3D12 selecionar \_ \_ modo de seleção, bool FrontCounterClockwise, int DepthBias, float DepthBiasClamp, float SlopeScaledDepthBias, BOOL DepthClipEnable, bool MultisampleEnable, bool antialiasedLineEnable, uint forcedSampleCount, \_ D3D12 \_ modo de rasterização conservador conservativeRaster \_ )**
</dt> <dd>

Cria uma nova instância de um \_ rasterizador CD3DX12 \_ DESC, inicializando os seguintes parâmetros:

[**D3D12 \_ \_Modo de preenchimento**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) fillMode

[**D3D12 \_ \_Modo de seleção**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode) de seleção

FrontCounterClockwise BOOL

DepthBias INT

DepthBiasClamp flutuante

SlopeScaledDepthBias flutuante

DepthClipEnable BOOL

MultisampleEnable BOOL

AntialiasedLineEnable BOOL

ForcedSampleCount UINT

[**D3D12 \_ \_ \_ Modo de rasterização conservador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) conservativeRaster

</dd> <dt>

**~ CD3DX12 \_ do rasterizador \_ DESC ()**
</dt> <dd>

Destrói uma instância de um \_ rasterizador CD3DX12 \_ desc.

</dd> <dt>

**\_const de D3D12 const do rasterizador \_ desc& () constante**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3D12 do \_ rasterizador \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





