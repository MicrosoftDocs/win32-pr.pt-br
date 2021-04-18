---
title: Entender o pipeline de renderização do Direct3D 11
description: Anteriormente, você examinou como criar uma janela que pode ser usada para desenhar em funcionamento com recursos de dispositivo do DirectX. Agora, você aprende como criar o pipeline de gráficos e onde pode conectá-lo.
ms.assetid: 73cf62d0-7e4f-4e93-aa65-12741588d4fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50f9a387b2d44fe750abcf5a8856f75e6d0110e
ms.sourcegitcommit: 07b756a2f350efa5cfd5024a723ef392274ac3d9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/17/2021
ms.locfileid: "105772738"
---
# <a name="understand-the-direct3d-11-rendering-pipeline"></a><span data-ttu-id="ba607-104">Entender o pipeline de renderização do Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="ba607-104">Understand the Direct3D 11 rendering pipeline</span></span>

<span data-ttu-id="ba607-105">Anteriormente, você examinou como criar uma janela que pode ser usada para desenhar em [funcionamento com recursos de dispositivo do DirectX](work-with-dxgi.md).</span><span class="sxs-lookup"><span data-stu-id="ba607-105">Previously, you looked at how to create a window you can use for drawing in [Work with DirectX device resources](work-with-dxgi.md).</span></span> <span data-ttu-id="ba607-106">Agora, você aprende como criar o pipeline de gráficos e onde pode conectá-lo.</span><span class="sxs-lookup"><span data-stu-id="ba607-106">Now, you learn how to build the graphics pipeline, and where you can hook into it.</span></span>

<span data-ttu-id="ba607-107">Você se lembrará de que há duas interfaces Direct3D que definem o pipeline de gráficos: [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2), que fornece uma representação virtual da GPU e seus recursos; e [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2), que representa o processamento de gráficos para o pipeline.</span><span class="sxs-lookup"><span data-stu-id="ba607-107">You'll recall that there are two Direct3D interfaces that define the graphics pipeline: [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2), which provides a virtual representation of the GPU and its resources; and [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2), which represents the graphics processing for the pipeline.</span></span> <span data-ttu-id="ba607-108">Normalmente, você usa uma instância de **ID3D11Device** para configurar e obter os recursos de GPU necessários para começar a processar os gráficos em uma cena, e você usa o **ID3D11DeviceContext** para processar esses recursos em cada estágio de sombreador apropriado no pipeline de gráficos.</span><span class="sxs-lookup"><span data-stu-id="ba607-108">Typically, you use an instance of **ID3D11Device** to configure and obtain the GPU resources you need to start processing the graphics in a scene, and you use **ID3D11DeviceContext** to process those resources at each appropriate shader stage in the graphics pipeline.</span></span> <span data-ttu-id="ba607-109">Normalmente, você chama métodos **ID3D11Device** com pouca frequência — ou seja, somente quando você configura uma cena ou quando o dispositivo é alterado.</span><span class="sxs-lookup"><span data-stu-id="ba607-109">You usually call **ID3D11Device** methods infrequently—that is, only when you set up a scene or when the device changes.</span></span> <span data-ttu-id="ba607-110">Por outro lado, você chamará **ID3D11DeviceContext** toda vez que processar um quadro para exibição.</span><span class="sxs-lookup"><span data-stu-id="ba607-110">On the other hand, you'll call **ID3D11DeviceContext** every time you process a frame for display.</span></span>

<span data-ttu-id="ba607-111">Este exemplo cria e configura um pipeline de gráficos mínimo adequado para exibir um cubo simples de rotação de vértices.</span><span class="sxs-lookup"><span data-stu-id="ba607-111">This example creates and configures a minimal graphics pipeline suitable for displaying a simple spinning, vertex-shaded cube.</span></span> <span data-ttu-id="ba607-112">Ele demonstra aproximadamente o menor conjunto de recursos necessário para a exibição.</span><span class="sxs-lookup"><span data-stu-id="ba607-112">It demonstrates approximately the smallest set of resources necessary for display.</span></span> <span data-ttu-id="ba607-113">Ao ler as informações aqui, observe as limitações do exemplo fornecido, em que você pode precisar estendê-las para dar suporte à cena que deseja renderizar.</span><span class="sxs-lookup"><span data-stu-id="ba607-113">As you read the info here, note the limitations of the given example where you may have to extend it to support the scene you want to render.</span></span>

<span data-ttu-id="ba607-114">Este exemplo aborda duas classes C++ para gráficos: uma classe do Gerenciador de recursos de dispositivo e uma classe de renderizador de cena 3D.</span><span class="sxs-lookup"><span data-stu-id="ba607-114">This example covers two C++ classes for graphics: a device resource manager class, and 3D scene renderer class.</span></span> <span data-ttu-id="ba607-115">Este tópico se concentra especificamente no renderizador de cena 3D.</span><span class="sxs-lookup"><span data-stu-id="ba607-115">This topic focuses specifically on the 3D scene renderer.</span></span>

## <a name="what-does-the-cube-renderer-do"></a><span data-ttu-id="ba607-116">O que o renderizador de cubo faz?</span><span class="sxs-lookup"><span data-stu-id="ba607-116">What does the cube renderer do?</span></span>

