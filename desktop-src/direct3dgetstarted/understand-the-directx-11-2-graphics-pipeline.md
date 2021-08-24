---
title: Entender o pipeline de renderização do Direct3D 11
description: Anteriormente, você viu como criar uma janela que pode ser usada para desenhar em Trabalhar com recursos de dispositivo DirectX. Agora, você aprenderá a criar o pipeline de gráficos e onde você pode se conectar a ele.
ms.assetid: 73cf62d0-7e4f-4e93-aa65-12741588d4fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41a3e0fa7e3f7775c5cd51d49f9867864e7a204975fd982565491a63db829aa7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119727516"
---
# <a name="understand-the-direct3d-11-rendering-pipeline"></a>Entender o pipeline de renderização do Direct3D 11

Anteriormente, você analisou como criar uma janela que pode ser usada para desenhar em [Trabalhar com recursos do dispositivo DirectX.](work-with-dxgi.md) Agora, você aprenderá a criar o pipeline de gráficos e onde você pode se conectar a ele.

Você se lembrará de que há duas interfaces Direct3D que definem o pipeline de gráficos: [**ID3D11Device,**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2)que fornece uma representação virtual da GPU e seus recursos; e [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2), que representa o processamento de gráficos para o pipeline. Normalmente, você usa uma instância de **ID3D11Device** para configurar e obter os recursos de GPU necessários para começar a processar os gráficos em uma cena e usa **ID3D11DeviceContext** para processar esses recursos em cada estágio de sombreador apropriado no pipeline de gráficos. Normalmente, você chama **métodos ID3D11Device** com pouca pouca segurança, ou seja, somente quando você configura uma cena ou quando o dispositivo muda. Por outro lado, você chamará **ID3D11DeviceContext** sempre que processar um quadro para exibição.

Este exemplo cria e configura um pipeline de gráficos mínimo adequado para exibir um cubo simples com sombreamento de vértice. Ele demonstra aproximadamente o menor conjunto de recursos necessários para exibição. Conforme você lê as informações aqui, observe as limitações do exemplo determinado em que talvez seja necessário estendá-lo para dar suporte à cena que deseja renderizar.

Este exemplo aborda duas classes C++ para gráficos: uma classe do gerenciador de recursos de dispositivo e uma classe de renderização de cena 3D. Este tópico se concentra especificamente no renderador de cena 3D.

## <a name="what-does-the-cube-renderer-do"></a>O que o renderador de cubo faz?

O pipeline de gráficos é definido pela classe de renderização de cena 3D. O renderdor de cena é capaz de:

-   Defina buffers constantes para armazenar seus dados uniformes.
-   Defina buffers de vértice para manter os dados de vértice do objeto e buffers de índice correspondentes para permitir que o sombreador de vértice ande corretamente nos triângulos.
-   Crie recursos de textura e exibições de recursos.
-   Carregue seus objetos de sombreador.
-   Atualize os dados gráficos para exibir cada quadro.
-   Renderizar (desenhar) os gráficos para a cadeia de permuta.

Os primeiros quatro processos normalmente usam os métodos de interface [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) para inicializar e gerenciar recursos gráficos, e os dois últimos usam os métodos de interface [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) para gerenciar e executar o pipeline gráfico.

Uma instância da classe **Renderer** é criada e gerenciada como uma variável de membro na classe de projeto principal. A **instância DeviceResources** é gerenciada como um ponteiro compartilhado em várias classes, incluindo a classe de projeto principal, a classe **App** view-provider e **o Renderer**. Se você substituir **Renderer** por sua própria classe, considere declarar e atribuir a instância **DeviceResources** como um membro de ponteiro compartilhado também:

`std::shared_ptr<DX::DeviceResources> m_deviceResources;`

Basta passar o ponteiro para o construtor de classe (ou outro método de inicialização) depois que a instância **DeviceResources** for criada no método **Initialize** da **classe App.** Você também pode passar uma **referência \_ ptr** fraca se, em vez disso, você quiser que sua classe principal seja completamente a propriedade da **instância DeviceResources.**

## <a name="create-the-cube-renderer"></a>Criar o renderador de cubo

Neste exemplo, organizamos a classe do renderador de cena com os seguintes métodos:

