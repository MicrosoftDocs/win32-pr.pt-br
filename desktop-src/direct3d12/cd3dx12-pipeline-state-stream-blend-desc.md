---
title: CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC (D3dx12.h)
description: Uma estrutura auxiliar usada para descrever uma descrição de mesclagem como um único objeto adequado para uma descrição de fluxo.
ms.assetid: A629B05D-0A70-4C96-9F66-1508F2667BF6
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC estrutura
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
ms.openlocfilehash: 300506d2c41be5a5380f4f0f64c93779185fd59ced2e0dd613d926f8397ea85c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752166"
---
# <a name="cd3dx12_pipeline_state_stream_blend_desc-structure"></a>Estrutura CD3DX12 \_ PIPELINE STATE STREAM BLEND \_ \_ \_ \_ DESC

Uma estrutura auxiliar usada para descrever uma descrição de mesclagem como um único objeto adequado para uma descrição de fluxo.

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

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ BLEND \_ DESC**
</dt> <dd>

Cria uma nova instância, não reinicializada, de uma CD3DX12 \_ PIPELINE STATE STREAM BLEND \_ \_ \_ \_ DESC.

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM BLEND \_ \_ \_ \_ DESC(CD3DX12 \_ BLEND \_ DESC const &i)**
</dt> <dd>

Cria uma nova instância de um CD3DX12 PIPELINE STATE STREAM BLEND DESC, inicializada com um \_ \_ tipo de \_ \_ \_ subobjeto **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT \_ TYPE \_ BLEND** e dados de subobjeto copiados de i , uma estrutura [**CD3DX12 \_ BLEND \_ DESC.**](cd3dx12-blend-desc.md)

</dd> <dt>

**operator=(CD3DX12 \_ BLEND \_ DESC const& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**operador CD3DX12 \_ BLEND \_ DESC() const**
</dt> <dd>

Conversão implícita em uma [**estrutura CD3DX12 \_ BLEND \_ DESC.**](cd3dx12-blend-desc.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

CD3DX12 PIPELINE STATE STREAM BLEND DESC é uma especialização typedef do modelo \_ \_ \_ \_ \_ [**\_ \_ \_ \_ SUBOBJECT DE**](cd3dx12-pipeline-state-stream-subobject.md) FLUXO DE ESTADO DO PIPELINE CD3DX12 e é definido da seguinte forma:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_BLEND_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_BLEND, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_BLEND_DESC;
          
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

 

