---
title: 'Interfaces de sombreador (elementos gráficos do Direct3D 11) '
description: Esta seção contém informações sobre as interfaces de sombreador.
ms.assetid: 1791d2c9-3791-47fe-b887-a8117ecc798b
keywords:
- interfaces, sombreador do Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d55e591d56442b641482a76a4ec93c0055029fc0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369111"
---
# <a name="shader-interfaces-direct3d-11-graphics"></a><span data-ttu-id="7aefc-104">Interfaces de sombreador (elementos gráficos do Direct3D 11) </span><span class="sxs-lookup"><span data-stu-id="7aefc-104">Shader Interfaces (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="7aefc-105">Esta seção contém informações sobre as interfaces de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7aefc-105">This section contains information about the shader interfaces.</span></span>

<span data-ttu-id="7aefc-106">Cada uma dessas interfaces de sombreador gerencia um sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="7aefc-106">Each of these shader interfaces manages a compiled shader.</span></span> <span data-ttu-id="7aefc-107">A interface é criada quando um sombreador é compilado e, em seguida, é passada para várias APIs que precisam de acesso a um sombreador compilado; como ao associar um sombreador a um estágio de pipeline ou obter uma assinatura de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7aefc-107">The interface is created when a shader is compiled, and is then passed to various APIs that need access to a compiled shader; such as when binding a shader to a pipeline stage or getting a shader signature.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="7aefc-108">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="7aefc-108">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7aefc-109">Tópico</span><span class="sxs-lookup"><span data-stu-id="7aefc-109">Topic</span></span></th>
<th><span data-ttu-id="7aefc-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="7aefc-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7aefc-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance"><strong>ID3D11ClassInstance</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aefc-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance"><strong>ID3D11ClassInstance</strong></a></span></span><br/></td>
<td><span data-ttu-id="7aefc-112">Essa interface encapsula uma classe HLSL.</span><span class="sxs-lookup"><span data-stu-id="7aefc-112">This interface encapsulates an HLSL class.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7aefc-113"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage"><strong>ID3D11ClassLinkage</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aefc-113"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage"><strong>ID3D11ClassLinkage</strong></a></span></span><br/></td>
<td><span data-ttu-id="7aefc-114">Essa interface encapsula uma vinculação dinâmica HLSL.</span><span class="sxs-lookup"><span data-stu-id="7aefc-114">This interface encapsulates an HLSL dynamic linkage.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7aefc-115"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader"><strong>ID3D11ComputeShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aefc-115"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader"><strong>ID3D11ComputeShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="7aefc-116">Uma interface de sombreador de computação gerencia um programa executável (um sombreador de computação) que controla o estágio Compute-Shader.</span><span class="sxs-lookup"><span data-stu-id="7aefc-116">A compute-shader interface manages an executable program (a compute shader) that controls the compute-shader stage.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7aefc-117"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader"><strong>ID3D11DomainShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aefc-117"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader"><strong>ID3D11DomainShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="7aefc-118">Uma interface de sombreador de domínio gerencia um programa executável (um sombreador de domínio) que controla o estágio Domain-Shader.</span><span class="sxs-lookup"><span data-stu-id="7aefc-118">A domain-shader interface manages an executable program (a domain shader) that controls the domain-shader stage.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7aefc-119"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aefc-119"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a></span></span><br/></td>
<td><span data-ttu-id="7aefc-120">Uma interface de grafo de vinculação de função é usada para construir sombreadores que consistem em uma sequência de chamadas de função pré-compiladas que passam valores entre si.</span><span class="sxs-lookup"><span data-stu-id="7aefc-120">A function-linking-graph interface is used for constructing shaders that consist of a sequence of precompiled function calls that pass values to each other.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7aefc-121">Essa interface faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas do Direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="7aefc-121">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7aefc-122"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionreflection"><strong>ID3D11FunctionReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aefc-122"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionreflection"><strong>ID3D11FunctionReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="7aefc-123">Uma interface de reflexão de função acessa informações de função.</span><span class="sxs-lookup"><span data-stu-id="7aefc-123">A function-reflection interface accesses function info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7aefc-124">Essa interface faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas do Direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="7aefc-124">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7aefc-125"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionparameterreflection"><strong>ID3D11FunctionParameterReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aefc-125"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionparameterreflection"><strong>ID3D11FunctionParameterReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="7aefc-126">Uma interface de função-parâmetro-Reflection acessa informações de parâmetro de função.</span><span class="sxs-lookup"><span data-stu-id="7aefc-126">A function-parameter-reflection interface accesses function-parameter info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7aefc-127">Essa interface faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas do Direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="7aefc-127">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7aefc-128"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader"><strong>ID3D11GeometryShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aefc-128"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader"><strong>ID3D11GeometryShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="7aefc-129">Uma interface Geometry-Shader gerencia um programa executável (um sombreador geometry) que controla o estágio Geometry-Shader.</span><span class="sxs-lookup"><span data-stu-id="7aefc-129">A geometry-shader interface manages an executable program (a geometry shader) that controls the geometry-shader stage.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7aefc-130"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader"><strong>ID3D11HullShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aefc-130"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader"><strong>ID3D11HullShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="7aefc-131">Uma interface envoltória-Shader gerencia um programa executável (um sombreador envoltória) que controla o estágio envoltória-Shader.</span><span class="sxs-lookup"><span data-stu-id="7aefc-131">A hull-shader interface manages an executable program (a hull shader) that controls the hull-shader stage.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7aefc-132"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11libraryreflection"><strong>ID3D11LibraryReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aefc-132"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11libraryreflection"><strong>ID3D11LibraryReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="7aefc-133">Uma interface de reflexão de biblioteca acessa informações da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="7aefc-133">A library-reflection interface accesses library info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7aefc-134">Essa interface faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas do Direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="7aefc-134">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7aefc-135"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aefc-135"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a></span></span><br/></td>
<td><span data-ttu-id="7aefc-136">Uma interface de vinculador é usada para vincular um módulo de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7aefc-136">A linker interface is used to link a shader module.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7aefc-137">Essa interface faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas do Direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="7aefc-137">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7aefc-138"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linkingnode"><strong>ID3D11LinkingNode</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aefc-138"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linkingnode"><strong>ID3D11LinkingNode</strong></a></span></span><br/></td>
<td><span data-ttu-id="7aefc-139">Uma interface de nó de vinculação é usada para vinculação de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7aefc-139">A linking-node interface is used for shader linking.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7aefc-140">Essa interface faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas do Direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="7aefc-140">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7aefc-141"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module"><strong>ID3D11Module</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aefc-141"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module"><strong>ID3D11Module</strong></a></span></span><br/></td>
<td><span data-ttu-id="7aefc-142">Uma interface de módulo cria uma instância de um módulo que é usada para a reassociação de recursos.</span><span class="sxs-lookup"><span data-stu-id="7aefc-142">A module interface creates an instance of a module that is used for resource rebinding.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7aefc-143">Essa interface faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas do Direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="7aefc-143">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7aefc-144"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance"><strong>ID3D11ModuleInstance</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aefc-144"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance"><strong>ID3D11ModuleInstance</strong></a></span></span><br/></td>
<td><span data-ttu-id="7aefc-145">Uma interface de instância de módulo é usada para reassociação de recursos.</span><span class="sxs-lookup"><span data-stu-id="7aefc-145">A module-instance interface is used for resource rebinding.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7aefc-146">Essa interface faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas do Direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="7aefc-146">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7aefc-147"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader"><strong>ID3D11PixelShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aefc-147"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader"><strong>ID3D11PixelShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="7aefc-148">Uma interface de sombreador de pixel gerencia um programa executável (um sombreador de pixel) que controla o estágio pixel-shader.</span><span class="sxs-lookup"><span data-stu-id="7aefc-148">A pixel-shader interface manages an executable program (a pixel shader) that controls the pixel-shader stage.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7aefc-149"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflection"><strong>ID3D11ShaderReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aefc-149"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflection"><strong>ID3D11ShaderReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="7aefc-150">Uma interface Shader-Reflection acessa informações de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7aefc-150">A shader-reflection interface accesses shader information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7aefc-151"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer"><strong>ID3D11ShaderReflectionConstantBuffer</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aefc-151"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer"><strong>ID3D11ShaderReflectionConstantBuffer</strong></a></span></span><br/></td>
<td><span data-ttu-id="7aefc-152">Esta interface Shader-Reflection fornece acesso a um buffer constante.</span><span class="sxs-lookup"><span data-stu-id="7aefc-152">This shader-reflection interface provides access to a constant buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7aefc-153"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectiontype"><strong>ID3D11ShaderReflectionType</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aefc-153"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectiontype"><strong>ID3D11ShaderReflectionType</strong></a></span></span><br/></td>
<td><span data-ttu-id="7aefc-154">Esta interface Shader-Reflection fornece acesso ao tipo de variável.</span><span class="sxs-lookup"><span data-stu-id="7aefc-154">This shader-reflection interface provides access to variable type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7aefc-155"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionvariable"><strong>ID3D11ShaderReflectionVariable</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aefc-155"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionvariable"><strong>ID3D11ShaderReflectionVariable</strong></a></span></span><br/></td>
<td><span data-ttu-id="7aefc-156">Essa interface Shader-Reflection fornece acesso a uma variável.</span><span class="sxs-lookup"><span data-stu-id="7aefc-156">This shader-reflection interface provides access to a variable.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7aefc-157"><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aefc-157"><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a></span></span><br/></td>
<td><span data-ttu-id="7aefc-158">Uma interface <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a> implementa métodos para obter rastreamentos de execuções de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7aefc-158">An <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a> interface implements methods for obtaining traces of shader executions.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7aefc-159"><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aefc-159"><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a></span></span><br/></td>
<td><span data-ttu-id="7aefc-160">Uma interface <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a> implementa um método para gerar objetos de informações de rastreamento de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7aefc-160">An <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a> interface implements a method for generating shader trace information objects.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7aefc-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader"><strong>ID3D11VertexShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="7aefc-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader"><strong>ID3D11VertexShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="7aefc-162">Uma interface Vertex-Shader gerencia um programa executável (um sombreador de vértice) que controla o estágio Vertex-Shader.</span><span class="sxs-lookup"><span data-stu-id="7aefc-162">A vertex-shader interface manages an executable program (a vertex shader) that controls the vertex-shader stage.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="7aefc-163">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7aefc-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7aefc-164">Referência do sombreador</span><span class="sxs-lookup"><span data-stu-id="7aefc-164">Shader Reference</span></span>](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

