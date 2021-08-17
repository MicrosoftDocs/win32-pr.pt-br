---
description: Uma técnica de efeito é declarada com a sintaxe a seguir.
ms.assetid: 84f9b74d-8397-4cd5-91a0-7f910ba7b19e
title: Sintaxe da técnica de efeito (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3c0ff0c0f1b5e9c1fac4cdb12aac21e42d89771c0eae89d1cd9538d0281acee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914481"
---
# <a name="effect-technique-syntax-direct3d-10"></a>Sintaxe da técnica de efeito (Direct3D 10)

Uma técnica de efeito é declarada com a sintaxe a seguir.

Anotações *technique10 TechniqueName* \[  <  > \]

{

<dl> anotações *passName* \[  <  > \]  
{
<dl> \[*SetStateGroup*; \] \[ *SetStateGroup*;\]  
...  
\[*SetStateGroup*;\]
</dl> </dd> }  
</dl>

}

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="technique10"></span><span id="TECHNIQUE10"></span>technique10
</dt> <dd>

Palavra-chave necessária.

</dd> <dt>

<span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>*TechniqueName*
</dt> <dd>

Opcional. Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da técnica de efeito.

</dd> <dt>

<span id="Annotations"></span><span id="annotations"></span><span id="ANNOTATIONS"></span>*Anotações*
</dt> <dd>

\[em \] Opcional. Uma ou mais partes de informações fornecidas pelo usuário (metadados) que são ignoradas pelo sistema de efeito. Para sintaxe, consulte [Sintaxe de anotação (Direct3D 10)](d3d10-effect-annotation-syntax.md).

</dd> <dt>

<span id="pass"></span><span id="PASS"></span>Passar
</dt> <dd>

Palavra-chave necessária.

</dd> <dt>

<span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*PassName*
</dt> <dd>

\[em \] Opcional. Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da passagem.

</dd> <dt>

<span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*SetStateGroup*
</dt> <dd>

\[em \] Definir um ou mais grupos de estado, como:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>StateGroup</th>
<th>Syntax</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Estado de mesclagem</td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetBlendState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

<p>Consulte [<strong>OMSetBlendState</strong>](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetblendstate) para a lista de argumentos.</p></td>
</tr>
<tr class="even">
<td>Estado de estêncil de profundidade</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetRasterizerState( arguments ); </code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>Consulte [<strong>RSSetState</strong>](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-rssetstate) para a lista de argumentos.</p></td>
</tr>
<tr class="even">
<td>Estado do sombreador</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<col style="width: 100%" />
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
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( NULL );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>SetXXXShader é um de <strong>SetVertexShader,</strong> <strong>SetGeometryShader</strong>ou <strong>SetPixelShader</strong> (que são semelhantes aos métodos de API <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader"><strong>VSSetShader,</strong></a> <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshader"><strong>GSSetShader</strong></a>e <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshader"><strong>PSSetShader</strong></a>).</p></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

Os grupos de estado de efeito são listados [no estado de efeito](d3d10-effect-states.md).

## <a name="examples"></a>Exemplos

Este exemplo (da amostra [CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) define o estado de mesclagem.


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



Este exemplo define o estado do sombreador [(da amostra BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)); que usa um vértice e um sombreador de pixel.


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

[Formato de efeito](d3d10-effect-format.md)
</dt> </dl>

 

 



