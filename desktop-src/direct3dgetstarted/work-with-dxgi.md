---
title: Trabalhar com recursos do dispositivo DirectX
description: Entenda a função do DXGI (Microsoft DirectX Graphic Infrastructure) em seu jogo Windows Store DirectX.
ms.assetid: 24c0c81d-6b55-4116-868a-154addf0f04c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 600af9c5ca2d2ba8ce8a7b078c769e195c4a7898384d102a21be3aaaf2c936bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068656"
---
# <a name="work-with-directx-device-resources"></a>Trabalhar com recursos do dispositivo DirectX

Entenda a função do DXGI (Microsoft DirectX Graphic Infrastructure) em seu jogo Windows Store DirectX. O DXGI é um conjunto de APIs usadas para configurar e gerenciar recursos de adaptador gráfico e gráfico de baixo nível. Sem ele, você não teria como desenhar os gráficos do jogo para uma janela.

Pense no DXGI dessa maneira: para acessar diretamente a GPU e gerenciar seus recursos, você deve ter uma maneira de descrevê-lo para seu aplicativo. A parte mais importante das informações que você precisa sobre a GPU é o local para desenhar pixels para que ela possa enviar esses pixels para a tela. Normalmente, isso é chamado de "buffer de fundo", um local na memória da GPU em que você pode desenhar os pixels e, em seguida, fazer com que ele seja "invertido" ou "trocado" e enviado para a tela em um sinal de atualização. O DXGI permite que você adquira esse  local e os meios para usar esse buffer (chamado de cadeia de permuta porque é uma cadeia de buffers permutáveis, permitindo várias estratégias de buffer).

Para fazer isso, você precisa de acesso para gravar na cadeia de permuta e um alça para a janela que exibirá o buffer de fundo atual para a cadeia de permuta. Você também precisa conectar os dois para garantir que o sistema operacional atualize a janela com o conteúdo do buffer de fundo quando você solicitar isso.

O processo geral para desenhar na tela é o seguinte:

-   Obter um [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) para seu aplicativo.
-   Obter uma interface para o contexto e o dispositivo Direct3D.
-   Crie a cadeia de permuta para exibir a imagem renderizada no [**CoreWindow.**](/uwp/api/Windows.UI.Core.CoreWindow)
-   Crie um destino de renderização para desenhar e populá-lo com pixels.
-   Apresente a cadeia de permuta!

## <a name="create-a-window-for-your-app"></a>Criar uma janela para seu aplicativo

A primeira coisa que precisamos fazer é criar uma janela. Primeiro, crie uma classe de janela populando uma instância [**do WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)e registre-a [**usando RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa). A classe window contém propriedades essenciais da janela, incluindo o ícone que ela usa, a função de processamento de mensagens estáticas (mais sobre isso posteriormente) e um nome exclusivo para a classe de janela.


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



Em seguida, crie a janela. Também precisamos fornecer informações de tamanho para a janela e o nome da classe de janela que criamos. Ao chamar [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa), você obterá de volta um ponteiro opaco para a janela chamado HWND; Você precisará manter o ponteiro HWND e usá-lo sempre que precisar referenciar a janela, incluindo destruir ou recriar e (especialmente importante) ao criar a cadeia de permuta DXGI usada para desenhar na janela.


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



O Windows aplicativo da área de trabalho inclui um gancho no loop Windows mensagem. Você precisará basear o loop do programa principal fora desse gancho escrevendo uma função "StaticWindowProc" para processar eventos de janela. Essa deve ser uma função estática porque Windows a chamará fora do contexto de qualquer instância de classe. Aqui está um exemplo muito simples de uma função de processamento de mensagem estática.


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



Este exemplo simples verifica apenas as condições de saída do programa: [**WM \_ CLOSE**](/windows/desktop/winmsg/wm-close), enviado quando a janela é solicitada para ser fechada e [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy), que é enviado depois que a janela é realmente removida da tela. Um aplicativo de produção completo também precisa lidar com outros eventos de janela – para ver a lista completa de eventos de janela, consulte [Notificações de janela.](/windows/desktop/winmsg/window-notifications)

O próprio loop do programa principal precisa reconhecer Windows mensagens, permitindo Windows a oportunidade de executar o proc de mensagem estática. Ajude o programa a ser executado com eficiência ao forcar o comportamento: cada iteração deverá optar por processar novas mensagens Windows se elas estão disponíveis e, se nenhuma mensagem estiver na fila, deverá renderizar um novo quadro. Aqui está um exemplo muito simples:


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



