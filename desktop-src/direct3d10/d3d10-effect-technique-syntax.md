---
description: Uma técnica de efeito é declarada com a sintaxe a seguir.
ms.assetid: 84f9b74d-8397-4cd5-91a0-7f910ba7b19e
title: Sintaxe da técnica de efeito (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 106abd47e1148ce30127733f113a1b43a0058f60
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625122"
---
# <a name="effect-technique-syntax-direct3d-10"></a>Sintaxe da técnica de efeito (Direct3D 10)

Uma técnica de efeito é declarada com a sintaxe a seguir.

anotações de technique10 da *técnica* \[  <  > \]

{

<dl> anotações *de passto* \[  <  > \]  
{
<dl> \[*SetState*; \] \[ *SetState*;\]  
...  
\[*SetState*;\]
</dl> </dd> }  
</dl>

}

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="technique10"></span><span id="TECHNIQUE10"></span>technique10
</dt> <dd>

Palavra-chave required.

</dd> <dt>

<span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>*Técnicaname*
</dt> <dd>

Opcional. Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da técnica de efeito.

</dd> <dt>

<span id="Annotations"></span><span id="annotations"></span><span id="ANNOTATIONS"></span>*Anotações*
</dt> <dd>

\[em \] opcional. Uma ou mais partes de informações fornecidas pelo usuário (metadados) que são ignoradas pelo sistema de efeito. Para obter a sintaxe, consulte [sintaxe de anotação (Direct3D 10)](d3d10-effect-annotation-syntax.md).

</dd> <dt>

<span id="pass"></span><span id="PASS"></span>passá
</dt> <dd>

Palavra-chave required.

</dd> <dt>

<span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*Passagem*
</dt> <dd>

\[em \] opcional. Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da passagem.

</dd> <dt>

<span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*SetState*
</dt> <dd>

\[em \] definir um ou mais grupos de Estados, como:



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>StateGroup</th>
<th>Sintaxe</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Estado de mesclagem</td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetBlendState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

<p>Consulte [<strong>OMSetBlendState</strong>] (/Windows/Desktop/API/d3d10/NF-d3d10-id3d10device-omsetblendstate) para a lista de argumentos.</p></td>
</tr>
<tr class="even">
<td>Estado do estêncil de profundidade</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetDepthStencilState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>Consulte <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetdepthstencilstate"><strong>OMSetDepthStencilState</strong></a> para a lista de argumentos.</p></td>
</tr>
<tr class="odd">
<td>Estado do rasterizador</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetRasterizerState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>Consulte [<strong>RSSetState</strong>] (/Windows/Desktop/API/d3d10/NF-d3d10-id3d10device-rssetstate) para a lista de argumentos.</p></td>
</tr>
<tr class="even">
<td>Estado do sombreador</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( CompileShader( shader_profile, ShaderFunction( args ) ) );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>ou</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( CompileShader( NULL ) );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>ou</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( NULL );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>SetXXXShader é um de <strong>SetVertexShader</strong>, <strong>SetGeometryShader</strong>ou <strong>SetPixelShader</strong> (que são semelhantes aos métodos de API <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader"><strong>VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshader"><strong>GSSetShader</strong></a>e <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshader"><strong>PSSetShader</strong></a>).</p></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

Os grupos de estado de efeito são listados em [estado de efeito](d3d10-effect-states.md).

## <a name="examples"></a>Exemplos

Este exemplo (de [exemplo CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) define o estado de mesclagem.


```
BlendState NoBlend
{ 
    BlendEnable[0] = False;
};

...

technique10
{
    pass p2 
    {
        ...
        SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    }
}
```



Este exemplo configura o estado do rasterizador para renderizar um objeto em wireframe.


```
RasterizerState rsWireframe { FillMode = WireFrame; };

...

technique10
{
    pass p1 
    {
        ....
        SetRasterizerState( rsWireframe );
    }
}
```



Este exemplo define o estado do sombreador (de [exemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)); que usa um vértice e um sombreador de pixel.


```
technique10 RenderSceneWithTexture1Light
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, RenderSceneVS( 1, true, true ) ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, RenderScenePS( true ) ) );
    }
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato do efeito](d3d10-effect-format.md)
</dt> </dl>

 

 



