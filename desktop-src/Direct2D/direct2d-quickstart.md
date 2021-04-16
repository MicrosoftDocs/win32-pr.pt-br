---
title: Criando um aplicativo Direct2D simples
description: Percorre o processo de criação de uma janela que processa o conteúdo do Direct2D.
ms.assetid: a627523e-417a-40cd-82c0-4f0380a3a0b1
keywords:
- Direct2D, tutorial
- Direct2D, Walkthrough
- Direct2D, criando aplicativos
- Direct2D, aplicativos
- aplicativos para Direct2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d023e348e30b4e421ffe177f30c0c55a344fba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104566384"
---
# <a name="creating-a-simple-direct2d-application"></a><span data-ttu-id="0da21-108">Criando um aplicativo Direct2D simples</span><span class="sxs-lookup"><span data-stu-id="0da21-108">Creating a Simple Direct2D Application</span></span>

<span data-ttu-id="0da21-109">Este tópico orienta você pelo processo de criação da classe DemoApp, que cria uma janela e usa Direct2D para desenhar uma grade e dois retângulos.</span><span class="sxs-lookup"><span data-stu-id="0da21-109">This topic walks you through the process of creating the DemoApp class, which creates a window and uses Direct2D to draw a grid and two rectangles.</span></span> <span data-ttu-id="0da21-110">Neste tutorial, você aprenderá a criar recursos do Direct2D e desenhar formas básicas.</span><span class="sxs-lookup"><span data-stu-id="0da21-110">In this tutorial, you learn how to create Direct2D resources and draw basic shapes.</span></span> <span data-ttu-id="0da21-111">Você também aprenderá a estruturar seu aplicativo para melhorar o desempenho, minimizando a criação de recursos.</span><span class="sxs-lookup"><span data-stu-id="0da21-111">You also learn how to structure your application to enhance performance by minimizing resource creation.</span></span>

<span data-ttu-id="0da21-112">Para seguir o tutorial, você pode usar Microsoft Visual Studio 2008 para criar um projeto do Win32 e, em seguida, substituir o código no cabeçalho do aplicativo principal e no arquivo cpp pelo código descrito neste tutorial.</span><span class="sxs-lookup"><span data-stu-id="0da21-112">To follow the tutorial, you can use Microsoft Visual Studio 2008 to create a Win32 project and then replace the code in the main application header and cpp file with the code described in this tutorial.</span></span>

> [!Note]  
> <span data-ttu-id="0da21-113">Se você quiser criar um aplicativo da Windows Store que usa Direct2D, consulte o tópico [início rápido do Direct2D para Windows 8](direct2d-quickstart-with-device-context.md) .</span><span class="sxs-lookup"><span data-stu-id="0da21-113">If you want to create a Windows Store app that uses Direct2D, see the [Direct2D Quickstart for Windows 8](direct2d-quickstart-with-device-context.md) topic.</span></span>

 

<span data-ttu-id="0da21-114">Para obter uma visão geral das interfaces que você pode usar para criar conteúdo do Direct2D, consulte [visão geral da API do Direct2D](the-direct2d-api.md).</span><span class="sxs-lookup"><span data-stu-id="0da21-114">For an overview of the interfaces you can use to create Direct2D content, see the [Direct2D API Overview](the-direct2d-api.md).</span></span>

<span data-ttu-id="0da21-115">Este tutorial contém as seguintes partes:</span><span class="sxs-lookup"><span data-stu-id="0da21-115">This tutorial contains the following parts:</span></span>

