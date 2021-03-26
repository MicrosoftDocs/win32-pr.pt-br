---
title: Objeto Geometry-Shader
description: Um objeto Geometry-Shader processa primitivos inteiros. Use a sintaxe a seguir para declarar um objeto Geometry-Shader.
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
ms.openlocfilehash: dadb0e8bb3ddda16305ac701b34523668bd9c1a5
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2019
ms.locfileid: "103638986"
---
# <a name="geometry-shader-object"></a>Objeto Geometry-Shader

Um objeto Geometry-Shader processa primitivos inteiros. Use a sintaxe a seguir para declarar um objeto Geometry-Shader.



|                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|
| \[maxvertexcount (*NumVerts*) \] void *shadername* ( *Primitivatype nome do tipo de dados \[ \] NumElements*, inout *StreamOutputObject* ); |



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount (*NumVerts*)\]
</dt> <dd>

\[em \] declaração para o número máximo de vértices a serem criados.

-   \[maxvertexcount () \] -palavra-chave necessária; colchetes e parênteses são caracteres necessários para a sintaxe correta.
-   *NumVerts* -um número inteiro que representa o número de vértices.

</dd> <dt>

<span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*Shadername*
</dt> <dd>

\[em \] uma cadeia de caracteres ASCII que contém um nome exclusivo para a função Geometry-Shader.

</dd> <dt>

<span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*Nome do tipo de dados primitivotype \[ NumElements \]*
</dt> <dd>

Tipo *primitivo* -Primitive, que determina a ordem dos dados primitivos.



| Tipo primitivo | Description                                                   |
|----------------|---------------------------------------------------------------|
| *empresas*        | Lista de pontos                                                    |
| *descritos*         | Lista de linhas ou faixa de linha                                       |
| *ângulo*     | Lista de triângulos ou a faixa de triângulo                               |
| *lineadj*      | Lista de linhas com adjacência ou faixa de linha com adjacência         |
| *triangleadj*  | Lista de triângulos com uma faixa de adjacência ou triângulo com adjacência |



 

*Tipo de dados*  -  \[ em \] um tipo de dados de entrada, pode ser qualquer [tipo de dados HLSL](dx-graphics-hlsl-data-types.md).

*Nome-nome* do argumento; Esta é uma cadeia de caracteres ASCII.

*NumElements* -tamanho da matriz da entrada, que depende do *primitivatype* , conforme mostrado na tabela a seguir.

| Tipo primitivo | NumElements                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------|
| *empresas*        | \[1\]<br/> Você opera em apenas um ponto por vez.<br/>                                         |
| *descritos*         | \[2\]<br/> Uma linha requer dois vértices.<br/>                                                    |
| *ângulo*     | \[3\]<br/> Um triângulo requer três vértices.<br/>                                              |
| *lineadj*      | \[4\]<br/> Um lineadj tem duas extremidades; Portanto, ele requer quatro vértices.<br/>                    |
| *triangleadj*  | \[6\]<br/> Uma triangleadj bordas mais três triângulos; Portanto, ele requer seis vértices.<br/> |



 

</dd> <dt>

<span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*
</dt> <dd>

A declaração do [objeto Stream-output](dx-graphics-hlsl-so-type.md).

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Nenhum

## <a name="remarks"></a>Comentários

O diagrama a seguir mostra os vários tipos primitivos para um objeto de sombreador de geometria.

![Ilustração dos vários tipos primitivos para um objeto de sombreador Geometry](images/d3d11-gsinputs1.png)

O diagrama a seguir mostra invocações de sombreador de geometria.

![ilustração de invocações do sombreador de geometria](images/d3d11-gsinputs2.png)

## <a name="examples"></a>Exemplos

Este exemplo é do exercício 1 do [Workshop 4,0 do sombreador do Direct3D 10](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).


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



## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Esse objeto tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                        | Com suporte |
|---------------------------------------------------------------------|-----------|
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) e modelos de sombreador mais altos | sim       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





