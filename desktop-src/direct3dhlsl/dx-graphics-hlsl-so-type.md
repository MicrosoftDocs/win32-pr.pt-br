---
title: Stream-Output objeto
description: Um objeto stream-output é um objeto modelo que transmite dados do estágio geometry-shader. Use a sintaxe a seguir para declarar um objeto stream-output.
ms.assetid: 07a5489c-c238-4466-9282-5b168448aff7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 79e0247b424ebb6f72622565845c17b622ab715cd8860a83ce24ae58ac7420c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789476"
---
# <a name="stream-output-object"></a>Stream-Output objeto

Um objeto stream-output é um objeto modelo que transmite dados do estágio [geometry-shader](/previous-versions//bb205146(v=vs.85)). Use a sintaxe a seguir para declarar um objeto stream-output.



| inout *StreamOutputObject* < *DataType* >  *Name;* |
|------------------------------------------------------|



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*StreamOutputObject*  <  *DataType*  >    *Nome*
</dt> <dd>

A declaração so (objeto de saída de fluxo).



| Stream-Output tipos de objeto | Descrição                       |
|----------------------------|-----------------------------------|
| *PointStream*              | Uma sequência de primitivos de ponto    |
| *LineStream*               | Uma sequência de primitivos de linha     |
| *TriangleStream*           | Uma sequência de primitivos de triângulo |



 

*DataType* – tipo de dados de saída; pode ser qualquer [tipo de dados HLSL.](dx-graphics-hlsl-data-types.md) Deve estar entre colchetes angulares.

*Nome* – Nome da variável; uma cadeia de caracteres ASCII que identifica exclusivamente o objeto .

</dd> </dl>

## <a name="example"></a>Exemplo

Este é um exemplo de uma declaração de objeto de saída de fluxo que transmite primitivos de triângulo cujos dados são definidos pela estrutura PS \_ CUBEMAP \_ IN. O sombreador de geometria é limitado à geração de 18 vértices.


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



Este é um snippet de código do [Exemplo de CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx).

## <a name="stream-output-object-methods"></a>Stream-Output de objeto de Stream-Output

Use a sintaxe a seguir para chamar métodos stream-output-object.


```
Object.Method
```



Os métodos a seguir são implementados.



| Métodos                                              | Descrição                                                      |
|------------------------------------------------------|------------------------------------------------------------------|
| [Append](dx-graphics-hlsl-so-append.md)             | Anexar dados de saída a um fluxo existente.                        |
| [RestartStrip](dx-graphics-hlsl-so-restartstrip.md) | Termine a faixa primitiva atual e inicie uma nova faixa primitiva. |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esse objeto tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                        | Com suporte |
|---------------------------------------------------------------------|-----------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e modelos de sombreador superior | sim       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 