<span data-ttu-id="ba607-117">O pipeline de gráficos é definido pela classe renderizador de cena 3D.</span><span class="sxs-lookup"><span data-stu-id="ba607-117">The graphics pipeline is defined by the 3D scene renderer class.</span></span> <span data-ttu-id="ba607-118">O renderizador de cena é capaz de:</span><span class="sxs-lookup"><span data-stu-id="ba607-118">The scene renderer is able to:</span></span>

-   <span data-ttu-id="ba607-119">Defina buffers de constantes para armazenar seus dados uniformes.</span><span class="sxs-lookup"><span data-stu-id="ba607-119">Define constant buffers to store your uniform data.</span></span>
-   <span data-ttu-id="ba607-120">Defina os buffers de vértice para manter os dados de vértice do objeto e os buffers de índice correspondentes para habilitar o sombreador de vértice para percorrer os triângulos corretamente.</span><span class="sxs-lookup"><span data-stu-id="ba607-120">Define vertex buffers to hold your object vertex data, and corresponding index buffers to enable the vertex shader to walk the triangles correctly.</span></span>
-   <span data-ttu-id="ba607-121">Criar recursos de textura e exibições de recursos.</span><span class="sxs-lookup"><span data-stu-id="ba607-121">Create texture resources and resource views.</span></span>
-   <span data-ttu-id="ba607-122">Carregue os objetos do sombreador.</span><span class="sxs-lookup"><span data-stu-id="ba607-122">Load your shader objects.</span></span>
-   <span data-ttu-id="ba607-123">Atualize os dados gráficos para exibir cada quadro.</span><span class="sxs-lookup"><span data-stu-id="ba607-123">Update the graphics data to display each frame.</span></span>
-   <span data-ttu-id="ba607-124">Renderizar (desenhar) os gráficos para a cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="ba607-124">Render (draw) the graphics to the swap chain.</span></span>

<span data-ttu-id="ba607-125">Os quatro primeiros processos normalmente usam os métodos de interface [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) para inicializar e gerenciar recursos gráficos, e os dois últimos usam os métodos de interface [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) para gerenciar e executar o pipeline de gráficos.</span><span class="sxs-lookup"><span data-stu-id="ba607-125">The first four processes typically use the [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) interface methods for initializing and managing graphics resources, and the last two use the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) interface methods to manage and execute the graphics pipeline.</span></span>

<span data-ttu-id="ba607-126">Uma instância da classe **Renderer** é criada e gerenciada como uma variável de membro na classe de projeto principal.</span><span class="sxs-lookup"><span data-stu-id="ba607-126">An instance of the **Renderer** class is created and managed as a member variable on the main project class.</span></span> <span data-ttu-id="ba607-127">A instância de **DeviceResources** é gerenciada como um ponteiro compartilhado entre várias classes, incluindo a classe do projeto principal, a classe do provedor de exibição do **aplicativo** e o **processador**.</span><span class="sxs-lookup"><span data-stu-id="ba607-127">The **DeviceResources** instance is managed as a shared pointer across several classes, including the main project class, the **App** view-provider class, and **Renderer**.</span></span> <span data-ttu-id="ba607-128">Se você substituir o **renderizador** pela sua própria classe, considere declarar e atribuir a instância **DeviceResources** como um membro de ponteiro compartilhado também:</span><span class="sxs-lookup"><span data-stu-id="ba607-128">If you replace **Renderer** with your own class, consider declaring and assigning the **DeviceResources** instance as a shared pointer member as well:</span></span>

`std::shared_ptr<DX::DeviceResources> m_deviceResources;`

<span data-ttu-id="ba607-129">Basta passar o ponteiro para o construtor da classe (ou outro método de inicialização) depois que a instância **DeviceResources** for criada no método **Initialize** da classe **app** .</span><span class="sxs-lookup"><span data-stu-id="ba607-129">Just pass the pointer into the class constructor (or other initialization method) after the **DeviceResources** instance is created in the **Initialize** method of the **App** class.</span></span> <span data-ttu-id="ba607-130">Você também pode passar uma referência de **\_ PTR de fraco** se, em vez disso, deseja que sua classe principal seja completamente proprietária da instância de **DeviceResources** .</span><span class="sxs-lookup"><span data-stu-id="ba607-130">You can also pass a **weak\_ptr** reference if, instead, you want your main class to completely own the **DeviceResources** instance.</span></span>

## <a name="create-the-cube-renderer"></a><span data-ttu-id="ba607-131">Criar o renderizador de cubo</span><span class="sxs-lookup"><span data-stu-id="ba607-131">Create the cube renderer</span></span>

<span data-ttu-id="ba607-132">Neste exemplo, organizamos a classe de renderização de cena com os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="ba607-132">In this example, we organize the scene renderer class with the following methods:</span></span>

