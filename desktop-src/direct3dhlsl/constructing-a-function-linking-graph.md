---
title: Construindo um grafo de vinculação de função e vinculá-lo ao código compilado
description: Aqui, mostramos como construir FLGs (função-vinculação-grafos) para sombreadores e como vincular esses sombreadores a uma biblioteca de sombreador para produzir blobs de sombreador que o tempo de execução do Direct3D pode usar.
ms.assetid: 82C3109E-8571-49D2-A8BF-298E30E1281B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c037e7ea111d11d24df173ffba7e56c8f486af82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823902"
---
# <a name="constructing-a-function-linking-graph-and-linking-it-to-compiled-code"></a><span data-ttu-id="9055f-103">Construindo um grafo de vinculação de função e vinculá-lo ao código compilado</span><span class="sxs-lookup"><span data-stu-id="9055f-103">Constructing a function-linking-graph and linking it to compiled code</span></span>

<span data-ttu-id="9055f-104">Aqui, mostramos como construir FLGs (função-vinculação-grafos) para sombreadores e como vincular esses sombreadores a uma biblioteca de sombreador para produzir blobs de sombreador que o tempo de execução do Direct3D pode usar.</span><span class="sxs-lookup"><span data-stu-id="9055f-104">Here we show you how to construct function-linking-graphs (FLGs) for shaders and how to link those shaders with a shader library to produce shader blobs that the Direct3D runtime can use.</span></span>

<span data-ttu-id="9055f-105">**Objetivo:** Para construir um grafo de vinculação de função e vinculá-lo ao código compilado.</span><span class="sxs-lookup"><span data-stu-id="9055f-105">**Objective:** To construct a function-linking-graph and link it to compiled code.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9055f-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="9055f-106">Prerequisites</span></span>

<span data-ttu-id="9055f-107">Partimos do princípio de que você conhece C++.</span><span class="sxs-lookup"><span data-stu-id="9055f-107">We assume that you are familiar with C++.</span></span> <span data-ttu-id="9055f-108">Você também precisa ter experiência básica com conceitos de programação de elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="9055f-108">You also need basic experience with graphics programming concepts.</span></span>

<span data-ttu-id="9055f-109">Também presumimos que você tenha entrado no [empacotamento de uma biblioteca de sombreador](pachaging-a-shader-library.md).</span><span class="sxs-lookup"><span data-stu-id="9055f-109">We also assume that you went through [Packaging a shader library](pachaging-a-shader-library.md).</span></span>

<span data-ttu-id="9055f-110">**Tempo para concluir:** 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="9055f-110">**Time to complete:** 30 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="9055f-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="9055f-111">Instructions</span></span>

### <a name="1-construct-a-function-linking-graph-for-the-vertex-shader"></a><span data-ttu-id="9055f-112">1. Construa um grafo de vinculação de função para o sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="9055f-112">1. Construct a function-linking-graph for the vertex shader.</span></span>

<span data-ttu-id="9055f-113">Chame a função [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) para criar um [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)(Function-link-Graph) para representar o sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="9055f-113">Call the [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) function to create a function-linking-graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) to represent the vertex shader.</span></span>

<span data-ttu-id="9055f-114">Use uma matriz de [**estruturas \_ \_ desc de parâmetro D3D11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) para definir os parâmetros de entrada para o sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="9055f-114">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the input parameters for the vertex shader.</span></span> <span data-ttu-id="9055f-115">O [estágio Input-Assembler](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage) alimenta os parâmetros de entrada para o sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="9055f-115">The [Input-Assembler Stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-input-assembler-stage) feeds the input parameters to the vertex shader.</span></span> <span data-ttu-id="9055f-116">O layout dos parâmetros de entrada do sombreador de vértice corresponde ao layout do sombreador de vértice no código compilado.</span><span class="sxs-lookup"><span data-stu-id="9055f-116">The layout of the vertex shader’s input parameters matches the layout of the vertex shader in the compiled code.</span></span> <span data-ttu-id="9055f-117">Depois de definir os parâmetros de entrada, chame o método [**ID3D11FunctionLinkingGraph:: SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) para definir o nó de entrada ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) para o sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="9055f-117">After you define the input parameters, call the [**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) method to define the input node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the vertex shader.</span></span>


