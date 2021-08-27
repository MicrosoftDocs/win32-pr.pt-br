---
title: CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK (D3dx12.h)
description: Uma estrutura auxiliar usada para descrever uma máscara de nó como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 5C770D9A-D692-46CF-8D60-EE5EB04998C8
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK estrutura
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
ms.openlocfilehash: 0f4850ff986f2006c506d79a8ece1ced873529c2a4939869cd704a4b7c3c4b03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119676"
---
# <a name="cd3dx12_pipeline_state_stream_node_mask-structure"></a>Estrutura CD3DX12 \_ PIPELINE STATE STREAM NODE \_ \_ \_ \_ MASK

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

**MÁSCARA DE NÓ DE FLUXO DE \_ ESTADO DO PIPELINE CD3DX12 \_ \_ \_ \_**
</dt> <dd>

Cria uma nova instância, não reinicializada, de uma MÁSCARA DE NÓ DE FLUXO DE ESTADO DE PIPELINE CD3DX12. \_ \_ \_ \_ \_

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM NODE \_ \_ \_ \_ MASK(UINT const &i)**
</dt> <dd>

Cria uma nova instância de uma MÁSCARA DE NÓ DE FLUXO DE ESTADO DE PIPELINE CD3DX12, inicializada com um \_ \_ tipo de \_ \_ \_ subobjeto **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT \_ TYPE NODE \_ \_ MASK** e dados de subobjeto   copiados de i , uma máscara de nó UINT.

</dd> <dt>

**operator=(UINT const& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**operator UINT() const**
</dt> <dd>

Conversão implícita em uma **máscara de nó UINT.**

</dd> </dl>

## <a name="remarks"></a>Comentários

CD3DX12 PIPELINE STATE STREAM NODE MASK é uma especialização typedef do modelo \_ \_ \_ \_ \_ [**\_ \_ \_ \_ SUBOBJECT DE**](cd3dx12-pipeline-state-stream-subobject.md) FLUXO DE ESTADO DO PIPELINE CD3DX12 e é definido da seguinte forma:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<UINT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_NODE_MASK>
    CD3DX12_PIPELINE_STATE_STREAM_NODE_MASK;
          
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ SUBOBJECT**](cd3dx12-pipeline-state-stream-subobject.md)
</dt> <dt>

[**TIPO DE \_ \_ \_ SUBOBJETO DE ESTADO DO PIPELINE D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

