---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC (D3dx12. h)
description: Uma estrutura auxiliar usada para descrever uma descrição de exemplo como um único objeto adequado para uma descrição de fluxo.
ms.assetid: D84C5373-AC0F-430A-97A1-6125611869B2
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fea786dc0429da28f9c26f0203b06059aff1c17
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813484"
---
# <a name="cd3dx12_pipeline_state_stream_sample_desc-structure"></a>\_ \_ \_ \_ Estrutura desc de amostra de fluxo de estado de pipeline CD3DX12 \_

Uma estrutura auxiliar usada para descrever uma descrição de exemplo como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC {
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
                                            CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC(DXGI_SAMPLE_DESC const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC operator=(DXGI_SAMPLE_DESC const& i);
                                            operator DXGI_SAMPLE_DESC() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Exemplo de fluxo de estado do pipeline CD3DX12 \_ \_ \_ \_ desc**
</dt> <dd>

Cria uma nova instância, não inicializada, de um \_ exemplo de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ desc.

</dd> <dt>

**\_ \_ \_ \_ Exemplo de fluxo de estado \_ do pipeline CD3DX12 DESC (exemplo de dxgi \_ \_ desc const &i)**
</dt> <dd>

Cria uma nova instância de um \_ exemplo de fluxo de estado de pipeline CD3DX12 \_ \_ \_ \_ DESC, inicializada com um tipo de subobjeto de tipo de subobjeto de **estado de pipeline D3D12 amostra de dados \_ \_ \_ \_ \_ \_ desc** e subobjeto copiado de *i*, uma estrutura [**\_ \_ desc de amostra de dxgi**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) .

</dd> <dt>

**Operator = ( \_ exemplo \_ DESC constante& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**\_ \_ const do exemplo de dxgi do operador DESC ()**
</dt> <dd>

Conversão implícita em uma [**estrutura \_ \_ desc de amostra de dxgi**](https://www.bing.com/search?q=**DXGI\_SAMPLE\_DESC**) .

</dd> </dl>

## <a name="remarks"></a>Comentários

\_ \_ \_ \_ Exemplo de fluxo de estado \_ de pipeline CD3DX12 DESC é uma especialização de TYPEDEF do modelo de [**\_ \_ \_ \_ subobjeto Stream do estado do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-subobject.md) e é definida da seguinte maneira:


```C++
typedef CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT<DXGI_SAMPLE_DESC, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_DESC>
    CD3DX12_PIPELINE_STATE_STREAM_SAMPLE_DESC;
          
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

 

