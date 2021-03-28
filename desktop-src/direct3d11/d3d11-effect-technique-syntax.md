---
title: Sintaxe da técnica de efeito (Direct3D 11)
description: Uma técnica de efeito é declarada com a sintaxe descrita nesta seção.
ms.assetid: 54a6ebd1-a6b4-473b-bf53-a3323445de71
keywords:
- technique11, efeito do Direct3D 11
- Pass, efeito do Direct3D 11
- CompileShader, efeito do Direct3D 11
- Efeito de controle de estado, Direct3D 11
- Autoblendstate, efeito do Direct3D 11
- SetDepthStencilState, efeito do Direct3D 11
- SetRasterizerState, efeito do Direct3D 11
- SetVertexShader, efeito do Direct3D 11
- SetGeometryShader, efeito do Direct3D 11
- SetPixelShader, efeito do Direct3D 11
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73fb668f308869ef9cca5cce99d522f18a287f3c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104084277"
---
# <a name="effect-technique-syntax-direct3d-11"></a>Sintaxe da técnica de efeito (Direct3D 11)

Uma técnica de efeito é declarada com a sintaxe descrita nesta seção.

Anotações de TechniqueVersion da *técnica* \[  <  > \]

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
<td><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion<br/></td>
<td>Technique10 ou technique11. As técnicas que usam a funcionalidade nova para o Direct3D 11 (5_0 shaders, BindInterfaces, etc.) devem usar technique11.<br/></td>
</tr>
<tr class="even">
<td><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span><em>Técnicaname</em><br/></td>
<td>Opcional. Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da técnica de efeito.<br/></td>
</tr>
<tr class="odd">
<td><span id="______________Annotations__"></span><span id="______________annotations__"></span><span id="______________ANNOTATIONS__"></span> <<em>Anotações</em> ><br/></td>
<td>[in] Opcional. Uma ou mais partes de informações fornecidas pelo usuário (metadados) que são ignoradas pelo sistema de efeito. Para obter a sintaxe, consulte <a href="d3d11-effect-annotation-syntax.md">sintaxe de anotação (Direct3D 11)</a>.<br/></td>
</tr>
<tr class="even">
<td><span id="pass"></span><span id="PASS"></span>passá<br/></td>
<td>Palavra-chave required.<br/></td>
</tr>
<tr class="odd">
<td><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span><em>Passagem</em><br/></td>
<td>[in] Opcional. Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da passagem.<br/></td>
</tr>
<tr class="even">
<td><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span><em>SetState</em><br/></td>
<td>no Defina um ou mais grupos de Estados, como: <br/> 
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

<p>Consulte [<strong>ID3D11DeviceContext:: OMSetBlendState</strong>] (/Windows/Desktop/API/D3D11/NF-D3D11-id3d11devicecontext-omsetblendstate) para a lista de argumentos.</p></td>
</tr>
<tr class="even">
<td>Estado do estêncil de profundidade</td>
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
<p>Consulte <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate"><strong>ID3D11DeviceContext:: OMSetDepthStencilState</strong></a> para a lista de argumentos.</p></td>
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
<p>Consulte [<strong>ID3D11DeviceContext:: RSSetState</strong>] (/Windows/Desktop/API/D3D11/NF-D3D11-id3d11devicecontext-rssetstate) para a lista de argumentos.</p></td>
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
<td><pre><code>SetXXXShader( Shader );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>SetXXXShader é um de SetVertexShader, SetDomainShader, SetHullShader, SetGeometryShader, SetPixelShader ou SetComputeShader (que são semelhantes aos métodos de API <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader"><strong>ID3D11DeviceContext:: VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader"><strong>ID3D11DeviceContext::D ssetshader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader"><strong>ID3D11DeviceContext:: HSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetshader"><strong>ID3D11DeviceContext:: GSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader"><strong>ID3D11DeviceContext::P ssetshader</strong></a> e <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetshader"><strong>ID3D11DeviceContext:: CSSetShader</strong></a>).</p>
<p>O sombreador é uma variável de sombreador, que pode ser Obtida de várias maneiras:</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetXXXShader( CompileShader( shader_profile, ShaderFunction( args ) ) );
SetXXXShader( CompileShader( NULL ) );
SetXXXShader( NULL );
SetXXXShader( myShaderVar );
SetXXXShader( myShaderArray[2] );
SetXXXShader( myShaderArray[uIndex] );
SetGeometryShader( ConstructGSWithSO( Shader, strStream0 ) );
SetGeometryShader( ConstructGSWithSO( Shader, strStream0, strStream1, strStream2, strStream3, RastStream ) );</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>Processar estado de destino</td>
<td>Um destes:
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SetRenderTargets( RTV0, DSV );
SetRenderTargets( RTV0, RTV1, DSV );
...
SetRenderTargets( RTV0, RTV1, RTV2, RTV3, RTV4, RTV5, RTV6, RTV7, DSV );</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>Semelhante a <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets"><strong>ID3D11DeviceContext:: OMSetRenderTargets</strong></a>.</p></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a>Exemplos

Este exemplo define o estado de mesclagem.


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



Este exemplo define o estado do sombreador.


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

[Formato do efeito](d3d11-effect-format.md)
</dt> <dt>

[Sintaxe do grupo de efeitos (Direct3D 11)](d3d11-effect-group-syntax.md)
</dt> <dt>

[Grupos de estado de efeito](d3d11-effect-states.md)
</dt> </dl>

 

 