-   [<span data-ttu-id="0da21-116">Parte 1: criar o cabeçalho DemoApp</span><span class="sxs-lookup"><span data-stu-id="0da21-116">Part 1: Create the DemoApp Header</span></span>](#part-1-create-the-demoapp-header)
-   [<span data-ttu-id="0da21-117">Parte 2: implementar a infraestrutura de classe</span><span class="sxs-lookup"><span data-stu-id="0da21-117">Part 2: Implement the Class Infrastructure</span></span>](#part-2-implement-the-class-infrastructure)
-   [<span data-ttu-id="0da21-118">Parte 3: criar recursos do Direct2D</span><span class="sxs-lookup"><span data-stu-id="0da21-118">Part 3: Create Direct2D Resources</span></span>](#part-3-create-direct2d-resources)
-   [<span data-ttu-id="0da21-119">Parte 4: renderizar conteúdo Direct2D</span><span class="sxs-lookup"><span data-stu-id="0da21-119">Part 4: Render Direct2D Content</span></span>](#part-4-render-direct2d-content)
-   [<span data-ttu-id="0da21-120">Resumo</span><span class="sxs-lookup"><span data-stu-id="0da21-120">Summary</span></span>](#summary)
-   [<span data-ttu-id="0da21-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0da21-121">Related topics</span></span>](#related-topics)

<span data-ttu-id="0da21-122">Após a conclusão, a classe DemoApp produz a saída mostrada na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="0da21-122">Upon completion, the DemoApp class produces the output shown in the following illustration.</span></span>

![ilustração de dois retângulos em um plano de fundo de grade](images/drawrectangleexample-small.png)

## <a name="part-1-create-the-demoapp-header"></a><span data-ttu-id="0da21-124">Parte 1: criar o cabeçalho DemoApp</span><span class="sxs-lookup"><span data-stu-id="0da21-124">Part 1: Create the DemoApp Header</span></span>

<span data-ttu-id="0da21-125">Nesta etapa, você configura seu aplicativo para usar o Direct2D adicionando os cabeçalhos e macros necessários.</span><span class="sxs-lookup"><span data-stu-id="0da21-125">In this step, you set up your application to use Direct2D by adding the necessary headers and macros.</span></span> <span data-ttu-id="0da21-126">Você também declara os métodos e membros de dados que serão usados nas partes posteriores deste tutorial.</span><span class="sxs-lookup"><span data-stu-id="0da21-126">You also declare the methods and data members you'll use in later parts of this tutorial.</span></span>

1.  <span data-ttu-id="0da21-127">No arquivo de cabeçalho do aplicativo, inclua os seguintes cabeçalhos usados com frequência.</span><span class="sxs-lookup"><span data-stu-id="0da21-127">In your application header file, include the following frequently used headers.</span></span>
```C++
    // Windows Header Files:
    #include <windows.h>

    // C RunTime Header Files:
    #include <stdlib.h>
    #include <malloc.h>
    #include <memory.h>
    #include <wchar.h>
    #include <math.h>

    #include <d2d1.h>
    #include <d2d1helper.h>
    #include <dwrite.h>
    #include <wincodec.h>
```

    

2.  <span data-ttu-id="0da21-128">Declare funções adicionais para liberar interfaces e macros para tratamento de erros e recuperar o endereço base do módulo.</span><span class="sxs-lookup"><span data-stu-id="0da21-128">Declare additional functions for releasing interfaces and macros for error handling and retrieving the module's base address.</span></span>
```C++
    template<class Interface>
    inline void SafeRelease(
        Interface **ppInterfaceToRelease
        )
    {
        if (*ppInterfaceToRelease != NULL)
        {
            (*ppInterfaceToRelease)->Release();

            (*ppInterfaceToRelease) = NULL;
        }
    }


    #ifndef Assert
    #if defined( DEBUG ) || defined( _DEBUG )
    #define Assert(b) do {if (!(b)) {OutputDebugStringA("Assert: " #b "\n");}} while(0)
    #else
    #define Assert(b)
    #endif //DEBUG || _DEBUG
    #endif



    #ifndef HINST_THISCOMPONENT
    EXTERN_C IMAGE_DOS_HEADER __ImageBase;
    #define HINST_THISCOMPONENT ((HINSTANCE)&__ImageBase)
    #endif
```

    

3.  <span data-ttu-id="0da21-129">Declare métodos para inicializar a classe, criar e descartar recursos, manipular o loop de mensagem, renderizar conteúdo e o procedimento do Windows.</span><span class="sxs-lookup"><span data-stu-id="0da21-129">Declare methods for initializing the class, creating and discarding resources, handling the message loop, rendering content, and the windows procedure.</span></span>
```C++
    class DemoApp
    {
    public:
        DemoApp();
        ~DemoApp();

        // Register the window class and call methods for instantiating drawing resources
        HRESULT Initialize();

        // Process and dispatch messages
        void RunMessageLoop();

    private:
        // Initialize device-independent resources.
        HRESULT CreateDeviceIndependentResources();

        // Initialize device-dependent resources.
        HRESULT CreateDeviceResources();

        // Release device-dependent resource.
        void DiscardDeviceResources();

        // Draw content.
        HRESULT OnRender();

        // Resize the render target.
        void OnResize(
            UINT width,
            UINT height
            );

        // The windows procedure.
        static LRESULT CALLBACK WndProc(
            HWND hWnd,
            UINT message,
            WPARAM wParam,
            LPARAM lParam
            );

    
};
```



    

4.  <span data-ttu-id="0da21-130">Declare ponteiros para um objeto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , um objeto [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) e dois objetos [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) como membros de classe.</span><span class="sxs-lookup"><span data-stu-id="0da21-130">Declare pointers for an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) object, an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) object, and two [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) objects as class members.</span></span>
```C++
    private:
    HWND m_hwnd;
    ID2D1Factory* m_pDirect2dFactory;
    ID2D1HwndRenderTarget* m_pRenderTarget;
    ID2D1SolidColorBrush* m_pLightSlateGrayBrush;
    ID2D1SolidColorBrush* m_pCornflowerBlueBrush;
```

    

## <a name="part-2-implement-the-class-infrastructure"></a><span data-ttu-id="0da21-131">Parte 2: implementar a infraestrutura de classe</span><span class="sxs-lookup"><span data-stu-id="0da21-131">Part 2: Implement the Class Infrastructure</span></span>

<span data-ttu-id="0da21-132">Nesta parte, você implementa o Construtor DemoApp e o destruidor, seus métodos de inicialização e loop de mensagem e a função WinMain.</span><span class="sxs-lookup"><span data-stu-id="0da21-132">In this part, you implement the DemoApp constructor and destructor, its initialization and message looping methods, and the WinMain function.</span></span> <span data-ttu-id="0da21-133">A maioria desses métodos tem a mesma aparência que aqueles encontrados em qualquer outro aplicativo Win32.</span><span class="sxs-lookup"><span data-stu-id="0da21-133">Most of these methods look the same as those found in any other Win32 application.</span></span> <span data-ttu-id="0da21-134">A única exceção é o método Initialize, que chama o método CreateDeviceIndependentResources (que você define na próxima parte) que cria vários recursos do Direct2D.</span><span class="sxs-lookup"><span data-stu-id="0da21-134">The only exception is the Initialize method, which calls the CreateDeviceIndependentResources method (which you define in the next part) that creates several Direct2D resources.</span></span>

1.  <span data-ttu-id="0da21-135">No arquivo de implementação de classe, implemente o construtor de classe e o destruidor.</span><span class="sxs-lookup"><span data-stu-id="0da21-135">In the class implementation file, implement the class constructor and destructor.</span></span> <span data-ttu-id="0da21-136">O construtor deve inicializar seus membros como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0da21-136">The constructor should initialize its members to **NULL**.</span></span> <span data-ttu-id="0da21-137">O destruidor deve liberar qualquer interface armazenada como membros da classe.</span><span class="sxs-lookup"><span data-stu-id="0da21-137">The destructor should release any interfaces stored as class members.</span></span>
```C++
    DemoApp::DemoApp() :
        m_hwnd(NULL),
        m_pDirect2dFactory(NULL),
        m_pRenderTarget(NULL),
        m_pLightSlateGrayBrush(NULL),
        m_pCornflowerBlueBrush(NULL)
    {
    }

    
DemoApp::~DemoApp()
    {
        SafeRelease(&m_pDirect2dFactory);
        SafeRelease(&m_pRenderTarget);
        SafeRelease(&m_pLightSlateGrayBrush);
        SafeRelease(&m_pCornflowerBlueBrush);

    }
```



    

2.  <span data-ttu-id="0da21-138">Implemente o método DemoApp:: RunMessageLoop que traduz e despacha mensagens.</span><span class="sxs-lookup"><span data-stu-id="0da21-138">Implement the DemoApp::RunMessageLoop method that translates and dispatches messages.</span></span>
```C++
    void DemoApp::RunMessageLoop()
    {
        MSG msg;

        while (GetMessage(&msg, NULL, 0, 0))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }
```

    

3.  <span data-ttu-id="0da21-139">Implemente o método Initialize que cria a janela, mostra-o e chama o método DemoApp:: CreateDeviceIndependentResources.</span><span class="sxs-lookup"><span data-stu-id="0da21-139">Implement the Initialize method that creates the window, shows it, and calls the DemoApp::CreateDeviceIndependentResources method.</span></span> <span data-ttu-id="0da21-140">Você implementa o método CreateDeviceIndependentResources na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="0da21-140">You implement the CreateDeviceIndependentResources method in the next section.</span></span>
```C++
    HRESULT DemoApp::Initialize()
    {
        HRESULT hr;

        // Initialize device-indpendent resources, such
        // as the Direct2D factory.
        hr = CreateDeviceIndependentResources();

        if (SUCCEEDED(hr))
        {
            // Register the window class.
            WNDCLASSEX wcex = { sizeof(WNDCLASSEX) };
            wcex.style         = CS_HREDRAW | CS_VREDRAW;
            wcex.lpfnWndProc   = DemoApp::WndProc;
            wcex.cbClsExtra    = 0;
            wcex.cbWndExtra    = sizeof(LONG_PTR);
            wcex.hInstance     = HINST_THISCOMPONENT;
            wcex.hbrBackground = NULL;
            wcex.lpszMenuName  = NULL;
            wcex.hCursor       = LoadCursor(NULL, IDI_APPLICATION);
            wcex.lpszClassName = L"D2DDemoApp";

            RegisterClassEx(&wcex);


            // Because the CreateWindow function takes its size in pixels,
            // obtain the system DPI and use it to scale the window size.
            FLOAT dpiX, dpiY;

            // The factory returns the current system DPI. This is also the value it will use
            // to create its own windows.
            m_pDirect2dFactory->GetDesktopDpi(&dpiX, &dpiY);


            // Create the window.
            m_hwnd = CreateWindow(
                L"D2DDemoApp",
                L"Direct2D Demo App",
                WS_OVERLAPPEDWINDOW,
                CW_USEDEFAULT,
                CW_USEDEFAULT,
                static_cast<UINT>(ceil(640.f * dpiX / 96.f)),
                static_cast<UINT>(ceil(480.f * dpiY / 96.f)),
                NULL,
                NULL,
                HINST_THISCOMPONENT,
                this
                );
            hr = m_hwnd ? S_OK : E_FAIL;
            if (SUCCEEDED(hr))
            {
                ShowWindow(m_hwnd, SW_SHOWNORMAL);
                UpdateWindow(m_hwnd);
            }
        }

        return hr;
    }
```

    

4.  <span data-ttu-id="0da21-141">Crie o método WinMain que serve como o ponto de entrada do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0da21-141">Create the WinMain method that serves as the application entry point.</span></span> <span data-ttu-id="0da21-142">Inicialize uma instância da classe DemoApp e inicie seu loop de mensagem.</span><span class="sxs-lookup"><span data-stu-id="0da21-142">Initialize an instance of the DemoApp class and begin its message loop.</span></span>
```C++
    int WINAPI WinMain(
        HINSTANCE /* hInstance */,
        HINSTANCE /* hPrevInstance */,
        LPSTR /* lpCmdLine */,
        int /* nCmdShow */
        )
    {
        // Use HeapSetInformation to specify that the process should
        // terminate if the heap manager detects an error in any heap used
        // by the process.
        // The return value is ignored, because we want to continue running in the
        // unlikely event that HeapSetInformation fails.
        HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

        if (SUCCEEDED(CoInitialize(NULL)))
        {
            {
                DemoApp app;

                if (SUCCEEDED(app.Initialize()))
                {
                    app.RunMessageLoop();
                }
            }
            CoUninitialize();
        }

        return 0;
    }
```

    

## <a name="part-3-create-direct2d-resources"></a><span data-ttu-id="0da21-143">Parte 3: criar recursos do Direct2D</span><span class="sxs-lookup"><span data-stu-id="0da21-143">Part 3: Create Direct2D Resources</span></span>

<span data-ttu-id="0da21-144">Nesta parte, você cria os recursos de Direct2D que você usa para desenhar.</span><span class="sxs-lookup"><span data-stu-id="0da21-144">In this part, you create the Direct2D resources that you use to draw.</span></span> <span data-ttu-id="0da21-145">O Direct2D fornece dois tipos de recursos: recursos independentes de dispositivo que podem durar pela duração do aplicativo e recursos dependentes do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0da21-145">Direct2D provides two types of resources: device-independent resources that can last for the duration of the application, and device-dependent resources.</span></span> <span data-ttu-id="0da21-146">Os recursos dependentes do dispositivo são associados a um determinado dispositivo de renderização e deixarão de funcionar se o dispositivo for removido.</span><span class="sxs-lookup"><span data-stu-id="0da21-146">Device-dependent resources are associated with a particular rendering device and will cease to function if that device is removed.</span></span>

1.  <span data-ttu-id="0da21-147">Implemente o método DemoApp:: CreateDeviceIndependentResources.</span><span class="sxs-lookup"><span data-stu-id="0da21-147">Implement the DemoApp::CreateDeviceIndependentResources method.</span></span> <span data-ttu-id="0da21-148">No método, crie um [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), um recurso independente de dispositivo, para criar outros recursos do Direct2D.</span><span class="sxs-lookup"><span data-stu-id="0da21-148">In the method, create an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), a device-independent resource, for creating other Direct2D resources.</span></span> <span data-ttu-id="0da21-149">Use o membro da classe **m \_ pDirect2DdFactory** para armazenar a fábrica.</span><span class="sxs-lookup"><span data-stu-id="0da21-149">Use the **m\_pDirect2DdFactory** class member to store the factory.</span></span>
```C++
    HRESULT DemoApp::CreateDeviceIndependentResources()
    {
        HRESULT hr = S_OK;

        // Create a Direct2D factory.
        hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

        return hr;
    }
```

    

2.  <span data-ttu-id="0da21-150">Implemente o método DemoApp:: CreateDeviceResources.</span><span class="sxs-lookup"><span data-stu-id="0da21-150">Implement the DemoApp::CreateDeviceResources method.</span></span> <span data-ttu-id="0da21-151">Esse método cria os recursos dependentes do dispositivo da janela, um destino de renderização e dois pincéis.</span><span class="sxs-lookup"><span data-stu-id="0da21-151">This method creates the window's device-dependent resources, a render target, and two brushes.</span></span> <span data-ttu-id="0da21-152">Recupere o tamanho da área do cliente e crie um [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) do mesmo tamanho que é processado para o **HWND** da janela.</span><span class="sxs-lookup"><span data-stu-id="0da21-152">Retrieve the size of the client area and create an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) of the same size that renders to the window's **HWND**.</span></span> <span data-ttu-id="0da21-153">Armazene o destino de renderização no membro da classe **m \_ pRenderTarget** .</span><span class="sxs-lookup"><span data-stu-id="0da21-153">Store the render target in the **m\_pRenderTarget** class member.</span></span>
```C++
            RECT rc;
            GetClientRect(m_hwnd, &rc);

            D2D1_SIZE_U size = D2D1::SizeU(
                rc.right - rc.left,
                rc.bottom - rc.top
                );

            // Create a Direct2D render target.
            hr = m_pDirect2dFactory->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(m_hwnd, size),
                &m_pRenderTarget
                );
    
```

    

3.  <span data-ttu-id="0da21-154">Use o destino render para criar um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) cinza e um-centáurea azul **ID2D1SolidColorBrush**.</span><span class="sxs-lookup"><span data-stu-id="0da21-154">Use the render target to create a gray [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) and a cornflower blue **ID2D1SolidColorBrush**.</span></span>
```C++
            if (SUCCEEDED(hr))
            {
                // Create a gray brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::LightSlateGray),
                    &m_pLightSlateGrayBrush
                    );
            }
            if (SUCCEEDED(hr))
            {
                // Create a blue brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::CornflowerBlue),
                    &m_pCornflowerBlueBrush
                    );
            }
```

    

4.  <span data-ttu-id="0da21-155">Como esse método será chamado repetidamente, adicione uma instrução If para verificar se o destino de renderização (**m \_ pRenderTarget** ) já existe.</span><span class="sxs-lookup"><span data-stu-id="0da21-155">Because this method will be called repeatedly, add an if statement to check whether the render target (**m\_pRenderTarget** ) already exists.</span></span> <span data-ttu-id="0da21-156">O código a seguir mostra o método CreateDeviceResources completo.</span><span class="sxs-lookup"><span data-stu-id="0da21-156">The following code shows the complete CreateDeviceResources method.</span></span>
```C++
    HRESULT DemoApp::CreateDeviceResources()
    {
        HRESULT hr = S_OK;

        if (!m_pRenderTarget)
        {
            RECT rc;
            GetClientRect(m_hwnd, &rc);

            D2D1_SIZE_U size = D2D1::SizeU(
                rc.right - rc.left,
                rc.bottom - rc.top
                );

            // Create a Direct2D render target.
            hr = m_pDirect2dFactory->CreateHwndRenderTarget(
                D2D1::RenderTargetProperties(),
                D2D1::HwndRenderTargetProperties(m_hwnd, size),
                &m_pRenderTarget
                );


            if (SUCCEEDED(hr))
            {
                // Create a gray brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::LightSlateGray),
                    &m_pLightSlateGrayBrush
                    );
            }
            if (SUCCEEDED(hr))
            {
                // Create a blue brush.
                hr = m_pRenderTarget->CreateSolidColorBrush(
                    D2D1::ColorF(D2D1::ColorF::CornflowerBlue),
                    &m_pCornflowerBlueBrush
                    );
            }
        }

        return hr;
    }
```

    

5.  <span data-ttu-id="0da21-157">Implemente o método DemoApp::D iscardDeviceResources.</span><span class="sxs-lookup"><span data-stu-id="0da21-157">Implement the DemoApp::DiscardDeviceResources method.</span></span> <span data-ttu-id="0da21-158">Nesse método, libere o destino de renderização e os dois pincéis que você criou no método DemoApp:: CreateDeviceResources.</span><span class="sxs-lookup"><span data-stu-id="0da21-158">In this method, release the render target and the two brushes you created in the DemoApp::CreateDeviceResources method.</span></span>
```C++
    void DemoApp::DiscardDeviceResources()
    {
        SafeRelease(&m_pRenderTarget);
        SafeRelease(&m_pLightSlateGrayBrush);
        SafeRelease(&m_pCornflowerBlueBrush);
    }
```

    

## <a name="part-4-render-direct2d-content"></a><span data-ttu-id="0da21-159">Parte 4: renderizar conteúdo Direct2D</span><span class="sxs-lookup"><span data-stu-id="0da21-159">Part 4: Render Direct2D Content</span></span>

<span data-ttu-id="0da21-160">Nesta parte, você implementa o procedimento do Windows, o método OnRender que pinta o conteúdo e o método OnResize que ajusta o tamanho do destino de renderização quando a janela é redimensionada.</span><span class="sxs-lookup"><span data-stu-id="0da21-160">In this part, you implement the windows procedure, the OnRender method that paints content, and the OnResize method that adjusts the size of the render target when the window is resized.</span></span>

1.  <span data-ttu-id="0da21-161">Implemente o método DemoApp:: WndProc para lidar com mensagens de janela.</span><span class="sxs-lookup"><span data-stu-id="0da21-161">Implement the DemoApp::WndProc method to handle window messages.</span></span> <span data-ttu-id="0da21-162">Para a mensagem de [**\_ tamanho do WM**](../winmsg/wm-size.md) , chame o método demoApp:: OnResize e passe-o para a nova largura e altura.</span><span class="sxs-lookup"><span data-stu-id="0da21-162">For the [**WM\_SIZE**](../winmsg/wm-size.md) message, call the DemoApp::OnResize method and pass it the new width and height.</span></span> <span data-ttu-id="0da21-163">Para as mensagens do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) e do [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) , chame o método demoApp:: OnRender para pintar a janela.</span><span class="sxs-lookup"><span data-stu-id="0da21-163">For the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) and [**WM\_DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) messages, call the DemoApp::OnRender method to paint the window.</span></span> <span data-ttu-id="0da21-164">Você implementa os métodos OnRender e OnResize nas etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="0da21-164">You implement the OnRender and OnResize methods in the steps that follow.</span></span>
```C++
    LRESULT CALLBACK DemoApp::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
    {
        LRESULT result = 0;

        if (message == WM_CREATE)
        {
            LPCREATESTRUCT pcs = (LPCREATESTRUCT)lParam;
            DemoApp *pDemoApp = (DemoApp *)pcs->lpCreateParams;

            ::SetWindowLongPtrW(
                hwnd,
                GWLP_USERDATA,
                reinterpret_cast<LONG_PTR>(pDemoApp)
                );

            result = 1;
        }
        else
        {
            DemoApp *pDemoApp = reinterpret_cast<DemoApp *>(static_cast<LONG_PTR>(
                ::GetWindowLongPtrW(
                    hwnd,
                    GWLP_USERDATA
                    )));

            bool wasHandled = false;

            if (pDemoApp)
            {
                switch (message)
                {
                case WM_SIZE:
                    {
                        UINT width = LOWORD(lParam);
                        UINT height = HIWORD(lParam);
                        pDemoApp->OnResize(width, height);
                    }
                    result = 0;
                    wasHandled = true;
                    break;

                case WM_DISPLAYCHANGE:
                    {
                        InvalidateRect(hwnd, NULL, FALSE);
                    }
                    result = 0;
                    wasHandled = true;
                    break;

                case WM_PAINT:
                    {
                        pDemoApp->OnRender();
                        ValidateRect(hwnd, NULL);
                    }
                    result = 0;
                    wasHandled = true;
                    break;

                case WM_DESTROY:
                    {
                        PostQuitMessage(0);
                    }
                    result = 1;
                    wasHandled = true;
                    break;
                }
            }

            if (!wasHandled)
            {
                result = DefWindowProc(hwnd, message, wParam, lParam);
            }
        }

        return result;
    }
    
```

    

