---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever a topologia primitiva como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 7DC73B75-2B8D-4DAB-A0AA-6DF6F4039093
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e597da8ea1ed4a4291142065e8e06f89d2664e03
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781563"
---
# <a name="cd3dx12_pipeline_state_stream_primitive_topology-structure"></a>\_Estrutura de \_ \_ \_ topologia primitiva de fluxo de estado de pipeline CD3DX12 \_

Uma estrutura auxiliar usada para descrever a topologia primitiva como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY {
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
                                                   CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY(D3D12_PRIMITIVE_TOPOLOGY_TYPE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY operator=(D3D12_PRIMITIVE_TOPOLOGY_TYPE const& i);
                                                   operator D3D12_PRIMITIVE_TOPOLOGY_TYPE() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_ \_ \_ Topologia primitiva de fluxo de estado \_ de pipeline CD3DX12 \_**
</dt> <dd>

Cria uma nova instância, não inicializada, de uma \_ topologia primitiva de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**\_ \_ \_ \_ Topologia primitiva de fluxo de estado de pipeline CD3DX12 \_ ( \_ tipo de topologia primitivo D3D12 \_ \_ const &i)**
</dt> <dd>

Cria uma nova instância de uma \_ topologia primitiva de fluxo de estado de pipeline do CD3DX12 \_ \_ \_ \_ , inicializada com um tipo de subobjeto do tipo de subobjeto de **perfil de pipeline D3D12 de \_ \_ \_ \_ \_ \_ topologia primitivo** e dados de subobjeto copiados de *i*, uma estrutura de [**\_ \_ \_ tipo de topologia primitivo D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) .

</dd> <dt>

**Operator = ( \_ tipo de topologia D3D12 primitivo \_ \_ const& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**\_ \_ \_ const do tipo de topologia primitiva do operador D3D12 ()**
</dt> <dd>

Conversão implícita em uma estrutura de [**\_ \_ \_ tipo de topologia primitiva de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) .

</dd> </dl>

## <a name="remarks"></a>Comentários

A \_ \_ \_ \_ topologia primitiva de fluxo \_ de estado do pipeline CD3DX12 é uma especialização de TYPEDEF do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definida da seguinte maneira:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PRIMITIVE_TOPOLOGY_TYPE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PRIMITIVE_TOPOLOGY>
    CD3DX12_PIPELINE_STATE_STREAM_PRIMITIVE_TOPOLOGY;
          
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

 