```C++
            ComPtr<ID3D11FunctionLinkingGraph> vertexShaderGraph;
            DX::ThrowIfFailed(D3DCreateFunctionLinkingGraph(0, &vertexShaderGraph));

            // Define the main input node which will be fed by the Input Assembler pipeline stage.
            static const D3D11_PARAMETER_DESC vertexShaderInputParameters[] =
            {
                {"inputPos",  "POSITION0", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_LINEAR, D3D_PF_IN, 0, 0, 0, 0},
                {"inputTex",  "TEXCOORD0", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 2, D3D_INTERPOLATION_LINEAR, D3D_PF_IN, 0, 0, 0, 0},
                {"inputNorm", "NORMAL0",   D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_LINEAR, D3D_PF_IN, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> vertexShaderInputNode;
            LinkingThrowIfFailed(vertexShaderGraph->SetInputSignature(vertexShaderInputParameters, ARRAYSIZE(vertexShaderInputParameters), 
                &vertexShaderInputNode), vertexShaderGraph.Get());
```



<span data-ttu-id="9055f-118">Chame o método [**ID3D11FunctionLinkingGraph:: CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) para criar um nó para a função de sombreador de vértice principal e fazer chamadas para [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) para passar valores do nó de entrada para o nó da função de sombreador de vértice principal.</span><span class="sxs-lookup"><span data-stu-id="9055f-118">Call the [**ID3D11FunctionLinkingGraph::CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) method to create a node for the main vertex shader function and make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from the input node to the node for the main vertex shader function.</span></span>


```C++
            // Create a node for the main VertexFunction call using the output of the helper functions.
            ComPtr<ID3D11LinkingNode> vertexFunctionCallNode;
            LinkingThrowIfFailed(vertexShaderGraph->CallFunction("", shaderLibrary.Get(), "VertexFunction", &vertexFunctionCallNode), 
                vertexShaderGraph.Get());

            // Define the graph edges from the input node and helper function nodes.
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(homogenizeCallNodeForPos.Get(), D3D_RETURN_PARAMETER_INDEX, 
                vertexFunctionCallNode.Get(), 0), vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexShaderInputNode.Get(), 1, vertexFunctionCallNode.Get(), 1), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(homogenizeCallNodeForNorm.Get(), D3D_RETURN_PARAMETER_INDEX, 
                vertexFunctionCallNode.Get(), 2), vertexShaderGraph.Get());
```



<span data-ttu-id="9055f-119">Use uma matriz de [**estruturas \_ \_ desc de parâmetro D3D11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) para definir os parâmetros de saída para o sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="9055f-119">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the output parameters for the vertex shader.</span></span> <span data-ttu-id="9055f-120">O sombreador de vértice alimenta seus parâmetros de saída para o sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="9055f-120">The vertex shader feeds its output parameters to the pixel shader.</span></span> <span data-ttu-id="9055f-121">O layout dos parâmetros de saída do sombreador de vértice corresponde ao layout do sombreador de pixel no código compilado.</span><span class="sxs-lookup"><span data-stu-id="9055f-121">The layout of the vertex shader’s output parameters matches the layout of the pixel shader in the compiled code.</span></span> <span data-ttu-id="9055f-122">Depois de definir os parâmetros de saída, chame o método [**ID3D11FunctionLinkingGraph:: SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) para definir o nó de saída ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) para o sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="9055f-122">After you define the output parameters, call the [**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) method to define the output node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the vertex shader.</span></span>


