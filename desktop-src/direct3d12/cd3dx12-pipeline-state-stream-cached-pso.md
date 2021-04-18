---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever um PSO armazenado em cache como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 86CDC60A-275D-4B71-BE6D-C863C72E9C05
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ddb223dfd2baa7bc6bee1b5a36950fc47d65d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781623"
---
# <a name="cd3dx12_pipeline_state_stream_cached_pso-structure"></a>\_ \_ \_ \_ Estrutura PSO em cache do fluxo de estado do pipeline \_ do CD3DX12

Uma estrutura auxiliar usada para descrever um PSO armazenado em cache como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO {
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO(D3D12_CACHED_PIPELINE_STATE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO operator=(D3D12_CACHED_PIPELINE_STATE const& i);
                                           operator D3D12_CACHED_PIPELINE_STATE() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**PSO do fluxo de estado do pipeline do CD3DX12 \_ \_ \_ \_ em cache \_**
</dt> <dd>

Cria uma nova instância, não inicializada, de um CD3DX12 de \_ fluxo de estado de pipeline do \_ \_ \_ codecache \_ .

</dd> <dt>

**CD3DX12 \_ \_ \_ \_ do fluxo de estado do pipeline \_ do D3D12 do PSO cache do estado de \_ pipeline em cache \_ \_ constante &i)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 de \_ fluxo de estado de pipeline do \_ \_ \_ \_ D3D12, inicializada com um tipo de subobjeto do tipo de subobjeto do estado do pipeline do codeD3D12 **\_ \_ \_ \_ \_ armazenado em cache do \_ PSO** e dos dados de subobjetos copiados de *i*, uma estrutura de [**\_ \_ \_ estado de pipeline em cache em**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) .

</dd> <dt>

**Operator = (D3D12 de \_ estado de pipeline em cache \_ \_ const& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**operador D3D12 \_ \_ de estado de pipeline armazenado em cache \_ () const**
</dt> <dd>

Conversão implícita em uma estrutura de [**\_ \_ \_ estado de pipeline em cache D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) .

</dd> </dl>

## <a name="remarks"></a>Comentários

\_O CD3DX12 \_ do \_ fluxo \_ de estado \_ de pipeline do CD3DX12 de um controle de perfil é uma especialização de TYPEDEF do modelo de [**\_ \_ \_ \_ subobjeto de fluxo do estado do pipeline**](cd3dx12-pipeline-state-stream-subobject.md) e é definido da seguinte maneira:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_CACHED_PIPELINE_STATE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CACHED_PSO>
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
          
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

 

