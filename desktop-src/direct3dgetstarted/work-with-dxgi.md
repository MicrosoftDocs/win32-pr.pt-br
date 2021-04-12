---
title: Trabalhar com recursos do dispositivo DirectX
description: Entenda a função da Microsoft DirectX Graphics Infrastructure (DXGI) no seu jogo DirectX da Windows Store.
ms.assetid: 24c0c81d-6b55-4116-868a-154addf0f04c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 096e2be6f957d99bc6e5055f845c14448ecd647f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454170"
---
# <a name="work-with-directx-device-resources"></a>Trabalhar com recursos do dispositivo DirectX

Entenda a função da Microsoft DirectX Graphics Infrastructure (DXGI) no seu jogo DirectX da Windows Store. DXGI é um conjunto de APIs usado para configurar e gerenciar gráficos de baixo nível e recursos de adaptador gráfico. Sem ele, você não teria como desenhar os elementos gráficos de seu jogo em uma janela.

Considere o DXGI desta forma: para acessar diretamente a GPU e gerenciar seus recursos, você deve ter uma maneira de descrevê-la em seu aplicativo. A informação mais importante que você precisa sobre a GPU é o lugar para desenhar pixels para que possa enviar esses pixels para a tela. Normalmente, isso é chamado de "buffer de fundo" — um local na memória GPU em que você pode desenhar os pixels e, em seguida, fazer com que ele seja "invertido" ou "trocado" e enviado à tela em um sinal de atualização. DXGI permite que você adquira esse local e os meios para usar esse buffer (chamado de *cadeia de permuta* porque ele é uma cadeia de buffers intercambiáveis, permitindo várias estratégias de buffer).

Para fazer isso, você precisa ter acesso para gravar na cadeia de permuta e um identificador para a janela que exibirá o buffer de fundo atual da cadeia de permuta. Você também precisa conectar os dois para garantir que o sistema operacional atualizará a janela com o conteúdo do buffer de fundo quando solicitá-la.

O processo geral para desenhar na tela é o seguinte:

-   Obtenha um [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) para seu aplicativo.
-   Obtenha uma interface para o dispositivo e o contexto do Direct3D.
-   Crie a cadeia de permuta para exibir a imagem renderizada no [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).
-   Crie um destino de renderização para desenhar e preencha-o com pixels.
-   Apresente a cadeia de permuta!

## <a name="create-a-window-for-your-app"></a>Criar uma janela para seu aplicativo

A primeira coisa que precisamos fazer é criar uma janela. Primeiro, crie uma classe de janela populando uma instância de [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)e, em seguida, registre-a usando [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa). A classe Window contém as propriedades essenciais da janela, incluindo o ícone que ela usa, a função estática de processamento de mensagens (mais informações sobre isso posteriormente) e um nome exclusivo para a classe Window.


```C++
if(m_hInstance == NULL) 
    m_hInstance = (HINSTANCE)GetModuleHandle(NULL);

HICON hIcon = NULL;
WCHAR szExePath[MAX_PATH];
    GetModuleFileName(NULL, szExePath, MAX_PATH);

// If the icon is NULL, then use the first one found in the exe
if(hIcon == NULL)
    hIcon = ExtractIcon(m_hInstance, szExePath, 0); 

// Register the windows class
WNDCLASS wndClass;
wndClass.style = CS_DBLCLKS;
wndClass.lpfnWndProc = MainClass::StaticWindowProc;
wndClass.cbClsExtra = 0;
wndClass.cbWndExtra = 0;
wndClass.hInstance = m_hInstance;
wndClass.hIcon = hIcon;
wndClass.hCursor = LoadCursor(NULL, IDC_ARROW);
wndClass.hbrBackground = (HBRUSH)GetStockObject(BLACK_BRUSH);
wndClass.lpszMenuName = NULL;
wndClass.lpszClassName = m_windowClassName.c_str();

if(!RegisterClass(&wndClass))
{
    DWORD dwError = GetLastError();
    if(dwError != ERROR_CLASS_ALREADY_EXISTS)
        return HRESULT_FROM_WIN32(dwError);
}
```



Em seguida, você cria a janela. Também precisamos fornecer informações de tamanho para a janela e o nome da classe de janela que acabamos de criar. Ao chamar [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa), você obtém um ponteiro opaco para a janela chamada HWND; Você precisará manter o ponteiro do HWND e usá-lo sempre que precisar fazer referência à janela, incluindo destruir ou recriá-la, e (especialmente importante) ao criar a cadeia de permuta DXGI usada para desenhar na janela.


