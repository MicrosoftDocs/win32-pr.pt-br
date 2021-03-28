---
title: Objeto Stream-Output
description: Um objeto Stream-output é um objeto modelo que transmite dados para fora do estágio Geometry-Shader. Use a sintaxe a seguir para declarar um objeto Stream-output.
ms.assetid: 07a5489c-c238-4466-9282-5b168448aff7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98063ddb45633dda6c897abf0f82f29a394c3f95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366166"
---
# <a name="stream-output-object"></a>Objeto Stream-Output

Um objeto Stream-output é um objeto modelo que transmite dados para fora do [estágio Geometry-Shader](/previous-versions//bb205146(v=vs.85)). Use a sintaxe a seguir para declarar um objeto Stream-output.



| nome de DataType *StreamOutputObject* de InOut <  >  *;* |
|------------------------------------------------------|



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*StreamOutputObject*  <  *Tipo de dados*  >    *Nome* do
</dt> <dd>

A declaração do objeto Stream-Output (portanto).



| Stream-Output tipos de objeto | Description                       |
|----------------------------|-----------------------------------|
| *PointStream*              | Uma sequência de primitivos de ponto    |
| *LineStream*               | Uma sequência de primitivas de linha     |
| *TriangleStream*           | Uma sequência de primitivas de triângulo |



 

*DataType* -tipo de dados de saída; pode ser qualquer [tipo de dados HLSL](dx-graphics-hlsl-data-types.md). Deve estar entre colchetes angulares.

*Nome-variável* nome; uma cadeia de caracteres ASCII que identifica exclusivamente o objeto.

</dd> </dl>

## <a name="example"></a>Exemplo

Este é um exemplo de uma declaração de objeto de saída de fluxo que transfere primitivas de triângulo cujos dados são definidos pelo CUBEMAP do PS \_ \_ na estrutura. O Geometry-Shader é limitado à geração de 18 vértices.


```
struct PS_CUBEMAP_IN
{
    float4 Pos : SV_POSITION;     // Projection coord
    float2 Tex : TEXCOORD0;       // Texture coord
    uint RTIndex : SV_RenderTargetArrayIndex;
};

[maxvertexcount(18)]
void main( inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream, triangle PS_CUBEMAP_INT[3] )
{
    ...
}
```



Este é um trecho de código do [exemplo CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx).

## <a name="stream-output-object-methods"></a>Métodos de objeto Stream-Output

Use a sintaxe a seguir para chamar métodos Stream-output-Object.


```
Object.Method
```



Os métodos a seguir são implementados.



| Métodos                                              | Descrição                                                      |
|------------------------------------------------------|------------------------------------------------------------------|
| [Append](dx-graphics-hlsl-so-append.md)             | Acrescente dados de saída a um fluxo existente.                        |
| [RestartStrip](dx-graphics-hlsl-so-restartstrip.md) | Finalize a faixa primitiva atual e inicie uma nova faixa primitiva. |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Esse objeto tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                        | Com suporte |
|---------------------------------------------------------------------|-----------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e modelos de sombreador mais altos | sim       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 