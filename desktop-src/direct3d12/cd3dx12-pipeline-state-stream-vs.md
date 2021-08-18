---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_VS (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever um sombreador de vértice como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 27EAB08C-D3B9-4920-B7D2-754AA3562A94
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_VS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_VS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4361cf50a97cd3d7bf2abc6995182e9ca24bad6b824505408aca98bd4b3ead42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045724"
---
# <a name="cd3dx12_pipeline_state_stream_vs-structure"></a>\_ \_ \_ Estrutura vs do fluxo de estado do pipeline do CD3DX12 \_

Uma estrutura auxiliar usada para descrever um sombreador de vértice como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_VS {
                                   CD3DX12_PIPELINE_STATE_STREAM_VS;
                                   CD3DX12_PIPELINE_STATE_STREAM_VS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_VS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Fluxo de estado do pipeline CD3DX12 \_ \_ \_ vs**
</dt> <dd>

Cria uma nova instância, não inicializada, de um \_ fluxo de estado de pipeline CD3DX12 \_ \_ \_ versus

</dd> <dt>

**\_ \_ \_ Fluxo de estado do pipeline CD3DX12 \_ vs (D3D12 do \_ código de bytes do sombreador do \_ se&i)**
</dt> <dd>

Cria uma nova instância de um fluxo de estado do pipeline do CD3DX12 \_ \_ \_ \_ versus inicializado com um tipo de subobjeto do tipo de subobjeto do **estado do \_ pipeline D3D12 \_ \_ \_ \_ vs** e dados de subobjetos copiados de *i*, uma estrutura de [**código de \_ \_ bytes do sombreador D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

</dd> <dt>

**Operator = (D3D12 do \_ código de bytes do sombreador de \_ Radio& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**\_ \_ constante de código de bytes do sombreador D3D12 do operador ()**
</dt> <dd>

Conversão implícita em uma estrutura de [**\_ código de \_ bytes do sombreador D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

</dd> </dl>

## <a name="remarks"></a>Comentários

\_ \_ O fluxo de estado do pipeline CD3DX12 \_ \_ vs é uma especialização de typedef do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definido da seguinte maneira:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_VS>
    CD3DX12_PIPELINE_STATE_STREAM_VS;
          
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

 