## <a name="get-an-interface-for-the-direct3d-device-and-context"></a>Obter uma interface para o contexto e o dispositivo Direct3D

A primeira etapa para usar o Direct3D é adquirir uma interface para o hardware direct3D (a GPU), representado como instâncias [**de ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) e [**ID3D11DeviceContext.**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) O primeiro é uma representação virtual dos recursos de GPU, e o último é uma abstração de dispositivos agnostic do pipeline e do processo de renderização. Esta é uma maneira fácil de pensar nisso: **ID3D11Device** contém os métodos gráficos que você chama com pouca pouca experiência, geralmente antes de qualquer renderização, para adquirir e configurar o conjunto de recursos que você precisa para começar a desenhar pixels. **ID3D11DeviceContext,** por outro lado, contém os métodos que você chama a cada quadro: carregar em buffers e exibições e outros recursos, alterar o estado de fusão de saída e de rasterizador, gerenciar sombreadores e desenhar os resultados da passagem desses recursos pelos estados e sombreadores.

Há uma parte muito importante desse processo: definir o nível do recurso. O nível de recurso informa ao DirectX o nível mínimo de hardware compatível com seu aplicativo, com D3D FEATURE LEVEL 9 1 como o menor conjunto de recursos e \_ \_ \_ \_ D3D \_ FEATURE \_ LEVEL \_ 11 \_ 1 como o mais alto atual. Você deverá dar suporte a \_ 9 1 como o mínimo se quiser alcançar o público mais amplo possível. Leve algum tempo para ler [](/previous-versions/windows/apps/hh994923(v=win.10)) os níveis de recursos do Direct3D e avalie por conta própria os níveis mínimos e máximos de recursos aos quais você deseja que seu jogo dê suporte e entenda as implicações de sua escolha.

Obtenha referências (ponteiros) para o contexto do dispositivo e do dispositivo Direct3D e armazene-as como variáveis de nível de classe na instância **DeviceResources** (como ponteiros **inteligentes comPtr).** Use essas referências sempre que precisar acessar o contexto do dispositivo ou do dispositivo Direct3D.


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

Ok: você tem uma janela para desenhar e tem uma interface para enviar dados e dar comandos à GPU. Agora, vamos ver como reuni-los.

Primeiro, você diz ao DXGI quais valores usar para as propriedades da cadeia de permuta. Faça isso usando uma estrutura [**DXGI \_ SWAP \_ CHAIN \_ DESC.**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) Seis campos são particularmente importantes para aplicativos da área de trabalho:

-   **Janela:** indica se a cadeia de permuta é de tela inteira ou recortada na janela. De definido como TRUE para colocar a cadeia de permuta na janela que você criou anteriormente.
-   **BufferUsage:** de definido como SAÍDA DE DESTINO DE RENDERIZAÇÃO DE USO \_ DXGI. \_ \_ \_ Isso indica que a cadeia de permuta será uma superfície de desenho, permitindo que você a use como um destino de renderização Direct3D.
-   **SwapEffect:** de definido como DXGI \_ SWAP EFFECT FLIP \_ \_ \_ SEQUENCIAL.
-   **Formato:** o formato DXGI \_ \_ B8G8R8A8 UNORM especifica a cor de 32 bits: 8 bits para cada um dos três canais de cores RGB e 8 bits para o \_ canal alfa.
-   **BufferCount:** de definido como 2 para um comportamento tradicional de buffer duplo para evitar a rebaixamento. De definir a contagem de buffers como 3 se o conteúdo de gráficos levar mais de um ciclo de atualização do monitor para renderizar um único quadro (a 60 Hz, por exemplo, o limite é maior que 16 ms).
-   **SampleDesc:** esse campo controla várias respostas. Definir **Contagem** como 1 e **Qualidade** como 0 para cadeias de permuta de flip-model. (Para usar multisampling com cadeias de permuta de flip-model, desenhe em um destino de renderização multisampled separado e resolva esse destino para a cadeia de permuta logo antes de apresentá-lo. O código de exemplo é fornecido [em Multisampling em aplicativos Windows Store](/previous-versions/windows/apps/dn458384(v=win.10)).)

Depois de especificar uma configuração para a cadeia de permuta, você deve usar a mesma fábrica DXGI que criou o dispositivo Direct3D (e o contexto do dispositivo) para criar a cadeia de permuta.

**Forma curta: **