```C++
            // Define the main output node which will feed the Pixel Shader pipeline stage.
            static const D3D11_PARAMETER_DESC vertexShaderOutputParameters[] =
            {
                {"outputTex",  "TEXCOORD0",   D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 2, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0},
                {"outputNorm", "NORMAL0",     D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0},
                {"outputPos",  "SV_POSITION", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 4, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> vertexShaderOutputNode;
            LinkingThrowIfFailed(vertexShaderGraph->SetOutputSignature(vertexShaderOutputParameters, ARRAYSIZE(vertexShaderOutputParameters), 
                &vertexShaderOutputNode), vertexShaderGraph.Get());
```



<span data-ttu-id="9055f-123">Faça chamadas para [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) para passar valores do nó para a função de sombreador de vértice principal para o nó de saída.</span><span class="sxs-lookup"><span data-stu-id="9055f-123">Make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from the node for the main vertex shader function to the output node.</span></span>


```C++
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 0, vertexShaderOutputNode.Get(), 2), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 1, vertexShaderOutputNode.Get(), 0), 
                vertexShaderGraph.Get());
            LinkingThrowIfFailed(vertexShaderGraph->PassValue(vertexFunctionCallNode.Get(), 2, vertexShaderOutputNode.Get(), 1), 
                vertexShaderGraph.Get());
```



<span data-ttu-id="9055f-124">Chame o método [**ID3D11FunctionLinkingGraph:: CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) para finalizar o grafo do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="9055f-124">Call the [**ID3D11FunctionLinkingGraph::CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) method to finalize the vertex shader graph.</span></span>


```C++
            // Finalize the vertex shader graph.
            ComPtr<ID3D11ModuleInstance> vertexShaderGraphInstance;
            LinkingThrowIfFailed(vertexShaderGraph->CreateModuleInstance(&vertexShaderGraphInstance, nullptr), vertexShaderGraph.Get());
```



### <a name="2-link-the-vertex-shader"></a><span data-ttu-id="9055f-125">2. vincular o sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="9055f-125">2. Link the vertex shader</span></span>

