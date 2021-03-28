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
# <a name="effect-technique-syntax-direct3d-11"></a><span data-ttu-id="09f33-113">Sintaxe da técnica de efeito (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="09f33-113">Effect Technique Syntax (Direct3D 11)</span></span>

<span data-ttu-id="09f33-114">Uma técnica de efeito é declarada com a sintaxe descrita nesta seção.</span><span class="sxs-lookup"><span data-stu-id="09f33-114">An effect technique is declared with the syntax described in this section.</span></span>

<span data-ttu-id="09f33-115">Anotações de TechniqueVersion da *técnica* \[  <  > \]</span><span class="sxs-lookup"><span data-stu-id="09f33-115">TechniqueVersion *TechniqueName* \[ <*Annotations* > \]</span></span>

<span data-ttu-id="09f33-116">{</span><span class="sxs-lookup"><span data-stu-id="09f33-116">{</span></span>

<dl> <span data-ttu-id="09f33-117">anotações *de passto* \[  <  > \]</span><span class="sxs-lookup"><span data-stu-id="09f33-117">pass *PassName* \[ <*Annotations* > \]</span></span>  
<span data-ttu-id="09f33-118">{</span><span class="sxs-lookup"><span data-stu-id="09f33-118">{</span></span>
<dl> <span data-ttu-id="09f33-119">\[*SetState*; \] \[ *SetState*;\]</span><span class="sxs-lookup"><span data-stu-id="09f33-119">\[ *SetStateGroup*; \] \[ *SetStateGroup*; \]</span></span>  
<span data-ttu-id="09f33-120">...</span><span class="sxs-lookup"><span data-stu-id="09f33-120">...</span></span>  
<span data-ttu-id="09f33-121">\[*SetState*;\]</span><span class="sxs-lookup"><span data-stu-id="09f33-121">\[ *SetStateGroup*; \]</span></span>
</dl> </dd> }  
</dl>

<span data-ttu-id="09f33-122">}</span><span class="sxs-lookup"><span data-stu-id="09f33-122">}</span></span>

## <a name="parameters"></a><span data-ttu-id="09f33-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09f33-123">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09f33-124">Item</span><span class="sxs-lookup"><span data-stu-id="09f33-124">Item</span></span></th>
<th><span data-ttu-id="09f33-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="09f33-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="09f33-126"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span><span class="sxs-lookup"><span data-stu-id="09f33-126"><span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion</span></span><br/></td>
<td><span data-ttu-id="09f33-127">Technique10 ou technique11.</span><span class="sxs-lookup"><span data-stu-id="09f33-127">Either technique10 or technique11.</span></span> <span data-ttu-id="09f33-128">As técnicas que usam a funcionalidade nova para o Direct3D 11 (5_0 shaders, BindInterfaces, etc.) devem usar technique11.</span><span class="sxs-lookup"><span data-stu-id="09f33-128">Techniques which use functionality new to Direct3D 11 (5_0 shaders, BindInterfaces, etc) must use technique11.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09f33-129"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span><em>Técnicaname</em></span><span class="sxs-lookup"><span data-stu-id="09f33-129"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span><em>TechniqueName</em></span></span><br/></td>
<td><span data-ttu-id="09f33-130">Opcional.</span><span class="sxs-lookup"><span data-stu-id="09f33-130">Optional.</span></span> <span data-ttu-id="09f33-131">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da técnica de efeito.</span><span class="sxs-lookup"><span data-stu-id="09f33-131">An ASCII string that uniquely identifies the name of the effect technique.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09f33-132"><span id="______________Annotations__"></span><span id="______________annotations__"></span><span id="______________ANNOTATIONS__"></span> <<em>Anotações</em> ></span><span class="sxs-lookup"><span data-stu-id="09f33-132"><span id="______________Annotations__"></span><span id="______________annotations__"></span><span id="______________ANNOTATIONS__"></span> <<em>Annotations</em> ></span></span><br/></td>
<td><span data-ttu-id="09f33-133">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="09f33-133">[in] Optional.</span></span> <span data-ttu-id="09f33-134">Uma ou mais partes de informações fornecidas pelo usuário (metadados) que são ignoradas pelo sistema de efeito.</span><span class="sxs-lookup"><span data-stu-id="09f33-134">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="09f33-135">Para obter a sintaxe, consulte <a href="d3d11-effect-annotation-syntax.md">sintaxe de anotação (Direct3D 11)</a>.</span><span class="sxs-lookup"><span data-stu-id="09f33-135">For syntax, see <a href="d3d11-effect-annotation-syntax.md">Annotation Syntax (Direct3D 11)</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09f33-136"><span id="pass"></span><span id="PASS"></span>passá</span><span class="sxs-lookup"><span data-stu-id="09f33-136"><span id="pass"></span><span id="PASS"></span>pass</span></span><br/></td>
<td><span data-ttu-id="09f33-137">Palavra-chave required.</span><span class="sxs-lookup"><span data-stu-id="09f33-137">Required keyword.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09f33-138"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span><em>Passagem</em></span><span class="sxs-lookup"><span data-stu-id="09f33-138"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span><em>PassName</em></span></span><br/></td>
<td><span data-ttu-id="09f33-139">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="09f33-139">[in] Optional.</span></span> <span data-ttu-id="09f33-140">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da passagem.</span><span class="sxs-lookup"><span data-stu-id="09f33-140">An ASCII string that uniquely identifies the name of the pass.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09f33-141"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span><em>SetState</em></span><span class="sxs-lookup"><span data-stu-id="09f33-141"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span><em>SetStateGroup</em></span></span><br/></td>
<td><span data-ttu-id="09f33-142">no Defina um ou mais grupos de Estados, como:</span><span class="sxs-lookup"><span data-stu-id="09f33-142">[in] Set one or more state groups such as:</span></span> <br/> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="09f33-143">StateGroup</span><span class="sxs-lookup"><span data-stu-id="09f33-143">StateGroup</span></span></th>
<th><span data-ttu-id="09f33-144">Syntax</span><span class="sxs-lookup"><span data-stu-id="09f33-144">Syntax</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="09f33-145">Estado de mesclagem</span><span class="sxs-lookup"><span data-stu-id="09f33-145">Blend State</span></span></td>
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

<p><span data-ttu-id="09f33-146">Consulte [<strong>ID3D11DeviceContext:: OMSetBlendState</strong>] (/Windows/Desktop/API/D3D11/NF-D3D11-id3d11devicecontext-omsetblendstate) para a lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="09f33-146">See [<strong>ID3D11DeviceContext::OMSetBlendState</strong>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09f33-147">Estado do estêncil de profundidade</span><span class="sxs-lookup"><span data-stu-id="09f33-147">Depth-stencil State</span></span></td>
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
<p><span data-ttu-id="09f33-148">Consulte <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate"><strong>ID3D11DeviceContext:: OMSetDepthStencilState</strong></a> para a lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="09f33-148">See <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetdepthstencilstate"><strong>ID3D11DeviceContext::OMSetDepthStencilState</strong></a> for the argument list.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="09f33-149">Estado do rasterizador</span><span class="sxs-lookup"><span data-stu-id="09f33-149">Rasterizer State</span></span></td>
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
<p><span data-ttu-id="09f33-150">Consulte [<strong>ID3D11DeviceContext:: RSSetState</strong>] (/Windows/Desktop/API/D3D11/NF-D3D11-id3d11devicecontext-rssetstate) para a lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="09f33-150">See [<strong>ID3D11DeviceContext::RSSetState</strong>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="09f33-151">Estado do sombreador</span><span class="sxs-lookup"><span data-stu-id="09f33-151">Shader State</span></span></td>
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
<p><span data-ttu-id="09f33-152">SetXXXShader é um de SetVertexShader, SetDomainShader, SetHullShader, SetGeometryShader, SetPixelShader ou SetComputeShader (que são semelhantes aos métodos de API <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader"><strong>ID3D11DeviceContext:: VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader"><strong>ID3D11DeviceContext::D ssetshader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader"><strong>ID3D11DeviceContext:: HSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetshader"><strong>ID3D11DeviceContext:: GSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader"><strong>ID3D11DeviceContext::P ssetshader</strong></a> e <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetshader"><strong>ID3D11DeviceContext:: CSSetShader</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="09f33-152">SetXXXShader is one of SetVertexShader, SetDomainShader, SetHullShader, SetGeometryShader, SetPixelShader or SetComputeShader (which are similar to the API methods <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-vssetshader"><strong>ID3D11DeviceContext::VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader"><strong>ID3D11DeviceContext::DSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader"><strong>ID3D11DeviceContext::HSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-gssetshader"><strong>ID3D11DeviceContext::GSSetShader</strong></a>, <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader"><strong>ID3D11DeviceContext::PSSetShader</strong></a> and <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetshader"><strong>ID3D11DeviceContext::CSSetShader</strong></a>).</span></span></p>
<p><span data-ttu-id="09f33-153">O sombreador é uma variável de sombreador, que pode ser Obtida de várias maneiras:</span><span class="sxs-lookup"><span data-stu-id="09f33-153">Shader is a shader variable, which can be obtained in many ways:</span></span></p>
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
<td><span data-ttu-id="09f33-154">Processar estado de destino</span><span class="sxs-lookup"><span data-stu-id="09f33-154">Render Target State</span></span></td>
<td><span data-ttu-id="09f33-155">Um destes:</span><span class="sxs-lookup"><span data-stu-id="09f33-155">One of:</span></span>
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
<p><span data-ttu-id="09f33-156">Semelhante a <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets"><strong>ID3D11DeviceContext:: OMSetRenderTargets</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="09f33-156">Similar to <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets"><strong>ID3D11DeviceContext::OMSetRenderTargets</strong></a>.</span></span></p></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="examples"></a><span data-ttu-id="09f33-157">Exemplos</span><span class="sxs-lookup"><span data-stu-id="09f33-157">Examples</span></span>

<span data-ttu-id="09f33-158">Este exemplo define o estado de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="09f33-158">This example sets blending state.</span></span>


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



<span data-ttu-id="09f33-159">Este exemplo configura o estado do rasterizador para renderizar um objeto em wireframe.</span><span class="sxs-lookup"><span data-stu-id="09f33-159">This example sets up the rasterizer state to render an object in wireframe.</span></span>


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



<span data-ttu-id="09f33-160">Este exemplo define o estado do sombreador.</span><span class="sxs-lookup"><span data-stu-id="09f33-160">This example sets shader state.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="09f33-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="09f33-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09f33-162">Formato do efeito</span><span class="sxs-lookup"><span data-stu-id="09f33-162">Effect Format</span></span>](d3d11-effect-format.md)
</dt> <dt>

[<span data-ttu-id="09f33-163">Sintaxe do grupo de efeitos (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="09f33-163">Effect Group Syntax (Direct3D 11)</span></span>](d3d11-effect-group-syntax.md)
</dt> <dt>

[<span data-ttu-id="09f33-164">Grupos de estado de efeito</span><span class="sxs-lookup"><span data-stu-id="09f33-164">Effect State Groups</span></span>](d3d11-effect-states.md)
</dt> </dl>

 

 





