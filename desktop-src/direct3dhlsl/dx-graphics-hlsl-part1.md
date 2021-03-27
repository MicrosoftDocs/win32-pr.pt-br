---
title: Compilar um sombreador
description: Agora, vamos examinar várias maneiras de compilar o código do sombreador e as convenções de extensões de arquivo para o código do sombreador.
ms.assetid: a4e6b7cd-c5cc-4165-ba73-205155e449c9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ea71da99dd68769324b07d3fc76a0c5ca00009d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294190"
---
# <a name="compiling-shaders"></a><span data-ttu-id="1a04e-103">Compilando sombreadores</span><span class="sxs-lookup"><span data-stu-id="1a04e-103">Compiling shaders</span></span>

> [!NOTE]
> <span data-ttu-id="1a04e-104">Este tópico aborda o `FXC.EXE` compilador usado para os modelos de sombreador 2 a 5,1.</span><span class="sxs-lookup"><span data-stu-id="1a04e-104">This topic covers the `FXC.EXE` compiler used for Shader Models 2 through 5.1.</span></span> <span data-ttu-id="1a04e-105">Para o Shader Model 6, você usa `DXC.EXE` em vez disso, que está documentado em [usando dxc.exe e dxcompiler.dll](https://github.com/microsoft/DirectXShaderCompiler/wiki/Using-dxc.exe-and-dxcompiler.dll).</span><span class="sxs-lookup"><span data-stu-id="1a04e-105">For Shader Model 6, you use `DXC.EXE` instead, which is documented in [Using dxc.exe and dxcompiler.dll](https://github.com/microsoft/DirectXShaderCompiler/wiki/Using-dxc.exe-and-dxcompiler.dll).</span></span>

<span data-ttu-id="1a04e-106">Microsoft Visual Studio 2012 agora pode compilar o código do sombreador de \* arquivos. HLSL que você inclui em seu projeto C++.</span><span class="sxs-lookup"><span data-stu-id="1a04e-106">Microsoft Visual Studio 2012 can now compile shader code from \*.hlsl files that you include in your C++ project.</span></span>

<span data-ttu-id="1a04e-107">Como parte do processo de compilação, o Visual Studio 2012 usa o compilador de código [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL para compilar os arquivos. HLSL em arquivos de objeto de sombreador binário ou em matrizes de bytes que são definidas em arquivos de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="1a04e-107">As part of the build process, Visual Studio 2012 uses the [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL code compiler to compile the .hlsl files into binary shader object files or into byte arrays that are defined in header files.</span></span> <span data-ttu-id="1a04e-108">Como o compilador de código HLSL compila cada arquivo. HLSL em seu projeto depende de como você especifica a propriedade de **arquivos de saída** para esse arquivo.</span><span class="sxs-lookup"><span data-stu-id="1a04e-108">How the HLSL code compiler compiles each .hlsl file in your project depends on how you specify the **Ouput Files** property for that file.</span></span> <span data-ttu-id="1a04e-109">Para obter mais informações sobre páginas de propriedades do HLSL, consulte [páginas de propriedades do HLSL](/previous-versions/visualstudio/visual-studio-2012/jj620902(v=vs.110)).</span><span class="sxs-lookup"><span data-stu-id="1a04e-109">For more info about HLSL property pages, see [HLSL Property Pages](/previous-versions/visualstudio/visual-studio-2012/jj620902(v=vs.110)).</span></span>

<span data-ttu-id="1a04e-110">O método de compilação que você usa normalmente depende do tamanho do seu \* arquivo. HLSL.</span><span class="sxs-lookup"><span data-stu-id="1a04e-110">The compile method that you use typically depends on the size of your \*.hlsl file.</span></span> <span data-ttu-id="1a04e-111">Se você incluir uma grande quantidade de código de byte em um cabeçalho, aumentará o tamanho e o tempo de carregamento inicial do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1a04e-111">If you include a large amount of byte code in a header, you increase the size and the initial load time of your app.</span></span> <span data-ttu-id="1a04e-112">Você também força todo o código de byte a residir na memória mesmo depois que o sombreador é criado, o que desperdiça recursos.</span><span class="sxs-lookup"><span data-stu-id="1a04e-112">You also force all byte code to reside in memory even after the shader is created, which wastes resources.</span></span> <span data-ttu-id="1a04e-113">Mas quando você inclui um código de byte em um cabeçalho, pode reduzir a complexidade do código e simplificar a criação do sombreador.</span><span class="sxs-lookup"><span data-stu-id="1a04e-113">But when you include byte code in a header, you can reduce code complexity and simplify shader creation.</span></span>

<span data-ttu-id="1a04e-114">Agora, vamos examinar várias maneiras de compilar o código do sombreador e as convenções de extensões de arquivo para o código do sombreador.</span><span class="sxs-lookup"><span data-stu-id="1a04e-114">Let's now look at various ways to compile your shader code and conventions for file extensions for shader code.</span></span>

-   [<span data-ttu-id="1a04e-115">Usando extensões de arquivo de código do sombreador</span><span class="sxs-lookup"><span data-stu-id="1a04e-115">Using shader code file extensions</span></span>](#using-shader-code-file-extensions)
-   [<span data-ttu-id="1a04e-116">Compilando no momento da compilação para arquivos de objeto</span><span class="sxs-lookup"><span data-stu-id="1a04e-116">Compiling at build time to object files</span></span>](#compiling-at-build-time-to-object-files)
-   [<span data-ttu-id="1a04e-117">Compilando no momento da compilação para arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1a04e-117">Compiling at build time to header files</span></span>](#compiling-at-build-time-to-header-files)
-   [<span data-ttu-id="1a04e-118">Compilando com D3DCompileFromFile</span><span class="sxs-lookup"><span data-stu-id="1a04e-118">Compiling with D3DCompileFromFile</span></span>](#compiling-with-d3dcompilefromfile)
-   [<span data-ttu-id="1a04e-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1a04e-119">Related Topics</span></span>](#related-topics)
-   [<span data-ttu-id="1a04e-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1a04e-120">Related topics</span></span>](#related-topics)

## <a name="using-shader-code-file-extensions"></a><span data-ttu-id="1a04e-121">Usando extensões de arquivo de código do sombreador</span><span class="sxs-lookup"><span data-stu-id="1a04e-121">Using shader code file extensions</span></span>

<span data-ttu-id="1a04e-122">Para estar de acordo com a Convenção da Microsoft, use estas extensões de arquivo para o código do sombreador:</span><span class="sxs-lookup"><span data-stu-id="1a04e-122">To conform to Microsoft convention, use these file extensions for your shader code:</span></span>

-   <span data-ttu-id="1a04e-123">Um arquivo com a extensão. HLSL contém código-fonte de[HLSL](dx-graphics-hlsl-reference.md)(linguagem de sombreamento de alto nível).</span><span class="sxs-lookup"><span data-stu-id="1a04e-123">A file with the .hlsl extension holds High Level Shading Language ([HLSL](dx-graphics-hlsl-reference.md)) source code.</span></span>
-   <span data-ttu-id="1a04e-124">Um arquivo com a extensão .cso contém um objeto de sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="1a04e-124">A file with the .cso extension holds a compiled shader object.</span></span>
-   <span data-ttu-id="1a04e-125">Um arquivo com a extensão .h é um arquivo de cabeçalho, mas, em um contexto de código de sombreador, esse arquivo de cabeçalho define uma matriz de bytes que contém dados de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1a04e-125">A file with the .h extension is a header file, but in a shader code context, this header file defines a byte array that holds shader data.</span></span>

## <a name="compiling-at-build-time-to-object-files"></a><span data-ttu-id="1a04e-126">Compilando no momento da compilação para arquivos de objeto</span><span class="sxs-lookup"><span data-stu-id="1a04e-126">Compiling at build time to object files</span></span>

<span data-ttu-id="1a04e-127">Se você compilar seus arquivos. HLSL em arquivos de objeto de sombreador binário, seu aplicativo precisará ler os dados desses arquivos de objeto (. CSO é a extensão padrão para esses arquivos de objeto), atribuir os dados a matrizes de bytes e criar objetos de sombreador a partir dessas matrizes de bytes.</span><span class="sxs-lookup"><span data-stu-id="1a04e-127">If you compile your .hlsl files into binary shader object files, your app needs to read the data from those object files (.cso is the default extension for these object files), assign the data to byte arrays, and create shader objects from those byte arrays.</span></span> <span data-ttu-id="1a04e-128">Por exemplo, para criar um sombreador de vértice ([**ID3D11VertexShader**](/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader) \* \* ), chame o método [**ID3D11Device:: CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) com uma matriz de bytes que contém o código de byte do sombreador de vértices compilado.</span><span class="sxs-lookup"><span data-stu-id="1a04e-128">For example, to create a vertex shader ([**ID3D11VertexShader**](/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader)\*\*), call the [**ID3D11Device::CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) method with a byte array that contains compiled vertex shader byte code.</span></span> <span data-ttu-id="1a04e-129">O [exemplo de tutorial do Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) mostra como criar objetos de sombreador a partir de matrizes de bytes que ele obteve de arquivos de objeto de sombreador binário. cso.</span><span class="sxs-lookup"><span data-stu-id="1a04e-129">The [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) shows how to create shader objects from byte arrays that it obtained from .cso binary shader object files.</span></span> <span data-ttu-id="1a04e-130">Neste exemplo de código do [exemplo de tutorial do Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample), a propriedade arquivos de **saída** do arquivo SimpleVertexShader. HLSL especifica a compilação no arquivo de objeto SimpleVertexShader. cso.</span><span class="sxs-lookup"><span data-stu-id="1a04e-130">In this example code from the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample), the **Ouput Files** property for the SimpleVertexShader.hlsl file specifies to compile into the SimpleVertexShader.cso object file.</span></span>

```cpp
        auto vertexShaderBytecode = reader->ReadData("SimpleVertexShader.cso");
        ComPtr<ID3D11VertexShader> vertexShader;
        DX::ThrowIfFailed(
            m_d3dDevice->CreateVertexShader(
                vertexShaderBytecode->Data,
                vertexShaderBytecode->Length,
                nullptr,
                &vertexShader
                )
```

## <a name="compiling-at-build-time-to-header-files"></a><span data-ttu-id="1a04e-131">Compilando no momento da compilação para arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1a04e-131">Compiling at build time to header files</span></span>

<span data-ttu-id="1a04e-132">Se você compilar seus arquivos. HLSL em matrizes de bytes definidas em arquivos de cabeçalho, precisará incluir esses arquivos de cabeçalho em seu código.</span><span class="sxs-lookup"><span data-stu-id="1a04e-132">If you compile your .hlsl files into byte arrays that are defined in header files, you need to include those header files in your code.</span></span> <span data-ttu-id="1a04e-133">O [exemplo de extensões de mídia](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample) mostra como criar objetos de sombreador a partir de matrizes de bytes que são definidas em arquivos de cabeçalho e que você inclui em seu projeto no momento da compilação.</span><span class="sxs-lookup"><span data-stu-id="1a04e-133">The [Media extensions sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample) shows how to create shader objects from byte arrays that are defined in header files and that you include in your project at compile time.</span></span> <span data-ttu-id="1a04e-134">Neste exemplo de código do [exemplo de extensões de mídia](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample), a propriedade arquivos de **saída** para o arquivo PixelShader. HLSL especifica a compilação na matriz de bytes *g \_ psshader* que é definida no arquivo de cabeçalho PixelShader. h.</span><span class="sxs-lookup"><span data-stu-id="1a04e-134">In this example code from the [Media extensions sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample), the **Ouput Files** property for the PixelShader.hlsl file specifies to compile into the *g\_psshader* byte array that is defined in the PixelShader.h header file.</span></span>


```C++
#       include "PixelShader.h"
        ComPtr<ID3D11PixelShader> m_pPixelShader;
        hr = pDevice->CreatePixelShader(g_psshader, sizeof(g_psshader), nullptr, &m_pPixelShader);
```



## <a name="compiling-with-d3dcompilefromfile"></a><span data-ttu-id="1a04e-135">Compilando com D3DCompileFromFile</span><span class="sxs-lookup"><span data-stu-id="1a04e-135">Compiling with D3DCompileFromFile</span></span>

<span data-ttu-id="1a04e-136">Você também pode usar a função [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) em tempo de execução para compilar o código do sombreador.</span><span class="sxs-lookup"><span data-stu-id="1a04e-136">You can also use the [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) function at run time to compile shader code.</span></span> <span data-ttu-id="1a04e-137">Para obter mais informações sobre como fazer isso, consulte [como compilar um sombreador](/windows/desktop/direct3d11/how-to--compile-a-shader).</span><span class="sxs-lookup"><span data-stu-id="1a04e-137">For more info about how to do this, see [How To: Compile a Shader](/windows/desktop/direct3d11/how-to--compile-a-shader).</span></span>

> [!Note]  
> <span data-ttu-id="1a04e-138">Os aplicativos da Windows Store dão suporte ao uso do [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) para desenvolvimento, mas não para implantação.</span><span class="sxs-lookup"><span data-stu-id="1a04e-138">Windows Store apps support using [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) for development but not for deployment.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1a04e-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1a04e-139">Related Topics</span></span>

[<span data-ttu-id="1a04e-140">Guia de programação para HLSL</span><span class="sxs-lookup"><span data-stu-id="1a04e-140">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a><span data-ttu-id="1a04e-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1a04e-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a04e-142">Guia de programação para HLSL</span><span class="sxs-lookup"><span data-stu-id="1a04e-142">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 