---
title: Criando um componente básico do Direct3D 12
description: Este tópico descreve o fluxo de chamadas para criar um componente básico do Direct3D 12.
ms.assetid: A0FB108B-15C1-42AD-9277-D5CB63FA8329
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: d0c7ead9ce67ee23a0668304a006d6cd67fb3d67
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2021
ms.locfileid: "104758856"
---
# <a name="creating-a-basic-direct3d-12-component"></a><span data-ttu-id="5ee0e-103">Criando um componente básico do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="5ee0e-103">Creating a basic Direct3D 12 component</span></span>

> [!NOTE]
> <span data-ttu-id="5ee0e-104">Consulte o repositório [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) para exemplos de gráficos do DirectX 12 que demonstram como criar aplicativos com uso intensivo de gráficos para o Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-104">See the [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) repo for DirectX 12 Graphics samples that demonstrate how to build graphics-intensive applications for Windows 10.</span></span>

<span data-ttu-id="5ee0e-105">Este tópico descreve o fluxo de chamadas para criar um componente básico do Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-105">This topic describes the call flow to create a basic Direct3D 12 component.</span></span>

-   [<span data-ttu-id="5ee0e-106">Fluxo de código para um aplicativo simples</span><span class="sxs-lookup"><span data-stu-id="5ee0e-106">Code flow for a simple app</span></span>](#code-flow-for-a-simple-app)
    -   [<span data-ttu-id="5ee0e-107">Inicializar</span><span class="sxs-lookup"><span data-stu-id="5ee0e-107">Initialize</span></span>](#initialize)
    -   [<span data-ttu-id="5ee0e-108">Atualizar</span><span class="sxs-lookup"><span data-stu-id="5ee0e-108">Update</span></span>](#update)
    -   [<span data-ttu-id="5ee0e-109">Render</span><span class="sxs-lookup"><span data-stu-id="5ee0e-109">Render</span></span>](#render)
    -   [<span data-ttu-id="5ee0e-110">Destruir</span><span class="sxs-lookup"><span data-stu-id="5ee0e-110">Destroy</span></span>](#destroy)
-   [<span data-ttu-id="5ee0e-111">Exemplo de código para um aplicativo simples</span><span class="sxs-lookup"><span data-stu-id="5ee0e-111">Code example for a simple app</span></span>](#code-example-for-a-simple-app)
    -   [<span data-ttu-id="5ee0e-112">D3D12HelloTriangle de classe</span><span class="sxs-lookup"><span data-stu-id="5ee0e-112">class D3D12HelloTriangle</span></span>](#class-d3d12hellotriangle)
    -   [<span data-ttu-id="5ee0e-113">OnInit ()</span><span class="sxs-lookup"><span data-stu-id="5ee0e-113">OnInit()</span></span>](#oninit)
    -   [<span data-ttu-id="5ee0e-114">LoadPipe ()</span><span class="sxs-lookup"><span data-stu-id="5ee0e-114">LoadPipeline()</span></span>](#loadpipeline)
    -   [<span data-ttu-id="5ee0e-115">Loadassets ()</span><span class="sxs-lookup"><span data-stu-id="5ee0e-115">LoadAssets()</span></span>](#loadassets)
    -   [<span data-ttu-id="5ee0e-116">OnUpdate ()</span><span class="sxs-lookup"><span data-stu-id="5ee0e-116">OnUpdate()</span></span>](#onupdate)
    -   [<span data-ttu-id="5ee0e-117">OnRender ()</span><span class="sxs-lookup"><span data-stu-id="5ee0e-117">OnRender()</span></span>](#onrender)
    -   [<span data-ttu-id="5ee0e-118">PopulateCommandList()</span><span class="sxs-lookup"><span data-stu-id="5ee0e-118">PopulateCommandList()</span></span>](#populatecommandlist)
    -   [<span data-ttu-id="5ee0e-119">WaitForPreviousFrame()</span><span class="sxs-lookup"><span data-stu-id="5ee0e-119">WaitForPreviousFrame()</span></span>](#waitforpreviousframe)
    -   [<span data-ttu-id="5ee0e-120">OnDestroy ()</span><span class="sxs-lookup"><span data-stu-id="5ee0e-120">OnDestroy()</span></span>](#ondestroy)
-   [<span data-ttu-id="5ee0e-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5ee0e-121">Related topics</span></span>](#related-topics)

## <a name="code-flow-for-a-simple-app"></a><span data-ttu-id="5ee0e-122">Fluxo de código para um aplicativo simples</span><span class="sxs-lookup"><span data-stu-id="5ee0e-122">Code flow for a simple app</span></span>

<span data-ttu-id="5ee0e-123">O loop mais externo de um programa do D3D 12 segue um processo gráfico muito padrão:</span><span class="sxs-lookup"><span data-stu-id="5ee0e-123">The outermost loop of a D3D 12 program follows a very standard graphics process:</span></span>

> [!TIP]
> <span data-ttu-id="5ee0e-124">Os recursos novos para o Direct3D 12 são seguidos de uma observação.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-124">Features new to Direct3D 12 are followed by a note.</span></span>

-   [<span data-ttu-id="5ee0e-125">Inicializar</span><span class="sxs-lookup"><span data-stu-id="5ee0e-125">Initialize</span></span>](#initialize)
-   <span data-ttu-id="5ee0e-126">**Pete**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-126">**Repeat**</span></span>
    -   [<span data-ttu-id="5ee0e-127">Atualizar</span><span class="sxs-lookup"><span data-stu-id="5ee0e-127">Update</span></span>](#update)
    -   [<span data-ttu-id="5ee0e-128">Render</span><span class="sxs-lookup"><span data-stu-id="5ee0e-128">Render</span></span>](#render)
-   [<span data-ttu-id="5ee0e-129">Destruir</span><span class="sxs-lookup"><span data-stu-id="5ee0e-129">Destroy</span></span>](#destroy)

### <a name="initialize"></a><span data-ttu-id="5ee0e-130">Inicializar</span><span class="sxs-lookup"><span data-stu-id="5ee0e-130">Initialize</span></span>

<span data-ttu-id="5ee0e-131">A inicialização envolve primeiro a configuração das variáveis e das classes globais, e uma função de inicialização deve preparar o pipeline e os ativos.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-131">Initialization involves first setting up the global variables and classes, and an initialize function must prepare the pipeline and assets.</span></span>

-   <span data-ttu-id="5ee0e-132">Inicialize o pipeline.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-132">Initialize the pipeline.</span></span>
    -   <span data-ttu-id="5ee0e-133">Habilite a camada de depuração.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-133">Enable the debug layer.</span></span>
    -   <span data-ttu-id="5ee0e-134">Crie o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-134">Create the device.</span></span>
    -   <span data-ttu-id="5ee0e-135">Crie a fila de comandos.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-135">Create the command queue.</span></span>
    -   <span data-ttu-id="5ee0e-136">Crie a cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-136">Create the swap chain.</span></span>
    -   <span data-ttu-id="5ee0e-137">Criar um heap de descritor de RTV (exibição de destino de renderização).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-137">Create a render target view (RTV) descriptor heap.</span></span>
        > [!Note]  
        > <span data-ttu-id="5ee0e-138">Um [heap de descritor](descriptor-heaps.md) pode ser considerado como uma matriz [de descritores.](descriptors.md)</span><span class="sxs-lookup"><span data-stu-id="5ee0e-138">A [descriptor heap](descriptor-heaps.md) can be thought of as an array of [descriptors](descriptors.md).</span></span> <span data-ttu-id="5ee0e-139">Onde cada descritor descreve totalmente um objeto para a GPU.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-139">Where each descriptor fully describes an object to the GPU.</span></span>

    -   <span data-ttu-id="5ee0e-140">Crie recursos de quadro (uma exibição de destino de renderização para cada quadro).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-140">Create frame resources (a render target view for each frame).</span></span>
    -   <span data-ttu-id="5ee0e-141">Crie um alocador de comando.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-141">Create a command allocator.</span></span>
        > [!Note]  
        > <span data-ttu-id="5ee0e-142">Um alocador de comando gerencia o armazenamento subjacente para [listas de comandos e pacotes](recording-command-lists-and-bundles.md).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-142">A command allocator manages the underlying storage for [command lists and bundles](recording-command-lists-and-bundles.md).</span></span>
         
-   <span data-ttu-id="5ee0e-143">Inicialize os ativos.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-143">Initialize the assets.</span></span>
    -   <span data-ttu-id="5ee0e-144">Crie uma assinatura raiz vazia.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-144">Create an empty root signature.</span></span>
        > [!Note]  
        > <span data-ttu-id="5ee0e-145">Uma [assinatura raiz](root-signatures.md) gráfica define quais recursos estão associados ao pipeline de gráficos.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-145">A graphics [root signature](root-signatures.md) defines what resources are bound to the graphics pipeline.</span></span>

    -   <span data-ttu-id="5ee0e-146">Compile os sombreadores.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-146">Compile the shaders.</span></span>
    -   <span data-ttu-id="5ee0e-147">Crie o layout de entrada do vértice.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-147">Create the vertex input layout.</span></span>
    -   <span data-ttu-id="5ee0e-148">Crie uma descrição de [objeto de estado de pipeline](managing-graphics-pipeline-state-in-direct3d-12.md) e crie o objeto.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-148">Create a [pipeline state object](managing-graphics-pipeline-state-in-direct3d-12.md) description, then create the object.</span></span>
        > [!Note]  
        > <span data-ttu-id="5ee0e-149">Um objeto de estado de pipeline mantém o estado de todos os sombreadores definidos atualmente, bem como determinados objetos de estado de função fixa (como o *Assembler de entrada*, *tesselator*, *rasterizador* e *mesclagem de saída*).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-149">A pipeline state object maintains the state of all currently set shaders as well as certain fixed function state objects (such as the *input assembler*, *tesselator*, *rasterizer* and *output merger*).</span></span>

    -   <span data-ttu-id="5ee0e-150">Crie a lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-150">Create the command list.</span></span>
    -   <span data-ttu-id="5ee0e-151">Feche a lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-151">Close the command list.</span></span>
    -   <span data-ttu-id="5ee0e-152">Crie e carregue os buffers de vértice.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-152">Create and load the vertex buffers.</span></span>
    -   <span data-ttu-id="5ee0e-153">Crie as exibições do buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-153">Create the vertex buffer views.</span></span>
    -   <span data-ttu-id="5ee0e-154">Criar uma cerca.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-154">Create a fence.</span></span>
        > [!Note]  
        > <span data-ttu-id="5ee0e-155">Uma cerca é usada para sincronizar a CPU com a GPU (consulte [sincronização de vários mecanismos](./user-mode-heap-synchronization.md)).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-155">A fence is used to synchronize the CPU with the GPU (see [Multi-engine synchronization](./user-mode-heap-synchronization.md)).</span></span>

    -   <span data-ttu-id="5ee0e-156">Crie um identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-156">Create an event handle.</span></span>
    -   <span data-ttu-id="5ee0e-157">Aguarde a conclusão da GPU.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-157">Wait for the GPU to finish.</span></span>
        > [!Note]  
        > <span data-ttu-id="5ee0e-158">Verifique o limite.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-158">Check on the fence!</span></span>

<span data-ttu-id="5ee0e-159">Consulte a [classe D3D12HelloTriangle](#class-d3d12hellotriangle), [OnInit](#oninit), [Loadcanalization](#loadpipeline) e [loadassets](#loadassets).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-159">Refer to [class D3D12HelloTriangle](#class-d3d12hellotriangle), [OnInit](#oninit), [LoadPipeline](#loadpipeline) and [LoadAssets](#loadassets).</span></span>

### <a name="update"></a><span data-ttu-id="5ee0e-160">Atualizar</span><span class="sxs-lookup"><span data-stu-id="5ee0e-160">Update</span></span>

<span data-ttu-id="5ee0e-161">Atualizar tudo o que deve ser alterado desde o último quadro.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-161">Update everything that should change since the last frame.</span></span>

-   <span data-ttu-id="5ee0e-162">Modifique a constante, o vértice, os buffers de índice e todo o resto, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-162">Modify the constant, vertex, index buffers, and everything else, as necessary.</span></span>

<span data-ttu-id="5ee0e-163">Consulte [OnUpdate](#onupdate).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-163">Refer to [OnUpdate](#onupdate).</span></span>

### <a name="render"></a><span data-ttu-id="5ee0e-164">Renderizar</span><span class="sxs-lookup"><span data-stu-id="5ee0e-164">Render</span></span>

<span data-ttu-id="5ee0e-165">Desenhe o novo mundo.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-165">Draw the new world.</span></span>

-   <span data-ttu-id="5ee0e-166">Preencha a lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-166">Populate the command list.</span></span>
    -   <span data-ttu-id="5ee0e-167">Redefina o alocador de lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-167">Reset the command list allocator.</span></span>
        > [!Note]  
        > <span data-ttu-id="5ee0e-168">Use novamente a memória associada ao alocador de comando.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-168">Re-use the memory that is associated with the command allocator.</span></span>

         

    -   <span data-ttu-id="5ee0e-169">Redefina a lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-169">Reset the command list.</span></span>
    -   <span data-ttu-id="5ee0e-170">Defina a assinatura raiz de gráficos.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-170">Set the graphics root signature.</span></span>
        > [!Note]  
        > <span data-ttu-id="5ee0e-171">Define a assinatura raiz de gráficos a ser usada para a lista de comandos atual.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-171">Sets the graphics root signature to use for the current command list.</span></span>

         

    -   <span data-ttu-id="5ee0e-172">Defina os retângulos de visor e de mola.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-172">Set the viewport and scissor rectangles.</span></span>
    -   <span data-ttu-id="5ee0e-173">Defina uma barreira de recurso, indicando que o buffer de fundo deve ser usado como um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-173">Set a resource barrier, indicating the back buffer is to be used as a render target.</span></span>
        > [!Note]  
        > <span data-ttu-id="5ee0e-174">As barreiras de recursos são usadas para gerenciar transições de recursos.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-174">Resource barriers are used to manage resource transitions.</span></span>

         

    -   <span data-ttu-id="5ee0e-175">Grave os comandos na lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-175">Record commands into the command list.</span></span>
    -   <span data-ttu-id="5ee0e-176">Indique que o buffer de fundo será usado para apresentar após a execução da lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-176">Indicate the back buffer will be used to present after the command list has executed.</span></span>
        > [!Note]  
        > <span data-ttu-id="5ee0e-177">Outra chamada para definir uma barreira de recurso.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-177">Another call to set a resource barrier.</span></span>

         

    -   <span data-ttu-id="5ee0e-178">Feche a lista de comandos para gravar mais.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-178">Close the command list to further recording.</span></span>
-   <span data-ttu-id="5ee0e-179">Execute a lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-179">Execute the command list.</span></span>
-   <span data-ttu-id="5ee0e-180">Apresente o quadro.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-180">Present the frame.</span></span>
-   <span data-ttu-id="5ee0e-181">Aguarde a conclusão da GPU.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-181">Wait for the GPU to finish.</span></span>
    > [!Note]  
    > <span data-ttu-id="5ee0e-182">Continue atualizando e verificando a cerca.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-182">Keep updating and checking the fence.</span></span>

<span data-ttu-id="5ee0e-183">Consulte [OnRender](#onrender).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-183">Refer to [OnRender](#onrender).</span></span>

### <a name="destroy"></a><span data-ttu-id="5ee0e-184">Destruir</span><span class="sxs-lookup"><span data-stu-id="5ee0e-184">Destroy</span></span>

<span data-ttu-id="5ee0e-185">Fechar o aplicativo corretamente.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-185">Cleanly close down the app.</span></span>

-   <span data-ttu-id="5ee0e-186">Aguarde a conclusão da GPU.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-186">Wait for the GPU to finish.</span></span>
    > [!Note]  
    > <span data-ttu-id="5ee0e-187">Verificação final da cerca.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-187">Final check on the fence.</span></span>

-   <span data-ttu-id="5ee0e-188">Feche o identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-188">Close the event handle.</span></span>

<span data-ttu-id="5ee0e-189">Consulte [OnDestroy](#ondestroy).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-189">Refer to [OnDestroy](#ondestroy).</span></span>

## <a name="code-example-for-a-simple-app"></a><span data-ttu-id="5ee0e-190">Exemplo de código para um aplicativo simples</span><span class="sxs-lookup"><span data-stu-id="5ee0e-190">Code example for a simple app</span></span>

<span data-ttu-id="5ee0e-191">O seguinte expande o fluxo de código acima para incluir o código necessário para um exemplo básico.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-191">The following expands the code flow above to include the code required for a basic sample.</span></span>

### <a name="class-d3d12hellotriangle"></a><span data-ttu-id="5ee0e-192">D3D12HelloTriangle de classe</span><span class="sxs-lookup"><span data-stu-id="5ee0e-192">class D3D12HelloTriangle</span></span>

<span data-ttu-id="5ee0e-193">Primeiro, defina a classe em um arquivo de cabeçalho, incluindo um visor, um retângulo de recorte e um buffer de vértice usando as estruturas:</span><span class="sxs-lookup"><span data-stu-id="5ee0e-193">First define the class in a header file, including a viewport, scissor rectangle and vertex buffer using the structures:</span></span>

-   [<span data-ttu-id="5ee0e-194">**\_Visor D3D12**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-194">**D3D12\_VIEWPORT**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_viewport)
-   [<span data-ttu-id="5ee0e-195">**D3D12 \_ Rect**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-195">**D3D12\_RECT**</span></span>](d3d12-rect.md)
-   [<span data-ttu-id="5ee0e-196">**\_Exibição do \_ buffer de vértice D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-196">**D3D12\_VERTEX\_BUFFER\_VIEW**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view)

```cpp
#include "DXSample.h"

using namespace DirectX;
using namespace Microsoft::WRL;

class D3D12HelloTriangle : public DXSample
{
public:
    D3D12HelloTriangle(UINT width, UINT height, std::wstring name);

    virtual void OnInit();
    virtual void OnUpdate();
    virtual void OnRender();
    virtual void OnDestroy();

private:
    static const UINT FrameCount = 2;

    struct Vertex
    {
        XMFLOAT3 position;
        XMFLOAT4 color;
    };

    // Pipeline objects.
    D3D12_VIEWPORT m_viewport;
    D3D12_RECT m_scissorRect;
    ComPtr<IDXGISwapChain3> m_swapChain;
    ComPtr<ID3D12Device> m_device;
    ComPtr<ID3D12Resource> m_renderTargets[FrameCount];
    ComPtr<ID3D12CommandAllocator> m_commandAllocator;
    ComPtr<ID3D12CommandQueue> m_commandQueue;
    ComPtr<ID3D12RootSignature> m_rootSignature;
    ComPtr<ID3D12DescriptorHeap> m_rtvHeap;
    ComPtr<ID3D12PipelineState> m_pipelineState;
    ComPtr<ID3D12GraphicsCommandList> m_commandList;
    UINT m_rtvDescriptorSize;

    // App resources.
    ComPtr<ID3D12Resource> m_vertexBuffer;
    D3D12_VERTEX_BUFFER_VIEW m_vertexBufferView;

    // Synchronization objects.
    UINT m_frameIndex;
    HANDLE m_fenceEvent;
    ComPtr<ID3D12Fence> m_fence;
    UINT64 m_fenceValue;

    void LoadPipeline();
    void LoadAssets();
    void PopulateCommandList();
    void WaitForPreviousFrame();
};
```

### <a name="oninit"></a><span data-ttu-id="5ee0e-197">OnInit ()</span><span class="sxs-lookup"><span data-stu-id="5ee0e-197">OnInit()</span></span>

<span data-ttu-id="5ee0e-198">No arquivo de origem principal dos projetos, comece inicializando os objetos:</span><span class="sxs-lookup"><span data-stu-id="5ee0e-198">In the projects main source file, start initializing the objects:</span></span>

```cpp
void D3D12HelloTriangle::OnInit()
{
    LoadPipeline();
    LoadAssets();
}
```

### <a name="loadpipeline"></a><span data-ttu-id="5ee0e-199">LoadPipe ()</span><span class="sxs-lookup"><span data-stu-id="5ee0e-199">LoadPipeline()</span></span>

<span data-ttu-id="5ee0e-200">O código a seguir cria as noções básicas para um pipeline de gráficos.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-200">The following code creates the basics for a graphics pipeline.</span></span> <span data-ttu-id="5ee0e-201">O processo de criação de dispositivos e cadeias de troca é muito semelhante ao Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-201">The process of creating devices and swap chains is very similar to Direct3D 11.</span></span>

-   <span data-ttu-id="5ee0e-202">Habilite a camada de depuração, com chamadas para:</span><span class="sxs-lookup"><span data-stu-id="5ee0e-202">Enable the debug layer, with calls to:</span></span><dl>

[<span data-ttu-id="5ee0e-203">**D3D12GetDebugInterface**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-203">**D3D12GetDebugInterface**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12getdebuginterface)  
    [<span data-ttu-id="5ee0e-204">**ID3D12Debug::EnableDebugLayer**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-204">**ID3D12Debug::EnableDebugLayer**</span></span>](/windows/win32/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer)  
    </dl>
-   <span data-ttu-id="5ee0e-205">Crie o dispositivo:</span><span class="sxs-lookup"><span data-stu-id="5ee0e-205">Create the device:</span></span><dl>

[<span data-ttu-id="5ee0e-206">**CreateDXGIFactory1**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-206">**CreateDXGIFactory1**</span></span>](/windows/win32/api/dxgi/nf-dxgi-createdxgifactory1)  
    [<span data-ttu-id="5ee0e-207">**D3D12CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-207">**D3D12CreateDevice**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12createdevice)  
    </dl>
-   <span data-ttu-id="5ee0e-208">Preencha uma descrição da fila de comandos e crie a fila de comandos:</span><span class="sxs-lookup"><span data-stu-id="5ee0e-208">Fill out a command queue description, then create the command queue:</span></span><dl>

[<span data-ttu-id="5ee0e-209">**D3D12 \_ de \_ fila de comando \_ desc**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-209">**D3D12\_COMMAND\_QUEUE\_DESC**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc)  
    [<span data-ttu-id="5ee0e-210">**ID3D12Device::CreateCommandQueue**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-210">**ID3D12Device::CreateCommandQueue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue)  
    </dl>
-   <span data-ttu-id="5ee0e-211">Preencha uma descrição de SwapChain e crie a cadeia de permuta:</span><span class="sxs-lookup"><span data-stu-id="5ee0e-211">Fill out a swapchain description, then create the swap chain:</span></span> <dl>

[<span data-ttu-id="5ee0e-212">**\_desc de \_ cadeia de permuta dxgi \_**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-212">**DXGI\_SWAP\_CHAIN\_DESC**</span></span>](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)  
    [<span data-ttu-id="5ee0e-213">**IDXGIFactory::CreateSwapChain**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-213">**IDXGIFactory::CreateSwapChain**</span></span>](/windows/win32/api/dxgi/nf-dxgi-idxgifactory-createswapchain)  
    [<span data-ttu-id="5ee0e-214">**IDXGISwapChain3::GetCurrentBackBufferIndex**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-214">**IDXGISwapChain3::GetCurrentBackBufferIndex**</span></span>](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex)  
    </dl>
-   <span data-ttu-id="5ee0e-215">Preencha uma descrição de heap.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-215">Fill out a heap description.</span></span> <span data-ttu-id="5ee0e-216">em seguida, crie um heap de descritor:</span><span class="sxs-lookup"><span data-stu-id="5ee0e-216">then create a descriptor heap:</span></span> <dl>

[<span data-ttu-id="5ee0e-217">**D3D12 de \_ heap de descritor \_ \_ desc**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-217">**D3D12\_DESCRIPTOR\_HEAP\_DESC**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc)  
    [<span data-ttu-id="5ee0e-218">**ID3D12Device::CreateDescriptorHeap**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-218">**ID3D12Device::CreateDescriptorHeap**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap)  
    [<span data-ttu-id="5ee0e-219">**ID3D12Device::GetDescriptorHandleIncrementSize**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-219">**ID3D12Device::GetDescriptorHandleIncrementSize**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)  
    </dl>
-   <span data-ttu-id="5ee0e-220">Criar o modo de exibição de destino de renderização:</span><span class="sxs-lookup"><span data-stu-id="5ee0e-220">Create the render target view:</span></span> <dl>

[<span data-ttu-id="5ee0e-221">**\_Identificador do \_ descritor de CPU CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-221">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE**</span></span>](cd3dx12-cpu-descriptor-handle.md)  
    [<span data-ttu-id="5ee0e-222">**GetCPUDescriptorHandleForHeapStart**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-222">**GetCPUDescriptorHandleForHeapStart**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [<span data-ttu-id="5ee0e-223">**IDXGISwapChain::GetBuffer**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-223">**IDXGISwapChain::GetBuffer**</span></span>](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer)  
    [<span data-ttu-id="5ee0e-224">**ID3D12Device::CreateRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-224">**ID3D12Device::CreateRenderTargetView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)  
    </dl>
-   <span data-ttu-id="5ee0e-225">Crie o alocador de comando: [**ID3D12Device:: CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-225">Create the command allocator: [**ID3D12Device::CreateCommandAllocator**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandallocator).</span></span>

<span data-ttu-id="5ee0e-226">Em etapas posteriores, as listas de comandos são obtidas do alocador de comandos e enviadas à fila de comandos.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-226">In later steps, command lists are obtained from the command allocator and submitted to the command queue.</span></span>

<span data-ttu-id="5ee0e-227">Carregue as dependências do pipeline de renderização (Observe que a criação de um dispositivo de detorção de software é totalmente opcional).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-227">Load the rendering pipeline dependencies (note that the creation of a software WARP device is entirely optional).</span></span>


```cpp
void D3D12HelloTriangle::LoadPipeline()
{
#if defined(_DEBUG)
    // Enable the D3D12 debug layer.
    {
        
        ComPtr<ID3D12Debug> debugController;
        if (SUCCEEDED(D3D12GetDebugInterface(IID_PPV_ARGS(&debugController))))
        {
            debugController->EnableDebugLayer();
        }
    }
#endif

    ComPtr<IDXGIFactory4> factory;
    ThrowIfFailed(CreateDXGIFactory1(IID_PPV_ARGS(&factory)));

    if (m_useWarpDevice)
    {
        ComPtr<IDXGIAdapter> warpAdapter;
        ThrowIfFailed(factory->EnumWarpAdapter(IID_PPV_ARGS(&warpAdapter)));

        ThrowIfFailed(D3D12CreateDevice(
            warpAdapter.Get(),
            D3D_FEATURE_LEVEL_11_0,
            IID_PPV_ARGS(&m_device)
            ));
    }
    else
    {
        ComPtr<IDXGIAdapter1> hardwareAdapter;
        GetHardwareAdapter(factory.Get(), &hardwareAdapter);

        ThrowIfFailed(D3D12CreateDevice(
            hardwareAdapter.Get(),
            D3D_FEATURE_LEVEL_11_0,
            IID_PPV_ARGS(&m_device)
            ));
    }

    // Describe and create the command queue.
    D3D12_COMMAND_QUEUE_DESC queueDesc = {};
    queueDesc.Flags = D3D12_COMMAND_QUEUE_FLAG_NONE;
    queueDesc.Type = D3D12_COMMAND_LIST_TYPE_DIRECT;

    ThrowIfFailed(m_device->CreateCommandQueue(&queueDesc, IID_PPV_ARGS(&m_commandQueue)));

    // Describe and create the swap chain.
    DXGI_SWAP_CHAIN_DESC swapChainDesc = {};
    swapChainDesc.BufferCount = FrameCount;
    swapChainDesc.BufferDesc.Width = m_width;
    swapChainDesc.BufferDesc.Height = m_height;
    swapChainDesc.BufferDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
    swapChainDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
    swapChainDesc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_DISCARD;
    swapChainDesc.OutputWindow = Win32Application::GetHwnd();
    swapChainDesc.SampleDesc.Count = 1;
    swapChainDesc.Windowed = TRUE;

    ComPtr<IDXGISwapChain> swapChain;
    ThrowIfFailed(factory->CreateSwapChain(
        m_commandQueue.Get(),        // Swap chain needs the queue so that it can force a flush on it.
        &swapChainDesc,
        &swapChain
        ));

    ThrowIfFailed(swapChain.As(&m_swapChain));

    // This sample does not support fullscreen transitions.
    ThrowIfFailed(factory->MakeWindowAssociation(Win32Application::GetHwnd(), DXGI_MWA_NO_ALT_ENTER));

    m_frameIndex = m_swapChain->GetCurrentBackBufferIndex();

    // Create descriptor heaps.
    {
        // Describe and create a render target view (RTV) descriptor heap.
        D3D12_DESCRIPTOR_HEAP_DESC rtvHeapDesc = {};
        rtvHeapDesc.NumDescriptors = FrameCount;
        rtvHeapDesc.Type = D3D12_DESCRIPTOR_HEAP_TYPE_RTV;
        rtvHeapDesc.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_NONE;
        ThrowIfFailed(m_device->CreateDescriptorHeap(&rtvHeapDesc, IID_PPV_ARGS(&m_rtvHeap)));

        m_rtvDescriptorSize = m_device->GetDescriptorHandleIncrementSize(D3D12_DESCRIPTOR_HEAP_TYPE_RTV);
    }

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

        // Create a RTV for each frame.
        for (UINT n = 0; n < FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
            m_device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);
            rtvHandle.Offset(1, m_rtvDescriptorSize);
        }
    }

    ThrowIfFailed(m_device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocator)));
}
```



### <a name="loadassets"></a><span data-ttu-id="5ee0e-228">Loadassets ()</span><span class="sxs-lookup"><span data-stu-id="5ee0e-228">LoadAssets()</span></span>

<span data-ttu-id="5ee0e-229">O carregamento e a preparação de ativos é um processo longo.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-229">Loading and preparing assets is a lengthy process.</span></span> <span data-ttu-id="5ee0e-230">Muitos desses estágios são semelhantes ao D3D 11, embora alguns sejam novos no D3D 12.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-230">Many of these stages are similar to D3D 11, though some are new to D3D 12.</span></span>

<span data-ttu-id="5ee0e-231">No Direct3D 12, o estado de pipeline necessário é anexado a uma lista de comandos por meio de um PSO ( [objeto de estado de pipeline](managing-graphics-pipeline-state-in-direct3d-12.md) ).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-231">In Direct3D 12, required pipeline state is attached to a command list via a [pipeline state object](managing-graphics-pipeline-state-in-direct3d-12.md) (PSO).</span></span> <span data-ttu-id="5ee0e-232">Este exemplo mostra como criar um PSO.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-232">This example shows how to create a PSO.</span></span> <span data-ttu-id="5ee0e-233">Você pode armazenar o PSO como uma variável de membro e reutilizá-lo quantas vezes forem necessárias.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-233">You can store the PSO as a member variable and reuse it as many times as needed.</span></span>

<span data-ttu-id="5ee0e-234">Um heap de descritores define as exibições e como acessar recursos (por exemplo, uma exibição de destino de renderização).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-234">A descriptor heap defines the views and how to access resources (for example, a render target view).</span></span>

<span data-ttu-id="5ee0e-235">Com a lista de comandos alocador e PSO, você pode criar a lista de comandos real, que será executada posteriormente.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-235">With the command list allocator and PSO, you can create the actual command list, which will be executed at a later time.</span></span>

<span data-ttu-id="5ee0e-236">As seguintes APIs e processos são chamados sucessivamente.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-236">The following APIs and processes are called in succession.</span></span>

-   <span data-ttu-id="5ee0e-237">Crie uma assinatura raiz vazia usando a estrutura auxiliar disponível:</span><span class="sxs-lookup"><span data-stu-id="5ee0e-237">Create an empty root signature, using the available helper structure:</span></span> <dl>

[<span data-ttu-id="5ee0e-238">**Desc. de \_ assinatura raiz CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-238">**CD3DX12\_ROOT\_SIGNATURE\_DESC**</span></span>](cd3dx12-root-signature-desc.md)  
    [<span data-ttu-id="5ee0e-239">**D3D12SerializeRootSignature**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-239">**D3D12SerializeRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature)  
    [<span data-ttu-id="5ee0e-240">**ID3D12Device::CreateRootSignature**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-240">**ID3D12Device::CreateRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrootsignature)  
    </dl>
-   <span data-ttu-id="5ee0e-241">Carregue e compile os sombreadores: [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-241">Load and compile the shaders: [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile).</span></span>
-   <span data-ttu-id="5ee0e-242">Crie o layout de entrada do vértice: [**\_ elemento de entrada D3D12 \_ \_ desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-242">Create the vertex input layout: [**D3D12\_INPUT\_ELEMENT\_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_input_element_desc).</span></span>
-   <span data-ttu-id="5ee0e-243">Preencha uma descrição do estado do pipeline, usando as estruturas auxiliares disponíveis e, em seguida, crie o estado do pipeline de gráficos:</span><span class="sxs-lookup"><span data-stu-id="5ee0e-243">Fill out a pipeline state description, using the helper structures available, then create the graphics pipeline state:</span></span> <dl>

[<span data-ttu-id="5ee0e-244">**Desc. de estado do pipeline de \_ gráficos D3D12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-244">**D3D12\_GRAPHICS\_PIPELINE\_STATE\_DESC**</span></span>](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc)  
    [<span data-ttu-id="5ee0e-245">**CD3DX12 do \_ rasterizador \_ desc**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-245">**CD3DX12\_RASTERIZER\_DESC**</span></span>](cd3dx12-rasterizer-desc.md)  
    [<span data-ttu-id="5ee0e-246">**CD3DX12 de \_ combinação \_ desc**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-246">**CD3DX12\_BLEND\_DESC**</span></span>](cd3dx12-blend-desc.md)  
    [<span data-ttu-id="5ee0e-247">**ID3D12Device::CreateGraphicsPipelineState**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-247">**ID3D12Device::CreateGraphicsPipelineState**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate)  
    </dl>
-   <span data-ttu-id="5ee0e-248">Criar e fechar uma lista de comandos:</span><span class="sxs-lookup"><span data-stu-id="5ee0e-248">Create, then close, a command list:</span></span> <dl>

[<span data-ttu-id="5ee0e-249">**ID3D12Device:: createcommandlist**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-249">**ID3D12Device::CreateCommandList**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist)  
    [<span data-ttu-id="5ee0e-250">**ID3D12GraphicsCommandList:: fechar**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-250">**ID3D12GraphicsCommandList::Close**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)  
    </dl>
-   <span data-ttu-id="5ee0e-251">Crie o buffer de vértice: [**ID3D12Device:: CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-251">Create the vertex buffer: [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).</span></span>
-   <span data-ttu-id="5ee0e-252">Copie os dados de vértice para o buffer de vértice:</span><span class="sxs-lookup"><span data-stu-id="5ee0e-252">Copy the vertex data to the vertex buffer:</span></span><dl>

[<span data-ttu-id="5ee0e-253">**ID3D12Resource:: map**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-253">**ID3D12Resource::Map**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map)  
    [<span data-ttu-id="5ee0e-254">**ID3D12Resource:: mapeamento**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-254">**ID3D12Resource::Unmap**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-unmap)  
    </dl>
-   <span data-ttu-id="5ee0e-255">Inicialize a exibição do buffer de vértice: [**GetGPUVirtualAddress**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-255">Initialize the vertex buffer view: [**GetGPUVirtualAddress**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-getgpuvirtualaddress).</span></span>
-   <span data-ttu-id="5ee0e-256">Crie e inicialize a cerca: [**ID3D12Device:: createfence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-256">Create and initialize the fence: [**ID3D12Device::CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence).</span></span>
-   <span data-ttu-id="5ee0e-257">Crie um identificador de evento para usar com a sincronização de quadros.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-257">Create an event handle for use with frame synchronization.</span></span>
-   <span data-ttu-id="5ee0e-258">Aguarde a conclusão da GPU.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-258">Wait for the GPU to finish.</span></span>


```cpp
void D3D12HelloTriangle::LoadAssets()
{
    // Create an empty root signature.
    {
        CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
        rootSignatureDesc.Init(0, nullptr, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

        ComPtr<ID3DBlob> signature;
        ComPtr<ID3DBlob> error;
        ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
        ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));
    }

    // Create the pipeline state, which includes compiling and loading shaders.
    {
        ComPtr<ID3DBlob> vertexShader;
        ComPtr<ID3DBlob> pixelShader;

#if defined(_DEBUG)
        // Enable better shader debugging with the graphics debugging tools.
        UINT compileFlags = D3DCOMPILE_DEBUG | D3DCOMPILE_SKIP_OPTIMIZATION;
#else
        UINT compileFlags = 0;
#endif

        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "VSMain", "vs_5_0", compileFlags, 0, &vertexShader, nullptr));
        ThrowIfFailed(D3DCompileFromFile(GetAssetFullPath(L"shaders.hlsl").c_str(), nullptr, nullptr, "PSMain", "ps_5_0", compileFlags, 0, &pixelShader, nullptr));

        // Define the vertex input layout.
        D3D12_INPUT_ELEMENT_DESC inputElementDescs[] =
        {
            { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 },
            { "COLOR", 0, DXGI_FORMAT_R32G32B32A32_FLOAT, 0, 12, D3D12_INPUT_CLASSIFICATION_PER_VERTEX_DATA, 0 }
        };

        // Describe and create the graphics pipeline state object (PSO).
        D3D12_GRAPHICS_PIPELINE_STATE_DESC psoDesc = {};
        psoDesc.InputLayout = { inputElementDescs, _countof(inputElementDescs) };
        psoDesc.pRootSignature = m_rootSignature.Get();
        psoDesc.VS = { reinterpret_cast<UINT8*>(vertexShader->GetBufferPointer()), vertexShader->GetBufferSize() };
        psoDesc.PS = { reinterpret_cast<UINT8*>(pixelShader->GetBufferPointer()), pixelShader->GetBufferSize() };
        psoDesc.RasterizerState = CD3DX12_RASTERIZER_DESC(D3D12_DEFAULT);
        psoDesc.BlendState = CD3DX12_BLEND_DESC(D3D12_DEFAULT);
        psoDesc.DepthStencilState.DepthEnable = FALSE;
        psoDesc.DepthStencilState.StencilEnable = FALSE;
        psoDesc.SampleMask = UINT_MAX;
        psoDesc.PrimitiveTopologyType = D3D12_PRIMITIVE_TOPOLOGY_TYPE_TRIANGLE;
        psoDesc.NumRenderTargets = 1;
        psoDesc.RTVFormats[0] = DXGI_FORMAT_R8G8B8A8_UNORM;
        psoDesc.SampleDesc.Count = 1;
        ThrowIfFailed(m_device->CreateGraphicsPipelineState(&psoDesc, IID_PPV_ARGS(&m_pipelineState)));
    }

    // Create the command list.
    ThrowIfFailed(m_device->CreateCommandList(0, D3D12_COMMAND_LIST_TYPE_DIRECT, m_commandAllocator.Get(), m_pipelineState.Get(), IID_PPV_ARGS(&m_commandList)));

    // Command lists are created in the recording state, but there is nothing
    // to record yet. The main loop expects it to be closed, so close it now.
    ThrowIfFailed(m_commandList->Close());

    // Create the vertex buffer.
    {
        // Define the geometry for a triangle.
        Vertex triangleVertices[] =
        {
            { { 0.0f, 0.25f * m_aspectRatio, 0.0f }, { 1.0f, 0.0f, 0.0f, 1.0f } },
            { { 0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 1.0f, 0.0f, 1.0f } },
            { { -0.25f, -0.25f * m_aspectRatio, 0.0f }, { 0.0f, 0.0f, 1.0f, 1.0f } }
        };

        const UINT vertexBufferSize = sizeof(triangleVertices);

        // Note: using upload heaps to transfer static data like vert buffers is not 
        // recommended. Every time the GPU needs it, the upload heap will be marshalled 
        // over. Please read up on Default Heap usage. An upload heap is used here for 
        // code simplicity and because there are very few verts to actually transfer.
        CD3DX12_HEAP_PROPERTIES heapProps(D3D12_HEAP_TYPE_UPLOAD);
        auto desc = CD3DX12_RESOURCE_DESC::Buffer(vertexBufferSize);
        ThrowIfFailed(m_device->CreateCommittedResource(
            &heapProps,
            D3D12_HEAP_FLAG_NONE,
            &desc,
            D3D12_RESOURCE_STATE_GENERIC_READ,
            nullptr,
            IID_PPV_ARGS(&m_vertexBuffer)));

        // Copy the triangle data to the vertex buffer.
        UINT8* pVertexDataBegin;
        CD3DX12_RANGE readRange(0, 0);        // We do not intend to read from this resource on the CPU.
        ThrowIfFailed(m_vertexBuffer->Map(0, &readRange, reinterpret_cast<void**>(&pVertexDataBegin)));
        memcpy(pVertexDataBegin, triangleVertices, sizeof(triangleVertices));
        m_vertexBuffer->Unmap(0, nullptr);

        // Initialize the vertex buffer view.
        m_vertexBufferView.BufferLocation = m_vertexBuffer->GetGPUVirtualAddress();
        m_vertexBufferView.StrideInBytes = sizeof(Vertex);
        m_vertexBufferView.SizeInBytes = vertexBufferSize;
    }

    // Create synchronization objects and wait until assets have been uploaded to the GPU.
    {
        ThrowIfFailed(m_device->CreateFence(0, D3D12_FENCE_FLAG_NONE, IID_PPV_ARGS(&m_fence)));
        m_fenceValue = 1;

        // Create an event handle to use for frame synchronization.
        m_fenceEvent = CreateEvent(nullptr, FALSE, FALSE, nullptr);
        if (m_fenceEvent == nullptr)
        {
            ThrowIfFailed(HRESULT_FROM_WIN32(GetLastError()));
        }

        // Wait for the command list to execute; we are reusing the same command 
        // list in our main loop but for now, we just want to wait for setup to 
        // complete before continuing.
        WaitForPreviousFrame();
    }
}
```



### <a name="onupdate"></a><span data-ttu-id="5ee0e-259">OnUpdate ()</span><span class="sxs-lookup"><span data-stu-id="5ee0e-259">OnUpdate()</span></span>

<span data-ttu-id="5ee0e-260">Para um exemplo simples, nada é atualizado.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-260">For a simple example, nothing is updated.</span></span>


```cpp
void D3D12HelloTriangle::OnUpdate()

{
}
```



### <a name="onrender"></a><span data-ttu-id="5ee0e-261">OnRender ()</span><span class="sxs-lookup"><span data-stu-id="5ee0e-261">OnRender()</span></span>

<span data-ttu-id="5ee0e-262">Durante a configuração, a variável de membro **m \_ commandlist** foi usada para registrar e executar todos os comandos set up.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-262">During set up, the member variable **m\_commandList** was used to record and execute all of the set up commands.</span></span> <span data-ttu-id="5ee0e-263">Agora você pode reutilizar esse membro no loop de renderização principal.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-263">You can now reuse that member in the main render loop.</span></span>

<span data-ttu-id="5ee0e-264">A renderização envolve uma chamada para popular a lista de comandos e, em seguida, a lista de comandos pode ser executada e o próximo buffer na cadeia de troca apresentada:</span><span class="sxs-lookup"><span data-stu-id="5ee0e-264">Rendering involves a call to populate the command list, then the command list can be executed and the next buffer in the swap chain presented:</span></span>

-   <span data-ttu-id="5ee0e-265">Preencha a lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-265">Populate the command list.</span></span>
-   <span data-ttu-id="5ee0e-266">Execute a lista de comandos: [**ID3D12CommandQueue:: ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-266">Execute the command list: [**ID3D12CommandQueue::ExecuteCommandLists**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).</span></span>
-   <span data-ttu-id="5ee0e-267">[**IDXGISwapChain1::P resent1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) o quadro.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-267">[**IDXGISwapChain1::Present1**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) the frame.</span></span>
-   <span data-ttu-id="5ee0e-268">Aguarde a conclusão da GPU.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-268">Wait on the GPU to finish.</span></span>


```cpp
void D3D12HelloTriangle::OnRender()
{
    // Record all the commands we need to render the scene into the command list.
    PopulateCommandList();

    // Execute the command list.
    ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
    m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

    // Present the frame.
    ThrowIfFailed(m_swapChain->Present(1, 0));

    WaitForPreviousFrame();
}
```



### <a name="populatecommandlist"></a><span data-ttu-id="5ee0e-269">PopulateCommandList()</span><span class="sxs-lookup"><span data-stu-id="5ee0e-269">PopulateCommandList()</span></span>

<span data-ttu-id="5ee0e-270">Você deve redefinir o alocador de lista de comandos e a própria lista de comandos antes de poder reutilizá-los.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-270">You must reset the command list allocator and the command list itself before you can reuse them.</span></span> <span data-ttu-id="5ee0e-271">Em cenários mais avançados, pode fazer sentido redefinir o alocador a cada vários quadros.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-271">In more advanced scenarios it might make sense to reset the allocator every several frames.</span></span> <span data-ttu-id="5ee0e-272">A memória é associada ao alocador que não pode ser liberado imediatamente após a execução de uma lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-272">Memory is associated with the allocator that can't be released immediately after executing a command list.</span></span> <span data-ttu-id="5ee0e-273">Este exemplo mostra como redefinir o alocador após cada quadro.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-273">This example shows how to reset the allocator after every frame.</span></span>

<span data-ttu-id="5ee0e-274">Agora, reutilize a lista de comandos para o quadro atual.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-274">Now, reuse the command list for the current frame.</span></span> <span data-ttu-id="5ee0e-275">Reanexe o visor à lista de comandos (que deve ser feito sempre que uma lista de comandos for redefinida e antes da execução da lista de comandos), indique que o recurso estará em uso como um destino de renderização, registre comandos e, em seguida, indique que o destino de renderização será usado para apresentar quando a execução da lista de comandos for concluída.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-275">Reattach the viewport to the command list (which must be done whenever a command list is reset, and before the command list is executed), indicate that the resource will be in use as a render target, record commands, and then indicate that the render target will be used to present when the command list is done executing.</span></span>

<span data-ttu-id="5ee0e-276">A população de listas de comandos chama os seguintes métodos e processos por sua vez:</span><span class="sxs-lookup"><span data-stu-id="5ee0e-276">Populating command lists calls the following methods and processes in turn:</span></span>

-   <span data-ttu-id="5ee0e-277">Redefina o alocador de comando e a lista de comandos:</span><span class="sxs-lookup"><span data-stu-id="5ee0e-277">Reset the command allocator, and command list:</span></span> <dl>

[<span data-ttu-id="5ee0e-278">**ID3D12CommandAllocator:: Reset**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-278">**ID3D12CommandAllocator::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandallocator-reset)  
    [<span data-ttu-id="5ee0e-279">**ID3D12GraphicsCommandList:: Reset**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-279">**ID3D12GraphicsCommandList::Reset**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)  
    </dl>
-   <span data-ttu-id="5ee0e-280">Defina os retângulos de assinatura raiz, visor e tesoura:</span><span class="sxs-lookup"><span data-stu-id="5ee0e-280">Set the root signature, viewport and scissors rectangles:</span></span> <dl>

[<span data-ttu-id="5ee0e-281">**ID3D12GraphicsCommandList::SetGraphicsRootSignature**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-281">**ID3D12GraphicsCommandList::SetGraphicsRootSignature**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootsignature)  
    [<span data-ttu-id="5ee0e-282">**ID3D12GraphicsCommandList::RSSetViewports**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-282">**ID3D12GraphicsCommandList::RSSetViewports**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports)  
    [<span data-ttu-id="5ee0e-283">**ID3D12GraphicsCommandList::RSSetScissorRects**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-283">**ID3D12GraphicsCommandList::RSSetScissorRects**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects)  
    </dl>
-   <span data-ttu-id="5ee0e-284">Indique que o buffer de fundo deve ser usado como um destino de renderização:</span><span class="sxs-lookup"><span data-stu-id="5ee0e-284">Indicate that the back buffer is to be used as a render target:</span></span> <dl>

[<span data-ttu-id="5ee0e-285">**ID3D12GraphicsCommandList::ResourceBarrier**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-285">**ID3D12GraphicsCommandList::ResourceBarrier**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)  
    [<span data-ttu-id="5ee0e-286">**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-286">**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)  
    [<span data-ttu-id="5ee0e-287">**ID3D12GraphicsCommandList::OMSetRenderTargets**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-287">**ID3D12GraphicsCommandList::OMSetRenderTargets**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)  
    </dl>
-   <span data-ttu-id="5ee0e-288">Registre os comandos:</span><span class="sxs-lookup"><span data-stu-id="5ee0e-288">Record the commands:</span></span><dl>

[<span data-ttu-id="5ee0e-289">**ID3D12GraphicsCommandList::ClearRenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-289">**ID3D12GraphicsCommandList::ClearRenderTargetView**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)  
    [<span data-ttu-id="5ee0e-290">**ID3D12GraphicsCommandList::IASetPrimitiveTopology**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-290">**ID3D12GraphicsCommandList::IASetPrimitiveTopology**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology)  
    [<span data-ttu-id="5ee0e-291">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-291">**ID3D12GraphicsCommandList::IASetVertexBuffers**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)  
    [<span data-ttu-id="5ee0e-292">**ID3D12GraphicsCommandList::D rawInstanced**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-292">**ID3D12GraphicsCommandList::DrawInstanced**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)  
    </dl>
-   <span data-ttu-id="5ee0e-293">Indique que o buffer de fundo agora será usado para apresentar: [**ID3D12GraphicsCommandList:: ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-293">Indicate the back buffer will now be used to present: [**ID3D12GraphicsCommandList::ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).</span></span>
-   <span data-ttu-id="5ee0e-294">Feche a lista de comandos: [**ID3D12GraphicsCommandList:: Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-294">Close the command list: [**ID3D12GraphicsCommandList::Close**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close).</span></span>


```cpp
void D3D12HelloTriangle::PopulateCommandList()
{
    // Command list allocators can only be reset when the associated 
    // command lists have finished execution on the GPU; apps should use 
    // fences to determine GPU execution progress.
    ThrowIfFailed(m_commandAllocator->Reset());

    // However, when ExecuteCommandList() is called on a particular command 
    // list, that command list can then be reset at any time and must be before 
    // re-recording.
    ThrowIfFailed(m_commandList->Reset(m_commandAllocator.Get(), m_pipelineState.Get()));

    // Set necessary state.
    m_commandList->SetGraphicsRootSignature(m_rootSignature.Get());
    m_commandList->RSSetViewports(1, &m_viewport);
    m_commandList->RSSetScissorRects(1, &m_scissorRect);

    // Indicate that the back buffer will be used as a render target.
    auto barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_PRESENT, D3D12_RESOURCE_STATE_RENDER_TARGET);
    m_commandList->ResourceBarrier(1, &barrier);

    CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart(), m_frameIndex, m_rtvDescriptorSize);
    m_commandList->OMSetRenderTargets(1, &rtvHandle, FALSE, nullptr);

    // Record commands.
    const float clearColor[] = { 0.0f, 0.2f, 0.4f, 1.0f };
    m_commandList->ClearRenderTargetView(rtvHandle, clearColor, 0, nullptr);
    m_commandList->IASetPrimitiveTopology(D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST);
    m_commandList->IASetVertexBuffers(0, 1, &m_vertexBufferView);
    m_commandList->DrawInstanced(3, 1, 0, 0);

    // Indicate that the back buffer will now be used to present.
    barrier = CD3DX12_RESOURCE_BARRIER::Transition(m_renderTargets[m_frameIndex].Get(), D3D12_RESOURCE_STATE_RENDER_TARGET, D3D12_RESOURCE_STATE_PRESENT);
    m_commandList->ResourceBarrier(1, &barrier);

    ThrowIfFailed(m_commandList->Close());
}
```



### <a name="waitforpreviousframe"></a><span data-ttu-id="5ee0e-295">WaitForPreviousFrame()</span><span class="sxs-lookup"><span data-stu-id="5ee0e-295">WaitForPreviousFrame()</span></span>

<span data-ttu-id="5ee0e-296">O código a seguir mostra um uso supersimplificado de limites.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-296">The following code shows an over-simplified use of fences.</span></span>

> [!Note]  
> <span data-ttu-id="5ee0e-297">Aguardar a conclusão de um quadro é muito ineficiente para a maioria dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-297">Waiting for a frame to complete is too inefficient for most apps.</span></span>

 

<span data-ttu-id="5ee0e-298">As seguintes APIs e processos são chamados na ordem:</span><span class="sxs-lookup"><span data-stu-id="5ee0e-298">The following APIs and processes are called in order:</span></span>

-   [<span data-ttu-id="5ee0e-299">**ID3D12CommandQueue:: Signal**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-299">**ID3D12CommandQueue::Signal**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal)
-   [<span data-ttu-id="5ee0e-300">**ID3D12Fence:: getcompletedvalue**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-300">**ID3D12Fence::GetCompletedValue**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue)
-   [<span data-ttu-id="5ee0e-301">**ID3D12Fence::SetEventOnCompletion**</span><span class="sxs-lookup"><span data-stu-id="5ee0e-301">**ID3D12Fence::SetEventOnCompletion**</span></span>](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion)
-   <span data-ttu-id="5ee0e-302">Aguarde o evento.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-302">Wait for the event.</span></span>
-   <span data-ttu-id="5ee0e-303">Atualize o índice do quadro: [**IDXGISwapChain3:: GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex).</span><span class="sxs-lookup"><span data-stu-id="5ee0e-303">Update the frame index: [**IDXGISwapChain3::GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex).</span></span>


```cpp
void D3D12HelloTriangle::WaitForPreviousFrame()
{
    // WAITING FOR THE FRAME TO COMPLETE BEFORE CONTINUING IS NOT BEST PRACTICE.
    // This is code implemented as such for simplicity. More advanced samples 
    // illustrate how to use fences for efficient resource usage.

    // Signal and increment the fence value.
    const UINT64 fence = m_fenceValue;
    ThrowIfFailed(m_commandQueue->Signal(m_fence.Get(), fence));
    m_fenceValue++;

    // Wait until the previous frame is finished.
    if (m_fence->GetCompletedValue() < fence)
    {
        ThrowIfFailed(m_fence->SetEventOnCompletion(fence, m_fenceEvent));
        WaitForSingleObject(m_fenceEvent, INFINITE);
    }

    m_frameIndex = m_swapChain->GetCurrentBackBufferIndex();
}
```



### <a name="ondestroy"></a><span data-ttu-id="5ee0e-304">OnDestroy ()</span><span class="sxs-lookup"><span data-stu-id="5ee0e-304">OnDestroy()</span></span>

<span data-ttu-id="5ee0e-305">Fechar o aplicativo corretamente.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-305">Cleanly close down the app.</span></span>

-   <span data-ttu-id="5ee0e-306">Aguarde a conclusão da GPU.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-306">Wait for the GPU to finish.</span></span>
-   <span data-ttu-id="5ee0e-307">Feche o evento.</span><span class="sxs-lookup"><span data-stu-id="5ee0e-307">Close the event.</span></span>


```cpp
void D3D12HelloTriangle::OnDestroy()
{

    // Wait for the GPU to be done with all resources.
    WaitForPreviousFrame();

    CloseHandle(m_fenceEvent);
}
```



## <a name="related-topics"></a><span data-ttu-id="5ee0e-308">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5ee0e-308">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ee0e-309">Entendendo o Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="5ee0e-309">Understanding Direct3D 12</span></span>](directx-12-getting-started.md)
</dt> <dt>

[<span data-ttu-id="5ee0e-310">Exemplos de trabalho</span><span class="sxs-lookup"><span data-stu-id="5ee0e-310">Working Samples</span></span>](working-samples.md)
</dt> </dl>

 

 
