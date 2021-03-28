---
title: Argumentos da função
description: Uma função usa um ou mais argumentos de entrada; Use a sintaxe a seguir para declarar cada argumento.
ms.assetid: 80e0dbc8-26b7-4250-bb01-6856fc70f6b8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ba35ad04b20b67e45550644e842d69209ca5088
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104365490"
---
# <a name="function-arguments"></a>Argumentos da função

Uma função usa um ou mais argumentos de entrada; Use a sintaxe a seguir para declarar cada argumento.



|                                                                                             |
|---------------------------------------------------------------------------------------------|
| **\[\]Nome do tipo InputModifier \[ : Semantic \] \[ InterpolationModifier \] \[ = inicializadores\]** |



 

\[Tipo de modificador \] nome \[ : semântica \] \[ : modificador de interpolação \] \[ = inicializador (s)\]

Se houver vários argumentos de função, eles serão separados por vírgulas.

## <a name="parameters"></a>Parâmetros



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Item</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="InputModifier"></span><span id="inputmodifier"></span><span id="INPUTMODIFIER"></span><strong>InputModifier</strong><br/></td>
<td>Termo opcional que identifica um argumento como uma entrada, uma saída ou ambos.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Valor</td>
<td>Descrição</td>
</tr>
<tr class="even">
<td><strong>Em</strong></td>
<td>Somente entrada</td>
</tr>
<tr class="odd">
<td><strong>InOut</strong></td>
<td>Entrada e uma saída</td>
</tr>
<tr class="even">
<td><strong>out</strong></td>
<td>Somente saída</td>
</tr>
<tr class="odd">
<td><strong>universal</strong></td>
<td>Inserir somente dados constantes</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Os parâmetros são sempre passados por valor. no indica que o valor do parâmetro deve ser copiado do aplicativo de chamada antes que a função comece. out indica que o último valor do parâmetro deve ser copiado e retornado ao aplicativo de chamada quando a função retornar. Inout é uma abreviação para especificar ambos.</p>
<p>Um valor uniforme vem de um registro constante; cada invocação do sombreador de vértice ou de sombreador de pixel vê o mesmo valor inicial para uma variável uniforme. As variáveis globais são tratadas como se fossem declaradas uniformes. Para funções não de nível superior, uniforme é sinônimo de <strong>in</strong>. Se nenhum uso de parâmetro for especificado, o uso do parâmetro será considerado <strong>em</strong>.</p></td>
</tr>
<tr class="even">
<td><p><span id="Type"></span><span id="type"></span><span id="TYPE"></span><strong>Escreva</strong></p></td>
<td><p>O tipo de argumento; pode ser qualquer <a href="dx-graphics-hlsl-data-types.md">tipo</a>de HLSL válido.</p></td>
</tr>
<tr class="odd">
<td><p><span id="Name"></span><span id="name"></span><span id="NAME"></span><strong>Nomes</strong></p></td>
<td><p>Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da função de sombreador.</p></td>
</tr>
<tr class="even">
<td><p><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span><strong>Semântico</strong></p></td>
<td><p>Cadeia de caracteres opcional que identifica o uso pretendido dos dados (consulte a <a href="dx-graphics-hlsl-semantics.md">semântica (DirectX HLSL)</a>).</p></td>
</tr>
<tr class="odd">
<td><p><span id="InterpolationModifier"></span><span id="interpolationmodifier"></span><span id="INTERPOLATIONMODIFIER"></span><strong>InterpolationModifier</strong></p></td>
<td><p><a href="dx-graphics-hlsl-struct.md">Modificador de interpolação</a> opcional que permite que um sombreador determine o método de interpolação. Um modificador de interpolação em um argumento de função se aplica apenas a um argumento usado como uma entrada para uma função de sombreador de pixel.</p></td>
</tr>
<tr class="even">
<td><p><span id="Initializers"></span><span id="initializers"></span><span id="INITIALIZERS"></span><strong>Inicializadores</strong></p></td>
<td><p>Valores opcionais para inicialização; vários valores são necessários para inicializar tipos de dados de vários componentes.</p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Os argumentos de função são listados em uma lista de argumentos separados por vírgula em uma declaração de função. Como nas funções de C, cada argumento deve ter um nome de parâmetro e tipo declarado; um argumento para uma função HLSL opcionalmente pode incluir uma semântica, um valor inicial e uma entrada de sombreador de pixel pode incluir um tipo de interpolação.

O *tipo* de um argumento de função pode ser uma estrutura, que poderia incluir um modificador de interpolação por membro. Se o argumento de função também tiver um modificador de interpolação, o modificador de argumento de função substituirá modificadores de interpolação declarados no tipo.

## <a name="examples"></a>Exemplos

Este exemplo (do [exemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)) ilustra entradas uniformes e não uniformes para uma função de sombreador de vértice.


```
VS_OUTPUT RenderSceneVS( 
  float4 vPos : POSITION,
  float3 vNormal : NORMAL,
  float2 vTexCoord0 : TEXCOORD,
  uniform int nNumLights,
  uniform bool bTexture,
  uniform bool bAnimate )
{
  ...
}
```



Este exemplo (do [exemplo ContentStreaming](https://msdn.microsoft.com/library/Ee416397(v=VS.85).aspx)) usa uma estrutura de entrada para passar argumentos para uma função de sombreador de pixel.


```
VSBasicIn input
struct VSBasicIn
{
  float4 Pos    : POSITION;
  float3 Norm   : NORMAL;
  float2 Tex    : TEXCOORD0;
};

PSBasicIn VSBasic(VSBasicIn input)
{
  ...
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções (DirectX HLSL)](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 





