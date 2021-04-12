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
# <a name="work-with-directx-device-resources"></a><span data-ttu-id="71617-103">Trabalhar com recursos do dispositivo DirectX</span><span class="sxs-lookup"><span data-stu-id="71617-103">Work with DirectX device resources</span></span>

<span data-ttu-id="71617-104">Entenda a função da Microsoft DirectX Graphics Infrastructure (DXGI) no seu jogo DirectX da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="71617-104">Understand the role of the Microsoft DirectX Graphics Infrastructure (DXGI) in your Windows Store DirectX game.</span></span> <span data-ttu-id="71617-105">DXGI é um conjunto de APIs usado para configurar e gerenciar gráficos de baixo nível e recursos de adaptador gráfico.</span><span class="sxs-lookup"><span data-stu-id="71617-105">DXGI is a set of APIs used to configure and manage low-level graphics and graphics adapter resources.</span></span> <span data-ttu-id="71617-106">Sem ele, você não teria como desenhar os elementos gráficos de seu jogo em uma janela.</span><span class="sxs-lookup"><span data-stu-id="71617-106">Without it, you'd have no way to draw your game's graphics to a window.</span></span>

<span data-ttu-id="71617-107">Considere o DXGI desta forma: para acessar diretamente a GPU e gerenciar seus recursos, você deve ter uma maneira de descrevê-la em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="71617-107">Think of DXGI this way: to directly access the GPU and manage its resources, you must have a way to describe it to your app.</span></span> <span data-ttu-id="71617-108">A informação mais importante que você precisa sobre a GPU é o lugar para desenhar pixels para que possa enviar esses pixels para a tela.</span><span class="sxs-lookup"><span data-stu-id="71617-108">The most important piece of info you need about the GPU is the place to draw pixels so it can send those pixels to the screen.</span></span> <span data-ttu-id="71617-109">Normalmente, isso é chamado de "buffer de fundo" — um local na memória GPU em que você pode desenhar os pixels e, em seguida, fazer com que ele seja "invertido" ou "trocado" e enviado à tela em um sinal de atualização.</span><span class="sxs-lookup"><span data-stu-id="71617-109">Typically this is called the "back buffer"—a location in GPU memory where you can draw the pixels and then have it "flipped" or "swapped" and sent to the screen on a refresh signal.</span></span> <span data-ttu-id="71617-110">DXGI permite que você adquira esse local e os meios para usar esse buffer (chamado de *cadeia de permuta* porque ele é uma cadeia de buffers intercambiáveis, permitindo várias estratégias de buffer).</span><span class="sxs-lookup"><span data-stu-id="71617-110">DXGI lets you acquire that location and the means to use that buffer (called a *swap chain* because it is a chain of swappable buffers, allowing for multiple buffering strategies).</span></span>

<span data-ttu-id="71617-111">Para fazer isso, você precisa ter acesso para gravar na cadeia de permuta e um identificador para a janela que exibirá o buffer de fundo atual da cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="71617-111">To do this, you need access to write to the swap chain, and a handle to the window that will display the current back buffer for the swap chain.</span></span> <span data-ttu-id="71617-112">Você também precisa conectar os dois para garantir que o sistema operacional atualizará a janela com o conteúdo do buffer de fundo quando solicitá-la.</span><span class="sxs-lookup"><span data-stu-id="71617-112">You also need to connect the two to ensure that the operating system will refresh the window with the contents of the back buffer when you request it to do so.</span></span>

<span data-ttu-id="71617-113">O processo geral para desenhar na tela é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="71617-113">The overall process for drawing to the screen is as follows:</span></span>