<span data-ttu-id="9055f-126">Chame a função [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) para criar um vinculador ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) que você pode usar para vincular a instância da biblioteca de sombreador que você criou no [empacotamento de uma biblioteca de sombreador](pachaging-a-shader-library.md) com a instância do grafo do sombreador de vértice que você criou na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="9055f-126">Call the [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) function to create a linker ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) that you can use to link the instance of the shader library that you created in [Packaging a shader library](pachaging-a-shader-library.md) with the instance of the vertex shader graph that you created in the preceding step.</span></span> <span data-ttu-id="9055f-127">Chame o método [**ID3D11Linker:: UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) para especificar a biblioteca de sombreador a ser usada para vinculação.</span><span class="sxs-lookup"><span data-stu-id="9055f-127">Call the [**ID3D11Linker::UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) method to specify the shader library to use for linking.</span></span> <span data-ttu-id="9055f-128">Chame o método [**ID3D11Linker:: link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) para vincular a biblioteca de sombreador ao grafo do sombreador de vértice e produzir um ponteiro para a interface [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que você pode usar para acessar o código do sombreador do vértice compilado.</span><span class="sxs-lookup"><span data-stu-id="9055f-128">Call the [**ID3D11Linker::Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) method to link the shader library with the vertex shader graph and to produce a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access the compiled vertex shader code.</span></span> <span data-ttu-id="9055f-129">Em seguida, você pode passar esse código de sombreador de vértice compilado para o método [**ID3D11Device:: CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) para criar o objeto de sombreador de vértice e para o método [**ID3D11Device:: CreateInputLayout**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createinputlayout) para criar o objeto de layout de entrada.</span><span class="sxs-lookup"><span data-stu-id="9055f-129">You can then pass this compiled vertex shader code to the [**ID3D11Device::CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) method to create the vertex shader object and to the [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createinputlayout) method to create the input-layout object.</span></span>


```C++
            // Create a linker and hook up the module instance.
            ComPtr<ID3D11Linker> linker;
            DX::ThrowIfFailed(D3DCreateLinker(&linker));
            DX::ThrowIfFailed(linker->UseLibrary(shaderLibraryInstance.Get()));

            // Link the vertex shader.
            ComPtr<ID3DBlob> errorBlob;
            if (FAILED(linker->Link(vertexShaderGraphInstance.Get(), "main", ("vs" + m_shaderModelSuffix).c_str(), 0, &vertexShaderBlob, 
                &errorBlob)))
            {
                throw errorBlob;
            }


    ComPtr<ID3D11VertexShader> vertexShader;
    DX::ThrowIfFailed(
        device->CreateVertexShader(
            vertexShaderBlob->GetBufferPointer(),
            vertexShaderBlob->GetBufferSize(),
            nullptr,
            &vertexShader
            )
        );
    context->VSSetShader(vertexShader.Get(), nullptr, 0);
    D3D11_INPUT_ELEMENT_DESC inputLayoutDesc[] =
    {
        { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0,  D3D11_INPUT_PER_VERTEX_DATA, 0 },
        { "TEXCOORD", 0, DXGI_FORMAT_R32G32_FLOAT,    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
        { "NORMAL",   0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 20, D3D11_INPUT_PER_VERTEX_DATA, 0 }
    };
    ComPtr<ID3D11InputLayout> inputLayout;
    DX::ThrowIfFailed(device->CreateInputLayout(inputLayoutDesc, ARRAYSIZE(inputLayoutDesc), vertexShaderBlob->GetBufferPointer(), vertexShaderBlob->GetBufferSize(), &inputLayout));
    context->IASetInputLayout(inputLayout.Get());
```



### <a name="3-construct-a-function-linking-graph-for-the-pixel-shader"></a><span data-ttu-id="9055f-130">3. Construa um grafo de vinculação de função para o sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="9055f-130">3. Construct a function-linking-graph for the pixel shader.</span></span>

<span data-ttu-id="9055f-131">Chame a função [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) para criar um [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)(Function-link-Graph) para representar o sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="9055f-131">Call the [**D3DCreateFunctionLinkingGraph**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph) function to create a function-linking-graph ([**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)) to represent the pixel shader.</span></span>

<span data-ttu-id="9055f-132">Use uma matriz de [**estruturas \_ \_ desc de parâmetro D3D11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) para definir os parâmetros de entrada para o sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="9055f-132">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the input parameters for the pixel shader.</span></span> <span data-ttu-id="9055f-133">O estágio de sombreador de vértice alimenta os parâmetros de entrada para o sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="9055f-133">The vertex shader stage feeds the input parameters to the pixel shader.</span></span> <span data-ttu-id="9055f-134">O layout dos parâmetros de entrada do sombreador de pixel corresponde ao layout do sombreador de pixel no código compilado.</span><span class="sxs-lookup"><span data-stu-id="9055f-134">The layout of the pixel shader’s input parameters matches the layout of the pixel shader in the compiled code.</span></span> <span data-ttu-id="9055f-135">Depois de definir os parâmetros de entrada, chame o método [**ID3D11FunctionLinkingGraph:: SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) para definir o nó de entrada ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) para o sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="9055f-135">After you define the input parameters, call the [**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature) method to define the input node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the pixel shader.</span></span>


```C++
            ComPtr<ID3D11FunctionLinkingGraph> pixelShaderGraph;
            DX::ThrowIfFailed(D3DCreateFunctionLinkingGraph(0, &pixelShaderGraph));

            // Define the main input node which will be fed by the vertex shader pipeline stage.
            static const D3D11_PARAMETER_DESC pixelShaderInputParameters[] =
            {
                {"inputTex",  "TEXCOORD0",   D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 2, D3D_INTERPOLATION_UNDEFINED, D3D_PF_IN, 0, 0, 0, 0},
                {"inputNorm", "NORMAL0",     D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 3, D3D_INTERPOLATION_UNDEFINED, D3D_PF_IN, 0, 0, 0, 0},
                {"inputPos",  "SV_POSITION", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 4, D3D_INTERPOLATION_UNDEFINED, D3D_PF_IN, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> pixelShaderInputNode;
            LinkingThrowIfFailed(pixelShaderGraph->SetInputSignature(pixelShaderInputParameters, ARRAYSIZE(pixelShaderInputParameters), 
                &pixelShaderInputNode), pixelShaderGraph.Get());
```