2.  <span data-ttu-id="0da21-165">Implemente o método DemoApp:: OnRender.</span><span class="sxs-lookup"><span data-stu-id="0da21-165">Implement the DemoApp::OnRender method.</span></span> <span data-ttu-id="0da21-166">Primeiro, crie um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0da21-166">First, create an **HRESULT**.</span></span> <span data-ttu-id="0da21-167">Em seguida, chame o método CreateDeviceResource.</span><span class="sxs-lookup"><span data-stu-id="0da21-167">Then call the CreateDeviceResource method.</span></span> <span data-ttu-id="0da21-168">Esse método é chamado toda vez que a janela é pintada.</span><span class="sxs-lookup"><span data-stu-id="0da21-168">This method is called every time the window is painted.</span></span> <span data-ttu-id="0da21-169">Lembre-se de que, na etapa 4 da parte 3, você adicionou uma instrução **If** para impedir que o método faça qualquer trabalho se o destino de renderização já existir.</span><span class="sxs-lookup"><span data-stu-id="0da21-169">Recall that, in step 4 of Part 3, you added an **if** statement to prevent the method from doing any work if the render target already exists.</span></span>
```C++
    HRESULT DemoApp::OnRender()
    {
        HRESULT hr = S_OK;

        hr = CreateDeviceResources();
```

    

