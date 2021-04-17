---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever uma máscara de exemplo como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 20116DA1-F56D-42CA-A846-42509FAF88C1
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 868a498bec1bbf8c4f55f320765272d04cbdd81c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105790495"
---
# <a name="cd3dx12_pipeline_state_stream_sample_mask-structure"></a>\_Estrutura da \_ \_ máscara de exemplo do fluxo de estado do \_ pipeline CD3DX12 \_

Uma estrutura auxiliar usada para descrever uma máscara de exemplo como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK {
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK;
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK(UINT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK operator=(UINT const& i);
                                            operator UINT() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Máscara de \_ exemplo de fluxo de estado de pipeline CD3DX12 \_ \_ \_**
</dt> <dd>

Cria uma nova instância, não inicializada, de uma \_ máscara de exemplo de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**\_ \_ \_ \_ \_ Máscara de exemplo de fluxo de estado de PIPELINE CD3DX12 (UINT const &i)**
</dt> <dd>

Cria uma nova instância de uma \_ máscara de exemplo de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ , inicializada com um tipo de subobjeto de tipo de subobjeto de **estado de pipeline D3D12 \_ \_ \_ \_ \_ \_ máscara de exemplo** e dados de subobjeto copiados de *i*, uma máscara de exemplo **uint** .

</dd> <dt>

**Operator = (UINT const& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**constante de operador UINT ()**
</dt> <dd>

Conversão implícita em uma máscara de exemplo **uint** .

</dd> </dl>

## <a name="remarks"></a>Comentários

\_ \_ \_ \_ \_ A máscara de exemplo de fluxo de estado do pipeline CD3DX12 é uma especialização de TYPEDEF do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definida da seguinte maneira:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<UINT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_MASK>
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_MASK;
          
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

 

