---
title: Funções de compilador (referência de HLSL)
description: Esta seção contém informações sobre as seguintes funções do compilador do Direct3D HLSL
ms.assetid: aacc5207-3ec8-4031-b5c9-f7c0fb7b7095
keywords:
- funções, compilador
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee63fa17cc9216fdb92f69fed4d77bc65bb49048
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "104968760"
---
# <a name="compiler-functions-hlsl-reference"></a><span data-ttu-id="98885-104">Funções de compilador (referência de HLSL)</span><span class="sxs-lookup"><span data-stu-id="98885-104">Compiler functions (HLSL reference)</span></span>

<span data-ttu-id="98885-105">Esta seção contém informações sobre as seguintes funções do compilador do Direct3D HLSL:</span><span class="sxs-lookup"><span data-stu-id="98885-105">This section contains information about the following Direct3D HLSL compiler functions:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="98885-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="98885-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98885-107">Tópico</span><span class="sxs-lookup"><span data-stu-id="98885-107">Topic</span></span></th>
<th><span data-ttu-id="98885-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="98885-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="98885-109"><a href="d3d11reflect.md"><strong>D3D11Reflect</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-109"><a href="d3d11reflect.md"><strong>D3D11Reflect</strong></a></span></span><br/></td>
<td><span data-ttu-id="98885-110">Obtém um ponteiro para uma interface de reflexão.</span><span class="sxs-lookup"><span data-stu-id="98885-110">Gets a pointer to a reflection interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98885-111"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile"><strong>D3DCompile</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-111"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile"><strong>D3DCompile</strong></a></span></span><br/></td>
<td><span data-ttu-id="98885-112">Compile o código de HLSL ou um arquivo de efeito no código de bytes para um determinado destino.</span><span class="sxs-lookup"><span data-stu-id="98885-112">Compile HLSL code or an effect file into bytecode for a given target.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98885-113"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-113"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a></span></span><br/></td>
<td><span data-ttu-id="98885-114">Compila o código de HLSL (linguagem de sombreamento de alto nível) da Microsoft em bytes de um determinado destino.</span><span class="sxs-lookup"><span data-stu-id="98885-114">Compiles Microsoft High Level Shader Language (HLSL) code into bytecode for a given target.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98885-115"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-115"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="98885-116">Você pode usar essa API para desenvolver seus aplicativos da Windows Store, mas não pode usá-los em aplicativos que você envia para a Windows Store.</span><span class="sxs-lookup"><span data-stu-id="98885-116">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span> <span data-ttu-id="98885-117">Consulte a seção, &quot; compilando sombreadores para UWP &quot; , em comentários para <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="98885-117">Refer to the section, &quot;Compiling shaders for UWP&quot;, in the remarks for <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="98885-118">Compila o código de HLSL em bytes para um determinado destino.</span><span class="sxs-lookup"><span data-stu-id="98885-118">Compiles HLSL code into bytecode for a given target.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98885-119"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompressshaders"><strong>D3DCompressShaders</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-119"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompressshaders"><strong>D3DCompressShaders</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="98885-120">Você pode usar essa API para desenvolver seus aplicativos da Windows Store, mas não pode usá-los em aplicativos que você envia para a Windows Store.</span><span class="sxs-lookup"><span data-stu-id="98885-120">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="98885-121">Compacta um conjunto de sombreadores em uma forma mais compacta.</span><span class="sxs-lookup"><span data-stu-id="98885-121">Compresses a set of shaders into a more compact form.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98885-122"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcreateblob"><strong>D3DCreateBlob</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-122"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcreateblob"><strong>D3DCreateBlob</strong></a></span></span><br/></td>
<td><span data-ttu-id="98885-123">Cria um buffer.</span><span class="sxs-lookup"><span data-stu-id="98885-123">Creates a buffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98885-124"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph"><strong>D3DCreateFunctionLinkingGraph</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-124"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph"><strong>D3DCreateFunctionLinkingGraph</strong></a></span></span><br/></td>
<td><span data-ttu-id="98885-125">Cria uma interface de grafo de vinculação de função.</span><span class="sxs-lookup"><span data-stu-id="98885-125">Creates a function-linking-graph interface.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="98885-126">Essa função faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas do Direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="98885-126">This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98885-127"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker"><strong>D3DCreateLinker</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-127"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker"><strong>D3DCreateLinker</strong></a></span></span><br/></td>
<td><span data-ttu-id="98885-128">Cria uma interface de vinculador.</span><span class="sxs-lookup"><span data-stu-id="98885-128">Creates a linker interface.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="98885-129">Essa função faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas do Direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="98885-129">This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98885-130"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddecompressshaders"><strong>D3DDecompressShaders</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-130"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddecompressshaders"><strong>D3DDecompressShaders</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="98885-131">Você pode usar essa API para desenvolver seus aplicativos da Windows Store, mas não pode usá-los em aplicativos que você envia para a Windows Store.</span><span class="sxs-lookup"><span data-stu-id="98885-131">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="98885-132">Descompacta um ou mais sombreadores de um conjunto compactado.</span><span class="sxs-lookup"><span data-stu-id="98885-132">Decompresses one or more shaders from a compressed set.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98885-133"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble"><strong>D3DDisassemble</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-133"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble"><strong>D3DDisassemble</strong></a></span></span><br/></td>
<td><span data-ttu-id="98885-134">Desmonta o código HLSL compilado.</span><span class="sxs-lookup"><span data-stu-id="98885-134">Disassembles compiled HLSL code.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98885-135"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect"><strong>D3DDisassemble10Effect</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-135"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect"><strong>D3DDisassemble10Effect</strong></a></span></span><br/></td>
<td><span data-ttu-id="98885-136">Desmonta o código HLSL compilado de um efeito de Direct3D10.</span><span class="sxs-lookup"><span data-stu-id="98885-136">Disassembles compiled HLSL code from a Direct3D10 effect.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98885-137"><a href="/windows/win32/api/d3d11shadertracing/nf-d3d11shadertracing-d3ddisassemble11trace"><strong>D3DDisassemble11Trace</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-137"><a href="/windows/win32/api/d3d11shadertracing/nf-d3d11shadertracing-d3ddisassemble11trace"><strong>D3DDisassemble11Trace</strong></a></span></span><br/></td>
<td><span data-ttu-id="98885-138">Desmonta uma seção do código HLSL compilado que é especificada pelas etapas de rastreamento do sombreador.</span><span class="sxs-lookup"><span data-stu-id="98885-138">Disassembles a section of compiled HLSL code that is specified by shader trace steps.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98885-139"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassembleregion"><strong>D3DDisassembleRegion</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-139"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassembleregion"><strong>D3DDisassembleRegion</strong></a></span></span><br/></td>
<td><span data-ttu-id="98885-140">Desmonta uma região específica do código HLSL compilado.</span><span class="sxs-lookup"><span data-stu-id="98885-140">Disassembles a specific region of compiled HLSL code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98885-141"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-141"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a></span></span><br/></td>
<td><span data-ttu-id="98885-142">Recupera uma parte específica de um resultado de compilação.</span><span class="sxs-lookup"><span data-stu-id="98885-142">Retrieves a specific part from a compilation result.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98885-143"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetdebuginfo"><strong>D3DGetDebugInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-143"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetdebuginfo"><strong>D3DGetDebugInfo</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="98885-144">Você pode usar essa API para desenvolver seus aplicativos da Windows Store, mas não pode usá-los em aplicativos que você envia para a Windows Store.</span><span class="sxs-lookup"><span data-stu-id="98885-144">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="98885-145">Obtém informações de depuração do sombreador.</span><span class="sxs-lookup"><span data-stu-id="98885-145">Gets shader debug information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98885-146"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-146"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br /><span data-ttu-id="98885-147">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a> pode ser alterado ou indisponível para versões após Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="98885-147">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a> may be altered or unavailable for releases after Windows 8.1.</span></span> <span data-ttu-id="98885-148">Em vez disso, use <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> com o valor <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_AND_OUTPUT_SIGNATURE_BLOB</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="98885-148">Instead use <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> with the <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_AND_OUTPUT_SIGNATURE_BLOB</strong></a> value.</span></span>
</blockquote>
<br/> <span data-ttu-id="98885-149">Obtém as assinaturas de entrada e saída de um resultado de compilação.</span><span class="sxs-lookup"><span data-stu-id="98885-149">Gets the input and output signatures from a compilation result.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98885-150">[<strong>D3DGetInputSignatureBlob</strong>] (/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob)</span><span class="sxs-lookup"><span data-stu-id="98885-150">[<strong>D3DGetInputSignatureBlob</strong>](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob)</span></span><br/></td>
<td><blockquote>
[!Note]<br /><span data-ttu-id="98885-151">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob"><strong>D3DGetInputSignatureBlob</strong></a> pode ser alterado ou indisponível para versões após Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="98885-151">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob"><strong>D3DGetInputSignatureBlob</strong></a> may be altered or unavailable for releases after Windows 8.1.</span></span> <span data-ttu-id="98885-152">Em vez disso, use <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> com o valor <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_SIGNATURE_BLOB</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="98885-152">Instead use <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> with the <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_SIGNATURE_BLOB</strong></a> value.</span></span>
</blockquote>
<br/> <span data-ttu-id="98885-153">Obtém a assinatura de entrada de um resultado de compilação.</span><span class="sxs-lookup"><span data-stu-id="98885-153">Gets the input signature from a compilation result.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98885-154"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-154"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br /><span data-ttu-id="98885-155">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a> pode ser alterado ou indisponível para versões após Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="98885-155">
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a> may be altered or unavailable for releases after Windows 8.1.</span></span> <span data-ttu-id="98885-156">Em vez disso, use <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> com o valor <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_OUTPUT_SIGNATURE_BLOB</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="98885-156">Instead use <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> with the <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_OUTPUT_SIGNATURE_BLOB</strong></a> value.</span></span>
</blockquote>
<br/> <span data-ttu-id="98885-157">Obtém a assinatura de saída de um resultado de compilação.</span><span class="sxs-lookup"><span data-stu-id="98885-157">Gets the output signature from a compilation result.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98885-158"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgettraceinstructionoffsets"><strong>D3DGetTraceInstructionOffsets</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-158"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgettraceinstructionoffsets"><strong>D3DGetTraceInstructionOffsets</strong></a></span></span><br/></td>
<td><span data-ttu-id="98885-159">Recupera os deslocamentos de byte para obter instruções em uma seção de código de sombreador.</span><span class="sxs-lookup"><span data-stu-id="98885-159">Retrieves the byte offsets for instructions within a section of shader code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98885-160"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule"><strong>D3DLoadModule</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-160"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule"><strong>D3DLoadModule</strong></a></span></span><br/></td>
<td><span data-ttu-id="98885-161">Cria uma interface de módulo do sombreador a partir dos dados de origem do módulo do sombreador.</span><span class="sxs-lookup"><span data-stu-id="98885-161">Creates a shader module interface from source data for the shader module.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="98885-162">Essa função faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas do Direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="98885-162">This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98885-163"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess"><strong>D3DPreprocess</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-163"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess"><strong>D3DPreprocess</strong></a></span></span><br/></td>
<td><span data-ttu-id="98885-164">Pré-processa o código HLSL não compilado.</span><span class="sxs-lookup"><span data-stu-id="98885-164">Preprocesses uncompiled HLSL code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98885-165"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreadfiletoblob"><strong>D3DReadFileToBlob</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-165"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreadfiletoblob"><strong>D3DReadFileToBlob</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="98885-166">Você pode usar essa API para desenvolver seus aplicativos da Windows Store, mas não pode usá-los em aplicativos que você envia para a Windows Store.</span><span class="sxs-lookup"><span data-stu-id="98885-166">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="98885-167">Lê um arquivo que está no disco na memória.</span><span class="sxs-lookup"><span data-stu-id="98885-167">Reads a file that is on disk into memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98885-168"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect"><strong>D3DReflect</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-168"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect"><strong>D3DReflect</strong></a></span></span><br/></td>
<td><span data-ttu-id="98885-169">Obtém um ponteiro para uma interface de reflexão.</span><span class="sxs-lookup"><span data-stu-id="98885-169">Gets a pointer to a reflection interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98885-170"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dreflectlibrary"><strong>D3DReflectLibrary</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-170"><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dreflectlibrary"><strong>D3DReflectLibrary</strong></a></span></span><br/></td>
<td><span data-ttu-id="98885-171">Cria uma interface de reflexão de biblioteca a partir de dados de origem que contém uma biblioteca HLSL de funções.</span><span class="sxs-lookup"><span data-stu-id="98885-171">Creates a library-reflection interface from source data that contains an HLSL library of functions.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="98885-172">Essa função faz parte da tecnologia de vinculação do sombreador HLSL que você pode usar em todas as plataformas do Direct3D 11 para criar funções HLSL pré-compiladas, empacotá-las em bibliotecas e vinculá-las a sombreadores completos em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="98885-172">This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98885-173"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dsetblobpart"><strong>D3DSetBlobPart</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-173"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dsetblobpart"><strong>D3DSetBlobPart</strong></a></span></span><br/></td>
<td><span data-ttu-id="98885-174">Define informações em um resultado de compilação.</span><span class="sxs-lookup"><span data-stu-id="98885-174">Sets information in a compilation result.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98885-175"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dstripshader"><strong>D3DStripShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-175"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dstripshader"><strong>D3DStripShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="98885-176">Remove BLOBs indesejados de um resultado de compilação.</span><span class="sxs-lookup"><span data-stu-id="98885-176">Removes unwanted blobs from a compilation result.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98885-177"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dwriteblobtofile"><strong>D3DWriteBlobToFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="98885-177"><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dwriteblobtofile"><strong>D3DWriteBlobToFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="98885-178">Você pode usar essa API para desenvolver seus aplicativos da Windows Store, mas não pode usá-los em aplicativos que você envia para a Windows Store.</span><span class="sxs-lookup"><span data-stu-id="98885-178">You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</span></span>
</blockquote>
<br/> <span data-ttu-id="98885-179">Grava um blob de memória em um arquivo no disco.</span><span class="sxs-lookup"><span data-stu-id="98885-179">Writes a memory blob to a file on disk.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="98885-180">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="98885-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98885-181">Referência de D3DCompiler</span><span class="sxs-lookup"><span data-stu-id="98885-181">D3DCompiler Reference</span></span>](dx-graphics-d3dcompiler-reference.md)
</dt> </dl>