3.  <span data-ttu-id="0da21-170">Verifique se o método CreateDeviceResource foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0da21-170">Verify that the CreateDeviceResource method succeeded.</span></span> <span data-ttu-id="0da21-171">Se não tiver, não realize nenhum desenho.</span><span class="sxs-lookup"><span data-stu-id="0da21-171">If it didn't, don't perform any drawing.</span></span>
```C++
        if (SUCCEEDED(hr))
        {
```

    

4.  <span data-ttu-id="0da21-172">Dentro da instrução **If** que você acabou de criar, inicie o desenho chamando o método BeginDraw do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="0da21-172">Inside the **if** statement you just created, initiate drawing by calling the render target's BeginDraw method.</span></span> <span data-ttu-id="0da21-173">Defina a transformação do destino de renderização para a matriz de identidade e desmarque a janela.</span><span class="sxs-lookup"><span data-stu-id="0da21-173">Set the render target's transform to the identity matrix, and clear the window.</span></span>
```C++
            m_pRenderTarget->BeginDraw();

            m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

            m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));
    
```

    

5.  <span data-ttu-id="0da21-174">Recupere o tamanho da área de desenho.</span><span class="sxs-lookup"><span data-stu-id="0da21-174">Retrieve the size of the drawing area.</span></span>
```C++
            D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
```

    

