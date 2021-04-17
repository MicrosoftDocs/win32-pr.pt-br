---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever os formatos de destino de renderização como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 8C5C2279-7985-41B6-87EA-ABB0007DAFD4
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a64f051ba56edf176c87bbc99551cd974fc3a43
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105797546"
---
# <a name="cd3dx12_pipeline_state_stream_render_target_formats-structure"></a>\_Estrutura de \_ \_ formatos de \_ destino de renderização de fluxo de \_ estado de pipeline \_ CD3DX12

Uma estrutura auxiliar usada para descrever os formatos de destino de renderização como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS {
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
                                                      CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS(D3D12_RT_FORMAT_ARRAY const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS operator=(D3D12_RT_FORMAT_ARRAY const& i);
                                                      operator D3D12_RT_FORMAT_ARRAY() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Formatos de \_ \_ destino de renderização de fluxo de estado \_ de \_ pipeline CD3DX12 \_**
</dt> <dd>

Cria uma nova instância, não inicializada, de um fluxo de estado do pipeline do CD3DX12 \_ formatos de \_ destino de \_ \_ renderização \_ \_ .

</dd> <dt>

**\_ \_ \_ \_ \_ \_ Formatos de destino de renderização de fluxo de estado de pipeline CD3DX12 ( \_ matriz de formato D3D12 RT \_ \_ &i)**
</dt> <dd>

Cria uma nova instância de um \_ fluxo de estado do pipeline CD3DX12 \_ \_ \_ \_ \_ formatos de destino, inicializados com um tipo de subobjeto do **tipo de \_ subobjeto do estado do pipeline D3D12 \_ \_ \_ \_ renderizar os \_ \_ formatos de destino** e os dados de subobjeto copiados de *i*, uma estrutura de [**\_ \_ \_ matriz de formato D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .

</dd> <dt>

**Operator = ( \_ matriz de formato D3D12 RT \_ \_ const& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**\_ \_ matriz de formato D3D12 RT \_ do operador () const**
</dt> <dd>

Conversão implícita em uma estrutura de [**\_ matriz de \_ formato \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .

</dd> </dl>

## <a name="remarks"></a>Comentários

\_ \_ \_ \_ \_ \_ Os formatos de destino de renderização de fluxo de estado de pipeline CD3DX12 é uma especialização de typedef do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definido da seguinte maneira:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_RT_FORMAT_ARRAY, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RENDER_TARGET_FORMATS>
    CD3DX12_PIPELINE_STATE_STREAM_RENDER_TARGET_FORMATS;
          
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

 