```C++
m_rc;
int x = CW_USEDEFAULT;
int y = CW_USEDEFAULT;

// No menu in this example.
m_hMenu = NULL;

// This example uses a non-resizable 640 by 480 viewport for simplicity.
int nDefaultWidth = 640;
int nDefaultHeight = 480;
SetRect(&m_rc, 0, 0, nDefaultWidth, nDefaultHeight);        
AdjustWindowRect(
    &m_rc,
    WS_OVERLAPPEDWINDOW,
    (m_hMenu != NULL) ? true : false
    );

// Create the window for our viewport.
m_hWnd = CreateWindow(
    m_windowClassName.c_str(),
    L"Cube11",
    WS_OVERLAPPEDWINDOW,
    x, y,
    (m_rc.right-m_rc.left), (m_rc.bottom-m_rc.top),
    0,
    m_hMenu,
    m_hInstance,
    0
    );

if(m_hWnd == NULL)
{
    DWORD dwError = GetLastError();
    return HRESULT_FROM_WIN32(dwError);
}
```



O modelo de aplicativo da área de trabalho do Windows inclui um gancho no loop de mensagem do Windows. Você precisará basear o loop do programa principal desse gancho escrevendo uma função "StaticWindowProc" para processar eventos de janela. Essa deve ser uma função estática, pois o Windows a chamará fora do contexto de qualquer instância de classe. Veja um exemplo muito simples de uma função de processamento de mensagem estática.


```C++
LRESULT CALLBACK MainClass::StaticWindowProc(
    HWND hWnd,
    UINT uMsg,
    WPARAM wParam,
    LPARAM lParam
    )
{
    switch(uMsg)
    {
        case WM_CLOSE:
        {
            HMENU hMenu;
            hMenu = GetMenu(hWnd);
            if (hMenu != NULL)
            {
                DestroyMenu(hMenu);
            }
            DestroyWindow(hWnd);
            UnregisterClass(
                m_windowClassName.c_str(),
                m_hInstance
                );
            return 0;
        }

        case WM_DESTROY:
            PostQuitMessage(0);
            break;
    }
    
    return DefWindowProc(hWnd, uMsg, wParam, lParam);
}
```



Este exemplo simples verifica apenas as condições de saída do programa: [**WM \_ Close**](/windows/desktop/winmsg/wm-close), enviado quando a janela é solicitada para ser fechada e o [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy), que é enviado depois que a janela é realmente removida da tela. Um aplicativo de produção completo também precisa lidar com outros eventos de janela — para obter a lista completa de eventos de janela, consulte [notificações de janela](/windows/desktop/winmsg/window-notifications).

O próprio loop do programa principal precisa reconhecer mensagens do Windows, permitindo ao Windows a oportunidade de executar o processo de mensagem estático. Ajude o programa a ser executado com eficiência com a bifurcação do comportamento: cada iteração deve optar por processar novas mensagens do Windows, se estiverem disponíveis, e se nenhuma mensagem estiver na fila, ela deverá renderizar um novo quadro. Veja um exemplo muito simples:


```C++
bool bGotMsg;
MSG  msg;
msg.message = WM_NULL;
PeekMessage(&msg, NULL, 0U, 0U, PM_NOREMOVE);

while (WM_QUIT != msg.message)
{
    // Process window events.
    // Use PeekMessage() so we can use idle time to render the scene. 
    bGotMsg = (PeekMessage(&msg, NULL, 0U, 0U, PM_REMOVE) != 0);

    if (bGotMsg)
    {
        // Translate and dispatch the message
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }
    else
    {
        // Update the scene.
        renderer->Update();

        // Render frames during idle time (when no messages are waiting).
        renderer->Render();

        // Present the frame to the screen.
        deviceResources->Present();
    }
}
```



## <a name="get-an-interface-for-the-direct3d-device-and-context"></a>Obter uma interface para o dispositivo e contexto do Direct3D