6.  <span data-ttu-id="0da21-175">Desenhe um plano **de fundo de** grade usando um loop for e o método [**DrawLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawline) do destino render para desenhar uma série de linhas.</span><span class="sxs-lookup"><span data-stu-id="0da21-175">Draw a grid background by using a **for** loop and the render target's [**DrawLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawline) method to draw a series of lines.</span></span>
```C++
            // Draw a grid background.
            int width = static_cast<int>(rtSize.width);
            int height = static_cast<int>(rtSize.height);

            for (int x = 0; x < width; x += 10)
            {
                m_pRenderTarget->DrawLine(
                    D2D1::Point2F(static_cast<FLOAT>(x), 0.0f),
                    D2D1::Point2F(static_cast<FLOAT>(x), rtSize.height),
                    m_pLightSlateGrayBrush,
                    0.5f
                    );
            }

            for (int y = 0; y < height; y += 10)
            {
                m_pRenderTarget->DrawLine(
                    D2D1::Point2F(0.0f, static_cast<FLOAT>(y)),
                    D2D1::Point2F(rtSize.width, static_cast<FLOAT>(y)),
                    m_pLightSlateGrayBrush,
                    0.5f
                    );
            }
```

    

7.  <span data-ttu-id="0da21-176">Crie dois primitivos de retângulo que são centralizados na tela.</span><span class="sxs-lookup"><span data-stu-id="0da21-176">Create two rectangle primitives that are centered on the screen.</span></span>
```C++
            // Draw two rectangles.
            D2D1_RECT_F rectangle1 = D2D1::RectF(
                rtSize.width/2 - 50.0f,
                rtSize.height/2 - 50.0f,
                rtSize.width/2 + 50.0f,
                rtSize.height/2 + 50.0f
                );

            D2D1_RECT_F rectangle2 = D2D1::RectF(
                rtSize.width/2 - 100.0f,
                rtSize.height/2 - 100.0f,
                rtSize.width/2 + 100.0f,
                rtSize.height/2 + 100.0f
                );
    
```

    