-   **CreateDeviceDependentResources:** chamado sempre que a cena deve ser inicializada ou reiniciada. Esse método carrega seus dados iniciais de vértice, texturas, sombreadores e outros recursos e constrói a constante inicial e os buffers de vértice. Normalmente, a maioria do trabalho aqui é feita com métodos [**ID3D11Device,**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) não métodos [**ID3D11DeviceContext.**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2)
-   **CreateWindowSizeDependentResources:** chamado sempre que o estado da janela muda, como quando ocorre o resizing ou quando a orientação é muda. Esse método recria matrizes de transformação, como aquelas para sua câmera.
-   **Atualização:** normalmente chamado da parte do programa que gerencia o estado imediato do jogo; neste exemplo, basta chamá-lo da **classe** Main. Fazer com que esse método leia de qualquer informação de estado do jogo que afete a renderização, como atualizações para a posição do objeto ou quadros de animação, além de quaisquer dados globais do jogo, como níveis de luz ou alterações na física do jogo. Essas entradas são usadas para atualizar os buffers constantes por quadro e os dados do objeto.
-   **Renderizar**: normalmente chamado da parte do programa que gerencia o loop do jogo; nesse caso, ele é chamado da **classe Main.** Esse método constrói o pipeline gráfico: ele vincula sombreadores, vincula buffers e recursos aos estágios do sombreador e invoca o desenho para o quadro atual.

Esses métodos compõem o corpo dos comportamentos para renderizar uma cena com o Direct3D usando seus ativos. Se você estender este exemplo com uma nova classe de renderização, declare-o na classe de projeto principal. Portanto, isso:

`std::unique_ptr<Sample3DSceneRenderer> m_sceneRenderer;`

se torna isso:

`std::unique_ptr<MyAwesomeNewSceneRenderer> m_sceneRenderer;`

Novamente, observe que este exemplo presume que os métodos têm as mesmas assinaturas em sua implementação. Se as assinaturas foram alteradas, revise o loop **Principal** e faça as alterações de acordo.

Vamos dar uma olhada nos métodos de renderização de cena mais detalhadamente.

## <a name="create-device-dependent-resources"></a>Criar recursos dependentes do dispositivo

**CreateDeviceDependentResources** consolida todas as operações para inicializar a cena e seus recursos usando [**chamadas ID3D11Device.**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) Esse método presume que o dispositivo Direct3D acabou de ser inicializado (ou foi recriado) para uma cena. Ele recria ou recarrega todos os recursos gráficos específicos da cena, como os sombreadores de vértice e pixel, o vértice e os buffers de índice para objetos e quaisquer outros recursos (por exemplo, como texturas e suas exibições correspondentes).

Aqui está o código de exemplo **para CreateDeviceDependentResources:**


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



Sempre que você carregar recursos do disco , recursos como arquivos ou texturas do objeto de sombreador compilado (CSO ou .cso), faça isso de forma assíncrona. Isso permite que você mantenha outros trabalhos ao mesmo tempo (como outras tarefas de instalação) e, como o loop principal não está bloqueado, você pode continuar exibindo algo visualmente interessante para o usuário (como uma animação de carregamento para seu jogo). Este exemplo usa a API Concurrency::Tasks que está disponível a partir do Windows 8; observe a sintaxe lambda usada para encapsular tarefas de carregamento assíncrono. Esses lambdas representam as funções chamadas off-thread, portanto, um ponteiro para o objeto de classe atual (**este**) é capturado explicitamente.

Aqui está um exemplo de como você pode carregar o código de byte do sombreador:


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



Veja um exemplo de como criar buffers de vértice e índice:


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



Este exemplo não carrega malhas ou texturas. Você deve criar os métodos para carregar os tipos de malha e textura específicos ao seu jogo e chamá-los de forma assíncrona.

Preencha os valores iniciais para seus buffers constantes por cena aqui também. Exemplos de buffer constante por cena incluem luzes fixas ou outros elementos e dados de cena estáticos.

## <a name="implement-the-createwindowsizedependentresources-method"></a>Implementar o método CreateWindowSizeDependentResources

**Os métodos CreateWindowSizeDependentResources** são chamados sempre que o tamanho da janela, a orientação ou a resolução são alterações.

Os recursos de tamanho da janela são atualizados da seguinte forma: o proc de mensagem estática obtém um dos vários eventos possíveis que indicam uma alteração no estado da janela. Em seguida, o loop principal é informado sobre o evento e chama **CreateWindowSizeDependentResources** na instância da classe principal, que chama a implementação **CreateWindowSizeDependentResources** na classe do renderador de cena.

O principal trabalho desse método é verificar se os objetos visuais não ficaram confusos ou se tornaram inválidos devido a uma alteração nas propriedades da janela. Neste exemplo, atualizamos as matrizes do projeto com um novo FOV (campo de exibição) para a janela ressalvada ou reorientada.

