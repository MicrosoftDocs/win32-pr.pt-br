---
title: CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT (D3dx12.h)
description: Uma estrutura auxiliar modelo usada para encapsular pares de dados de subobjeto e tipo de subobjeto como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 4C59D483-6ED8-49BD-B91B-2A912AFE2409
keywords:
- CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT estrutura
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
ms.openlocfilehash: 5d945296ae4ee09710b74b9fdf2259251632d25fb309ede2983858c0c59be72d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729476"
---
# <a name="cd3dx12_pipeline_state_stream_subobject-structure"></a>Estrutura \_ \_ \_ \_ SUBOBJECT DO FLUXO DE ESTADO DO PIPELINE CD3DX12

Uma estrutura auxiliar modelo usada para encapsular pares de dados de subobjeto e tipo de subobjeto como um único objeto adequado para uma descrição de fluxo.

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

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ SUBOBJECT**
</dt> <dd>

Cria uma nova instância, não reinicializada, de um \_ \_ \_ SUBOBJECT DE FLUXO DE ESTADO DE PIPELINE CD3DX12. \_

</dd> <dt>

**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ SUBOBJECT(** InnerStructType** const &i)**
</dt> <dd>

Cria uma nova instância de modelo SUBOBJECT DE FLUXO DE ESTADO DE PIPELINE CD3DX12, inicializada com um \_ \_ tipo de \_ \_ subobjeto [**D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT \_ TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) e dados de subobjeto copiados de i . O tipo de subobjeto e o tipo de dados subobjeto são dados como parâmetros de modelo, **Type** e **InnerStructType,** respectivamente. Para obter mais informações, consulte Comentários abaixo.

</dd> <dt>

**operator=(** InnerStructType** const& i)**
</dt> <dd>

Operador de atribuição de cópia.

</dd> <dt>

**operator **InnerStructType**() const**
</dt> <dd>

Conversão implícita para o tipo de dados subobjeto dado pelo **parâmetro de modelo InnerStructType.**

</dd> </dl>

## <a name="remarks"></a>Comentários

CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ SUBOBJECT é um modelo definido da seguinte forma:


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



O parâmetro **de modelo InnerStructType** especifica o tipo de dados subobjeto; ou seja, os detalhes do subobjeto a serem codificados em um fluxo. O parâmetro de **modelo Type** especifica o tipo de subobjeto; ou seja, o tipo da estrutura especificada pelo parâmetro de modelo **InnerStructType**. O parâmetro de modelo **DefaultArg** especifica um valor opcional para o quais os dados de subobjeto serão inicializados quando uma instância da instanciação de modelo correspondente for construída por padrão; por exemplo, para construir um [**CD3DX12 \_ PIPELINE STATE STREAM BLEND \_ \_ \_ \_ DESC**](cd3dx12-pipeline-state-stream-blend-desc.md) inicializado com padrões comuns de blend-state usando [**CD3DX12 \_ DEFAULT**](cd3dx12-default.md).

Aqui estão as instações de modelo definidas:

-   [**SINALIZADORES DE FLUXO DE ESTADO DO PIPELINE CD3DX12 \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-flags.md)
-   [**MÁSCARA DE NÓ DE FLUXO DE \_ ESTADO DO PIPELINE CD3DX12 \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-node-mask.md)
-   [**ASSINATURA RAIZ DO FLUXO DE \_ ESTADO DO PIPELINE CD3DX12 \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-root-signature.md)
-   [**LAYOUT DE ENTRADA DE FLUXO DE \_ ESTADO DO PIPELINE CD3DX12 \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-input-layout.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ IB \_ STRIP \_ CUT \_ VALUE**](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)
-   [**TOPOLOGIA PRIMITIVA DO FLUXO DE \_ ESTADO DO PIPELINE CD3DX12 \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-primitive-topology.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ VS**](cd3dx12-pipeline-state-stream-vs.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ GS**](cd3dx12-pipeline-state-stream-gs.md)
-   [**SAÍDA DE FLUXO DE FLUXO DE \_ ESTADO DO PIPELINE CD3DX12 \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-stream-output.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ HS**](cd3dx12-pipeline-state-stream-hs.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ DS**](cd3dx12-pipeline-state-stream-ds.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ PS**](cd3dx12-pipeline-state-stream-ps.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ CS**](cd3dx12-pipeline-state-stream-cs.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ BLEND \_ DESC**](cd3dx12-pipeline-state-stream-blend-desc.md)
-   [**ESTÊNCIL DE PROFUNDIDADE DE FLUXO \_ DE ESTADO DO PIPELINE CD3DX12 \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-depth-stencil.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ DEPTH \_ STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md)
-   [**FORMATO DE \_ \_ \_ \_ \_ ESTÊNCIL DE PROFUNDIDADE DO FLUXO DE ESTADO DO PIPELINE \_ CD3DX12**](cd3dx12-pipeline-state-stream-depth-stencil-format.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ RASTERIZER**](cd3dx12-pipeline-state-stream-rasterizer.md)
-   [**FORMATOS DE DESTINO DE RENDERIZAÇÃO DO \_ FLUXO DE ESTADO DO PIPELINE CD3DX12 \_ \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-render-target-formats.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ SAMPLE \_ DESC**](cd3dx12-pipeline-state-stream-sample-desc.md)
-   [**MÁSCARA DE EXEMPLO DE FLUXO DE \_ ESTADO DO PIPELINE CD3DX12 \_ \_ \_ \_**](cd3dx12-pipeline-state-stream-sample-mask.md)
-   [**CD3DX12 \_ PIPELINE \_ STATE \_ STREAM \_ CACHED \_ PSO**](cd3dx12-pipeline-state-stream-cached-pso.md)

As estruturas CD3DX12 PIPELINE STATE STREAM [**\_ BLEND \_ \_ \_ \_ DESC**](cd3dx12-pipeline-state-stream-blend-desc.md), [**CD3DX12 PIPELINE \_ STATE STREAM DEPTH \_ \_ \_ \_ STENCIL**](cd3dx12-pipeline-state-stream-depth-stencil.md), [**CD3DX12 \_ PIPELINE STATE STREAM DEPTH \_ \_ \_ \_ STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md)e [**CD3DX12 \_ PIPELINE STATE STREAM \_ \_ \_ RASTERIZER**](cd3dx12-pipeline-state-stream-rasterizer.md) são definidas para inicializar seus dados de subobjeto com padrões comuns usando [**CD3DX12 \_ DEFAULT**](cd3dx12-default.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**TIPO DE \_ \_ \_ SUBOBJETO DE ESTADO DO PIPELINE D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

