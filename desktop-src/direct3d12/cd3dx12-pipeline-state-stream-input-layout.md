---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever um layout de entrada como um único objeto adequado para uma descrição de fluxo.
ms.assetid: CEAD9FA6-4FB0-492E-9E81-8C4900A1FBC5
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d467d60444588001a115f9b1ad3667f35fc9edab69a64402f42b4885d70a86d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117912955"
---
# <a name="cd3dx12_pipeline_state_stream_input_layout-structure"></a>\_Estrutura de \_ \_ layout de entrada de fluxo de estado de \_ pipeline CD3DX12 \_

Uma estrutura auxiliar usada para descrever um layout de entrada como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT {
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
                                             CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT(D3D12_INPUT_LAYOUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT operator=(D3D12_INPUT_LAYOUT_DESC const& i);
                                             operator D3D12_INPUT_LAYOUT_DESC() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Layout de \_ entrada de fluxo de estado de pipeline CD3DX12 \_ \_ \_**
</dt> <dd>

Cria uma nova instância, não inicializada, de um \_ layout de entrada de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**\_ \_ \_ \_ \_ Layout de entrada de fluxo de estado de pipeline CD3DX12 (D3D12 de \_ layout de entrada \_ \_ desc const &i)**
</dt> <dd>

Cria uma nova instância de um \_ layout de entrada de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ , inicializada com um tipo de subobjeto do tipo de subobjeto de **estado de pipeline D3D12 \_ \_ \_ \_ \_ \_ layout de entrada** e dados de subobjeto copiados de *i*, uma estrutura [**\_ \_ \_ desc de layout de entrada D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) .

</dd> <dt>

**Operator = (D3D12 \_ Input \_ layout \_ desc const& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**D3D12 \_ \_ \_ de layout de entrada do operador DESC () const**
</dt> <dd>

Conversão implícita em uma [**estrutura \_ \_ \_ desc de layout de entrada D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_input_layout_desc) .

</dd> </dl>

## <a name="remarks"></a>Comentários

\_ \_ \_ \_ \_ O layout de entrada do fluxo de estado do pipeline CD3DX12 é uma especialização de TYPEDEF do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definido da seguinte maneira:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_INPUT_LAYOUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_INPUT_LAYOUT>
    CD3DX12_PIPELINE_STATE_STREAM_INPUT_LAYOUT;
          
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

 

