---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever o valor de recorte da faixa de buffer de índice como um único objeto adequado para uma descrição de fluxo.
ms.assetid: AF8F0919-4601-4A95-832A-5E1DA0304939
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e204b4f89cced7cf0bd5cdcb21702c37c241a81abfbc12d8644eafdb3c7c7ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988406"
---
# <a name="cd3dx12_pipeline_state_stream_ib_strip_cut_value-structure"></a>\_Estrutura do \_ \_ valor de \_ \_ \_ recorte de \_ faixa do CD3DX12 de fluxo do Stream IB

Uma estrutura auxiliar usada para descrever o valor de recorte da faixa de buffer de índice como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE {
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
                                                   CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE operator=(D3D12_INDEX_BUFFER_STRIP_CUT_VALUE const& i);
                                                   operator D3D12_INDEX_BUFFER_STRIP_CUT_VALUE() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Valor de \_ \_ \_ \_ \_ recorte de faixa \_ do Stream IB do CD3DX12 pipeline**
</dt> <dd>

Cria uma instância nova e não inicializada de um valor de \_ \_ \_ \_ \_ \_ recorte de faixa \_ de CD3DX12 do fluxo de estado de pipeline.

</dd> <dt>

**CD3DX12 \_ pipeline \_ State \_ Stream \_ IB \_ faixa \_ \_ Value (D3D12 \_ index buffer de índice de \_ \_ \_ recorte de \_ valor const &i)**
</dt> <dd>

Cria uma nova instância de um fluxo de estado de pipeline do CD3DX12 \_ \_ Stream de \_ \_ \_ recorte de faixa \_ \_ , inicializado com um tipo de subobjeto do  **tipo de \_ \_ \_ subobjeto do estado \_ \_ \_ \_ \_ do pipeline de D3D12** e dados de subobjeto recortados da faixa de [**\_ buffer de índice \_ \_ \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) .

</dd> <dt>

**Operator = (D3D12 de \_ buffer de índice de distribuição de valor de \_ \_ \_ recorte \_ constante& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**\_ \_ \_ \_ valor de recorte de faixa \_ do buffer de índice do operador D3D12 () const**
</dt> <dd>

Conversão implícita em uma [**\_ faixa de \_ \_ \_ \_ valor de recorte de buffer de índice D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_index_buffer_strip_cut_value) .

</dd> </dl>

## <a name="remarks"></a>Comentários

\_ \_ \_ \_ \_ \_ O valor de recorte do Stream IB strip do CD3DX12 pipeline \_ é uma especialização de typedef do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definido da seguinte maneira:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INDEX_BUFFER_STRIP_CUT_VALUE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_IB_STRIP_CUT_VALUE>
    CD3DX12_PIPELINE_STATE_STREAM_IB_STRIP_CUT_VALUE;
          
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

 

