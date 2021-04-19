---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_CS (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever um sombreador de computação como um único objeto adequado para uma descrição de fluxo.
ms.assetid: B76B0CB4-FC76-4C5B-84FC-DCFF907BE2F8
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_CS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_CS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5796e0f96ad4e2a87d2a45519321c363078a34b1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763920"
---
# <a name="cd3dx12_pipeline_state_stream_cs-structure"></a>\_Estrutura de \_ cs do fluxo de estado do pipeline do \_ CD3DX12 \_

Uma estrutura auxiliar usada para descrever um sombreador de computação como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_CS {
                                   CD3DX12_PIPELINE_STATE_STREAM_CS;
                                   CD3DX12_PIPELINE_STATE_STREAM_CS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_CS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Fluxo de \_ estado do pipeline \_ do CD3DX12 \_**
</dt> <dd>

Cria uma instância nova e não inicializada de um fluxo de \_ estado do pipeline do CD3DX12 \_ \_ \_ .

</dd> <dt>

**CD3DX12 \_ pipeline \_ \_ de fluxo \_ de estado cs (D3D12 do \_ código de bytes do sombreador do \_ am&i)**
</dt> <dd>

Cria uma nova instância de um fluxo de estado do pipeline do CD3DX12 \_ \_ \_ \_ , inicializado com um tipo de subobjeto do tipo de subobjeto do **estado do \_ pipeline D3D12 \_ \_ \_ \_ cs** e os dados de subobjeto copiados de *i*, uma estrutura de [**código de \_ \_ bytes do sombreador D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

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

\_ \_ \_ O fluxo de estado \_ do pipeline CD3DX12 é uma especialização de typedef do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definido da seguinte maneira:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CS>
    CD3DX12_PIPELINE_STATE_STREAM_CS;
          
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

 

