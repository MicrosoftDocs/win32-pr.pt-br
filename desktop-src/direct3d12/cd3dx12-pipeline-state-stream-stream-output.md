---
title: CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT (D3dx12.h)
description: Uma estrutura auxiliar usada para descrever a descrição da saída do fluxo como um único objeto adequado para uma descrição de fluxo.
ms.assetid: CC7E1E76-CD44-4D70-A5B8-7C2B6210468E
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT estrutura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0dbaf9952575801846adfbbb825c2ddbdc2e90d9d8d64f60f373ea2bcc1be0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119666"
---
# <a name="cd3dx12_pipeline_state_stream_stream_output-structure"></a>Estrutura DE SAÍDA DE FLUXO DE FLUXO \_ DE ESTADO DO PIPELINE CD3DX12 \_ \_ \_ \_

Uma estrutura auxiliar usada para descrever a descrição da saída do fluxo como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT {
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
                                              CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT(D3D12_STREAM_OUTPUT_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT operator=(D3D12_STREAM_OUTPUT_DESC const& i);
                                              operator D3D12_STREAM_OUTPUT_DESC() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**SAÍDA DE FLUXO DE FLUXO DE \_ ESTADO DO PIPELINE CD3DX12 \_ \_ \_ \_**
</dt> <dd>

Cria uma nova instância, não reinicializada, de uma SAÍDA DE FLUXO DE FLUXO DE ESTADO DE PIPELINE CD3DX12. \_ \_ \_ \_ \_

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM STREAM OUTPUT \_ \_ \_ \_ (D3D12 \_ STREAM OUTPUT \_ \_ DESC const &i)**
</dt> <dd>

Cria uma nova instância de uma SAÍDA DE FLUXO DE FLUXO DE ESTADO DE PIPELINE CD3DX12, inicializada com um \_ \_ tipo de \_ \_ \_ subobjeto **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT \_ TYPE STREAM \_ \_ OUTPUT** e dados de subobjeto copiados de i , uma estrutura [**D3D12 \_ STREAM OUTPUT \_ \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)

</dd> <dt>

**operator=(D3D12 \_ STREAM \_ OUTPUT \_ DESC const& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**operador D3D12 \_ STREAM \_ OUTPUT \_ DESC() const**
</dt> <dd>

Conversão implícita em uma [**estrutura D3D12 \_ STREAM OUTPUT \_ \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc)

</dd> </dl>

## <a name="remarks"></a>Comentários

CD3DX12 PIPELINE STATE STREAM OUTPUT é uma especialização typedef do modelo \_ \_ \_ \_ \_ [**\_ \_ \_ \_ SUBOBJECT DE**](cd3dx12-pipeline-state-stream-subobject.md) FLUXO DE ESTADO DO PIPELINE CD3DX12 e é definida da seguinte forma:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_STREAM_OUTPUT_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_STREAM_OUTPUT>
    CD3DX12_PIPELINE_STATE_STREAM_STREAM_OUTPUT;
          
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

 