<span data-ttu-id="9055f-136">Chame o método [**ID3D11FunctionLinkingGraph:: CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) para criar um nó para a função de sombreador de pixel principal e fazer chamadas para [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) para passar valores do nó de entrada para o nó para a função de sombreador de pixel principal.</span><span class="sxs-lookup"><span data-stu-id="9055f-136">Call the [**ID3D11FunctionLinkingGraph::CallFunction**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-callfunction) method to create a node for the main pixel shader function and make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from the input node to the node for the main pixel shader function.</span></span>


```C++
            // Create a node for the main ColorFunction call and connect it to the pixel shader inputs.
            ComPtr<ID3D11LinkingNode> colorValueNode;
            LinkingThrowIfFailed(pixelShaderGraph->CallFunction("", shaderLibrary.Get(), "ColorFunction", &colorValueNode), 
                pixelShaderGraph.Get());

            // Define the graph edges from the input node.
            LinkingThrowIfFailed(pixelShaderGraph->PassValue(pixelShaderInputNode.Get(), 0, colorValueNode.Get(), 0), 
                pixelShaderGraph.Get());
            LinkingThrowIfFailed(pixelShaderGraph->PassValue(pixelShaderInputNode.Get(), 1, colorValueNode.Get(), 1), 
                pixelShaderGraph.Get());
```



<span data-ttu-id="9055f-137">Use uma matriz de [**estruturas \_ \_ desc de parâmetro D3D11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) para definir os parâmetros de saída para o sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="9055f-137">Use an array of [**D3D11\_PARAMETER\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_parameter_desc) structures to define the output parameters for the pixel shader.</span></span> <span data-ttu-id="9055f-138">O sombreador de pixel alimenta seus parâmetros de saída para o [estágio de mesclagem de saída](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage).</span><span class="sxs-lookup"><span data-stu-id="9055f-138">The pixel shader feeds its output parameters to the [Output-Merger Stage](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage).</span></span> <span data-ttu-id="9055f-139">Depois de definir os parâmetros de saída, chame o método [**ID3D11FunctionLinkingGraph:: SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) para definir o nó de saída ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) para o sombreador de pixel e fazer chamadas para [**ID3D11FunctionLinkingGraph::P assvalue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) para passar valores de um nó de função de sombreador de pixel para o nó de saída.</span><span class="sxs-lookup"><span data-stu-id="9055f-139">After you define the output parameters, call the [**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature) method to define the output node ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) for the pixel shader and make calls to [**ID3D11FunctionLinkingGraph::PassValue**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-passvalue) to pass values from a pixel shader function node to the output node.</span></span>


```C++
            // Define the main output node which will feed the Output Merger pipeline stage.
            D3D11_PARAMETER_DESC pixelShaderOutputParameters[] =
            {
                {"outputColor", "SV_TARGET", D3D_SVT_FLOAT, D3D_SVC_VECTOR, 1, 4, D3D_INTERPOLATION_UNDEFINED, D3D_PF_OUT, 0, 0, 0, 0}
            };
            ComPtr<ID3D11LinkingNode> pixelShaderOutputNode;
            LinkingThrowIfFailed(pixelShaderGraph->SetOutputSignature(pixelShaderOutputParameters, ARRAYSIZE(pixelShaderOutputParameters), 
                &pixelShaderOutputNode), pixelShaderGraph.Get());
            LinkingThrowIfFailed(pixelShaderGraph->PassValue(fillAlphaCallNode.Get(), D3D_RETURN_PARAMETER_INDEX, pixelShaderOutputNode.Get(), 0), 
                pixelShaderGraph.Get());
```