-   <span data-ttu-id="ba607-133">**CreateDeviceDependentResources**: chamado sempre que a cena deve ser inicializada ou reiniciada.</span><span class="sxs-lookup"><span data-stu-id="ba607-133">**CreateDeviceDependentResources**: Called whenever the scene must be initialized or restarted.</span></span> <span data-ttu-id="ba607-134">Esse método carrega os dados iniciais do vértice, as texturas, os sombreadores e outros recursos e constrói a constante e os buffers de vértice iniciais.</span><span class="sxs-lookup"><span data-stu-id="ba607-134">This method loads your initial vertex data, textures, shaders, and other resources, and constructs the initial constant and vertex buffers.</span></span> <span data-ttu-id="ba607-135">Normalmente, a maior parte do trabalho aqui é feita com métodos [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) , não métodos [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) .</span><span class="sxs-lookup"><span data-stu-id="ba607-135">Typically, most of the work here is done with [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) methods, not [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) methods.</span></span>
-   <span data-ttu-id="ba607-136">**CreateWindowSizeDependentResources**: chamado sempre que o estado da janela é alterado, como quando o redimensionamento ocorre ou quando a orientação é alterada.</span><span class="sxs-lookup"><span data-stu-id="ba607-136">**CreateWindowSizeDependentResources**: Called whenever the window state changes, such as when resizing occurs or when orientation changes.</span></span> <span data-ttu-id="ba607-137">Esse método recria as matrizes de transformação, como as de sua câmera.</span><span class="sxs-lookup"><span data-stu-id="ba607-137">This method rebuilds transform matrices, such as those for your camera.</span></span>
-   <span data-ttu-id="ba607-138">**Atualização**: normalmente chamado a partir da parte do programa que gerencia o estado de jogo imediato; Neste exemplo, basta chamá-lo da classe **principal** .</span><span class="sxs-lookup"><span data-stu-id="ba607-138">**Update**: Typically called from the part of the program that manages immediate game state; in this example, we just call it from the **Main** class.</span></span> <span data-ttu-id="ba607-139">Esse método leu de qualquer informação de estado de jogo que afete a renderização, como atualizações de posição de objeto ou quadros de animação, além de quaisquer dados de jogos globais, como níveis de luz ou alterações na física do jogo.</span><span class="sxs-lookup"><span data-stu-id="ba607-139">Have this method read from any game-state information that affects rendering, such as updates to object position or animation frames, plus any global game data like light levels or changes to game physics.</span></span> <span data-ttu-id="ba607-140">Essas entradas são usadas para atualizar os buffers de constante por quadro e os dados de objeto.</span><span class="sxs-lookup"><span data-stu-id="ba607-140">These inputs are used to update the per-frame constant buffers and object data.</span></span>
-   <span data-ttu-id="ba607-141">**Render**: normalmente chamado a partir da parte do programa que gerencia o loop de jogo; Nesse caso, ele é chamado a partir da classe **principal** .</span><span class="sxs-lookup"><span data-stu-id="ba607-141">**Render**: Typically called from the part of the program that manages the game loop; in this case, it's called from the **Main** class.</span></span> <span data-ttu-id="ba607-142">Esse método constrói o pipeline de gráficos: ele associa sombreadores, associa buffers e recursos a estágios de sombreador e invoca o desenho para o quadro atual.</span><span class="sxs-lookup"><span data-stu-id="ba607-142">This method constructs the graphics pipeline: it binds shaders, binds buffers and resources to shader stages, and invokes drawing for the current frame.</span></span>

<span data-ttu-id="ba607-143">Esses métodos incluem o corpo de comportamentos para renderizar uma cena com o Direct3D usando seus ativos.</span><span class="sxs-lookup"><span data-stu-id="ba607-143">These methods comprise the body of behaviors for rendering a scene with Direct3D using your assets.</span></span> <span data-ttu-id="ba607-144">Se você estender este exemplo com uma nova classe de renderização, declare-a na classe de projeto principal.</span><span class="sxs-lookup"><span data-stu-id="ba607-144">If you extend this example with a new rendering class, declare it on the main project class.</span></span> <span data-ttu-id="ba607-145">Portanto, isso:</span><span class="sxs-lookup"><span data-stu-id="ba607-145">So this:</span></span>

`std::unique_ptr<Sample3DSceneRenderer> m_sceneRenderer;`

<span data-ttu-id="ba607-146">se torna isso:</span><span class="sxs-lookup"><span data-stu-id="ba607-146">becomes this:</span></span>

`std::unique_ptr<MyAwesomeNewSceneRenderer> m_sceneRenderer;`

<span data-ttu-id="ba607-147">Novamente, observe que este exemplo pressupõe que os métodos tenham as mesmas assinaturas em sua implementação.</span><span class="sxs-lookup"><span data-stu-id="ba607-147">Again, note that this example assumes that the methods have the same signatures in your implementation.</span></span> <span data-ttu-id="ba607-148">Se as assinaturas tiverem sido alteradas, examine o loop **principal** e faça as alterações de acordo.</span><span class="sxs-lookup"><span data-stu-id="ba607-148">If the signatures have changed, review the **Main** loop and make the changes accordingly.</span></span>

<span data-ttu-id="ba607-149">Vamos dar uma olhada nos métodos de renderização de cena em mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="ba607-149">Let's take a look at scene-rendering methods in more detail.</span></span>

## <a name="create-device-dependent-resources"></a><span data-ttu-id="ba607-150">Criar recursos dependentes do dispositivo</span><span class="sxs-lookup"><span data-stu-id="ba607-150">Create device dependent resources</span></span>

