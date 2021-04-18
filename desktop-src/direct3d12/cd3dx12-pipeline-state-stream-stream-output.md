---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever a descrição da saída do fluxo como um único objeto adequado para uma descrição de fluxo.
ms.assetid: CC7E1E76-CD44-4D70-A5B8-7C2B6210468E
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acc8f7bf059c4eee72b0b22abfc424ee82ffd2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812274"
---
# <a name="cd3dx12_pipeline_state_stream_stream_output-structure"></a>\_Estrutura de \_ \_ saída do fluxo de fluxo do estado do \_ pipeline CD3DX12 \_

Uma estrutura auxiliar usada para descrever a descrição da saída do fluxo como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT {
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT(D3D12_STREAM_OUTPUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT operator=(D3D12_STREAM_OUTPUT_DESC const& i);
                                              operator D3D12_STREAM_OUTPUT_DESC() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Saída de \_ fluxo de fluxo de estado de pipeline CD3DX12 \_ \_ \_**
</dt> <dd>

Cria uma nova instância, não inicializada, de uma \_ saída de fluxo de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**\_ \_ \_ \_ \_ Saída de fluxo de fluxo de estado de pipeline CD3DX12 ( \_ saída de fluxo D3D12 \_ \_ desc const &i)**
</dt> <dd>

Cria uma nova instância de uma saída de fluxo de fluxo de estado de pipeline do CD3DX12 \_ \_ \_ \_ \_ , inicializada com um tipo de subobjeto do tipo de subobjeto do estado do  **pipeline D3D12 de \_ \_ \_ \_ \_ \_ saída de fluxo** e dados de subobjeto copiados de i, uma estrutura [**desc de saída do fluxo de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) .

</dd> <dt>

**Operator = (D3D12 \_ de \_ saída de fluxo \_ desc const& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**D3D12 \_ do operador \_ \_ de saída de fluxo DESC () const**
</dt> <dd>

Conversão implícita em uma [**estrutura \_ \_ \_ desc de saída de fluxo de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc) .

</dd> </dl>

## <a name="remarks"></a>Comentários

A \_ \_ \_ \_ \_ saída do fluxo de fluxo do estado do pipeline CD3DX12 é uma especialização de TYPEDEF do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definida da seguinte maneira:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_STREAM_OUTPUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_STREAM_OUTPUT>
    CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
          
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

 

