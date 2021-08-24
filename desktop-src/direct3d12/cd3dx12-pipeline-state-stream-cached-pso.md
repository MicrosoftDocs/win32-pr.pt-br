---
title: CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO (D3dx12.h)
description: Uma estrutura auxiliar usada para descrever um PSO armazenado em cache como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 86CDC60A-275D-4B71-BE6D-C863C72E9C05
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO estrutura
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11cb4e7a784b89a825f1e1b64083c50cc77731bbadf84d248106d69da9cf737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751916"
---
# <a name="cd3dx12_pipeline_state_stream_cached_pso-structure"></a>Estrutura \_ \_ \_ \_ \_ PSO EM CACHE DO FLUXO DE ESTADO DO PIPELINE CD3DX12

Uma estrutura auxiliar usada para descrever um PSO armazenado em cache como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO {
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
                                           CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO(D3D12_CACHED_PIPELINE_STATE const &i);
  CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO operator=(D3D12_CACHED_PIPELINE_STATE const& i);
                                           operator D3D12_CACHED_PIPELINE_STATE() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ CACHED \_ PSO**
</dt> <dd>

Cria uma nova instância, não reinicializada, de um \_ \_ \_ \_ PSO ARMAZENADO EM CACHE DE FLUXO DE ESTADO DE PIPELINE CD3DX12. \_

</dd> <dt>

**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ \_ PSO(D3D12 \_ CACHED PIPELINE STATE const &\_ \_ i)**
</dt> <dd>

Cria uma nova instância de um PSO COM CACHE DE FLUXO DE ESTADO DE PIPELINE CD3DX12, inicializado com um \_ \_ tipo de \_ \_ \_ subobjeto **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT \_ TYPE \_ CACHED \_ PSO** e dados de subobjeto copiados de i , uma estrutura [**D3D12 \_ ESTADO \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state) DE PIPELINE ARMAZENADO EM CACHE.

</dd> <dt>

**operator=(D3D12 \_ CACHED \_ PIPELINE STATE const \_& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**operador D3D12 \_ CACHED \_ PIPELINE \_ STATE() const**
</dt> <dd>

Conversão implícita em uma [**estrutura D3D12 \_ CACHED \_ PIPELINE \_ STATE.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state)

</dd> </dl>

## <a name="remarks"></a>Comentários

CD3DX12 PIPELINE STATE STREAM CACHED PSO é uma especialização typedef do modelo \_ \_ \_ \_ \_ [**\_ \_ \_ \_ SUBOBJECT DE**](cd3dx12-pipeline-state-stream-subobject.md) FLUXO DE ESTADO DO PIPELINE CD3DX12 e é definido da seguinte forma:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<D3D12_CACHED_PIPELINE_STATE, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CACHED_PSO>
    CD3DX12_PIPELINE_STATE_STREAM_CACHED_PSO;
          
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

 

