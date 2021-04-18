---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever uma descrição do rasterizador como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 650C2DA3-63FB-44D1-BE9A-E21E13DA24DB
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f656ad354430b00e757ece0aa2ce482de1f06e2e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105810694"
---
# <a name="cd3dx12_pipeline_state_stream_rasterizer-structure"></a>\_Estrutura do \_ \_ rasterizador de fluxo de estado do pipeline CD3DX12 \_

Uma estrutura auxiliar usada para descrever uma descrição do rasterizador como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER {
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
                                           CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER(CD3DX12_RASTERIZER_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER operator=(CD3DX12_RASTERIZER_DESC const& i);
                                           operator CD3DX12_RASTERIZER_DESC() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_ \_ \_ Rasterizador de fluxo de estado de pipeline CD3DX12 \_**
</dt> <dd>

Cria uma nova instância, não inicializada, de um \_ rasterizador de fluxo de estado de pipeline CD3DX12 \_ \_ \_ .

</dd> <dt>

**\_ \_ \_ \_ Rasterizador de fluxo de estado de pipeline CD3DX12 (CD3DX12 do \_ rasterizador \_ desc const &i)**
</dt> <dd>

Cria uma nova instância do \_ rasterizador de fluxo de estado do pipeline do CD3DX12 \_ \_ \_ , inicializada com um tipo de subobjeto do tipo de subobjeto do **\_ estado do pipeline \_ \_ \_ \_ D3D12** e dados de subobjetos copiados de *i*, uma estrutura [**\_ \_ Desc do rasterizador CD3DX12**](cd3dx12-rasterizer-desc.md) .

</dd> <dt>

**Operator = (CD3DX12 do \_ rasterizador \_ DESC const& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**\_const do rasterizador CD3DX12 \_ do operador DESC ()**
</dt> <dd>

Conversão implícita em uma [**estrutura \_ \_ Desc do rasterizador CD3DX12**](cd3dx12-rasterizer-desc.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

\_ \_ \_ \_ O rasterizador de fluxo de estado de pipeline CD3DX12 é uma especialização de typedef do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definido da seguinte maneira:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_RASTERIZER_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RASTERIZER, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER;
          
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

 

