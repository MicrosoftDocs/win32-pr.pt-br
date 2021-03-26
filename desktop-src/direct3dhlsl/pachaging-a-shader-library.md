---
title: Empacotando uma biblioteca de sombreador
description: Aqui, mostramos como compilar o código do sombreador, carregar o código compilado em uma biblioteca de sombreador e associar recursos dos slots de origem aos slots de destino.
ms.assetid: ED2EB1DE-3C25-4633-BFA7-C535ABBBAD28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90124ca9753a390b924d5ba702e1986e32eee9e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988702"
---
# <a name="packaging-a-shader-library"></a><span data-ttu-id="a8569-103">Empacotando uma biblioteca de sombreador</span><span class="sxs-lookup"><span data-stu-id="a8569-103">Packaging a shader library</span></span>

<span data-ttu-id="a8569-104">Aqui, mostramos como compilar o código do sombreador, carregar o código compilado em uma biblioteca de sombreador e associar recursos dos slots de origem aos slots de destino.</span><span class="sxs-lookup"><span data-stu-id="a8569-104">Here we show you how to compile your shader code, load the compiled code into a shader library, and bind resources from source slots to destination slots.</span></span>

<span data-ttu-id="a8569-105">**Objetivo:** Para empacotar uma biblioteca de sombreador a ser usada para vinculação de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a8569-105">**Objective:** To package a shader library to use for shader linking.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a8569-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="a8569-106">Prerequisites</span></span>

<span data-ttu-id="a8569-107">Partimos do princípio de que você conhece C++.</span><span class="sxs-lookup"><span data-stu-id="a8569-107">We assume that you are familiar with C++.</span></span> <span data-ttu-id="a8569-108">Você também precisa ter experiência básica com conceitos de programação de elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="a8569-108">You also need basic experience with graphics programming concepts.</span></span>

<span data-ttu-id="a8569-109">**Tempo para concluir:** 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="a8569-109">**Time to complete:** 30 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="a8569-110">Instruções</span><span class="sxs-lookup"><span data-stu-id="a8569-110">Instructions</span></span>

### <a name="1-compiling-your-shader-code"></a><span data-ttu-id="a8569-111">1. compilando o código do sombreador</span><span class="sxs-lookup"><span data-stu-id="a8569-111">1. Compiling your shader code</span></span>

<span data-ttu-id="a8569-112">Compile o código do sombreador com uma das funções de compilação.</span><span class="sxs-lookup"><span data-stu-id="a8569-112">Compile your shader code with one of the compile functions.</span></span> <span data-ttu-id="a8569-113">Por exemplo, esse trecho de código usa [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile).</span><span class="sxs-lookup"><span data-stu-id="a8569-113">For example, this code snippet uses [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile).</span></span>

```cpp
    string source;
 
    ComPtr<ID3DBlob> codeBlob;
    ComPtr<ID3DBlob> errorBlob;
    HRESULT hr = D3DCompile(
        source.c_str(),
        source.size(),
        "ShaderModule",
        NULL,
        NULL,
        NULL,
        ("lib" + m_shaderModelSuffix).c_str(),
        D3DCOMPILE_OPTIMIZATION_LEVEL3,
        0,
        &codeBlob,
        &errorBlob
        );
```

<span data-ttu-id="a8569-114">A cadeia de caracteres de origem contém o código HLSL ASCII não compilado.</span><span class="sxs-lookup"><span data-stu-id="a8569-114">The source string contains the uncompiled ASCII HLSL code.</span></span>

### <a name="2-load-the-compiled-code-into-a-shader-library"></a><span data-ttu-id="a8569-115">2. Carregue o código compilado em uma biblioteca de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a8569-115">2. Load the compiled code into a shader library.</span></span>

<span data-ttu-id="a8569-116">Chame a função [**D3DLoadModule**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule) para carregar o código compilado ([**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))) em um módulo ([**ID3D11Module**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module)) que representa uma biblioteca de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a8569-116">Call the [**D3DLoadModule**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule) function to load the compiled code ([**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))) into a module ([**ID3D11Module**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module)) that represents a shader library.</span></span>


```C++
    // Load the compiled library code into a module object.
    ComPtr<ID3D11Module> shaderLibrary;
    DX::ThrowIfFailed(D3DLoadModule(codeBlob->GetBufferPointer(), codeBlob->GetBufferSize(), &shaderLibrary));
```



### <a name="3-bind-resources-from-source-slots-to-destination-slots"></a><span data-ttu-id="a8569-117">3. associar recursos dos slots de origem aos slots de destino.</span><span class="sxs-lookup"><span data-stu-id="a8569-117">3. Bind resources from source slots to destination slots.</span></span>

