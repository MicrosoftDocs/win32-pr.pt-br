---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever uma máscara de nó como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 5C770D9A-D692-46CF-8D60-EE5EB04998C8
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c364ecd20459d8c20bdd3d30b969cc3b9ae46d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105750183"
---
# <a name="cd3dx12_pipeline_state_stream_node_mask-structure"></a>\_Estrutura de \_ \_ máscara do \_ nó de fluxo \_ do CD3DX12 pipeline

Uma estrutura auxiliar usada para descrever uma máscara de nó como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK {
                                          CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
                                          CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK(UINT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK operator=(UINT const& i);
                                          operator UINT() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Máscara de \_ nó de fluxo de estado de pipeline CD3DX12 \_ \_ \_**
</dt> <dd>

Cria uma nova instância, não inicializada, de uma \_ máscara de nó de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**\_ \_ \_ \_ \_ Máscara do nó de fluxo do CD3DX12 pipeline (UINT const &i)**
</dt> <dd>

Cria uma nova instância de uma \_ máscara de nó de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ , inicializada com um tipo de subobjeto de  tipo de subobjeto de estado de **\_ pipeline \_ \_ \_ \_ \_ D3D12** e dados de subobjetos copiados de i, uma máscara de nó uint.

</dd> <dt>

**Operator = (UINT const& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**constante de operador UINT ()**
</dt> <dd>

Conversão implícita em uma máscara de nó **uint** .

</dd> </dl>

## <a name="remarks"></a>Comentários

\_ \_ \_ \_ \_ A máscara do nó de fluxo do estado do pipeline CD3DX12 é uma especialização de TYPEDEF do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definida da seguinte maneira:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<UINT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_NODE_MASK>
    CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
          
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

 