<span data-ttu-id="ba607-151">O **CreateDeviceDependentResources** consolida todas as operações para inicializar a cena e seus recursos usando chamadas [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) .</span><span class="sxs-lookup"><span data-stu-id="ba607-151">**CreateDeviceDependentResources** consolidates all the operations for initializing the scene and its resources using [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) calls.</span></span> <span data-ttu-id="ba607-152">Esse método pressupõe que o dispositivo Direct3D acabou de ser inicializado (ou foi recriado) para uma cena.</span><span class="sxs-lookup"><span data-stu-id="ba607-152">This method assumes that the Direct3D device has just been initialized (or has been recreated) for a scene.</span></span> <span data-ttu-id="ba607-153">Ele recria ou recarrega todos os recursos gráficos específicos da cena, como os sombreadores de vértice e pixel, os buffers de vértice e de índice para objetos e quaisquer outros recursos (por exemplo, como texturas e suas exibições correspondentes).</span><span class="sxs-lookup"><span data-stu-id="ba607-153">It recreates or reloads all scene-specific graphics resources, such as the vertex and pixel shaders, the vertex and index buffers for objects, and any other resources (for example, as textures and their corresponding views).</span></span>

<span data-ttu-id="ba607-154">Veja o exemplo de código para **CreateDeviceDependentResources**:</span><span class="sxs-lookup"><span data-stu-id="ba607-154">Here's example code for **CreateDeviceDependentResources**:</span></span>


```C++
void Renderer::CreateDeviceDependentResources()
{
    // Compile shaders using the Effects library.
    auto CreateShadersTask = Concurrency::create_task(
            [this]( )
            {
                CreateShaders();
            }
        );

    // Load the geometry for the spinning cube.
    auto CreateCubeTask = CreateShadersTask.then(
            [this]()
            {
                CreateCube();
            }
        );
}

void Renderer::CreateWindowSizeDependentResources()
{
    // Create the view matrix and the perspective matrix.
    CreateViewAndPerspective();
}
```



<span data-ttu-id="ba607-155">Sempre que você carregar recursos do disco — recursos como objetos de sombreador compilado (CSO ou. CSO) ou texturas, faça isso de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="ba607-155">Any time you load resources from disk—resources like compiled shader object (CSO, or .cso) files or textures—do so asynchronously.</span></span> <span data-ttu-id="ba607-156">Isso permite que você mantenha o trabalho em andamento ao mesmo tempo (como outras tarefas de instalação) e, como o loop principal não é bloqueado, você pode continuar a exibir algo visualmente interessante para o usuário (como uma animação de carregamento para seu jogo).</span><span class="sxs-lookup"><span data-stu-id="ba607-156">This allows you to keep other work going at the same time (like other setup tasks), and because the main loop isn't blocked you can keep displaying something visually interesting to the user (like a loading animation for your game).</span></span> <span data-ttu-id="ba607-157">Este exemplo usa a API Concurrency:: Tasks que está disponível a partir do Windows 8; Observe a sintaxe lambda usada para encapsular tarefas de carregamento assíncronas.</span><span class="sxs-lookup"><span data-stu-id="ba607-157">This example uses the Concurrency::Tasks API that is available starting in Windows 8; note the lambda syntax used to encapsulate asynchronous loading tasks.</span></span> <span data-ttu-id="ba607-158">Essas lambdas representam as funções chamadas off-thread, portanto, um ponteiro para o objeto de classe atual (**this**) é explicitamente capturado.</span><span class="sxs-lookup"><span data-stu-id="ba607-158">These lambdas represent the functions called off-thread, so a pointer to the current class object (**this**) is explicitly captured.</span></span>

<span data-ttu-id="ba607-159">Aqui está um exemplo de como você pode carregar o código de bytes do sombreador:</span><span class="sxs-lookup"><span data-stu-id="ba607-159">Here's an example of how you can load shader bytecode:</span></span>


```C++
HRESULT hr = S_OK;

// Use the Direct3D device to load resources into graphics memory.
ID3D11Device* device = m_deviceResources->GetDevice();

// You'll need to use a file loader to load the shader bytecode. In this
// example, we just use the standard library.
FILE* vShader, * pShader;
BYTE* bytes;

size_t destSize = 4096;
size_t bytesRead = 0;
bytes = new BYTE[destSize];

fopen_s(&vShader, "CubeVertexShader.cso", "rb");
bytesRead = fread_s(bytes, destSize, 1, 4096, vShader);
hr = device->CreateVertexShader(
    bytes,
    bytesRead,
    nullptr,
    &m_pVertexShader
    );

D3D11_INPUT_ELEMENT_DESC iaDesc [] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "COLOR", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayout
    );

delete bytes;


bytes = new BYTE[destSize];
bytesRead = 0;
fopen_s(&pShader, "CubePixelShader.cso", "rb");
bytesRead = fread_s(bytes, destSize, 1, 4096, pShader);
hr = device->CreatePixelShader(
    bytes,
    bytesRead,
    nullptr,
    m_pPixelShader.GetAddressOf()
    );

delete bytes;

CD3D11_BUFFER_DESC cbDesc(
    sizeof(ConstantBufferStruct),
    D3D11_BIND_CONSTANT_BUFFER
    );

hr = device->CreateBuffer(
    &cbDesc,
    nullptr,
    m_pConstantBuffer.GetAddressOf()
    );

fclose(vShader);
fclose(pShader);
```



<span data-ttu-id="ba607-160">Veja um exemplo de como criar um vértice e buffers de índice:</span><span class="sxs-lookup"><span data-stu-id="ba607-160">Here's an example of how to create vertex and index buffers:</span></span>