8.  <span data-ttu-id="0da21-177">Use o método [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) do destino de renderização para pintar o interior do primeiro retângulo com o pincel cinza.</span><span class="sxs-lookup"><span data-stu-id="0da21-177">Use the render target's [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) method to paint the interior of the first rectangle with the gray brush.</span></span>
```C++
            // Draw a filled rectangle.
            m_pRenderTarget->FillRectangle(&rectangle1, m_pLightSlateGrayBrush);
```

    

9.  <span data-ttu-id="0da21-178">Use o método [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) do destino de renderização para pintar o contorno do segundo retângulo com o pincel Azul-centáurea.</span><span class="sxs-lookup"><span data-stu-id="0da21-178">Use the render target's [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method to paint the outline of the second rectangle with the cornflower blue brush.</span></span>
```C++
            // Draw the outline of a rectangle.
            m_pRenderTarget->DrawRectangle(&rectangle2, m_pCornflowerBlueBrush);
```

    

10. <span data-ttu-id="0da21-179">Chame o método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="0da21-179">Call the render target's [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="0da21-180">O método **EndDraw** retorna um **HRESULT** para indicar se as operações de desenho foram bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="0da21-180">The **EndDraw** method returns an **HRESULT** to indicate whether the drawing operations were successful.</span></span> <span data-ttu-id="0da21-181">Feche a instrução **If** que você iniciou na etapa 3.</span><span class="sxs-lookup"><span data-stu-id="0da21-181">Close the **if** statement you began in Step 3.</span></span>
```C++
            hr = m_pRenderTarget->EndDraw();
        }
```

    

