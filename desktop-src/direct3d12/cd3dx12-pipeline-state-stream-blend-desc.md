---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever uma descrição de Blend como um único objeto adequado para uma descrição de fluxo.
ms.assetid: A629B05D-0A70-4C96-9F66-1508F2667BF6
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d251be9cc1423babc58e1d3c3be87c5345308874
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781434"
---
# <a name="cd3dx12_pipeline_state_stream_blend_desc-structure"></a>\_ \_ \_ \_ Estrutura desc de fluxo de estado do pipeline do \_ CD3DX12

Uma estrutura auxiliar usada para descrever uma descrição de Blend como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC {
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
                                           CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC(CD3DX12_BLEND_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC operator=(CD3DX12_BLEND_DESC const& i);
                                           operator CD3DX12_BLEND_DESC() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_ \_ \_ Stream \_ Blend de estado \_ do pipeline CD3DX12**
</dt> <dd>

Cria uma nova instância, não inicializada, de um \_ fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**\_ \_ \_ Stream \_ Blend do CD3DX12 pipeline \_ de transmissão de perfil (CD3DX12 \_ Blend \_ desc const &i)**
</dt> <dd>

Cria uma nova instância de um fluxo de estado de pipeline do CD3DX12 \_ \_ \_ \_ \_ , inicializado com um tipo de subobjeto do subobjeto de **estado do pipeline D3D12 de \_ \_ \_ \_ \_ mistura** e dados de subobjeto copiados de *i*, uma estrutura [**desc de CD3DX12 \_ Blend \_**](cd3dx12-blend-desc.md) .

</dd> <dt>

**Operator = (CD3DX12 \_ Blend \_ DESC const& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**\_constante do operador CD3DX12 Blend \_ () const**
</dt> <dd>

Conversão implícita em uma [**estrutura \_ \_ Desc do CD3DX12 Blend**](cd3dx12-blend-desc.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

\_ \_ \_ O fluxo de estado do pipeline do CD3DX12 \_ do Stream Blend \_ DESC é uma especialização de TYPEDEF do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definido da seguinte maneira:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_BLEND_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_BLEND, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
          
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

 