-   <span data-ttu-id="71617-114">Obtenha um [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="71617-114">Get a [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) for your app.</span></span>
-   <span data-ttu-id="71617-115">Obtenha uma interface para o dispositivo e o contexto do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="71617-115">Get an interface for the Direct3D device and context.</span></span>
-   <span data-ttu-id="71617-116">Crie a cadeia de permuta para exibir a imagem renderizada no [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span><span class="sxs-lookup"><span data-stu-id="71617-116">Create the swap chain to display your rendered image in the [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span>
-   <span data-ttu-id="71617-117">Crie um destino de renderização para desenhar e preencha-o com pixels.</span><span class="sxs-lookup"><span data-stu-id="71617-117">Create a render target for drawing and populate it with pixels.</span></span>
-   <span data-ttu-id="71617-118">Apresente a cadeia de permuta!</span><span class="sxs-lookup"><span data-stu-id="71617-118">Present the swap chain!</span></span>

## <a name="create-a-window-for-your-app"></a><span data-ttu-id="71617-119">Criar uma janela para seu aplicativo</span><span class="sxs-lookup"><span data-stu-id="71617-119">Create a window for your app</span></span>

<span data-ttu-id="71617-120">A primeira coisa que precisamos fazer é criar uma janela.</span><span class="sxs-lookup"><span data-stu-id="71617-120">The first thing we need to do is create a window.</span></span> <span data-ttu-id="71617-121">Primeiro, crie uma classe de janela populando uma instância de [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)e, em seguida, registre-a usando [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa).</span><span class="sxs-lookup"><span data-stu-id="71617-121">First, create a window class by populating an instance of [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa), then register it using [**RegisterClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa).</span></span> <span data-ttu-id="71617-122">A classe Window contém as propriedades essenciais da janela, incluindo o ícone que ela usa, a função estática de processamento de mensagens (mais informações sobre isso posteriormente) e um nome exclusivo para a classe Window.</span><span class="sxs-lookup"><span data-stu-id="71617-122">The window class contains essential properties of the window, including the icon it uses, the static message processing function (more on this later), and a unique name for the window class.</span></span>


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



<span data-ttu-id="71617-123">Em seguida, você cria a janela.</span><span class="sxs-lookup"><span data-stu-id="71617-123">Next, you create the window.</span></span> <span data-ttu-id="71617-124">Também precisamos fornecer informações de tamanho para a janela e o nome da classe de janela que acabamos de criar.</span><span class="sxs-lookup"><span data-stu-id="71617-124">We also need to provide size information for the window and the name of the window class we just created.</span></span> <span data-ttu-id="71617-125">Ao chamar [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa), você obtém um ponteiro opaco para a janela chamada HWND; Você precisará manter o ponteiro do HWND e usá-lo sempre que precisar fazer referência à janela, incluindo destruir ou recriá-la, e (especialmente importante) ao criar a cadeia de permuta DXGI usada para desenhar na janela.</span><span class="sxs-lookup"><span data-stu-id="71617-125">When you call [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa), you get back an opaque pointer to the window called an HWND; you'll need to keep the HWND pointer and use it any time you need to reference the window, including destroying or recreating it, and (especially important) when creating the DXGI swap chain you use to draw in the window.</span></span>


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



<span data-ttu-id="71617-126">O modelo de aplicativo da área de trabalho do Windows inclui um gancho no loop de mensagem do Windows.</span><span class="sxs-lookup"><span data-stu-id="71617-126">The Windows desktop app model includes a hook into the Windows message loop.</span></span> <span data-ttu-id="71617-127">Você precisará basear o loop do programa principal desse gancho escrevendo uma função "StaticWindowProc" para processar eventos de janela.</span><span class="sxs-lookup"><span data-stu-id="71617-127">You'll need to base your main program loop off of this hook by writing a "StaticWindowProc" function to process windowing events.</span></span> <span data-ttu-id="71617-128">Essa deve ser uma função estática, pois o Windows a chamará fora do contexto de qualquer instância de classe.</span><span class="sxs-lookup"><span data-stu-id="71617-128">This must be a static function because Windows will call it outside of the context of any class instance.</span></span> <span data-ttu-id="71617-129">Veja um exemplo muito simples de uma função de processamento de mensagem estática.</span><span class="sxs-lookup"><span data-stu-id="71617-129">Here's a very simple example of a static message processing function.</span></span>


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



<span data-ttu-id="71617-130">Este exemplo simples verifica apenas as condições de saída do programa: [**WM \_ Close**](/windows/desktop/winmsg/wm-close), enviado quando a janela é solicitada para ser fechada e o [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy), que é enviado depois que a janela é realmente removida da tela.</span><span class="sxs-lookup"><span data-stu-id="71617-130">This simple example only checks for program exit conditions: [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close), sent when the window is requested to be closed, and [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy), which is sent after the window is actually removed from the screen.</span></span> <span data-ttu-id="71617-131">Um aplicativo de produção completo também precisa lidar com outros eventos de janela — para obter a lista completa de eventos de janela, consulte [notificações de janela](/windows/desktop/winmsg/window-notifications).</span><span class="sxs-lookup"><span data-stu-id="71617-131">A full, production app needs to handle other windowing events too—for the complete list of windowing events, see [Window Notifications](/windows/desktop/winmsg/window-notifications).</span></span>

<span data-ttu-id="71617-132">O próprio loop do programa principal precisa reconhecer mensagens do Windows, permitindo ao Windows a oportunidade de executar o processo de mensagem estático.</span><span class="sxs-lookup"><span data-stu-id="71617-132">The main program loop itself needs to acknowledge Windows messages by allowing Windows the opportunity to run the static message proc.</span></span> <span data-ttu-id="71617-133">Ajude o programa a ser executado com eficiência com a bifurcação do comportamento: cada iteração deve optar por processar novas mensagens do Windows, se estiverem disponíveis, e se nenhuma mensagem estiver na fila, ela deverá renderizar um novo quadro.</span><span class="sxs-lookup"><span data-stu-id="71617-133">Help the program run efficiently by forking the behavior: each iteration should choose to process new Windows messages if they are available, and if no messages are in the queue it should render a new frame.</span></span> <span data-ttu-id="71617-134">Veja um exemplo muito simples:</span><span class="sxs-lookup"><span data-stu-id="71617-134">Here's a very simple example:</span></span>


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



## <a name="get-an-interface-for-the-direct3d-device-and-context"></a><span data-ttu-id="71617-135">Obter uma interface para o dispositivo e contexto do Direct3D</span><span class="sxs-lookup"><span data-stu-id="71617-135">Get an interface for the Direct3D device and context</span></span>

<span data-ttu-id="71617-136">A primeira etapa para usar o Direct3D é adquirir uma interface para o hardware do Direct3D (a GPU), representada como instâncias de [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) e [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2).</span><span class="sxs-lookup"><span data-stu-id="71617-136">The first step to using Direct3D is to acquire an interface for the Direct3D hardware (the GPU), represented as instances of [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) and [**ID3D11DeviceContext**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2).</span></span> <span data-ttu-id="71617-137">O primeiro é uma representação virtual dos recursos de GPU, e o último é uma abstração independente de dispositivo do pipeline de renderização e do processo.</span><span class="sxs-lookup"><span data-stu-id="71617-137">The former is a virtual representation of the GPU resources, and the latter is a device-agnostic abstraction of the rendering pipeline and process.</span></span> <span data-ttu-id="71617-138">Aqui está uma maneira fácil de considerar: **ID3D11Device** contém os métodos gráficos que você chama com pouca frequência, geralmente antes que qualquer renderização ocorra, para adquirir e configurar o conjunto de recursos de que você precisa para começar a desenhar pixels.</span><span class="sxs-lookup"><span data-stu-id="71617-138">Here's an easy way to think of it: **ID3D11Device** contains the graphics methods you call infrequently, usually before any rendering occurs, to acquire and configure the set of resources you need to start drawing pixels.</span></span> <span data-ttu-id="71617-139">**ID3D11DeviceContext**, por outro lado, contém os métodos que você chama a cada quadro: carregando em buffers e exibições e outros recursos, alterando o estado de mesclagem de saída e rasterizador, gerenciando sombreadores e desenhando os resultados da passagem desses recursos por meio de Estados e sombreadores.</span><span class="sxs-lookup"><span data-stu-id="71617-139">**ID3D11DeviceContext**, on the other hand, contains the methods you call every frame: loading in buffers and views and other resources, changing output-merger and rasterizer state, managing shaders, and drawing the results of passing those resources through the states and shaders.</span></span>

<span data-ttu-id="71617-140">Há uma parte muito importante desse processo: definir o nível de recurso.</span><span class="sxs-lookup"><span data-stu-id="71617-140">There's one very important part of this process: setting the feature level.</span></span> <span data-ttu-id="71617-141">O nível de recurso informa ao DirectX o nível mínimo de hardware com suporte do seu aplicativo, com o nível de recurso do D3D \_ \_ \_ 9 \_ 1 como o menor conjunto de recursos e o \_ \_ nível \_ de recurso do D3D 11 \_ 1 como o mais alto atual.</span><span class="sxs-lookup"><span data-stu-id="71617-141">The feature level tells DirectX the minimum level of hardware your app supports, with D3D\_FEATURE\_LEVEL\_9\_1 as the lowest feature set and D3D\_FEATURE\_LEVEL\_11\_1 as the current highest.</span></span> <span data-ttu-id="71617-142">Você deve dar suporte a 9 \_ 1 como o mínimo se quiser alcançar o público mais amplo possível.</span><span class="sxs-lookup"><span data-stu-id="71617-142">You should support 9\_1 as the minimum if you want to reach the widest possible audience.</span></span> <span data-ttu-id="71617-143">Reserve algum tempo para ler os níveis de [recursos](/previous-versions/windows/apps/hh994923(v=win.10)) do Direct3D e avaliar os níveis mínimo e máximo de recursos que você deseja que seu jogo dê suporte e entenda as implicações de sua escolha.</span><span class="sxs-lookup"><span data-stu-id="71617-143">Take some time to read up on Direct3D [feature levels](/previous-versions/windows/apps/hh994923(v=win.10)) and assess for yourself the minimum and maximum feature levels you want your game to support and to understand the implications of your choice.</span></span>

<span data-ttu-id="71617-144">Obtenha referências (ponteiros) para o dispositivo Direct3D e o contexto do dispositivo e armazene-os como variáveis de nível de classe na instância **DeviceResources** (como apontadores inteligentes **ComPtr** ).</span><span class="sxs-lookup"><span data-stu-id="71617-144">Obtain references (pointers) to both the Direct3D device and device context and store them as class-level variables on the **DeviceResources** instance (as **ComPtr** smart pointers).</span></span> <span data-ttu-id="71617-145">Use essas referências sempre que precisar acessar o dispositivo Direct3D ou o contexto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="71617-145">Use these references whenever you need to access the Direct3D device or device context.</span></span>


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



## <a name="create-the-swap-chain"></a><span data-ttu-id="71617-146">Criar a cadeia de permuta</span><span class="sxs-lookup"><span data-stu-id="71617-146">Create the swap chain</span></span>

<span data-ttu-id="71617-147">Ok: você tem uma janela para desenhar e tem uma interface para enviar dados e fornecer comandos para a GPU.</span><span class="sxs-lookup"><span data-stu-id="71617-147">Okay: You have a window to draw in, and you have an interface to send data and give commands to the GPU.</span></span> <span data-ttu-id="71617-148">Agora, vamos ver como reuni-los.</span><span class="sxs-lookup"><span data-stu-id="71617-148">Now let's see how to bring them together.</span></span>

<span data-ttu-id="71617-149">Primeiro, você informa ao DXGI quais valores usar para as propriedades da cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="71617-149">First, you tell DXGI what values to use for the properties of the swap chain.</span></span> <span data-ttu-id="71617-150">Faça isso usando uma [**estrutura \_ \_ \_ desc de cadeia de permuta dxgi**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) .</span><span class="sxs-lookup"><span data-stu-id="71617-150">Do this using a [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) structure.</span></span> <span data-ttu-id="71617-151">Seis campos são particularmente importantes para aplicativos da área de trabalho:</span><span class="sxs-lookup"><span data-stu-id="71617-151">Six fields are particularly important for desktop apps:</span></span>

-   <span data-ttu-id="71617-152">Em **janela**: indica se a cadeia de permuta é de tela inteira ou recortada na janela.</span><span class="sxs-lookup"><span data-stu-id="71617-152">**Windowed**: Indicates whether the swap chain is full-screen or clipped to the window.</span></span> <span data-ttu-id="71617-153">Defina como TRUE para colocar a cadeia de permuta na janela que você criou anteriormente.</span><span class="sxs-lookup"><span data-stu-id="71617-153">Set this to TRUE to put the swap chain in the window you created earlier.</span></span>
-   <span data-ttu-id="71617-154">**BufferUsage**: Defina isso como saída de destino de renderização de uso de dxgi \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="71617-154">**BufferUsage**: Set this to DXGI\_USAGE\_RENDER\_TARGET\_OUTPUT.</span></span> <span data-ttu-id="71617-155">Isso indica que a cadeia de permuta será uma superfície de desenho, permitindo que você a use como um destino de processamento Direct3D.</span><span class="sxs-lookup"><span data-stu-id="71617-155">This indicates that the swap chain will be a drawing surface, allowing you to use it as a Direct3D render-target.</span></span>
-   <span data-ttu-id="71617-156">**SwapEffect**: Defina isso como efeito de permuta de dxgi \_ \_ \_ inverter \_ sequencial.</span><span class="sxs-lookup"><span data-stu-id="71617-156">**SwapEffect**: Set this to DXGI\_SWAP\_EFFECT\_FLIP\_SEQUENTIAL.</span></span>
-   <span data-ttu-id="71617-157">**Formato**: o formato \_ dxgi \_ B8G8R8A8 \_ UNORM format especifica a cor de 32 bits: 8 bits para cada um dos três canais de cores RGB e 8 bits para o canal alfa.</span><span class="sxs-lookup"><span data-stu-id="71617-157">**Format**: The DXGI\_FORMAT\_B8G8R8A8\_UNORM format specifies 32-bit color: 8 bits for each of the three RGB color channels, and 8 bits for the alpha channel.</span></span>
-   <span data-ttu-id="71617-158">**BufferCount**: Defina isso como 2 para um comportamento de buffer duplo tradicional para evitar a subdivisão.</span><span class="sxs-lookup"><span data-stu-id="71617-158">**BufferCount**: Set this to 2 for a traditional double-buffered behavior to avoid tearing.</span></span> <span data-ttu-id="71617-159">Defina a contagem de buffer como 3 se o seu conteúdo de gráficos levar mais de um ciclo de atualização de monitor para renderizar um único quadro (a 60 Hz, por exemplo, o limite é maior que 16 MS).</span><span class="sxs-lookup"><span data-stu-id="71617-159">Set the buffer count to 3 if your graphics content takes more than one monitor refresh cycle to render a single frame (at 60 Hz for example, the threshold is more than 16 ms).</span></span>
-   <span data-ttu-id="71617-160">**SampleDesc**: Este campo controla a multiamostragem.</span><span class="sxs-lookup"><span data-stu-id="71617-160">**SampleDesc**: This field controls multisampling.</span></span> <span data-ttu-id="71617-161">Defina **contagem** como 1 e **qualidade** como 0 para cadeias de permuta de flip-Model.</span><span class="sxs-lookup"><span data-stu-id="71617-161">Set **Count** to 1 and **Quality** to 0 for flip-model swap chains.</span></span> <span data-ttu-id="71617-162">(Para usar multiamostragens com cadeias de permuta de flip-Model, desenhe em um destino de renderização multiamostrado separado e, em seguida, resolva esse destino para a cadeia de permuta antes de apresentá-lo.</span><span class="sxs-lookup"><span data-stu-id="71617-162">(To use multisampling with flip-model swap chains, draw on a separate multisampled render target and then resolve that target to the swap chain just before presenting it.</span></span> <span data-ttu-id="71617-163">O código de exemplo é fornecido em [multiamostrar em aplicativos da Windows Store](/previous-versions/windows/apps/dn458384(v=win.10)).)</span><span class="sxs-lookup"><span data-stu-id="71617-163">Example code is provided in [Multisampling in Windows Store apps](/previous-versions/windows/apps/dn458384(v=win.10)).)</span></span>

<span data-ttu-id="71617-164">Depois de especificar uma configuração para a cadeia de permuta, você deve usar a mesma fábrica de DXGI que criou o dispositivo Direct3D (e o contexto do dispositivo) para criar a cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="71617-164">After you have specified a configuration for the swap chain, you must use the same DXGI factory that created the Direct3D device (and device context) in order to create the swap chain.</span></span>

<span data-ttu-id="71617-165">**Forma abreviada:  **</span><span class="sxs-lookup"><span data-stu-id="71617-165">**Short form:  **</span></span>

<span data-ttu-id="71617-166">Obtenha a referência de [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) que você criou anteriormente.</span><span class="sxs-lookup"><span data-stu-id="71617-166">Get the [**ID3D11Device**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11device2) reference you created previously.</span></span> <span data-ttu-id="71617-167">Converta-o em [**IDXGIDevice3**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3) (se você ainda não tiver feito isso) e, em seguida, chame [**IDXGIDevice:: getadapter**](/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter) para adquirir o adaptador dxgi.</span><span class="sxs-lookup"><span data-stu-id="71617-167">Upcast it to [**IDXGIDevice3**](/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidevice3) (if you haven't already) and then call [**IDXGIDevice::GetAdapter**](/windows/desktop/api/dxgi/nf-dxgi-idxgidevice-getadapter) to acquire the DXGI adapter.</span></span> <span data-ttu-id="71617-168">Obtenha a fábrica pai para esse adaptador chamando [**IDXGIFactory2:: GetParent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent) ([**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) Inherits from [**IDXGIObject**](/windows/desktop/api/dxgi/nn-dxgi-idxgiobject)) – agora você pode usar essa fábrica para criar a cadeia de permuta chamando [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), como visto no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="71617-168">Get the parent factory for that adapter by calling [**IDXGIFactory2::GetParent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiobject-getparent) ([**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) inherits from [**IDXGIObject**](/windows/desktop/api/dxgi/nn-dxgi-idxgiobject))—now you can use that factory to create the swap chain by calling [**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd), as seen in the following code sample.</span></span>


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



<span data-ttu-id="71617-169">Se você estiver apenas começando, provavelmente é melhor usar a configuração mostrada aqui.</span><span class="sxs-lookup"><span data-stu-id="71617-169">If you're just starting out, it's probably best to use the configuration shown here.</span></span> <span data-ttu-id="71617-170">Agora, neste ponto, se você já estiver familiarizado com as versões anteriores do DirectX, talvez esteja se perguntando: "por que não criamos o dispositivo e a cadeia de troca ao mesmo tempo, em vez de voltar por todas essas classes?"</span><span class="sxs-lookup"><span data-stu-id="71617-170">Now at this point, if you are already familiar with previous versions of DirectX you might be asking: "Why didn't we create the device and swap chain at the same time, instead of walking back through all of those classes?"</span></span> <span data-ttu-id="71617-171">A resposta é eficiente: as cadeias de permuta são recursos de dispositivo Direct3D e os recursos de dispositivo estão vinculados ao dispositivo Direct3D específico que os criou.</span><span class="sxs-lookup"><span data-stu-id="71617-171">The answer is efficiency: swap chains are Direct3D device resources, and device resources are tied to the particular Direct3D device that created them.</span></span> <span data-ttu-id="71617-172">Se você criar um novo dispositivo com uma nova cadeia de permuta, precisará recriar todos os recursos do dispositivo usando o novo dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="71617-172">If you create a new device with a new swap chain, you have to recreate all your device resources using the new Direct3D device.</span></span> <span data-ttu-id="71617-173">Portanto, ao criar a cadeia de permuta com a mesma fábrica (como mostrado acima), você poderá recriar a cadeia de permuta e continuar usando os recursos do dispositivo Direct3D que você já carregou!</span><span class="sxs-lookup"><span data-stu-id="71617-173">So by creating the swap chain with the same factory (as shown above), you are able to recreate the swap chain and continue using the Direct3D device resources you already have loaded!</span></span>

<span data-ttu-id="71617-174">Agora você tem uma janela do sistema operacional, uma maneira de acessar a GPU e seus recursos e uma cadeia de permuta para exibir os resultados da renderização.</span><span class="sxs-lookup"><span data-stu-id="71617-174">Now you've got a window from the operating system, a way to access the GPU and its resources, and a swap chain to display the rendering results.</span></span> <span data-ttu-id="71617-175">Tudo o que resta é conectar tudo isso!</span><span class="sxs-lookup"><span data-stu-id="71617-175">All that's left is to wire the whole thing together!</span></span>

## <a name="create-a-render-target-for-drawing"></a><span data-ttu-id="71617-176">Criar um destino de renderização para desenho</span><span class="sxs-lookup"><span data-stu-id="71617-176">Create a render target for drawing</span></span>

<span data-ttu-id="71617-177">O pipeline do sombreador precisa de um recurso para desenhar pixels.</span><span class="sxs-lookup"><span data-stu-id="71617-177">The shader pipeline needs a resource to draw pixels into.</span></span> <span data-ttu-id="71617-178">A maneira mais simples de criar esse recurso é definir um recurso [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) como um buffer de fundo para o sombreador de pixel para desenhar e, em seguida, ler essa textura na cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="71617-178">The simplest way to create this resource is to define a [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) resource as a back buffer for the pixel shader to draw into, and then read that texture into the swap chain.</span></span>

<span data-ttu-id="71617-179">Para fazer isso, você cria uma *exibição* de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="71617-179">To do this, you create a render-target *view*.</span></span> <span data-ttu-id="71617-180">No Direct3D, uma exibição é uma maneira de acessar um recurso específico.</span><span class="sxs-lookup"><span data-stu-id="71617-180">In Direct3D, a view is a way to access a specific resource.</span></span> <span data-ttu-id="71617-181">Nesse caso, a exibição permite que o sombreador de pixel grave na textura à medida que conclui suas operações por pixel.</span><span class="sxs-lookup"><span data-stu-id="71617-181">In this case, the view enables the pixel shader to write into the texture as it completes its per-pixel operations.</span></span>

<span data-ttu-id="71617-182">Vamos examinar o código para isso.</span><span class="sxs-lookup"><span data-stu-id="71617-182">Let's look at the code for this.</span></span> <span data-ttu-id="71617-183">Quando você define \_ \_ a saída de destino de renderização de uso de dxgi \_ \_ na cadeia de permuta, isso habilitou o recurso do Direct3D subjacente a ser usado como uma superfície de desenho.</span><span class="sxs-lookup"><span data-stu-id="71617-183">When you set DXGI\_USAGE\_RENDER\_TARGET\_OUTPUT on the swap chain, that enabled the underlying Direct3D resource to be used as a drawing surface.</span></span> <span data-ttu-id="71617-184">Portanto, para obter nossa exibição de destino de renderização, precisamos apenas obter o buffer de fundo da cadeia de permuta e criar uma exibição de destino de renderização associada ao recurso de buffer de fundo.</span><span class="sxs-lookup"><span data-stu-id="71617-184">So to get our render target view, we just need to get the back buffer from the swap chain and create a render target view bound to the back buffer resource.</span></span>


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



<span data-ttu-id="71617-185">Crie também um *buffer de estêncil de profundidade*.</span><span class="sxs-lookup"><span data-stu-id="71617-185">Also create a *depth-stencil buffer*.</span></span> <span data-ttu-id="71617-186">Um buffer de estêncil de profundidade é apenas uma forma específica de recurso [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) , que é normalmente usada para determinar quais pixels têm prioridade de desenho durante a rasterização com base na distância dos objetos na cena da câmera.</span><span class="sxs-lookup"><span data-stu-id="71617-186">A depth-stencil buffer is just a particular form of [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) resource, which is typically used to determine which pixels have draw priority during rasterization based on the distance of the objects in the scene from the camera.</span></span> <span data-ttu-id="71617-187">Um buffer de estêncil de profundidade também pode ser usado para efeitos de estêncil, em que pixels específicos são descartados ou ignorados durante a rasterização.</span><span class="sxs-lookup"><span data-stu-id="71617-187">A depth-stencil buffer can also be used for stencil effects, where specific pixels are discarded or ignored during rasterization.</span></span> <span data-ttu-id="71617-188">Esse buffer deve ter o mesmo tamanho que o destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="71617-188">This buffer must be the same size as the render target.</span></span> <span data-ttu-id="71617-189">Observe que você não pode ler ou renderizar para a textura de estêncil de profundidade do buffer de quadro porque ele é usado exclusivamente pelo pipeline do sombreador antes e durante a rasterização final.</span><span class="sxs-lookup"><span data-stu-id="71617-189">Note that you cannot read from or render to the frame buffer depth-stencil texture because it is used exclusively by the shader pipeline before and during final rasterization.</span></span>

<span data-ttu-id="71617-190">Além disso, crie uma exibição para o buffer de estêncil de profundidade como um [**ID3D11DepthStencilView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview).</span><span class="sxs-lookup"><span data-stu-id="71617-190">Also create a view for the depth-stencil buffer as an [**ID3D11DepthStencilView**](/windows/desktop/api/d3d11/nn-d3d11-id3d11depthstencilview).</span></span> <span data-ttu-id="71617-191">A exibição informa ao pipeline do sombreador como interpretar o recurso [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) subjacente. portanto, se você não fornecer essa exibição, nenhum teste de profundidade por pixel será executado e os objetos em sua cena poderão parecer um pouco dentro do menos!</span><span class="sxs-lookup"><span data-stu-id="71617-191">The view tells the shader pipeline how to interpret the underlying [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) resource - so if you don't supply this view no per-pixel depth testing is performed, and the objects in your scene may seem a bit inside-out at the very least!</span></span>


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



<span data-ttu-id="71617-192">A última etapa é criar um visor.</span><span class="sxs-lookup"><span data-stu-id="71617-192">The last step is to create a viewport.</span></span> <span data-ttu-id="71617-193">Isso define o retângulo visível do buffer de fundo exibido na tela; Você pode alterar a parte do buffer que é exibida na tela alterando os parâmetros do visor.</span><span class="sxs-lookup"><span data-stu-id="71617-193">This defines the visible rectangle of the back buffer displayed on the screen; you can change the part of the buffer that is displayed on the screen by changing the parameters of the viewport.</span></span> <span data-ttu-id="71617-194">Esse código tem como alvo todo o tamanho da janela, ou a resolução da tela, no caso de cadeias de troca de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="71617-194">This code targets the whole window size—or the screen resolution, in the case of full-screen swap chains.</span></span> <span data-ttu-id="71617-195">Para diversão, altere os valores de coordenadas fornecidos e observe os resultados.</span><span class="sxs-lookup"><span data-stu-id="71617-195">For fun, change the supplied coordinate values and observe the results.</span></span>


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



<span data-ttu-id="71617-196">E é assim que você vai de nada para desenhar pixels em uma janela!</span><span class="sxs-lookup"><span data-stu-id="71617-196">And that's how you go from nothing to drawing pixels in a window!</span></span> <span data-ttu-id="71617-197">Ao começar, é uma boa ideia familiarizar-se com o modo como o DirectX, por DXGI, gerencia os principais recursos de que você precisa para começar a desenhar pixels.</span><span class="sxs-lookup"><span data-stu-id="71617-197">As you start out, it's a good idea to become familiar with how DirectX, through DXGI, manages the core resources you need to start drawing pixels.</span></span>

<span data-ttu-id="71617-198">Em seguida, você examinará a estrutura do pipeline de gráficos; consulte [entender o pipeline de renderização do modelo de aplicativo DirectX](understand-the-directx-11-2-graphics-pipeline.md).</span><span class="sxs-lookup"><span data-stu-id="71617-198">Next you'll look at the structure of the graphics pipeline; see [Understand the DirectX app template's rendering pipeline](understand-the-directx-11-2-graphics-pipeline.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="71617-199">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="71617-199">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="71617-200">**A seguir**</span><span class="sxs-lookup"><span data-stu-id="71617-200">**Up next**</span></span>
</dt> <dt>

[<span data-ttu-id="71617-201">Trabalhar com sombreadores e recursos de sombreador</span><span class="sxs-lookup"><span data-stu-id="71617-201">Work with shaders and shader resources</span></span>](work-with-shaders-and-shader-resources.md)
</dt> </dl>

 

 