```C++
HRESULT Renderer::CreateCube()
{
    HRESULT hr = S_OK;

    // Use the Direct3D device to load resources into graphics memory.
    ID3D11Device* device = m_deviceResources->GetDevice();

    // Create cube geometry.
    VertexPositionColor CubeVertices[] =
    {
        {DirectX::XMFLOAT3(-0.5f,-0.5f,-0.5f), DirectX::XMFLOAT3(  0,   0,   0),},
        {DirectX::XMFLOAT3(-0.5f,-0.5f, 0.5f), DirectX::XMFLOAT3(  0,   0,   1),},
        {DirectX::XMFLOAT3(-0.5f, 0.5f,-0.5f), DirectX::XMFLOAT3(  0,   1,   0),},
        {DirectX::XMFLOAT3(-0.5f, 0.5f, 0.5f), DirectX::XMFLOAT3(  0,   1,   1),},

        {DirectX::XMFLOAT3( 0.5f,-0.5f,-0.5f), DirectX::XMFLOAT3(  1,   0,   0),},
        {DirectX::XMFLOAT3( 0.5f,-0.5f, 0.5f), DirectX::XMFLOAT3(  1,   0,   1),},
        {DirectX::XMFLOAT3( 0.5f, 0.5f,-0.5f), DirectX::XMFLOAT3(  1,   1,   0),},
        {DirectX::XMFLOAT3( 0.5f, 0.5f, 0.5f), DirectX::XMFLOAT3(  1,   1,   1),},
    };
    
    // Create vertex buffer:
    
    CD3D11_BUFFER_DESC vDesc(
        sizeof(CubeVertices),
        D3D11_BIND_VERTEX_BUFFER
        );

    D3D11_SUBRESOURCE_DATA vData;
    ZeroMemory(&vData, sizeof(D3D11_SUBRESOURCE_DATA));
    vData.pSysMem = CubeVertices;
    vData.SysMemPitch = 0;
    vData.SysMemSlicePitch = 0;

    hr = device->CreateBuffer(
        &vDesc,
        &vData,
        &m_pVertexBuffer
        );

    // Create index buffer:
    unsigned short CubeIndices [] = 
    {
        0,2,1, // -x
        1,2,3,

        4,5,6, // +x
        5,7,6,

        0,1,5, // -y
        0,5,4,

        2,6,7, // +y
        2,7,3,

        0,4,6, // -z
        0,6,2,

        1,3,7, // +z
        1,7,5,
    };

    m_indexCount = ARRAYSIZE(CubeIndices);

    CD3D11_BUFFER_DESC iDesc(
        sizeof(CubeIndices),
        D3D11_BIND_INDEX_BUFFER
        );

    D3D11_SUBRESOURCE_DATA iData;
    ZeroMemory(&iData, sizeof(D3D11_SUBRESOURCE_DATA));
    iData.pSysMem = CubeIndices;
    iData.SysMemPitch = 0;
    iData.SysMemSlicePitch = 0;
    
    hr = device->CreateBuffer(
        &iDesc,
        &iData,
        &m_pIndexBuffer
        );

    return hr;
}
```



<span data-ttu-id="ba607-161">Este exemplo não carrega malhas nem texturas.</span><span class="sxs-lookup"><span data-stu-id="ba607-161">This example does not load any meshes or textures.</span></span> <span data-ttu-id="ba607-162">Você deve criar os métodos para carregar os tipos de malha e de textura que são específicos para seu jogo e chamá-los de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="ba607-162">You must create the methods for loading the mesh and texture types that are specific to your game, and call them asynchronously.</span></span>

<span data-ttu-id="ba607-163">Preencha os valores iniciais para seus buffers de constante por cena aqui também.</span><span class="sxs-lookup"><span data-stu-id="ba607-163">Populate initial values for your per-scene constant buffers here, too.</span></span> <span data-ttu-id="ba607-164">Exemplos de buffer de constante por cena incluem luzes fixas ou outros dados e elementos de cena estáticos.</span><span class="sxs-lookup"><span data-stu-id="ba607-164">Examples of per-scene constant buffer include fixed lights, or other static scene elements and data.</span></span>

## <a name="implement-the-createwindowsizedependentresources-method"></a><span data-ttu-id="ba607-165">Implementar o método CreateWindowSizeDependentResources</span><span class="sxs-lookup"><span data-stu-id="ba607-165">Implement the CreateWindowSizeDependentResources method</span></span>

<span data-ttu-id="ba607-166">Os métodos **CreateWindowSizeDependentResources** são chamados toda vez que o tamanho da janela, a orientação ou as alterações de resolução.</span><span class="sxs-lookup"><span data-stu-id="ba607-166">**CreateWindowSizeDependentResources** methods are called every time the window size, orientation, or resolution changes.</span></span>

<span data-ttu-id="ba607-167">Os recursos de tamanho de janela são atualizados da seguinte forma: o procedimento de mensagem estática Obtém um dos vários eventos possíveis indicando uma alteração no estado da janela.</span><span class="sxs-lookup"><span data-stu-id="ba607-167">Window size resources are updated like so: The static message proc gets one of several possible events indicating a change in window state.</span></span> <span data-ttu-id="ba607-168">O loop principal é então informado sobre o evento e chama **CreateWindowSizeDependentResources** na instância da classe principal, que chama a implementação de **CreateWindowSizeDependentResources** na classe do renderizador de cena.</span><span class="sxs-lookup"><span data-stu-id="ba607-168">Your main loop is then informed about the event and calls **CreateWindowSizeDependentResources** on the main class instance, which then calls the **CreateWindowSizeDependentResources** implementation on the scene renderer class.</span></span>