11. <span data-ttu-id="0da21-182">Verifique o **HRESULT** retornado por [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span><span class="sxs-lookup"><span data-stu-id="0da21-182">Check the **HRESULT** returned by [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span> <span data-ttu-id="0da21-183">Se ele indicar que o destino de renderização precisa ser recriado, chame o método DemoApp::D iscardDeviceResources para liberá-lo; Ela será recriada na próxima vez em que a janela receber uma mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) ou do [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) .</span><span class="sxs-lookup"><span data-stu-id="0da21-183">If it indicates that the render target needs to be recreated, call the DemoApp::DiscardDeviceResources method to release it; it will be recreated the next time the window receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) or [**WM\_DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) message.</span></span>
```C++
        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
```

    

12. <span data-ttu-id="0da21-184">Retorne o **HRESULT** e feche o método.</span><span class="sxs-lookup"><span data-stu-id="0da21-184">Return the **HRESULT** and close the method.</span></span>
```C++
        return hr;
    }
```

    

13. <span data-ttu-id="0da21-185">Implemente o método DemoApp:: OnResize para redimensionar o destino de renderização para o novo tamanho da janela.</span><span class="sxs-lookup"><span data-stu-id="0da21-185">Implement the DemoApp::OnResize method so that it resizes the render target to the new size of the window.</span></span>
```C++
    void DemoApp::OnResize(UINT width, UINT height)
    {
        if (m_pRenderTarget)
        {
            // Note: This method can fail, but it's okay to ignore the
            // error here, because the error will be returned again
            // the next time EndDraw is called.
            m_pRenderTarget->Resize(D2D1::SizeU(width, height));
        }
    }
```

    