<span data-ttu-id="a8569-118">Chame o método [**ID3D11Module:: CreateInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11module-createinstance) para criar uma instância ([**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)) da biblioteca para que você possa definir as associações de recurso para a instância.</span><span class="sxs-lookup"><span data-stu-id="a8569-118">Call the [**ID3D11Module::CreateInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11module-createinstance) method to create an instance ([**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)) of the library so you can then define resource bindings for the instance.</span></span>

<span data-ttu-id="a8569-119">Chame os métodos BIND de [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance) para associar os recursos necessários dos slots de origem aos slots de destino.</span><span class="sxs-lookup"><span data-stu-id="a8569-119">Call the bind methods of [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance) to bind the resources you need from source slots to destination slots.</span></span> <span data-ttu-id="a8569-120">Os recursos podem ser texturas, buffers, amostras, buffers de constantes ou UAVs.</span><span class="sxs-lookup"><span data-stu-id="a8569-120">The resources can be textures, buffers, samplers, constant buffers, or UAVs.</span></span> <span data-ttu-id="a8569-121">Normalmente, você usará os mesmos slots que a biblioteca de origem.</span><span class="sxs-lookup"><span data-stu-id="a8569-121">Typically, you will use the same slots as the source library.</span></span>


```C++
    // Create an instance of the library and define resource bindings for it.
    // In this sample we use the same slots as the source library however this is not required.
    ComPtr<ID3D11ModuleInstance> shaderLibraryInstance;
    DX::ThrowIfFailed(shaderLibrary->CreateInstance("", &shaderLibraryInstance));
    // HRESULTs for Bind methods are intentionally ignored as compiler optimizations may eliminate the source
    // bindings. In these cases, the Bind operation will fail, but the final shader will function normally.
    shaderLibraryInstance->BindResource(0, 0, 1);
    shaderLibraryInstance->BindSampler(0, 0, 1);
    shaderLibraryInstance->BindConstantBuffer(0, 0, 0);
    shaderLibraryInstance->BindConstantBuffer(1, 1, 0);
    shaderLibraryInstance->BindConstantBuffer(2, 2, 0);
```



<span data-ttu-id="a8569-122">Esse código HLSL mostra que a biblioteca de origem usa os mesmos slots (T0, S0, B0, B1 e B2) como os slots usados nos métodos de ligação anteriores de [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance).</span><span class="sxs-lookup"><span data-stu-id="a8569-122">This HLSL code shows that the source library uses the same slots (t0, s0, b0, b1, and b2) as the slots used in the preceding bind methods of [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance).</span></span>

``` syntax
// This is the default code in the fixed header section.
Texture2D<float3> Texture : register(t0);
SamplerState Anisotropic : register(s0);
cbuffer CameraData : register(b0)
{
    float4x4 Model;
    float4x4 View;
    float4x4 Projection;
};
cbuffer TimeVariantSignals : register(b1)
{
    float SineWave;
    float SquareWave;
    float TriangleWave;
    float SawtoothWave;
};

// This code is not displayed, but is used as part of the linking process.
cbuffer HiddenBuffer : register(b2)
{
    float3 LightDirection;
};
```

## <a name="summary-and-next-steps"></a><span data-ttu-id="a8569-123">Resumo e próximas etapas</span><span class="sxs-lookup"><span data-stu-id="a8569-123">Summary and next steps</span></span>

<span data-ttu-id="a8569-124">Compilamos o código do sombreador, carregamos o código compilado em uma biblioteca de sombreador e os recursos associados dos slots de origem para os slots de destino.</span><span class="sxs-lookup"><span data-stu-id="a8569-124">We compiled shader code, loaded the compiled code into a shader library, and bound resources from source slots to destination slots.</span></span>

<span data-ttu-id="a8569-125">Em seguida, construímos o function-link-Grafs (FLGs) para sombreadores, os vinculamos ao código compilado e geram blobs de sombreador que o tempo de execução do Direct3D pode usar.</span><span class="sxs-lookup"><span data-stu-id="a8569-125">Next we construct function-linking-graphs (FLGs) for shaders, link them to compiled code, and produce shader blobs that the Direct3D runtime can use.</span></span>

[<span data-ttu-id="a8569-126">Construindo um grafo de vinculação de função e vinculá-lo ao código compilado</span><span class="sxs-lookup"><span data-stu-id="a8569-126">Constructing a function-linking-graph and linking it to compiled code</span></span>](constructing-a-function-linking-graph.md)

## <a name="related-topics"></a><span data-ttu-id="a8569-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a8569-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8569-128">Usando vinculação de sombreador</span><span class="sxs-lookup"><span data-stu-id="a8569-128">Using shader linking</span></span>](using-shader-linking.md)
</dt> </dl>

 

 