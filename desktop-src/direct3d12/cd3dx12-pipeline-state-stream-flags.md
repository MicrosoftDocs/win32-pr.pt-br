---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_FLAGS (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever os sinalizadores de estado do pipeline como um único objeto adequado para uma descrição de fluxo.
ms.assetid: EF67936B-315A-4B3F-9E07-7CF4C5EE47CF
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_FLAGS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_FLAGS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 034f4a63c774ca41f28fbe9e6c2945fddee47c4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105749904"
---
# <a name="cd3dx12_pipeline_state_stream_flags-structure"></a>\_Estrutura de \_ sinalizadores de fluxo de estado do pipeline CD3DX12 \_ \_

Uma estrutura auxiliar usada para descrever os sinalizadores de estado do pipeline como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_FLAGS {
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS(D3D12_PIPELINE_STATE_FLAGS const &i);
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS operator=(D3D12_PIPELINE_STATE_FLAGS const& i);
                                      operator D3D12_PIPELINE_STATE_FLAGS() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Sinalizadores de \_ fluxo de estado do pipeline CD3DX12 \_ \_**
</dt> <dd>

Cria uma nova instância não inicializada de um CD3DX12 de \_ sinalizadores de \_ fluxo de estado de pipeline \_ \_ .

</dd> <dt>

**\_ \_ \_ \_ Sinalizadores de fluxo de estado de pipeline CD3DX12 ( \_ sinalizadores de estado de pipeline D3D12 \_ \_ const &i)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 \_ de fluxo de estado de pipeline \_ \_ \_ , inicializada com um tipo de subobjeto dos sinalizadores de tipo de subobjeto de **estado de \_ pipeline \_ \_ \_ \_ D3D12** e dados de subobjeto copiados de *i*, uma estrutura de [**\_ sinalizadores de \_ estado \_ de pipeline D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) .

</dd> <dt>

**Operator = ( \_ sinalizadores de estado do pipeline D3D12 \_ \_ const& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**D3D12 \_ do operador \_ \_ sinalizadores de estado do pipeline () const**
</dt> <dd>

Conversão implícita em uma estrutura de [**\_ sinalizadores de \_ estado \_ do pipeline D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags) .

</dd> </dl>

## <a name="remarks"></a>Comentários

\_ \_ \_ \_ Os sinalizadores de fluxo de estado do pipeline CD3DX12 é uma especialização de typedef do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definido da seguinte maneira:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PIPELINE_STATE_FLAGS, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_FLAGS>
    CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
          
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

 

