---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever uma descrição de estêncil de profundidade como um único objeto adequado para uma descrição de fluxo. | Estrutura de CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL (D3dx12. h)
ms.assetid: 4FB54EA5-FCC6-4B64-A747-27DFE4C1D2DC
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb24779aeff950bd213ce18774f55493777df9c9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105757181"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil-structure"></a>\_Estrutura de \_ \_ estêncil de profundidade do fluxo de estado do \_ pipeline CD3DX12 \_

Uma estrutura auxiliar usada para descrever uma descrição de estêncil de profundidade como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL {
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
                                              CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL(CD3DX12_DEPTH_STENCIL_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL operator=(CD3DX12_DEPTH_STENCIL_DESC const& i);
                                              operator CD3DX12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Estêncil de \_ profundidade do fluxo de estado do pipeline CD3DX12 \_ \_ \_**
</dt> <dd>

Cria uma nova instância, não inicializada, de um \_ estêncil de profundidade de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**\_ \_ \_ \_ \_ Estêncil de profundidade de fluxo de estado de pipeline CD3DX12 ( \_ estêncil de profundidade CD3DX12 \_ \_ desc const &i)**
</dt> <dd>

Cria uma nova instância de um estêncil de profundidade do fluxo de estado do pipeline do CD3DX12 \_ \_ \_ \_ \_ , inicializado com um tipo de subobjeto do subobjeto do **estado do pipeline D3D12 de \_ \_ \_ \_ \_ \_ estêncil** de profundidade e dados de subobjeto copiados de *i*, uma estrutura [**desc de \_ estêncil de profundidade \_ \_ CD3DX12**](cd3dx12-depth-stencil-desc.md) .

</dd> <dt>

**Operator = ( \_ estêncil de profundidade CD3DX12 \_ \_ desc const& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**\_ \_ \_ const do estêncil de profundidade do CD3DX12 do operador DESC ()**
</dt> <dd>

Conversão implícita em uma [**estrutura \_ \_ \_ desc de estêncil de profundidade de CD3DX12**](cd3dx12-depth-stencil-desc.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

\_ \_ \_ \_ \_ O estêncil de profundidade do fluxo de estado do pipeline CD3DX12 é uma especialização de TYPEDEF do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definido da seguinte maneira:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL;
          
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

 

