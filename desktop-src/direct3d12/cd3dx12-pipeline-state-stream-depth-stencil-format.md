---
title: CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT (D3dx12.h)
description: Uma estrutura auxiliar usada para descrever o formato de estêncil de profundidade como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 512DB46E-D8F0-482B-9174-C786FB91AFD2
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT estrutura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9658f1df1fbe316fa9f308b9f8e0589f0f93858916c6dbde4607fd11a6f0707f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751946"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil_format-structure"></a>Estrutura CD3DX12 \_ PIPELINE STATE STREAM DEPTH \_ \_ \_ \_ FORMAT \_

Uma estrutura auxiliar usada para descrever o formato de estêncil de profundidade como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT {
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
                                                     CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT(DXGI_FORMAT const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT operator=(DXGI_FORMAT const& i);
                                                     operator DXGI_FORMAT() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**FORMATO DE \_ \_ \_ \_ \_ ESTÊNCIL DE PROFUNDIDADE DO FLUXO DE ESTADO DO PIPELINE \_ CD3DX12**
</dt> <dd>

Cria uma nova instância, não reinicializada, de um FORMATO DE ESTÊNCIL DE PROFUNDIDADE DE FLUXO DE ESTADO DE PIPELINE CD3DX12. \_ \_ \_ \_ \_ \_

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM DEPTH \_ \_ \_ \_ STENCIL \_ FORMAT(DXGI \_ FORMAT const &i)**
</dt> <dd>

Cria uma nova instância de um FORMATO DE STENCIL DE PROFUNDIDADE DE FLUXO DE ESTADO DE PIPELINE CD3DX12, inicializado com um \_ \_ tipo de \_ \_ \_ \_ subobjeto **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT \_ TYPE DEPTH \_ \_ STENCIL \_ FORMAT** e dados de subobjeto copiados de *i*, uma enumeração [**DXGI \_ FORMAT.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

</dd> <dt>

**operator=(DXGI \_ FORMAT const& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**operator DXGI \_ FORMAT() const**
</dt> <dd>

Conversão implícita em uma [**enumeração DXGI \_ FORMAT.**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

</dd> </dl>

## <a name="remarks"></a>Comentários

CD3DX12 PIPELINE STATE STREAM DEPTH STENCIL FORMAT é uma especialização typedef do modelo \_ \_ \_ \_ \_ \_ [**\_ \_ \_ \_ SUBOBJECT DE**](cd3dx12-pipeline-state-stream-subobject.md) FLUXO DE ESTADO DO PIPELINE CD3DX12 e é definido da seguinte forma:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_FORMAT, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL_FORMAT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL_FORMAT;
          
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

 

