---
description: Uma técnica de efeito é declarada com a sintaxe a seguir.
ms.assetid: 84f9b74d-8397-4cd5-91a0-7f910ba7b19e
title: Sintaxe da técnica de efeito (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f781a0e1ea247e9ffae02e6afc9de77c8e0c6b68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089125"
---
# <a name="effect-technique-syntax-direct3d-10"></a><span data-ttu-id="8e9d5-103">Sintaxe da técnica de efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="8e9d5-103">Effect Technique Syntax (Direct3D 10)</span></span>

<span data-ttu-id="8e9d5-104">Uma técnica de efeito é declarada com a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="8e9d5-104">An effect technique is declared with the following syntax.</span></span>

<span data-ttu-id="8e9d5-105">anotações de technique10 da *técnica* \[  <  > \]</span><span class="sxs-lookup"><span data-stu-id="8e9d5-105">technique10 *TechniqueName* \[ <*Annotations* > \]</span></span>

<span data-ttu-id="8e9d5-106">{</span><span class="sxs-lookup"><span data-stu-id="8e9d5-106">{</span></span>

<dl> <span data-ttu-id="8e9d5-107">anotações *de passto* \[  <  > \]</span><span class="sxs-lookup"><span data-stu-id="8e9d5-107">pass *PassName* \[ <*Annotations* > \]</span></span>  
<span data-ttu-id="8e9d5-108">{</span><span class="sxs-lookup"><span data-stu-id="8e9d5-108">{</span></span>
<dl> <span data-ttu-id="8e9d5-109">\[*SetState*; \] \[ *SetState*;\]</span><span class="sxs-lookup"><span data-stu-id="8e9d5-109">\[ *SetStateGroup*; \] \[ *SetStateGroup*; \]</span></span>  
<span data-ttu-id="8e9d5-110">...</span><span class="sxs-lookup"><span data-stu-id="8e9d5-110">...</span></span>  
<span data-ttu-id="8e9d5-111">\[*SetState*;\]</span><span class="sxs-lookup"><span data-stu-id="8e9d5-111">\[ *SetStateGroup*; \]</span></span>
</dl> </dd> }  
</dl>

<span data-ttu-id="8e9d5-112">}</span><span class="sxs-lookup"><span data-stu-id="8e9d5-112">}</span></span>

## <a name="parameters"></a><span data-ttu-id="8e9d5-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e9d5-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e9d5-114"><span id="technique10"></span><span id="TECHNIQUE10"></span>technique10</span><span class="sxs-lookup"><span data-stu-id="8e9d5-114"><span id="technique10"></span><span id="TECHNIQUE10"></span>technique10</span></span>
</dt> <dd>

<span data-ttu-id="8e9d5-115">Palavra-chave required.</span><span class="sxs-lookup"><span data-stu-id="8e9d5-115">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="8e9d5-116"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>*Técnicaname*</span><span class="sxs-lookup"><span data-stu-id="8e9d5-116"><span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>*TechniqueName*</span></span>
</dt> <dd>

<span data-ttu-id="8e9d5-117">Opcional.</span><span class="sxs-lookup"><span data-stu-id="8e9d5-117">Optional.</span></span> <span data-ttu-id="8e9d5-118">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da técnica de efeito.</span><span class="sxs-lookup"><span data-stu-id="8e9d5-118">An ASCII string that uniquely identifies the name of the effect technique.</span></span>

</dd> <dt>

<span data-ttu-id="8e9d5-119"><span id="Annotations"></span><span id="annotations"></span><span id="ANNOTATIONS"></span>*Anotações*</span><span class="sxs-lookup"><span data-stu-id="8e9d5-119"><span id="Annotations"></span><span id="annotations"></span><span id="ANNOTATIONS"></span>*Annotations*</span></span>
</dt> <dd>

<span data-ttu-id="8e9d5-120">\[em \] opcional.</span><span class="sxs-lookup"><span data-stu-id="8e9d5-120">\[in\] Optional.</span></span> <span data-ttu-id="8e9d5-121">Uma ou mais partes de informações fornecidas pelo usuário (metadados) que são ignoradas pelo sistema de efeito.</span><span class="sxs-lookup"><span data-stu-id="8e9d5-121">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="8e9d5-122">Para obter a sintaxe, consulte [sintaxe de anotação (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="8e9d5-122">For syntax, see [Annotation Syntax (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="8e9d5-123"><span id="pass"></span><span id="PASS"></span>passá</span><span class="sxs-lookup"><span data-stu-id="8e9d5-123"><span id="pass"></span><span id="PASS"></span>pass</span></span>
</dt> <dd>

<span data-ttu-id="8e9d5-124">Palavra-chave required.</span><span class="sxs-lookup"><span data-stu-id="8e9d5-124">Required keyword.</span></span>

</dd> <dt>

<span data-ttu-id="8e9d5-125"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*Passagem*</span><span class="sxs-lookup"><span data-stu-id="8e9d5-125"><span id="PassName"></span><span id="passname"></span><span id="PASSNAME"></span>*PassName*</span></span>
</dt> <dd>

<span data-ttu-id="8e9d5-126">\[em \] opcional.</span><span class="sxs-lookup"><span data-stu-id="8e9d5-126">\[in\] Optional.</span></span> <span data-ttu-id="8e9d5-127">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da passagem.</span><span class="sxs-lookup"><span data-stu-id="8e9d5-127">An ASCII string that uniquely identifies the name of the pass.</span></span>

</dd> <dt>

<span data-ttu-id="8e9d5-128"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*SetState*</span><span class="sxs-lookup"><span data-stu-id="8e9d5-128"><span id="SetStateGroup"></span><span id="setstategroup"></span><span id="SETSTATEGROUP"></span>*SetStateGroup*</span></span>
</dt> <dd>

<span data-ttu-id="8e9d5-129">\[em \] definir um ou mais grupos de Estados, como:</span><span class="sxs-lookup"><span data-stu-id="8e9d5-129">\[in\] Set one or more state groups such as:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8e9d5-130">StateGroup</span><span class="sxs-lookup"><span data-stu-id="8e9d5-130">StateGroup</span></span></th>
<th><span data-ttu-id="8e9d5-131">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e9d5-131">Syntax</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8e9d5-132">Estado de mesclagem</span><span class="sxs-lookup"><span data-stu-id="8e9d5-132">Blend State</span></span></td>
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

<p><span data-ttu-id="8e9d5-133">Consulte [<strong>OMSetBlendState</strong>] (/Windows/Desktop/API/d3d10/NF-d3d10-id3d10device-omsetblendstate) para a lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="8e9d5-133">See [<strong>OMSetBlendState</strong>](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetblendstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e9d5-134">Estado do estêncil de profundidade</span><span class="sxs-lookup"><span data-stu-id="8e9d5-134">Depth-stencil State</span></span></td>
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
<p><span data-ttu-id="8e9d5-135">Consulte <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetdepthstencilstate"><strong>OMSetDepthStencilState</strong></a> para a lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="8e9d5-135">See <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetdepthstencilstate"><strong>OMSetDepthStencilState</strong></a> for the argument list.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8e9d5-136">Estado do rasterizador</span><span class="sxs-lookup"><span data-stu-id="8e9d5-136">Rasterizer State</span></span></td>
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
<p><span data-ttu-id="8e9d5-137">Consulte [<strong>RSSetState</strong>] (/Windows/Desktop/API/d3d10/NF-d3d10-id3d10device-rssetstate) para a lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="8e9d5-137">See [<strong>RSSetState</strong>](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-rssetstate) for the argument list.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e9d5-138">Estado do sombreador</span><span class="sxs-lookup"><span data-stu-id="8e9d5-138">Shader State</span></span></td>
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
<p><span data-ttu-id="8e9d5-139">ou</span><span class="sxs-lookup"><span data-stu-id="8e9d5-139">or</span></span></p>
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
<p><span data-ttu-id="8e9d5-140">ou</span><span class="sxs-lookup"><span data-stu-id="8e9d5-140">or</span></span></p>
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
<p><span data-ttu-id="8e9d5-141">SetXXXShader é um de <strong>SetVertexShader</strong>, <strong>SetGeometryShader</strong>ou <strong>SetPixelShader</strong> (que são semelhantes aos métodos de API <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader"><strong>VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshader"><strong>GSSetShader</strong></a>e <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshader"><strong>PSSetShader</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="8e9d5-141">SetXXXShader is one of <strong>SetVertexShader</strong>, <strong>SetGeometryShader</strong>, or <strong>SetPixelShader</strong> (which are similar to the API methods <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshader"><strong>VSSetShader</strong></a>, <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshader"><strong>GSSetShader</strong></a>, and <a href="/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshader"><strong>PSSetShader</strong></a>).</span></span></p></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

<span data-ttu-id="8e9d5-142">Os grupos de estado de efeito são listados em [estado de efeito](d3d10-effect-states.md).</span><span class="sxs-lookup"><span data-stu-id="8e9d5-142">Effect state groups are listed in [effect state](d3d10-effect-states.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8e9d5-143">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8e9d5-143">Examples</span></span>

<span data-ttu-id="8e9d5-144">Este exemplo (de [exemplo CubeMapGS](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) define o estado de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="8e9d5-144">This example (from [CubeMapGS sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) sets blending state.</span></span>


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



<span data-ttu-id="8e9d5-145">Este exemplo configura o estado do rasterizador para renderizar um objeto em wireframe.</span><span class="sxs-lookup"><span data-stu-id="8e9d5-145">This example sets up the rasterizer state to render an object in wireframe.</span></span>


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



<span data-ttu-id="8e9d5-146">Este exemplo define o estado do sombreador (de [exemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)); que usa um vértice e um sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="8e9d5-146">This example sets shader state (from [BasicHLSL10 sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx)); which uses a vertex and pixel shader.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8e9d5-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e9d5-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e9d5-148">Formato do efeito</span><span class="sxs-lookup"><span data-stu-id="8e9d5-148">Effect Format</span></span>](d3d10-effect-format.md)
</dt> </dl>

 

 