<span data-ttu-id="ba607-169">O principal trabalho desse método é verificar se os objetos visuais não ficaram confusos ou se tornaram inválidos devido a uma alteração nas propriedades da janela.</span><span class="sxs-lookup"><span data-stu-id="ba607-169">The primary job of this method is to make sure the visuals don't become confused or invalid because of a change in window properties.</span></span> <span data-ttu-id="ba607-170">Neste exemplo, atualizamos as matrizes de projeto com um novo campo de exibição (FOV) para a janela redimensionada ou reorientada.</span><span class="sxs-lookup"><span data-stu-id="ba607-170">In this example, we update the project matrices with a new field of view (FOV) for the resized or reoriented window.</span></span>

<span data-ttu-id="ba607-171">Já vimos o código para a criação de recursos de janela em **DeviceResources** – que era a cadeia de permuta (com buffer de fundo) e a exibição de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="ba607-171">We already saw the code for creating window resources in **DeviceResources** - that was the swap chain (with back buffer) and render target view.</span></span> <span data-ttu-id="ba607-172">Veja como o renderizador cria transformações dependentes de taxa de proporção:</span><span class="sxs-lookup"><span data-stu-id="ba607-172">Here's how the renderer creates aspect ratio-dependent transforms:</span></span>


```C++
void Renderer::CreateViewAndPerspective()
{
    // Use DirectXMath to create view and perspective matrices.

    DirectX::XMVECTOR eye = DirectX::XMVectorSet(0.0f, 0.7f, 1.5f, 0.f);
    DirectX::XMVECTOR at  = DirectX::XMVectorSet(0.0f,-0.1f, 0.0f, 0.f);
    DirectX::XMVECTOR up  = DirectX::XMVectorSet(0.0f, 1.0f, 0.0f, 0.f);

    DirectX::XMStoreFloat4x4(
        &m_constantBufferData.view,
        DirectX::XMMatrixTranspose(
            DirectX::XMMatrixLookAtRH(
                eye,
                at,
                up
                )
            )
        );

    float aspectRatioX = m_deviceResources->GetAspectRatio();
    float aspectRatioY = aspectRatioX < (16.0f / 9.0f) ? aspectRatioX / (16.0f / 9.0f) : 1.0f;

    DirectX::XMStoreFloat4x4(
        &m_constantBufferData.projection,
        DirectX::XMMatrixTranspose(
            DirectX::XMMatrixPerspectiveFovRH(
                2.0f * std::atan(std::tan(DirectX::XMConvertToRadians(70) * 0.5f) / aspectRatioY),
                aspectRatioX,
                0.01f,
                100.0f
                )
            )
        );
}
```



<span data-ttu-id="ba607-173">Se sua cena tiver um layout específico de componentes que depende da taxa de proporção, esse é o lugar para reorganizá-los para corresponder a essa taxa de proporção.</span><span class="sxs-lookup"><span data-stu-id="ba607-173">If your scene has a specific layout of components that depends on the aspect ratio, this is the place to rearrange them to match that aspect ratio.</span></span> <span data-ttu-id="ba607-174">Você também pode querer alterar a configuração do comportamento de pós-processamento aqui.</span><span class="sxs-lookup"><span data-stu-id="ba607-174">You may want to change the configuration of post-processing behavior here also.</span></span>

## <a name="implement-the-update-method"></a><span data-ttu-id="ba607-175">Implementar o método Update</span><span class="sxs-lookup"><span data-stu-id="ba607-175">Implement the Update method</span></span>

<span data-ttu-id="ba607-176">O método **Update** é chamado uma vez por loop de jogo – neste exemplo, ele é chamado pelo método da classe principal do mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="ba607-176">The **Update** method is called once per game loop - in this example, it is called by the main class's method of the same name.</span></span> <span data-ttu-id="ba607-177">Ele tem uma finalidade simples: atualizar a geometria da cena e o estado do jogo com base na quantidade de tempo decorrido (ou etapas de tempo decorrido) desde o quadro anterior.</span><span class="sxs-lookup"><span data-stu-id="ba607-177">It has a simple purpose: update scene geometry and game state based on the amount of elapsed time (or elapsed time steps) since the previous frame.</span></span> <span data-ttu-id="ba607-178">Neste exemplo, simplesmente giramos o cubo uma vez por quadro.</span><span class="sxs-lookup"><span data-stu-id="ba607-178">In this example, we simply rotate the cube once per frame.</span></span> <span data-ttu-id="ba607-179">Em uma cena de jogo real, esse método contém muito mais código para verificar o estado do jogo, atualizar os buffers de constantes por quadro (ou outros), buffers de geometria e outros ativos na memória de acordo.</span><span class="sxs-lookup"><span data-stu-id="ba607-179">In a real game scene, this method contains a lot more code for checking game state, updating per-frame (or other dynamic) constant buffers, geometry buffers, and other in-memory assets accordingly.</span></span> <span data-ttu-id="ba607-180">Como a comunicação entre a CPU e a GPU incorre em sobrecarga, certifique-se de atualizar somente os buffers que foram realmente alterados desde o último quadro-seus buffers de constante podem ser agrupados ou divididos, conforme necessário para tornar isso mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="ba607-180">Since communication between the CPU and GPU incurs overhead, make sure you only update buffers that have actually changed since the last frame - your constant buffers can be grouped, or split up, as needed to make this more efficient.</span></span>