Obter a [**referência ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) criada anteriormente. Upcast-lo para [**IDXGIDevice3**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3) (se você ainda não fez isso) e, em seguida, chame [**IDXGIDevice::GetAdapter**](/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter) para adquirir o adaptador DXGI. Obter a fábrica pai desse adaptador chamando [**IDXGIFactory2::GetParent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent) ([**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) herda de [**IDXGIObject**](/windows/desktop/api/dxgi/nn-dxgi-idxgiobject))— agora você pode usar essa fábrica para criar a cadeia de permuta chamando [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), conforme visto no exemplo de código a seguir.


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



Se você estiver apenas começando, provavelmente é melhor usar a configuração mostrada aqui. Agora, neste ponto, se você já estiver familiarizado com as versões anteriores do DirectX, poderá estar perguntando: "Por que não criamos o dispositivo e trocamos a cadeia ao mesmo tempo, em vez de voltar por todas essas classes?" A resposta é eficiência: as cadeias de permuta são recursos de dispositivo Direct3D e os recursos do dispositivo estão vinculados ao dispositivo Direct3D específico que os criou. Se você criar um novo dispositivo com uma nova cadeia de permuta, será necessário recriar todos os recursos do dispositivo usando o novo dispositivo Direct3D. Portanto, criando a cadeia de permuta com a mesma fábrica (conforme mostrado acima), você pode recriar a cadeia de permuta e continuar usando os recursos do dispositivo Direct3D que você já carregou!

Agora você tem uma janela do sistema operacional, uma maneira de acessar a GPU e seus recursos e uma cadeia de permuta para exibir os resultados da renderização. Tudo o que resta é unir tudo!

## <a name="create-a-render-target-for-drawing"></a>Criar um destino de renderização para desenho

O pipeline do sombreador precisa de um recurso para desenhar pixels. A maneira mais simples de criar esse recurso é definir um recurso [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) como um buffer de fundo para o sombreador de pixel para desenhar e, em seguida, ler essa textura na cadeia de permuta.

Para fazer isso, crie uma exibição de destino de *renderização*. No Direct3D, uma exibição é uma maneira de acessar um recurso específico. Nesse caso, a exibição permite que o sombreador de pixels escreva na textura à medida que conclui suas operações por pixel.

Vamos ver o código para isso. Quando você definir SAÍDA DE DESTINO DE RENDERIZAÇÃO DE USO DXGI na cadeia de permuta, isso permitiu que o recurso Direct3D subjacente fosse usado como \_ \_ uma superfície de \_ \_ desenho. Portanto, para obter nossa exibição de destino de renderização, precisamos apenas obter o buffer de fundo da cadeia de permuta e criar uma exibição de destino de renderização vinculada ao recurso de buffer de fundo.


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



Crie também um *buffer de estêncil de profundidade.* Um buffer de estêncil de profundidade é apenas uma forma específica do recurso [**ID3D11Texture2D,**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) que normalmente é usado para determinar quais pixels têm prioridade de desenho durante a rasterização com base na distância dos objetos na cena da câmera. Um buffer de estêncil de profundidade também pode ser usado para efeitos de estêncil, em que pixels específicos são descartados ou ignorados durante a rasterização. Esse buffer deve ter o mesmo tamanho que o destino de renderização. Observe que você não pode ler ou renderizar para a textura de profundidade e estêncil do buffer de quadros porque ela é usada exclusivamente pelo pipeline do sombreador antes e durante a rasterização final.

Crie também uma exibição para o buffer de estêncil de profundidade como [**um ID3D11DepthStencilView.**](/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview) A exibição informa ao pipeline de sombreador como interpretar o recurso [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) subjacente; portanto, se você não fornecer essa exibição, nenhum teste de profundidade por pixel será executado e os objetos em sua cena poderão parecer um pouco de dentro para fora, no mínimo!


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



A última etapa é criar um viewport. Isso define o retângulo visível do buffer de fundo exibido na tela; você pode alterar a parte do buffer que é exibida na tela alterando os parâmetros do visor. Esse código tem como alvo todo o tamanho da janela ou a resolução da tela, no caso de cadeias de troca de tela inteira. Para se divertido, altere os valores de coordenada fornecidos e observe os resultados.


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



E é assim que você passa do nada para desenhar pixels em uma janela! Conforme você começa, é uma boa ideia se familiarizar com como o DirectX, por meio do DXGI, gerencia os principais recursos necessários para começar a desenhar pixels.

Em seguida, você verá a estrutura do pipeline de gráficos; consulte Entender o pipeline de renderização do modelo de aplicativo [DirectX.](understand-the-directx-11-2-graphics-pipeline.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**A seguir**
</dt> <dt>

[Trabalhar com sombreadores e recursos de sombreador](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 