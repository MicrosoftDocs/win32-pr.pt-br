---
title: CD3DX12_PIPELINE_STATE_STREAM_HS (D3dx12.h)
description: Uma estrutura auxiliar usada para descrever um sombreador de chassi como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 4958161D-3E79-4227-ADD7-7F53E34B2175
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_HS estrutura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_HS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5b13c32c9da13a3cfce03605494bc8608a233f5979cb7b2757f203571c7901
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028356"
---
# <a name="cd3dx12_pipeline_state_stream_hs-structure"></a>Estrutura \_ \_ \_ \_ HS DO FLUXO DE ESTADO DO PIPELINE CD3DX12

Uma estrutura auxiliar usada para descrever um sombreador de chassi como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_HS {
                                   CD3DX12_PIPELINE_STATE_STREAM_HS;
                                   CD3DX12_PIPELINE_STATE_STREAM_HS(D3D12_SHADER_BYTECODE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_HS operator=(D3D12_SHADER_BYTECODE const& i);
                                   operator D3D12_SHADER_BYTECODE() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ HS**
</dt> <dd>

Cria uma nova instância, não reinicializada, de um CD3DX12 \_ PIPELINE \_ STATE STREAM \_ \_ HS.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ HS(D3D12 \_ \_ SHADER BYTECODE const &i)**
</dt> <dd>

Cria uma nova instância de um HS DE FLUXO DE ESTADO DE PIPELINE CD3DX12, inicializado com um \_ \_ tipo de \_ \_ subobjeto **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT \_ TYPE \_ HS** e dados de subobjeto copiados de *i*, uma estrutura [**\_ \_ BYTECODE D3D12 SHADER.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)

</dd> <dt>

**operator=(D3D12 \_ SHADER \_ BYTECODE const& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**operador D3D12 \_ SHADER \_ BYTECODE() const**
</dt> <dd>

Conversão implícita em uma [**estrutura D3D12 \_ \_ SHADER BYTECODE.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)

</dd> </dl>

## <a name="remarks"></a>Comentários

CD3DX12 PIPELINE STATE STREAM HS é uma especialização typedef do modelo \_ \_ \_ \_ [**\_ \_ \_ \_ SUBOBJECT DE**](cd3dx12-pipeline-state-stream-subobject.md) FLUXO DE ESTADO DO PIPELINE CD3DX12 e é definido da seguinte forma:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_SHADER_BYTECODE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_HS>
    CD3DX12_PIPELINE_STATE_STREAM_HS;
          
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

 