<span data-ttu-id="9055f-140">Chame o método [**ID3D11FunctionLinkingGraph:: CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) para finalizar o grafo do sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="9055f-140">Call the [**ID3D11FunctionLinkingGraph::CreateModuleInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-createmoduleinstance) method to finalize the pixel shader graph.</span></span>


```C++
            // Finalize the pixel shader graph.
            ComPtr<ID3D11ModuleInstance> pixelShaderGraphInstance;
            LinkingThrowIfFailed(pixelShaderGraph->CreateModuleInstance(&pixelShaderGraphInstance, nullptr), pixelShaderGraph.Get());
```



### <a name="4-link-the-pixel-shader"></a><span data-ttu-id="9055f-141">4. vincular o sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="9055f-141">4. Link the pixel shader</span></span>

<span data-ttu-id="9055f-142">Chame a função [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) para criar um vinculador ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) que você pode usar para vincular a instância da biblioteca de sombreador que você criou no [empacotamento de uma biblioteca de sombreador](pachaging-a-shader-library.md) com a instância do grafo do sombreador de pixel que você criou na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="9055f-142">Call the [**D3DCreateLinker**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker) function to create a linker ([**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)) that you can use to link the instance of the shader library that you created in [Packaging a shader library](pachaging-a-shader-library.md) with the instance of the pixel shader graph that you created in the preceding step.</span></span> <span data-ttu-id="9055f-143">Chame o método [**ID3D11Linker:: UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) para especificar a biblioteca de sombreador a ser usada para vinculação.</span><span class="sxs-lookup"><span data-stu-id="9055f-143">Call the [**ID3D11Linker::UseLibrary**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-uselibrary) method to specify the shader library to use for linking.</span></span> <span data-ttu-id="9055f-144">Chame o método [**ID3D11Linker:: link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) para vincular a biblioteca de sombreador ao grafo do sombreador de pixel e produzir um ponteiro para a interface [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que você pode usar para acessar o código do sombreador de pixel compilado.</span><span class="sxs-lookup"><span data-stu-id="9055f-144">Call the [**ID3D11Linker::Link**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11linker-link) method to link the shader library with the pixel shader graph and to produce a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access the compiled pixel shader code.</span></span> <span data-ttu-id="9055f-145">Em seguida, você pode passar esse código de sombreador de pixel compilado para o método [**ID3D11Device:: CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader) para criar o objeto de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="9055f-145">You can then pass this compiled pixel shader code to the [**ID3D11Device::CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader) method to create the pixel shader object.</span></span>


```C++
            // Create a linker and hook up the module instance.
            ComPtr<ID3D11Linker> linker;
            DX::ThrowIfFailed(D3DCreateLinker(&linker));
            DX::ThrowIfFailed(linker->UseLibrary(shaderLibraryInstance.Get()));

            // Link the pixel shader.
            ComPtr<ID3DBlob> errorBlob;
            if (FAILED(linker->Link(pixelShaderGraphInstance.Get(), "main", ("ps" + m_shaderModelSuffix).c_str(), 0, &pixelShaderBlob, &errorBlob)))
            {
                throw errorBlob;
            }


    ComPtr<ID3D11PixelShader> pixelShader;
    DX::ThrowIfFailed(
        device->CreatePixelShader(
            pixelShaderBlob->GetBufferPointer(),
            pixelShaderBlob->GetBufferSize(),
            nullptr,
            &pixelShader
            )
        );
    context->PSSetShader(pixelShader.Get(), nullptr, 0);
```



## <a name="summary"></a><span data-ttu-id="9055f-146">Resumo</span><span class="sxs-lookup"><span data-stu-id="9055f-146">Summary</span></span>

<span data-ttu-id="9055f-147">Usamos os métodos [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph) para construir os grafos de vértice e do sombreador de pixel e para especificar a estrutura do sombreador programaticamente.</span><span class="sxs-lookup"><span data-stu-id="9055f-147">We used the [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph) methods to construct the vertex and pixel shader graphs and to specify the shader structure programmatically.</span></span>

<span data-ttu-id="9055f-148">Essas construções de grafo consistem em sequências de chamadas de função pré-compiladas que passam valores entre si.</span><span class="sxs-lookup"><span data-stu-id="9055f-148">These graph constructions consist of sequences of precompiled function calls that pass values to each other.</span></span> <span data-ttu-id="9055f-149">Os nós FLG ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) representam nós do sombreador de entrada e saída e invocações de funções de biblioteca pré-compiladas.</span><span class="sxs-lookup"><span data-stu-id="9055f-149">FLG nodes ([**ID3D11LinkingNode**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linkingnode)) represent input and output shader nodes and invocations of precompiled library functions.</span></span> <span data-ttu-id="9055f-150">A ordem na qual você registra os nós de chamada de função define a sequência de invocações.</span><span class="sxs-lookup"><span data-stu-id="9055f-150">The order in which you register the function-call nodes defines the sequence of invocations.</span></span> <span data-ttu-id="9055f-151">Você deve especificar o nó de entrada ([**ID3D11FunctionLinkingGraph:: SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature)) primeiro e o nó de saída Last ([**ID3D11FunctionLinkingGraph:: SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature)).</span><span class="sxs-lookup"><span data-stu-id="9055f-151">You must specify the input node ([**ID3D11FunctionLinkingGraph::SetInputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setinputsignature)) first and the output node last ([**ID3D11FunctionLinkingGraph::SetOutputSignature**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11functionlinkinggraph-setoutputsignature)).</span></span> <span data-ttu-id="9055f-152">As bordas FLG definem como os valores são passados de um nó para outro.</span><span class="sxs-lookup"><span data-stu-id="9055f-152">FLG edges define how values are passed from one node to another.</span></span> <span data-ttu-id="9055f-153">Os tipos de dados dos valores passados devem ser os mesmos; Não há nenhuma conversão implícita de tipo.</span><span class="sxs-lookup"><span data-stu-id="9055f-153">The data types of passed values must be the same; there is no implicit type conversion.</span></span> <span data-ttu-id="9055f-154">As regras Shape e swizzling seguem o comportamento HLSL.</span><span class="sxs-lookup"><span data-stu-id="9055f-154">Shape and swizzling rules follow the HLSL behavior.</span></span> <span data-ttu-id="9055f-155">Os valores só podem ser passados para frente nesta sequência.</span><span class="sxs-lookup"><span data-stu-id="9055f-155">Values can only be passed forward in this sequence.</span></span>

<span data-ttu-id="9055f-156">Também usamos métodos [**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker) para vincular a biblioteca de sombreador aos grafos do sombreador e para produzir blobs de sombreador para uso do Direct3D Runtime.</span><span class="sxs-lookup"><span data-stu-id="9055f-156">We also used [**ID3D11Linker**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker) methods to link the shader library with the shader graphs and to produce shader blobs for the Direct3D runtime to use.</span></span>

<span data-ttu-id="9055f-157">Parabéns!</span><span class="sxs-lookup"><span data-stu-id="9055f-157">Congratulations!</span></span> <span data-ttu-id="9055f-158">Agora você está pronto para usar a vinculação de sombreador em seus próprios aplicativos.</span><span class="sxs-lookup"><span data-stu-id="9055f-158">You are now ready to use shader linking in your own apps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9055f-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9055f-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9055f-160">Usando vinculação de sombreador</span><span class="sxs-lookup"><span data-stu-id="9055f-160">Using shader linking</span></span>](using-shader-linking.md)
</dt> </dl>

 

 