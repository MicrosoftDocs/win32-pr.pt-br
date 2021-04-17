---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever uma descrição de estêncil de profundidade como um único objeto adequado para uma descrição de fluxo. | Estrutura de CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 (D3dx12. h)
ms.assetid: 7D3554D9-610D-43B5-94F0-68167E966A86
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee95e9e37ad1dfced119848c76f071564aaa9435
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105748668"
---
# <a name="cd3dx12_pipeline_state_stream_depth_stencil1-structure"></a>\_ \_ \_ \_ Estrutura STENCIL1 de profundidade de fluxo do CD3DX12 pipeline \_

Uma estrutura auxiliar usada para descrever uma descrição de estêncil de profundidade como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 {
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
                                               CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1(CD3DX12_DEPTH_STENCIL_DESC1 const &i);
  CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1 operator=(CD3DX12_DEPTH_STENCIL_DESC1 const& i);
                                               operator CD3DX12_DEPTH_STENCIL_DESC1() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_STENCIL1 de \_ profundidade de fluxo de estado de pipeline CD3DX12 \_ \_ \_**
</dt> <dd>

Cria uma instância nova e não inicializada de uma STENCIL1 de \_ profundidade de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ .

</dd> <dt>

**CD3DX12 \_ \_ \_ \_ de camada de estado \_ de pipeline de STENCIL1 ( \_ estêncil de profundidade CD3DX12 \_ \_ DESC1 const &i)**
</dt> <dd>

Cria uma nova instância de uma STENCIL1 de profundidade de fluxo de estado de pipeline do CD3DX12 \_ \_ \_ \_ \_ , inicializada com um tipo de subobjeto de subobjeto de **perfil de D3D12 do estado de \_ pipeline \_ \_ \_ \_ \_ STENCIL1** e dados de subobjeto copiados de *i*, uma estrutura [**CD3DX12 de \_ \_ estêncil \_ de profundidade**](cd3dx12-depth-stencil-desc1.md) DESC1.

</dd> <dt>

**Operator = (estêncil de profundidade de CD3DX12 \_ \_ \_ DESC1 const& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**\_ \_ \_ const de estêncil de profundidade de CD3DX12 de operador DESC1 ()**
</dt> <dd>

Conversão implícita em uma [**estrutura \_ \_ \_ DESC1 de estêncil de profundidade de CD3DX12**](cd3dx12-depth-stencil-desc1.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

\_O CD3DX12 \_ pipeline \_ \_ de extensão \_ de fluxo STENCIL1 é uma especialização de TYPEDEF do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definido da seguinte maneira:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<CD3DX12_DEPTH_STENCIL_DESC1, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL1, CD3DX12_DEFAULT>
    CD3DX12_PIPELINE_STATE_STREAM_DEPTH_STENCIL1;
          
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

 