A primeira etapa para usar o Direct3D é adquirir uma interface para o hardware do Direct3D (a GPU), representada como instâncias de [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) e [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2). O primeiro é uma representação virtual dos recursos de GPU, e o último é uma abstração independente de dispositivo do pipeline de renderização e do processo. Aqui está uma maneira fácil de considerar: **ID3D11Device** contém os métodos gráficos que você chama com pouca frequência, geralmente antes que qualquer renderização ocorra, para adquirir e configurar o conjunto de recursos de que você precisa para começar a desenhar pixels. **ID3D11DeviceContext**, por outro lado, contém os métodos que você chama a cada quadro: carregando em buffers e exibições e outros recursos, alterando o estado de mesclagem de saída e rasterizador, gerenciando sombreadores e desenhando os resultados da passagem desses recursos por meio de Estados e sombreadores.

Há uma parte muito importante desse processo: definir o nível de recurso. O nível de recurso informa ao DirectX o nível mínimo de hardware com suporte do seu aplicativo, com o nível de recurso do D3D \_ \_ \_ 9 \_ 1 como o menor conjunto de recursos e o \_ \_ nível \_ de recurso do D3D 11 \_ 1 como o mais alto atual. Você deve dar suporte a 9 \_ 1 como o mínimo se quiser alcançar o público mais amplo possível. Reserve algum tempo para ler os níveis de [recursos](/previous-versions/windows/apps/hh994923(v=win.10)) do Direct3D e avaliar os níveis mínimo e máximo de recursos que você deseja que seu jogo dê suporte e entenda as implicações de sua escolha.

Obtenha referências (ponteiros) para o dispositivo Direct3D e o contexto do dispositivo e armazene-os como variáveis de nível de classe na instância **DeviceResources** (como apontadores inteligentes **ComPtr** ). Use essas referências sempre que precisar acessar o dispositivo Direct3D ou o contexto do dispositivo.


```C++
D3D_FEATURE_LEVEL levels[] = {
    D3D_FEATURE_LEVEL_9_1,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_11_1
};

// This flag adds support for surfaces with a color-channel ordering different
// from the API default. It is required for compatibility with Direct2D.
UINT deviceFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;

#if defined(DEBUG) || defined(_DEBUG)
deviceFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif

// Create the Direct3D 11 API device object and a corresponding context.
Microsoft::WRL::ComPtr<ID3D11Device>        device;
Microsoft::WRL::ComPtr<ID3D11DeviceContext> context;

hr = D3D11CreateDevice(
    nullptr,                    // Specify nullptr to use the default adapter.
    D3D_DRIVER_TYPE_HARDWARE,   // Create a device using the hardware graphics driver.
    0,                          // Should be 0 unless the driver is D3D_DRIVER_TYPE_SOFTWARE.
    deviceFlags,                // Set debug and Direct2D compatibility flags.
    levels,                     // List of feature levels this app can support.
    ARRAYSIZE(levels),          // Size of the list above.
    D3D11_SDK_VERSION,          // Always set this to D3D11_SDK_VERSION for Windows Store apps.
    &device,                    // Returns the Direct3D device created.
    &m_featureLevel,            // Returns feature level of device created.
    &context                    // Returns the device immediate context.
    );

if (FAILED(hr))
{
    // Handle device interface creation failure if it occurs.
    // For example, reduce the feature level requirement, or fail over 
    // to WARP rendering.
}

// Store pointers to the Direct3D 11.1 API device and immediate context.
device.As(&m_pd3dDevice);
context.As(&m_pd3dDeviceContext);
```



## <a name="create-the-swap-chain"></a>Criar a cadeia de permuta

Ok: você tem uma janela para desenhar e tem uma interface para enviar dados e fornecer comandos para a GPU. Agora, vamos ver como reuni-los.

Primeiro, você informa ao DXGI quais valores usar para as propriedades da cadeia de permuta. Faça isso usando uma [**estrutura \_ \_ \_ desc de cadeia de permuta dxgi**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) . Seis campos são particularmente importantes para aplicativos da área de trabalho:

-   Em **janela**: indica se a cadeia de permuta é de tela inteira ou recortada na janela. Defina como TRUE para colocar a cadeia de permuta na janela que você criou anteriormente.
-   **BufferUsage**: Defina isso como saída de destino de renderização de uso de dxgi \_ \_ \_ \_ . Isso indica que a cadeia de permuta será uma superfície de desenho, permitindo que você a use como um destino de processamento Direct3D.
-   **SwapEffect**: Defina isso como efeito de permuta de dxgi \_ \_ \_ inverter \_ sequencial.
-   **Formato**: o formato \_ dxgi \_ B8G8R8A8 \_ UNORM format especifica a cor de 32 bits: 8 bits para cada um dos três canais de cores RGB e 8 bits para o canal alfa.
-   **BufferCount**: Defina isso como 2 para um comportamento de buffer duplo tradicional para evitar a subdivisão. Defina a contagem de buffer como 3 se o seu conteúdo de gráficos levar mais de um ciclo de atualização de monitor para renderizar um único quadro (a 60 Hz, por exemplo, o limite é maior que 16 MS).
-   **SampleDesc**: Este campo controla a multiamostragem. Defina **contagem** como 1 e **qualidade** como 0 para cadeias de permuta de flip-Model. (Para usar multiamostragens com cadeias de permuta de flip-Model, desenhe em um destino de renderização multiamostrado separado e, em seguida, resolva esse destino para a cadeia de permuta antes de apresentá-lo. O código de exemplo é fornecido em [multiamostrar em aplicativos da Windows Store](/previous-versions/windows/apps/dn458384(v=win.10)).)

Depois de especificar uma configuração para a cadeia de permuta, você deve usar a mesma fábrica de DXGI que criou o dispositivo Direct3D (e o contexto do dispositivo) para criar a cadeia de permuta.

**Forma abreviada:  **

Obtenha a referência de [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) que você criou anteriormente. Converta-o em [**IDXGIDevice3**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3) (se você ainda não tiver feito isso) e, em seguida, chame [**IDXGIDevice:: getadapter**](/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter) para adquirir o adaptador dxgi. Obtenha a fábrica pai para esse adaptador chamando [**IDXGIFactory2:: GetParent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent) ([**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) Inherits from [**IDXGIObject**](/windows/desktop/api/dxgi/nn-dxgi-idxgiobject)) – agora você pode usar essa fábrica para criar a cadeia de permuta chamando [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), como visto no exemplo de código a seguir.


```C++
DXGI_SWAP_CHAIN_DESC desc;
ZeroMemory(&desc, sizeof(DXGI_SWAP_CHAIN_DESC));
desc.Windowed = TRUE; // Sets the initial state of full-screen mode.
desc.BufferCount = 2;
desc.BufferDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
desc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
desc.SampleDesc.Count = 1;      //multisampling setting
desc.SampleDesc.Quality = 0;    //vendor-specific flag
desc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL;
desc.OutputWindow = hWnd;

// Create the DXGI device object to use in other factories, such as Direct2D.
Microsoft::WRL::ComPtr<IDXGIDevice3> dxgiDevice;
m_pd3dDevice.As(&dxgiDevice);

// Create swap chain.
Microsoft::WRL::ComPtr<IDXGIAdapter> adapter;
Microsoft::WRL::ComPtr<IDXGIFactory> factory;

hr = dxgiDevice->GetAdapter(&adapter);

if (SUCCEEDED(hr))
{
    adapter->GetParent(IID_PPV_ARGS(&factory));

    hr = factory->CreateSwapChain(
        m_pd3dDevice.Get(),
        &desc,
        &m_pDXGISwapChain
        );
}
```



Se você estiver apenas começando, provavelmente é melhor usar a configuração mostrada aqui. Agora, neste ponto, se você já estiver familiarizado com as versões anteriores do DirectX, talvez esteja se perguntando: "por que não criamos o dispositivo e a cadeia de troca ao mesmo tempo, em vez de voltar por todas essas classes?" A resposta é eficiente: as cadeias de permuta são recursos de dispositivo Direct3D e os recursos de dispositivo estão vinculados ao dispositivo Direct3D específico que os criou. Se você criar um novo dispositivo com uma nova cadeia de permuta, precisará recriar todos os recursos do dispositivo usando o novo dispositivo Direct3D. Portanto, ao criar a cadeia de permuta com a mesma fábrica (como mostrado acima), você poderá recriar a cadeia de permuta e continuar usando os recursos do dispositivo Direct3D que você já carregou!

Agora você tem uma janela do sistema operacional, uma maneira de acessar a GPU e seus recursos e uma cadeia de permuta para exibir os resultados da renderização. Tudo o que resta é conectar tudo isso!

## <a name="create-a-render-target-for-drawing"></a>Criar um destino de renderização para desenho

O pipeline do sombreador precisa de um recurso para desenhar pixels. A maneira mais simples de criar esse recurso é definir um recurso [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) como um buffer de fundo para o sombreador de pixel para desenhar e, em seguida, ler essa textura na cadeia de permuta.

