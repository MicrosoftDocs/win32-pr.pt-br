---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT (D3dx12. h)
description: Uma estrutura auxiliar de modelo usada para encapsular os pares de dados de tipo de subobjeto e subobjeto como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 4C59D483-6ED8-49BD-B91B-2A912AFE2409
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11353581dddc2bd0d438b955d1292b667fba39ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793837"
---
# <a name="cd3dx12_pipeline_state_stream_subobject-structure"></a>\_Estrutura de \_ \_ subobjeto de fluxo do estado do pipeline CD3DX12 \_

Uma estrutura auxiliar de modelo usada para encapsular os pares de dados de tipo de subobjeto e subobjeto como um único objeto adequado para uma descrição de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT {
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT;
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT operator=(InnerStructType const& i);
                                          operator InnerStructType() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**Subobjeto de fluxo do estado do \_ pipeline CD3DX12 \_ \_ \_**
</dt> <dd>

Cria uma nova instância, não inicializada, de um \_ subobjeto de fluxo de estado de pipeline CD3DX12 \_ \_ \_ .

</dd> <dt>

**CD3DX12 \_ \_Subobjeto \_ \_ de fluxo do estado do pipeline (** InnerStructType * * const &i) * *
</dt> <dd>

Cria uma nova \_ \_ \_ \_ instância de modelo de subobjeto de fluxo de estado de pipeline do CD3DX12, inicializada com um tipo de subobjeto do tipo de subobjeto do [**estado do \_ pipeline \_ \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) e dados de subobjeto copiados de i. Tanto o tipo de subobjeto quanto o tipo de dados de subobjeto são fornecidos como parâmetros de modelo, **Type** e **InnerStructType**, respectivamente. Para obter mais informações, consulte os comentários abaixo.

</dd> <dt>

**Operator = (** InnerStructType * * const& i) * *
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**constante **InnerStructType**() de operador**
</dt> <dd>

Conversão implícita para o tipo de dados de subobjeto fornecido pelo parâmetro de modelo **InnerStructType** .

</dd> </dl>

## <a name="remarks"></a>Comentários

O \_ \_ subobjeto de fluxo do estado do pipeline CD3DX12 \_ \_ é um modelo definido da seguinte maneira:


```C++
template <typename InnerStructType, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE Type, typename DefaultArg = InnerStructType>
class alignas(void*) CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
{
private:
    D3D12_PIPELINE_STATE_SUBOBJECT_TYPE _Type;
    InnerStructType _Inner;
public:
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT() : _Type(Type), _Inner(DefaultArg()) {}
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const& i) : _Type(Type), _Inner(i) {}
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT& operator=(InnerStructType const& i) { _Inner = i; return *this; }
    operator InnerStructType() const { return _Inner; }
};  
          
```



O parâmetro de modelo **InnerStructType** especifica o tipo de dados de subobjeto; ou seja, os detalhes do subobjeto a serem codificados em um fluxo. O **tipo** de parâmetro de modelo especifica o tipo de subobjeto; ou seja, o tipo da estrutura especificada pelo parâmetro de modelo **InnerStructType**. O parâmetro de modelo **defaultArg** especifica um valor opcional para o qual os dados de subobjeto serão inicializados quando uma instância da instanciação de modelo correspondente é construída por padrão; por exemplo, para construir por padrão um [**fluxo de estado do pipeline do CD3DX12, o \_ \_ \_ Stream \_ Blend \_ desc**](cd3dx12-pipeline-state-stream-blend-desc.md) foi inicializado com padrões de estado de mesclagem comuns usando o [**\_ padrão CD3DX12**](cd3dx12-default.md).

Aqui estão as instanciações de modelo que são definidas:

-   [**\_Sinalizadores de \_ fluxo de estado do pipeline CD3DX12 \_ \_**](cd3dx12-pipeline-state-stream-flags.md)
-   [**\_Máscara de \_ nó de fluxo de estado de pipeline CD3DX12 \_ \_ \_**](cd3dx12-pipeline-state-stream-node-mask.md)
-   [**\_ \_ \_ Assinatura raiz do fluxo de estado \_ do pipeline CD3DX12 \_**](cd3dx12-pipeline-state-stream-root-signature.md)
-   [**\_Layout de \_ entrada de fluxo de estado de pipeline CD3DX12 \_ \_ \_**](cd3dx12-pipeline-state-stream-input-layout.md)
-   [**\_Valor de \_ \_ \_ \_ \_ recorte de faixa \_ do Stream IB do CD3DX12 pipeline**](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)
-   [**\_ \_ \_ Topologia primitiva de fluxo de estado \_ de pipeline CD3DX12 \_**](cd3dx12-pipeline-state-stream-primitive-topology.md)
-   [**\_Fluxo de estado do pipeline CD3DX12 \_ \_ \_ vs**](cd3dx12-pipeline-state-stream-vs.md)
-   [**\_Fluxo de estado do pipeline CD3DX12 \_ \_ \_ GS**](cd3dx12-pipeline-state-stream-gs.md)
-   [**\_Saída de \_ fluxo de fluxo de estado de pipeline CD3DX12 \_ \_ \_**](cd3dx12-pipeline-state-stream-stream-output.md)
-   [**Fluxo de estado de pipeline do CD3DX12 \_ \_ \_ \_ HS**](cd3dx12-pipeline-state-stream-hs.md)
-   [**Fluxo de estado do pipeline do CD3DX12 \_ \_ \_ \_ DS**](cd3dx12-pipeline-state-stream-ds.md)
-   [**\_PS de \_ fluxo de estado do pipeline CD3DX12 \_ \_**](cd3dx12-pipeline-state-stream-ps.md)
-   [**\_Fluxo de \_ estado do pipeline \_ do CD3DX12 \_**](cd3dx12-pipeline-state-stream-cs.md)
-   [**\_ \_ \_ Stream \_ Blend de estado \_ do pipeline CD3DX12**](cd3dx12-pipeline-state-stream-blend-desc.md)
-   [**\_Estêncil de \_ profundidade do fluxo de estado do pipeline CD3DX12 \_ \_ \_**](cd3dx12-pipeline-state-stream-depth-stencil.md)
-   [**\_STENCIL1 de \_ profundidade de fluxo de estado de pipeline CD3DX12 \_ \_ \_**](cd3dx12-pipeline-state-stream-depth-stencil1.md)
-   [**\_Formato de \_ \_ estêncil de profundidade do fluxo de estado \_ do \_ pipeline CD3DX12 \_**](cd3dx12-pipeline-state-stream-depth-stencil-format.md)
-   [**\_ \_ \_ Rasterizador de fluxo de estado de pipeline CD3DX12 \_**](cd3dx12-pipeline-state-stream-rasterizer.md)
-   [**\_Formatos de \_ \_ destino de renderização de fluxo de estado \_ de \_ pipeline CD3DX12 \_**](cd3dx12-pipeline-state-stream-render-target-formats.md)
-   [**\_Exemplo de fluxo de estado do pipeline CD3DX12 \_ \_ \_ \_ desc**](cd3dx12-pipeline-state-stream-sample-desc.md)
-   [**\_Máscara de \_ exemplo de fluxo de estado de pipeline CD3DX12 \_ \_ \_**](cd3dx12-pipeline-state-stream-sample-mask.md)
-   [**PSO do fluxo de estado do pipeline do CD3DX12 \_ \_ \_ \_ em cache \_**](cd3dx12-pipeline-state-stream-cached-pso.md)

O [**CD3DX12 \_ pipeline \_ State \_ Stream \_ Blend \_**](cd3dx12-pipeline-state-stream-blend-desc.md), o [**\_ \_ \_ \_ \_ estêncil profundidade do fluxo do CD3DX12**](cd3dx12-pipeline-state-stream-depth-stencil.md)do pipeline, o CD3DX12 pipeline de nível de fluxo de perfil [**\_ \_ \_ \_ \_ STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md)e as estruturas do [**\_ \_ \_ \_ rasterizador de fluxo de perfil CD3DX12**](cd3dx12-pipeline-state-stream-rasterizer.md) são definidas para inicializar seus dados de subobjeto com padrões comuns usando [**CD3DX12 \_ padrão**](cd3dx12-default.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_Tipo de \_ subobjeto de estado de pipeline D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

