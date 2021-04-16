---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever o formato de estêncil de profundidade como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 512DB46E-D8F0-482B-9174-C786FB91AFD2
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dc7ae2703ac80ac155c04d42624a081723288bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105750119"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil_format-structure"></a>\_Estrutura do \_ \_ formato de \_ estêncil profundidade do fluxo de \_ estado do pipeline \_ CD3DX12

Uma estrutura auxiliar usada para descrever o formato de estêncil de profundidade como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT {
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT(DXGI_FORMAT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT operator=(DXGI_FORMAT const& i);
                                                     operator DXGI_FORMAT() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Formato de \_ \_ estêncil de profundidade do fluxo de estado \_ do \_ pipeline CD3DX12 \_**
</dt> <dd>

Cria uma nova instância, não inicializada, de um \_ formato de estêncil de profundidade de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ \_ .

</dd> <dt>

**\_ \_ \_ \_ \_ \_ Formato de estêncil de profundidade de fluxo de estado de PIPELINE CD3DX12 ( \_ formato dxgi const &i)**
</dt> <dd>

Cria uma nova instância de um \_ formato de estêncil de profundidade de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ \_ , inicializada com um tipo de subobjeto do **\_ \_ \_ \_ \_ \_ \_ formato de estêncil profundidade de tipo** de subobjeto de perfil de D3D12 e dados de subobjeto copiados de *i*, uma enumeração de [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .

</dd> <dt>

**Operator = ( \_ formato dxgi const& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**\_const do formato dxgi do operador ()**
</dt> <dd>

Conversão implícita em uma enumeração de [**\_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .

</dd> </dl>

## <a name="remarks"></a>Comentários

\_ \_ \_ \_ \_ \_ O formato de estêncil de profundidade do fluxo de estado do pipeline CD3DX12 é uma especialização de typedef do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definido da seguinte maneira:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_FORMAT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL_FORMAT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
          
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**Subobjeto de fluxo do estado do \_ pipeline CD3DX12 \_ \_ \_**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**\_Tipo de \_ subobjeto de estado de pipeline D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