Para fazer isso, você cria uma *exibição* de destino de renderização. No Direct3D, uma exibição é uma maneira de acessar um recurso específico. Nesse caso, a exibição permite que o sombreador de pixel grave na textura à medida que conclui suas operações por pixel.

Vamos examinar o código para isso. Quando você define \_ \_ a saída de destino de renderização de uso de dxgi \_ \_ na cadeia de permuta, isso habilitou o recurso do Direct3D subjacente a ser usado como uma superfície de desenho. Portanto, para obter nossa exibição de destino de renderização, precisamos apenas obter o buffer de fundo da cadeia de permuta e criar uma exibição de destino de renderização associada ao recurso de buffer de fundo.


```C++
hr = m_pDXGISwapChain->GetBuffer(
    0,
    __uuidof(ID3D11Texture2D),
    (void**) &m_pBackBuffer);

hr = m_pd3dDevice->CreateRenderTargetView(
    m_pBackBuffer.Get(),
    nullptr,
    m_pRenderTarget.GetAddressOf()
    );

m_pBackBuffer->GetDesc(&m_bbDesc);
```



Crie também um *buffer de estêncil de profundidade*. Um buffer de estêncil de profundidade é apenas uma forma específica de recurso [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) , que é normalmente usada para determinar quais pixels têm prioridade de desenho durante a rasterização com base na distância dos objetos na cena da câmera. Um buffer de estêncil de profundidade também pode ser usado para efeitos de estêncil, em que pixels específicos são descartados ou ignorados durante a rasterização. Esse buffer deve ter o mesmo tamanho que o destino de renderização. Observe que você não pode ler ou renderizar para a textura de estêncil de profundidade do buffer de quadro porque ele é usado exclusivamente pelo pipeline do sombreador antes e durante a rasterização final.

Além disso, crie uma exibição para o buffer de estêncil de profundidade como um [**ID3D11DepthStencilView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview). A exibição informa ao pipeline do sombreador como interpretar o recurso [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) subjacente. portanto, se você não fornecer essa exibição, nenhum teste de profundidade por pixel será executado e os objetos em sua cena poderão parecer um pouco dentro do menos!


```C++
CD3D11_TEXTURE2D_DESC depthStencilDesc(
    DXGI_FORMAT_D24_UNORM_S8_UINT,
    static_cast<UINT> (m_bbDesc.Width),
    static_cast<UINT> (m_bbDesc.Height),
    1, // This depth stencil view has only one texture.
    1, // Use a single mipmap level.
    D3D11_BIND_DEPTH_STENCIL
    );

m_pd3dDevice->CreateTexture2D(
    &depthStencilDesc,
    nullptr,
    &m_pDepthStencil
    );

CD3D11_DEPTH_STENCIL_VIEW_DESC depthStencilViewDesc(D3D11_DSV_DIMENSION_TEXTURE2D);

m_pd3dDevice->CreateDepthStencilView(
    m_pDepthStencil.Get(),
    &depthStencilViewDesc,
    &m_pDepthStencilView
    );
```



A última etapa é criar um visor. Isso define o retângulo visível do buffer de fundo exibido na tela; Você pode alterar a parte do buffer que é exibida na tela alterando os parâmetros do visor. Esse código tem como alvo todo o tamanho da janela, ou a resolução da tela, no caso de cadeias de troca de tela inteira. Para diversão, altere os valores de coordenadas fornecidos e observe os resultados.


```C++
ZeroMemory(&m_viewport, sizeof(D3D11_VIEWPORT));
m_viewport.Height = (float) m_bbDesc.Height;
m_viewport.Width = (float) m_bbDesc.Width;
m_viewport.MinDepth = 0;
m_viewport.MaxDepth = 1;

m_pd3dDeviceContext->RSSetViewports(
    1,
    &m_viewport
    );
```



E é assim que você vai de nada para desenhar pixels em uma janela! Ao começar, é uma boa ideia familiarizar-se com o modo como o DirectX, por DXGI, gerencia os principais recursos de que você precisa para começar a desenhar pixels.

Em seguida, você examinará a estrutura do pipeline de gráficos; consulte [entender o pipeline de renderização do modelo de aplicativo DirectX](understand-the-directx-11-2-graphics-pipeline.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**A seguir**
</dt> <dt>

[Trabalhar com sombreadores e recursos de sombreador](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 