<span data-ttu-id="0da21-186">Você concluiu o tutorial.</span><span class="sxs-lookup"><span data-stu-id="0da21-186">You've completed the tutorial.</span></span>

> [!Note]  
> <span data-ttu-id="0da21-187">Para usar o Direct2D, verifique se o aplicativo inclui o arquivo de cabeçalho d2d1. h e se compila em relação à biblioteca d2d1. lib.</span><span class="sxs-lookup"><span data-stu-id="0da21-187">To use Direct2D, ensure that your application includes the d2d1.h header file and compiles against the d2d1.lib library.</span></span> <span data-ttu-id="0da21-188">Você pode encontrar d2d1. h e d2d1. lib no [SDK (Software Development Kit) do Windows para Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="0da21-188">You can find d2d1.h and d2d1.lib in [Windows Software Development Kit (SDK) for Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).</span></span>

 

## <a name="summary"></a><span data-ttu-id="0da21-189">Resumo</span><span class="sxs-lookup"><span data-stu-id="0da21-189">Summary</span></span>

<span data-ttu-id="0da21-190">Neste tutorial, você aprendeu a criar recursos do Direct2D e a desenhar formas básicas.</span><span class="sxs-lookup"><span data-stu-id="0da21-190">In this tutorial, you learned how to create Direct2D resources and draw basic shapes.</span></span> <span data-ttu-id="0da21-191">Você também aprendeu como estruturar seu aplicativo para melhorar o desempenho, minimizando a criação de recursos.</span><span class="sxs-lookup"><span data-stu-id="0da21-191">You also learned how to structure your application to enhance performance by minimizing resource creation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0da21-192">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0da21-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0da21-193">Visão geral de API do Direct2D</span><span class="sxs-lookup"><span data-stu-id="0da21-193">Direct2D API Overview</span></span>](the-direct2d-api.md)
</dt> <dt>

[<span data-ttu-id="0da21-194">Melhorando o desempenho do Direct2D</span><span class="sxs-lookup"><span data-stu-id="0da21-194">Improving the Performance of Direct2D</span></span>](improving-direct2d-performance.md)
</dt> </dl>

 

 