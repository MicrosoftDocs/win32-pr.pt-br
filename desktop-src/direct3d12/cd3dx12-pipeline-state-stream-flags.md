---
title: CD3DX12_PIPELINE_STATE_STREAM_FLAGS (D3dx12.h)
description: Uma estrutura auxiliar usada para descrever sinalizadores de estado de pipeline como um único objeto adequado para uma descrição de fluxo.
ms.assetid: EF67936B-315A-4B3F-9E07-7CF4C5EE47CF
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_FLAGS estrutura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_FLAGS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d8789fb8c393ecaf83e0295654092b22aba7f497abf909c46bac422d442c6fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530703"
---
# <a name="cd3dx12_pipeline_state_stream_flags-structure"></a>Estrutura DE SINALIZADORES DE FLUXO \_ DE ESTADO DE PIPELINE CD3DX12 \_ \_ \_

Uma estrutura auxiliar usada para descrever sinalizadores de estado de pipeline como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_FLAGS {
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
                                      CD3DX12_PIPELINE_STATE_STREAM_FLAGS(D3D12_PIPELINE_STATE_FLAGS const &i);
  CD3DX12_PIPELINE_STATE_STREAM_FLAGS operator=(D3D12_PIPELINE_STATE_FLAGS const& i);
                                      operator D3D12_PIPELINE_STATE_FLAGS() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**SINALIZADORES DE FLUXO DE ESTADO DO PIPELINE CD3DX12 \_ \_ \_ \_**
</dt> <dd>

Cria uma nova instância, não reinicializada, de um SINALIZADOR DE FLUXO DE ESTADO DE PIPELINE CD3DX12. \_ \_ \_ \_

</dd> <dt>

**SINALIZADORES DE FLUXO DE ESTADO DE PIPELINE CD3DX12 \_ \_ \_ \_ (D3D12 \_ PIPELINE \_ STATE \_ FLAGS const &i)**
</dt> <dd>

Cria uma nova instância de UM SINALIZADOR DE FLUXO DE ESTADO DE PIPELINE CD3DX12, inicializado com um tipo de subobjeto de SINALIZADORES DE TIPO DE SUBOBJETO DE ESTADO DE PIPELINE \_ D3D12 e dados de subobjeto \_ \_ \_ **\_ \_ \_ \_ \_ copiados** de *i*, uma estrutura [**D3D12 \_ PIPELINE \_ STATE \_ FLAGS.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)

</dd> <dt>

**operator=(D3D12 \_ PIPELINE \_ STATE \_ FLAGS const& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**operador D3D12 \_ PIPELINE \_ STATE \_ FLAGS() const**
</dt> <dd>

Conversão implícita em uma [**estrutura D3D12 \_ PIPELINE STATE \_ \_ FLAGS.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_flags)

</dd> </dl>

## <a name="remarks"></a>Comentários

OS SINALIZADORES DE FLUXO DE ESTADO DE PIPELINE CD3DX12 é uma especialização typedef do modelo \_ \_ \_ \_ [**\_ \_ \_ \_ SUBOBJECT DE**](cd3dx12-pipeline-state-stream-subobject.md) FLUXO DE ESTADO DO PIPELINE CD3DX12 e é definido da seguinte forma:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_PIPELINE_STATE_FLAGS, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_FLAGS>
    CD3DX12_PIPELINE_STATE_STREAM_FLAGS;
          
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

 