```C++
void Renderer::Update()
{
    // Rotate the cube 1 degree per frame.
    DirectX::XMStoreFloat4x4(
        &m_constantBufferData.world,
        DirectX::XMMatrixTranspose(
            DirectX::XMMatrixRotationY(
                DirectX::XMConvertToRadians(
                    (float) m_frameCount++
                    )
                )
            )
        );

    if (m_frameCount == MAXUINT)  m_frameCount = 0;
}
```



<span data-ttu-id="ba607-181">Nesse caso, a **rotação** atualiza o buffer constante com uma nova matriz de transformação para o cubo.</span><span class="sxs-lookup"><span data-stu-id="ba607-181">In this case, **Rotate** updates the constant buffer with a new transformation matrix for the cube.</span></span> <span data-ttu-id="ba607-182">A matriz será multiplicada por vértice durante o estágio do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="ba607-182">The matrix will be multiplied per-vertex during the vertex shader stage.</span></span> <span data-ttu-id="ba607-183">Como esse método é chamado com cada quadro, esse é um bom local para agregar todos os métodos que atualizam seus buffers de constantes e de vértice dinâmicos, ou para executar outras operações que preparam os objetos na cena para transformação pelo pipeline de gráficos.</span><span class="sxs-lookup"><span data-stu-id="ba607-183">Since this method is called with every frame, this is a good place to aggregate any methods that update your dynamic constant and vertex buffers, or to perform any other operations that prepare the objects in the scene for transformation by the graphics pipeline.</span></span>

## <a name="implement-the-render-method"></a><span data-ttu-id="ba607-184">Implementar o método Render</span><span class="sxs-lookup"><span data-stu-id="ba607-184">Implement the Render method</span></span>

<span data-ttu-id="ba607-185">Esse método é chamado uma vez por loop de jogo depois de chamar **Update**.</span><span class="sxs-lookup"><span data-stu-id="ba607-185">This method is called once per game loop after calling **Update**.</span></span> <span data-ttu-id="ba607-186">Como **Update**, o método **render** também é chamado a partir da classe principal.</span><span class="sxs-lookup"><span data-stu-id="ba607-186">Like **Update**, the **Render** method is also called from the main class.</span></span> <span data-ttu-id="ba607-187">Esse é o método em que o pipeline de gráficos é construído e processado para o quadro usando métodos na instância [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) .</span><span class="sxs-lookup"><span data-stu-id="ba607-187">This is the method where the graphics pipeline is constructed and processed for the frame using methods on the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) instance.</span></span> <span data-ttu-id="ba607-188">Isso culmina em uma chamada final para [**ID3D11DeviceContext::D rawindexed**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed).</span><span class="sxs-lookup"><span data-stu-id="ba607-188">This culminates in a final call to [**ID3D11DeviceContext::DrawIndexed**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed).</span></span> <span data-ttu-id="ba607-189">É importante entender que essa chamada (ou outras **chamadas Draw _ semelhantes \* *definidas em _* ID3D11DeviceContext**) realmente executa o pipeline.</span><span class="sxs-lookup"><span data-stu-id="ba607-189">It’s important to understand that this call (or other similar \**Draw\**_ calls defined on _\* ID3D11DeviceContext\*\*) actually executes the pipeline.</span></span> <span data-ttu-id="ba607-190">Especificamente, isso ocorre quando o Direct3D se comunica com a GPU para definir o estado do desenho, executa cada estágio do pipeline e grava os resultados do pixel no recurso de buffer de destino de renderização para exibição pela cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="ba607-190">Specifically, this is when Direct3D communicates with the GPU to set drawing state, runs each pipeline stage, and writes the pixel results into the render-target buffer resource for display by the swap chain.</span></span> <span data-ttu-id="ba607-191">Como a comunicação entre a CPU e a GPU incorre em sobrecarga, combine várias chamadas de desenho em uma única se você puder, especialmente se sua cena tiver muitos objetos renderizados.</span><span class="sxs-lookup"><span data-stu-id="ba607-191">Since communication between the CPU and GPU incurs overhead, combine multiple draw calls into a single one if you can, especially if your scene has a lot of rendered objects.</span></span>


```C++
void Renderer::Render()
{
    // Use the Direct3D device context to draw.
    ID3D11DeviceContext* context = m_deviceResources->GetDeviceContext();

    ID3D11RenderTargetView* renderTarget = m_deviceResources->GetRenderTarget();
    ID3D11DepthStencilView* depthStencil = m_deviceResources->GetDepthStencil();

    context->UpdateSubresource(
        m_pConstantBuffer.Get(),
        0,
        nullptr,
        &m_constantBufferData,
        0,
        0
        );

    // Clear the render target and the z-buffer.
    const float teal [] = { 0.098f, 0.439f, 0.439f, 1.000f };
    context->ClearRenderTargetView(
        renderTarget,
        teal
        );
    context->ClearDepthStencilView(
        depthStencil,
        D3D11_CLEAR_DEPTH | D3D11_CLEAR_STENCIL,
        1.0f,
        0);

    // Set the render target.
    context->OMSetRenderTargets(
        1,
        &renderTarget,
        depthStencil
        );

    // Set up the IA stage by setting the input topology and layout.
    UINT stride = sizeof(VertexPositionColor);
    UINT offset = 0;

    context->IASetVertexBuffers(
        0,
        1,
        m_pVertexBuffer.GetAddressOf(),
        &stride,
        &offset
        );

    context->IASetIndexBuffer(
        m_pIndexBuffer.Get(),
        DXGI_FORMAT_R16_UINT,
        0
        );
    
    context->IASetPrimitiveTopology(
        D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST
        );

    context->IASetInputLayout(m_pInputLayout.Get());

    // Set up the vertex shader stage.
    context->VSSetShader(
        m_pVertexShader.Get(),
        nullptr,
        0
        );

    context->VSSetConstantBuffers(
        0,
        1,
        m_pConstantBuffer.GetAddressOf()
        );

    // Set up the pixel shader stage.
    context->PSSetShader(
        m_pPixelShader.Get(),
        nullptr,
        0
        );

    // Calling Draw tells Direct3D to start sending commands to the graphics device.
    context->DrawIndexed(
        m_indexCount,
        0,
        0
        );
}
```



