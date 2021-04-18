---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_PS (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever um sombreador de pixel como um único objeto adequado para uma descrição de fluxo.
ms.assetid: A71E2ABE-5B52-41B4-ACE0-25CA63EF2565
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_PS
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_PS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17f3b49328ad85bc68147ad58b043459c223e6a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105807213"
---
# <a name="cd3dx12_pipeline_state_stream_ps-structure"></a>\_ \_ \_ Estrutura PS do fluxo de estado do pipeline do CD3DX12 \_

Uma estrutura auxiliar usada para descrever um sombreador de pixel como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_PS {
                                   CD3DX12_PIPELINE_STATE_STREAM_PS;
                                   CD3DX12_PIPELINE_STATE_STREAM_PS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_PS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_PS de \_ fluxo de estado do pipeline CD3DX12 \_ \_**
</dt> <dd>

Cria uma nova instância, não inicializada, de um CD3DX12 \_ de \_ fluxo de estado de pipeline \_ \_ .

</dd> <dt>

**CD3DX12 \_ \_ \_ \_ do fluxo de estado do pipeline do PS (D3D12 do código de \_ \_ &bytes do sombreador**
</dt> <dd>

Cria uma nova instância de um CD3DX12 de \_ fluxo de estado de pipeline do \_ \_ \_ D3D12, inicializada com um tipo de subobjeto do **\_ \_ \_ \_ tipo \_** de subobjeto de estado de pipeline do D3D12 e os dados de subobjetos copiados de *i*, uma estrutura de [**código de \_ \_ bytes do sombreador**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) de

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

\_ \_ \_ \_ O PS do fluxo de estado do pipeline CD3DX12 é uma especialização de typedef do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definido da seguinte maneira:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PS>
    CD3DX12_PIPELINE_STATE_STREAM_PS;
          
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

 