Já vimos o código para criar recursos de janela em **DeviceResources** – que era a cadeia de permuta (com buffer de fundo) e a exibição de destino de renderização. Veja como o renderista cria as transformação dependentes da taxa de proporção:


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



Se sua cena tiver um layout específico de componentes que dependem da taxa de proporção, esse é o lugar para reorganizar para corresponder a essa taxa de proporção. Talvez você queira alterar a configuração do comportamento pós-processamento aqui também.

## <a name="implement-the-update-method"></a>Implementar o método Update

O **método Update** é chamado uma vez por loop de jogo – neste exemplo, ele é chamado pelo método da classe principal com o mesmo nome. Ele tem uma finalidade simples: atualizar a geometria da cena e o estado do jogo com base na quantidade de tempo decorrido (ou etapas de tempo decorrido) desde o quadro anterior. Neste exemplo, simplesmente giramos o cubo uma vez por quadro. Em uma cena de jogo real, esse método contém muito mais código para verificar o estado do jogo, atualizar buffers constantes por quadro (ou outros dinâmicos), buffers geometry e outros ativos na memória de acordo. Como a comunicação entre a CPU e a GPU incorre em sobrecarga, certifique-se de atualizar apenas os buffers que realmente foram alterados desde o último quadro– seus buffers constantes podem ser agrupados ou divididos, conforme necessário para tornar isso mais eficiente.


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



Nesse **caso,** Girar atualiza o buffer constante com uma nova matriz de transformação para o cubo. A matriz será multiplicada por vértice durante o estágio do sombreador de vértice. Como esse método é chamado a cada quadro, esse é um bom lugar para agregar quaisquer métodos que atualizem sua constante dinâmica e buffers de vértice ou para executar qualquer outra operação que prepare os objetos na cena para transformação pelo pipeline de gráficos.

## <a name="implement-the-render-method"></a>Implementar o método Render

Esse método é chamado uma vez por loop de jogo depois de chamar **Atualizar**. Como **Update**, o **método Render** também é chamado da classe principal. Esse é o método em que o pipeline de gráficos é construído e processado para o quadro usando métodos na [**instância ID3D11DeviceContext.**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) Isso desinteia em uma chamada final [**para ID3D11DeviceContext::D rawIndexed.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-drawindexed) É importante entender que essa chamada (ou outras chamadas draw _ semelhantes definidas em **\* *_* ID3D11DeviceContext**) realmente executa o pipeline. Especificamente, é quando o Direct3D se comunica com a GPU para definir o estado de desenho, executa cada estágio de pipeline e grava os resultados de pixel no recurso de buffer de destino de renderização para exibição pela cadeia de permuta. Como a comunicação entre a CPU e a GPU incorre em sobrecarga, combine várias chamadas de desenho em uma única, se possível, especialmente se a cena tiver muitos objetos renderizados.


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



É uma boa prática definir os vários estágios de pipeline de gráficos no contexto em ordem. Normalmente, a ordem é:

-   Atualize os recursos de buffer constante com novos dados conforme necessário (usando dados de **Atualização**).
-   IA (assembly de entrada): é aqui que anexamos o vértice e os buffers de índice que definem a geometria da cena. Você precisa anexar cada vértice e buffer de índice para cada objeto na cena. Como este exemplo tem apenas o cubo, é muito simples.
-   VS (sombreador de vértice): anexe todos os sombreadores de vértice que transformarão os dados nos buffers de vértice e anexam buffers constantes para o sombreador de vértice.
-   Sombreador de pixel (PS): anexe todos os sombreadores de pixel que executarão operações por pixel na cena rasterizada e anexe recursos do dispositivo para o sombreador de pixel (buffers constantes, texturas e assim por diante).
-   OM (fusão de saída): esse é o estágio em que os pixels são mesclados, depois que os sombreadores são concluídos. Essa é uma exceção à regra, pois você anexa seus estênciles de profundidade e renderiza destinos antes de definir qualquer um dos outros estágios. Você poderá ter vários estêncils e destinos se tiver sombreadores de vértice e pixel adicionais que geram texturas como mapas de sombra, mapas de altura ou outras técnicas de amostragem– nesse caso, cada passagem de desenho precisará dos destinos apropriados definidos antes de chamar uma função de desenho.

Em seguida, na seção final[(](work-with-shaders-and-shader-resources.md)Trabalhar com sombreadores e recursos de sombreador ), vamos ver os sombreadores e discutir como o Direct3D os executa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**A seguir**
</dt> <dt>

[Trabalhar com sombreadores e recursos de sombreador](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 