<span data-ttu-id="ba607-192">É uma boa prática definir os vários estágios de pipeline de gráficos no contexto na ordem.</span><span class="sxs-lookup"><span data-stu-id="ba607-192">It's good practice to set the various graphics pipeline stages on the context in order.</span></span> <span data-ttu-id="ba607-193">Normalmente, a ordem é:</span><span class="sxs-lookup"><span data-stu-id="ba607-193">Typically, the order is:</span></span>

-   <span data-ttu-id="ba607-194">Atualize os recursos de buffer constante com novos dados conforme necessário (usando dados da **atualização**).</span><span class="sxs-lookup"><span data-stu-id="ba607-194">Refresh constant buffer resources with new data as needed (using data from **Update**).</span></span>
-   <span data-ttu-id="ba607-195">Assembly de entrada (IA): é aqui que anexamos os buffers de vértice e de índice que definem a geometria da cena.</span><span class="sxs-lookup"><span data-stu-id="ba607-195">Input assembly (IA): This is where we attach the vertex and index buffers that define the scene geometry.</span></span> <span data-ttu-id="ba607-196">Você precisa anexar cada vértice e buffer de índice para cada objeto na cena.</span><span class="sxs-lookup"><span data-stu-id="ba607-196">You need to attach each vertex and index buffer for each object in the scene.</span></span> <span data-ttu-id="ba607-197">Como este exemplo tem apenas o cubo, ele é muito simples.</span><span class="sxs-lookup"><span data-stu-id="ba607-197">Because this example has just the cube, it's pretty simple.</span></span>
-   <span data-ttu-id="ba607-198">Sombreador de vértice (VS): Anexe qualquer sombreador de vértice que transforme os dados nos buffers de vértice e anexe buffers de constantes para o sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="ba607-198">Vertex shader (VS): Attach any vertex shaders that will transform the data in the vertex buffers, and attach constant buffers for the vertex shader.</span></span>
-   <span data-ttu-id="ba607-199">Sombreador de pixel (PS): Anexe qualquer sombreador de pixel que executará operações por pixel na cena rasterizada e anexe recursos de dispositivo para o sombreador de pixel (buffers de constantes, texturas e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="ba607-199">Pixel shader (PS): Attach any pixel shaders that will perform per-pixel operations in the rasterized scene, and attach device resources for the pixel shader (constant buffers, textures, and so on).</span></span>
-   <span data-ttu-id="ba607-200">Fusão de saída (OM): esse é o estágio em que os pixels são mesclados, depois que os sombreadores são concluídos.</span><span class="sxs-lookup"><span data-stu-id="ba607-200">Output merger (OM): This is the stage where pixels are blended, after the shaders are finished.</span></span> <span data-ttu-id="ba607-201">Essa é uma exceção à regra, pois você anexa seus estênceis de profundidade e renderiza destinos antes de definir qualquer uma das outras etapas.</span><span class="sxs-lookup"><span data-stu-id="ba607-201">This is an exception to the rule, because you attach your depth stencils and render targets before setting any of the other stages.</span></span> <span data-ttu-id="ba607-202">Você poderá ter vários estênceis e destinos se tiver um vértice adicional e sombreadores de pixel que gerem texturas como mapas de sombra, mapas de altura ou outras técnicas de amostragem. nesse caso, cada passagem de desenho precisará do conjunto de destino apropriado antes de chamar uma função de desenho.</span><span class="sxs-lookup"><span data-stu-id="ba607-202">You may have multiple stencils and targets if you have additional vertex and pixel shaders that generate textures such as shadow maps, height maps, or other sampling techniques - in this case, each drawing pass will need the appropriate target(s) set before you call a draw function.</span></span>

<span data-ttu-id="ba607-203">Em seguida, na seção final ([trabalhar com sombreadores e recursos de sombreador](work-with-shaders-and-shader-resources.md)), vamos examinar os sombreadores e discutir como o Direct3D os executa.</span><span class="sxs-lookup"><span data-stu-id="ba607-203">Next, in the final section ([Work with shaders and shader resources](work-with-shaders-and-shader-resources.md)), we'll look at the shaders and discuss how Direct3D executes them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba607-204">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ba607-204">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ba607-205">**A seguir**</span><span class="sxs-lookup"><span data-stu-id="ba607-205">**Up next**</span></span>
</dt> <dt>

[<span data-ttu-id="ba607-206">Trabalhar com sombreadores e recursos de sombreador</span><span class="sxs-lookup"><span data-stu-id="ba607-206">Work with shaders and shader resources</span></span>](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 
