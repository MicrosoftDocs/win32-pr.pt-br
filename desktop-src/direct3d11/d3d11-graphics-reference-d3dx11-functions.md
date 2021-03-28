---
title: Funções D3DX (gráficos do Direct3D 11)
description: Esta seção contém informações sobre as funções do D3DX 11.
ms.assetid: 7548c02e-c8c2-4629-95ac-d21ca7a39f0a
keywords:
- funções, DirectX 11 D3DX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b76c1764f464461b4800a9161ac37dcff8c539a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369054"
---
# <a name="d3dx-functions-direct3d-11-graphics"></a><span data-ttu-id="4c5c1-104">Funções D3DX (gráficos do Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="4c5c1-104">D3DX Functions (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="4c5c1-105">Esta seção contém informações sobre as funções do D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-105">This section contains information about the D3DX 11 functions.</span></span>

> [!Note]  
> <span data-ttu-id="4c5c1-106">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 


## <a name="in-this-section"></a><span data-ttu-id="4c5c1-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="4c5c1-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4c5c1-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="4c5c1-108">Topic</span></span></th>
<th><span data-ttu-id="4c5c1-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c5c1-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4c5c1-110"><a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-110"><a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-111">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-111">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-112">Em vez de usar essa função, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use uma das APIs de compilação HLSL, como a API <a href="/windows/desktop/direct3dhlsl/d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="4c5c1-112">Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the <a href="/windows/desktop/direct3dhlsl/d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-113">Compilar um sombreador ou um efeito de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-113">Compile a shader or an effect from a file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c5c1-114"><a href="d3dx11compilefrommemory.md"><strong>D3DX11CompileFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-114"><a href="d3dx11compilefrommemory.md"><strong>D3DX11CompileFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-115">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-115">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-116">Em vez de usar essa função, recomendamos que você compile offline usando o compilador de linha de comando Fxc.exe ou use uma das APIs de compilação HLSL, como a API <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="4c5c1-116">Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-117">Compile um sombreador ou um efeito que é carregado na memória.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-117">Compile a shader or an effect that is loaded in memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c5c1-118"><a href="d3dx11compilefromresource.md"><strong>D3DX11CompileFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-118"><a href="d3dx11compilefromresource.md"><strong>D3DX11CompileFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-119">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-119">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-120">Em vez de usar essa função, recomendamos que você use <a href="/windows/desktop/menurc/resources-functions">funções de recurso</a>e, em seguida, compile offline usando o compilador de linha de comando Fxc.exe ou use uma das APIs de compilação HLSL, como a API <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="4c5c1-120">Instead of using this function, we recommend that you use <a href="/windows/desktop/menurc/resources-functions">resource functions</a>, then compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-121">Compilar um sombreador ou um efeito de um recurso.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-121">Compile a shader or an effect from a resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c5c1-122"><a href="d3dx11computenormalmap.md"><strong>D3DX11ComputeNormalMap</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-122"><a href="d3dx11computenormalmap.md"><strong>D3DX11ComputeNormalMap</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-123">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-123">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-124">Em vez de usar essa função, recomendamos que você use a biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>ComputeNormalMap</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-124">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>ComputeNormalMap</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-125">Converte um mapa de altura em um mapa normal.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-125">Converts a height map into a normal map.</span></span> <span data-ttu-id="4c5c1-126">Os componentes (x, y, z) de cada normal são mapeados para os canais (r, g, b) da textura de saída.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-126">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c5c1-127"><a href="d3dx11createasynccompilerprocessor.md"><strong>D3DX11CreateAsyncCompilerProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-127"><a href="d3dx11createasynccompilerprocessor.md"><strong>D3DX11CreateAsyncCompilerProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-128">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-128">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="4c5c1-129">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-129">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-130">Crie um processador de dados assíncronos para um sombreador.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-130">Create an asynchronous-data processor for a shader.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c5c1-131"><a href="d3dx11createasyncfileloader.md"><strong>D3DX11CreateAsyncFileLoader</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-131"><a href="d3dx11createasyncfileloader.md"><strong>D3DX11CreateAsyncFileLoader</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-132">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-132">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="4c5c1-133">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-133">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-134">Crie um carregador de arquivo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-134">Create an asynchronous-file loader.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c5c1-135"><a href="d3dx11createasyncmemoryloader.md"><strong>D3DX11CreateAsyncMemoryLoader</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-135"><a href="d3dx11createasyncmemoryloader.md"><strong>D3DX11CreateAsyncMemoryLoader</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-136">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-136">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="4c5c1-137">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-137">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-138">Crie um carregador de memória assíncrona.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-138">Create an asynchronous-memory loader.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c5c1-139"><a href="d3dx11createasyncresourceloader.md"><strong>D3DX11CreateAsyncResourceLoader</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-139"><a href="d3dx11createasyncresourceloader.md"><strong>D3DX11CreateAsyncResourceLoader</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-140">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-140">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="4c5c1-141">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-141">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-142">Crie um carregador de recurso assíncrono.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-142">Create an asynchronous-resource loader.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c5c1-143"><a href="d3dx11createasyncshaderpreprocessprocessor.md"><strong>D3DX11CreateAsyncShaderPreprocessProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-143"><a href="d3dx11createasyncshaderpreprocessprocessor.md"><strong>D3DX11CreateAsyncShaderPreprocessProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-144">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-144">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="4c5c1-145">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-145">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-146">Crie um processador de dados para um sombreador de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-146">Create a data processor for a shader asynchronously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c5c1-147"><a href="d3dx11createasynctextureinfoprocessor.md"><strong>D3DX11CreateAsyncTextureInfoProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-147"><a href="d3dx11createasynctextureinfoprocessor.md"><strong>D3DX11CreateAsyncTextureInfoProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-148">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-148">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="4c5c1-149">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-149">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-150">Crie um processador de dados para ser usado com uma <a href="id3dx11threadpump.md"><strong>bomba de thread</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-150">Create a data processor to be used with a <a href="id3dx11threadpump.md"><strong>thread pump</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c5c1-151"><a href="d3dx11createasynctextureprocessor.md"><strong>D3DX11CreateAsyncTextureProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-151"><a href="d3dx11createasynctextureprocessor.md"><strong>D3DX11CreateAsyncTextureProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-152">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-152">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="4c5c1-153">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-153">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-154">Crie um processador de dados para ser usado com uma <a href="id3dx11threadpump.md"><strong>bomba de thread</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-154">Create a data processor to be used with a <a href="id3dx11threadpump.md"><strong>thread pump</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c5c1-155"><a href="d3dx11createasyncshaderresourceviewprocessor.md"><strong>D3DX11CreateAsyncShaderResourceViewProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-155"><a href="d3dx11createasyncshaderresourceviewprocessor.md"><strong>D3DX11CreateAsyncShaderResourceViewProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-156">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-156">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="4c5c1-157">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-157">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-158">Crie um processador de dados que carregará um recurso e, em seguida, crie uma exibição de recurso de sombreador para ele.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-158">Create a data processor that will load a resource and then create a shader-resource view for it.</span></span> <span data-ttu-id="4c5c1-159">Os processadores de dados são um componente do recurso de carregamento de dados assíncronos no D3DX11 que usa <a href="id3dx11threadpump.md"><strong>bombas de thread</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-159">Data processors are a component of the asynchronous data loading feature in D3DX11 that uses <a href="id3dx11threadpump.md"><strong>thread pumps</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c5c1-160"><a href="d3dx11createshaderresourceviewfromfile.md"><strong>D3DX11CreateShaderResourceViewFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-160"><a href="d3dx11createshaderresourceviewfromfile.md"><strong>D3DX11CreateShaderResourceViewFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-161">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-161">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="4c5c1-162">Em vez de usar essa função, recomendamos que você as use:</span><span class="sxs-lookup"><span data-stu-id="4c5c1-162">Instead of using this function, we recommend that you use these:</span></span></p>
<ul>
<li><span data-ttu-id="4c5c1-163"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (Runtime), <strong>CreateXXXTextureFromFile</strong> (em que xxx é DDS ou WIC)</span><span class="sxs-lookup"><span data-stu-id="4c5c1-163"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromFile</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="4c5c1-164">Biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (ferramentas), <strong>LoadFromXXXFile</strong> (em que xxx é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos) e, em seguida, <strong>CreateShaderResourceView</strong></span><span class="sxs-lookup"><span data-stu-id="4c5c1-164"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXFile</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateShaderResourceView</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="4c5c1-165">Criar um sombreador – modo de exibição de recursos de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-165">Create a shader-resource view from a file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c5c1-166"><a href="d3dx11createshaderresourceviewfrommemory.md"><strong>D3DX11CreateShaderResourceViewFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-166"><a href="d3dx11createshaderresourceviewfrommemory.md"><strong>D3DX11CreateShaderResourceViewFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-167">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-167">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="4c5c1-168">Em vez de usar essa função, recomendamos que você as use:</span><span class="sxs-lookup"><span data-stu-id="4c5c1-168">Instead of using this function, we recommend that you use these:</span></span></p>
<ul>
<li><span data-ttu-id="4c5c1-169"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (Runtime), <strong>CreateXXXTextureFromMemory</strong> (em que xxx é DDS ou WIC)</span><span class="sxs-lookup"><span data-stu-id="4c5c1-169"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromMemory</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="4c5c1-170">Biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (ferramentas), <strong>LoadFromXXXMemory</strong> (em que xxx é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos) e, em seguida, <strong>CreateShaderResourceView</strong></span><span class="sxs-lookup"><span data-stu-id="4c5c1-170"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateShaderResourceView</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="4c5c1-171">Criar um sombreador – modo de exibição de recursos de um arquivo na memória.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-171">Create a shader-resource view from a file in memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c5c1-172"><a href="d3dx11createshaderresourceviewfromresource.md"><strong>D3DX11CreateShaderResourceViewFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-172"><a href="d3dx11createshaderresourceviewfromresource.md"><strong>D3DX11CreateShaderResourceViewFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-173">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-173">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="4c5c1-174">Em vez de usar essa função, recomendamos que você use <a href="/windows/desktop/menurc/resources-functions">funções de recurso</a>e, em seguida, estas:</span><span class="sxs-lookup"><span data-stu-id="4c5c1-174">Instead of using this function, we recommend that you use <a href="/windows/desktop/menurc/resources-functions">resource functions</a>, then these:</span></span></p>
<ul>
<li><span data-ttu-id="4c5c1-175"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (Runtime), <strong>CreateXXXTextureFromMemory</strong> (em que xxx é DDS ou WIC)</span><span class="sxs-lookup"><span data-stu-id="4c5c1-175"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromMemory</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="4c5c1-176">Biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (ferramentas), <strong>LoadFromXXXMemory</strong> (em que xxx é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos) e, em seguida, <strong>CreateShaderResourceView</strong></span><span class="sxs-lookup"><span data-stu-id="4c5c1-176"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateShaderResourceView</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="4c5c1-177">Criar um sombreador – modo de exibição de recursos de um recurso.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-177">Create a shader-resource view from a resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c5c1-178"><a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-178"><a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-179">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-179">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="4c5c1-180">Em vez de usar essa função, recomendamos que você as use:</span><span class="sxs-lookup"><span data-stu-id="4c5c1-180">Instead of using this function, we recommend that you use these:</span></span></p>
<ul>
<li><span data-ttu-id="4c5c1-181"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (Runtime), <strong>CreateXXXTextureFromFile</strong> (em que xxx é DDS ou WIC)</span><span class="sxs-lookup"><span data-stu-id="4c5c1-181"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromFile</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="4c5c1-182">Biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (ferramentas), <strong>LoadFromXXXFile</strong> (em que xxx é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos) e <strong>CreateTexture</strong></span><span class="sxs-lookup"><span data-stu-id="4c5c1-182"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXFile</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateTexture</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="4c5c1-183">Crie um recurso de textura a partir de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-183">Create a texture resource from a file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c5c1-184"><a href="d3dx11createtexturefrommemory.md"><strong>D3DX11CreateTextureFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-184"><a href="d3dx11createtexturefrommemory.md"><strong>D3DX11CreateTextureFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-185">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-185">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="4c5c1-186">Em vez de usar essa função, recomendamos que você as use:</span><span class="sxs-lookup"><span data-stu-id="4c5c1-186">Instead of using this function, we recommend that you use these:</span></span></p>
<ul>
<li><span data-ttu-id="4c5c1-187"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (Runtime), <strong>CreateXXXTextureFromMemory</strong> (em que xxx é DDS ou WIC)</span><span class="sxs-lookup"><span data-stu-id="4c5c1-187"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromMemory</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="4c5c1-188">Biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (ferramentas), <strong>LoadFromXXXMemory</strong> (em que xxx é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos) e <strong>CreateTexture</strong></span><span class="sxs-lookup"><span data-stu-id="4c5c1-188"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateTexture</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="4c5c1-189">Crie um recurso de textura a partir de um arquivo que reside na memória do sistema.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-189">Create a texture resource from a file residing in system memory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c5c1-190"><a href="d3dx11createtexturefromresource.md"><strong>D3DX11CreateTextureFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-190"><a href="d3dx11createtexturefromresource.md"><strong>D3DX11CreateTextureFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-191">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-191">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="4c5c1-192">Em vez de usar essa função, recomendamos que você use <a href="/windows/desktop/menurc/resources-functions">funções de recurso</a>e, em seguida, estas:</span><span class="sxs-lookup"><span data-stu-id="4c5c1-192">Instead of using this function, we recommend that you use <a href="/windows/desktop/menurc/resources-functions">resource functions</a>, then these:</span></span></p>
<ul>
<li><span data-ttu-id="4c5c1-193"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (Runtime), <strong>CreateXXXTextureFromMemory</strong> (em que xxx é DDS ou WIC)</span><span class="sxs-lookup"><span data-stu-id="4c5c1-193"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromMemory</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="4c5c1-194">Biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (ferramentas), <strong>LoadFromXXXMemory</strong> (em que xxx é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos) e <strong>CreateTexture</strong></span><span class="sxs-lookup"><span data-stu-id="4c5c1-194"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateTexture</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="4c5c1-195">Crie uma textura de outro recurso.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-195">Create a texture from another resource.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c5c1-196"><a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-196"><a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-197">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-197">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="4c5c1-198">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-198">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-199">Criar uma bomba de thread.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-199">Create a thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c5c1-200"><a href="d3dx11filtertexture.md"><strong>D3DX11FilterTexture</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-200"><a href="d3dx11filtertexture.md"><strong>D3DX11FilterTexture</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-201">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-201">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-202">Em vez de usar essa função, recomendamos que você use a biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>GenerateMipMaps</strong> e <strong>GenerateMipMaps3D</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-202">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>GenerateMipMaps</strong> and <strong>GenerateMipMaps3D</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-203">Gera cadeia de mipmap usando um filtro de textura específico.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-203">Generates mipmap chain using a particular texture filter.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c5c1-204"><a href="d3dx11getimageinfofromfile.md"><strong>D3DX11GetImageInfoFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-204"><a href="d3dx11getimageinfofromfile.md"><strong>D3DX11GetImageInfoFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-205">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-205">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-206">Em vez de usar essa função, recomendamos que você use a biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>GetMetadataFromXXXFile</strong> (em que xxx é o WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos).</span><span class="sxs-lookup"><span data-stu-id="4c5c1-206">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>GetMetadataFromXXXFile</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-207">Recupera informações sobre um determinado arquivo de imagem.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-207">Retrieves information about a given image file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c5c1-208"><a href="d3dx11getimageinfofrommemory.md"><strong>D3DX11GetImageInfoFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-208"><a href="d3dx11getimageinfofrommemory.md"><strong>D3DX11GetImageInfoFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-209">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-209">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-210">Em vez de usar essa função, recomendamos que você use a biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>GetMetadataFromXXXMemory</strong> (em que xxx é o WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos).</span><span class="sxs-lookup"><span data-stu-id="4c5c1-210">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>GetMetadataFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-211">Obtenha informações sobre uma imagem já carregada na memória.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-211">Get information about an image already loaded into memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c5c1-212"><a href="d3dx11getimageinfofromresource.md"><strong>D3DX11GetImageInfoFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-212"><a href="d3dx11getimageinfofromresource.md"><strong>D3DX11GetImageInfoFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-213">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-213">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-214">Em vez de usar essa função, recomendamos que você use <a href="/windows/desktop/menurc/resources-functions">funções de recurso</a>e, em seguida, use <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (Tools), <strong>LoadFromXXXMemory</strong> (em que xxx é WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos).</span><span class="sxs-lookup"><span data-stu-id="4c5c1-214">Instead of using this function, we recommend that you use <a href="/windows/desktop/menurc/resources-functions">resource functions</a>, then use <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-215">Recupera informações sobre uma determinada imagem em um recurso.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-215">Retrieves information about a given image in a resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c5c1-216"><a href="d3dx11loadtexturefromtexture.md"><strong>D3DX11LoadTextureFromTexture</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-216"><a href="d3dx11loadtexturefromtexture.md"><strong>D3DX11LoadTextureFromTexture</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-217">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-217">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-218">Em vez de usar essa função, recomendamos que você use a biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>redimensione</strong>, <strong>converta</strong>, <strong>compacte</strong>, <strong>Descompacte</strong>e/ou <strong>CopyRectangle</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-218">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>Resize</strong>, <strong>Convert</strong>, <strong>Compress</strong>, <strong>Decompress</strong>, and/or <strong>CopyRectangle</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-219">Carregar uma textura de uma textura.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-219">Load a texture from a texture.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c5c1-220"><a href="d3dx11preprocessshaderfromfile.md"><strong>D3DX11PreprocessShaderFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-220"><a href="d3dx11preprocessshaderfromfile.md"><strong>D3DX11PreprocessShaderFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-221">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-221">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-222">Em vez de usar essa função, recomendamos que você use a API <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="4c5c1-222">Instead of using this function, we recommend that you use the <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-223">Crie um sombreador de um arquivo sem compilá-lo.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-223">Create a shader from a file without compiling it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c5c1-224"><a href="d3dx11preprocessshaderfrommemory.md"><strong>D3DX11PreprocessShaderFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-224"><a href="d3dx11preprocessshaderfrommemory.md"><strong>D3DX11PreprocessShaderFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-225">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-225">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-226">Em vez de usar essa função, recomendamos que você use a API <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="4c5c1-226">Instead of using this function, we recommend that you use the <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-227">Crie um sombreador da memória sem compilá-lo.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-227">Create a shader from memory without compiling it.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c5c1-228"><a href="d3dx11preprocessshaderfromresource.md"><strong>D3DX11PreprocessShaderFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-228"><a href="d3dx11preprocessshaderfromresource.md"><strong>D3DX11PreprocessShaderFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-229">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-229">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-230">Em vez de usar essa função, recomendamos que você use a API <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="4c5c1-230">Instead of using this function, we recommend that you use the <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-231">Crie um sombreador de um recurso sem compilá-lo.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-231">Create a shader from a resource without compiling it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c5c1-232"><a href="d3dx11savetexturetofile.md"><strong>D3DX11SaveTextureToFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-232"><a href="d3dx11savetexturetofile.md"><strong>D3DX11SaveTextureToFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-233">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-233">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-234">Em vez de usar essa função, recomendamos que você use a biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>CaptureTexture</strong> , <strong>SaveToXXXFile</strong> (em que xxx é o WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos).</span><span class="sxs-lookup"><span data-stu-id="4c5c1-234">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>CaptureTexture</strong> then <strong>SaveToXXXFile</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span> <span data-ttu-id="4c5c1-235">Para o cenário simplificado de criação de uma captura de tela de uma textura de destino de renderização, recomendamos que você use a biblioteca <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> , <strong>SaveDDSTextureToFile</strong> ou <strong>SaveWICTextureToFile</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-235">For the simplified scenario of creating a screen shot from a render target texture, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library, <strong>SaveDDSTextureToFile</strong> or <strong>SaveWICTextureToFile</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-236">Salvar uma textura em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-236">Save a texture to a file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c5c1-237"><a href="d3dx11savetexturetomemory.md"><strong>D3DX11SaveTextureToMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-237"><a href="d3dx11savetexturetomemory.md"><strong>D3DX11SaveTextureToMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-238">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-238">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-239">Em vez de usar essa função, recomendamos que você use a biblioteca <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>CaptureTexture</strong> , <strong>SaveToXXXMemory</strong> (em que xxx é o WIC, DDS ou TGA; O WIC não oferece suporte a DDS e TGA; O D3DX 9 TGA com suporte como um formato de origem de arte comum para jogos).</span><span class="sxs-lookup"><span data-stu-id="4c5c1-239">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>CaptureTexture</strong> then <strong>SaveToXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-240">Salve uma textura na memória.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-240">Save a texture to memory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4c5c1-241"><a href="d3dx11shprojectcubemap.md"><strong>D3DX11SHProjectCubeMap</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-241"><a href="d3dx11shprojectcubemap.md"><strong>D3DX11SHProjectCubeMap</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-242">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-242">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-243">Em vez de usar essa função, recomendamos que você use a biblioteca <a href="https://github.com/Microsoft/DirectXMath/tree/master/SHMath">matemática de harmônicas esféricas</a> , <strong>SHProjectCubeMap</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-243">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXMath/tree/master/SHMath">Spherical Harmonics Math</a> library, <strong>SHProjectCubeMap</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-244">Projeta uma função representada em um mapa de cubo em harmônicas esféricas.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-244">Projects a function represented in a cube map into spherical harmonics.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4c5c1-245"><a href="d3dx11unsetalldeviceobjects.md"><strong>D3DX11UnsetAllDeviceObjects</strong></a></span><span class="sxs-lookup"><span data-stu-id="4c5c1-245"><a href="d3dx11unsetalldeviceobjects.md"><strong>D3DX11UnsetAllDeviceObjects</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-246">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-246">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4c5c1-247">Em vez de usar essa função, recomendamos que você use o método <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate"><strong>ID3D11DeviceContext:: clearstate</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="4c5c1-247">Instead of using this function, we recommend that you use the <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate"><strong>ID3D11DeviceContext::ClearState</strong></a> method.</span></span>
</blockquote>
<br/> <span data-ttu-id="4c5c1-248">Remove todos os recursos do dispositivo definindo seus ponteiros como <strong>NULL</strong>.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-248">Removes all resources from the device by setting their pointers to <strong>NULL</strong>.</span></span> <span data-ttu-id="4c5c1-249">Isso deve ser chamado durante o desligamento do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-249">This should be called during shutdown of your application.</span></span> <span data-ttu-id="4c5c1-250">Ele ajuda a garantir que, quando um estiver liberando todos os seus recursos, nenhum deles esteja associado ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4c5c1-250">It helps ensure that when one is releasing all of their resources that none of them are bound to the device.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="4c5c1-251">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4c5c1-251">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c5c1-252">Referência do D3DX 11</span><span class="sxs-lookup"><span data-stu-id="4c5c1-252">D3DX 11 Reference</span></span>](d3d11-graphics-reference-d3dx11.md)
</dt> </dl>

 

