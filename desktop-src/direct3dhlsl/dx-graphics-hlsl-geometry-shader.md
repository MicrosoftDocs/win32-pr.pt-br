---
title: Geometry-Shader objeto
description: Um objeto de sombreador de geometria processa primitivos inteiros. Use a sintaxe a seguir para declarar um objeto de sombreador de geometria.
ms.assetid: d5c1c22b-6fa6-40a8-900f-6d74f74468c1
keywords:
- maxvertexcount (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e06bbc184a4b5f82d5edaaf7fdbfbd55f1906f12
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120611"
---
# <a name="geometry-shader-object"></a>Geometry-Shader objeto

Um objeto de sombreador de geometria processa primitivos inteiros. Use a sintaxe a seguir para declarar um objeto de sombreador de geometria.

\[maxvertexcount(*NumVerts*) \] void *ShaderName* ( *PrimitiveType DataType Name \[ NumElements, \]* inout *StreamOutputObject* );



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount(*NumVerts*)\]
</dt> <dd>

\[em \] Declaração para o número máximo de vértices a criar.

-   \[maxvertexcount() \] – palavra-chave necessária; colchetes e parênteses são caracteres necessários para a sintaxe correta.
-   *NumVerts* – um número inteiro que representa o número de vértices.

</dd> <dt>

<span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*
</dt> <dd>

\[em \] uma cadeia de caracteres ASCII que contém um nome exclusivo para a função geometry-shader.

</dd> <dt>

<span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*NumElements de nome primitiveType DataType \[\]*
</dt> <dd>

*PrimitiveType* – tipo primitivo, que determina a ordem dos dados primitivos.



| Tipo primitivo | Descrição                                                   |
|----------------|---------------------------------------------------------------|
| *Ponto*        | Lista de pontos                                                    |
| *Linha*         | Lista de linhas ou faixa de linhas                                       |
| *Triângulo*     | Lista de triângulos ou faixa de triângulo                               |
| *lineadj*      | Lista de linhas com adjacency ou faixa de linha com adjacency         |
| *triangleadj*  | Lista de triângulos com adjacency ou faixa de triângulo com adjacency |



 

*DataType*  -  \[ em \] Um tipo de dados de entrada; pode ser qualquer tipo de dados [HLSL](dx-graphics-hlsl-data-types.md).

*Nome* – Nome do argumento; esta é uma cadeia de caracteres ASCII.

*NumElements* – tamanho da matriz da entrada, que depende *do PrimitiveType,* conforme mostrado na tabela a seguir.

| Tipo primitivo | NumElements                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------|
| *Ponto*        | \[1\]<br/> Você opera em apenas um ponto por vez.<br/>                                         |
| *Linha*         | \[2\]<br/> Uma linha requer dois vértices.<br/>                                                    |
| *Triângulo*     | \[3\]<br/> Um triângulo requer três vértices.<br/>                                              |
| *lineadj*      | \[4\]<br/> Um lineadj tem duas extremidades; portanto, ele requer quatro vértices.<br/>                    |
| *triangleadj*  | \[6\]<br/> Um triânguloadj faz a bordas de mais três triângulos; portanto, ele requer seis vértices.<br/> |



 

</dd> <dt>

<span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*
</dt> <dd>

A declaração do [objeto stream-output](dx-graphics-hlsl-so-type.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Nenhum

## <a name="remarks"></a>Comentários

O diagrama a seguir mostra os vários tipos primitivos para um objeto de sombreador de geometria.

![ilustração dos vários tipos primitivos para um objeto de sombreador de geometria](images/d3d11-gsinputs1.png)

O diagrama a seguir mostra invocações de sombreador de geometria.

![ilustração de invocações de sombreador de geometria](images/d3d11-gsinputs2.png)

## <a name="examples"></a>Exemplos

Este exemplo é do exercício 1 do Workshop do Modelo de Sombreador [4.0 do Direct3D 10.](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx)


```
[maxvertexcount(3)]
void GSScene( triangleadj GSSceneIn input[6], inout TriangleStream<PSSceneIn> OutputStream )
{   
    PSSceneIn output = (PSSceneIn)0;

    for( uint i=0; i<6; i+=2 )
    {
        output.Pos = input[i].Pos;
        output.Norm = input[i].Norm;
        output.Tex = input[i].Tex;
        
        OutputStream.Append( output );
    }
    
    OutputStream.RestartStrip();
}
```



## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esse objeto tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                                        | Com suporte |
|---------------------------------------------------------------------|-----------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e modelos de sombreador superior | yes       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





