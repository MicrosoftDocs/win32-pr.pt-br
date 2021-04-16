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
# <a name="creating-a-simple-direct2d-application"></a>Criando um aplicativo Direct2D simples

Este tópico orienta você pelo processo de criação da classe DemoApp, que cria uma janela e usa Direct2D para desenhar uma grade e dois retângulos. Neste tutorial, você aprenderá a criar recursos do Direct2D e desenhar formas básicas. Você também aprenderá a estruturar seu aplicativo para melhorar o desempenho, minimizando a criação de recursos.

Para seguir o tutorial, você pode usar Microsoft Visual Studio 2008 para criar um projeto do Win32 e, em seguida, substituir o código no cabeçalho do aplicativo principal e no arquivo cpp pelo código descrito neste tutorial.

> [!Note]  
> Se você quiser criar um aplicativo da Windows Store que usa Direct2D, consulte o tópico [início rápido do Direct2D para Windows 8](direct2d-quickstart-with-device-context.md) .

 

Para obter uma visão geral das interfaces que você pode usar para criar conteúdo do Direct2D, consulte [visão geral da API do Direct2D](the-direct2d-api.md).

Este tutorial contém as seguintes partes:

-   [Parte 1: criar o cabeçalho DemoApp](#part-1-create-the-demoapp-header)
-   [Parte 2: implementar a infraestrutura de classe](#part-2-implement-the-class-infrastructure)
-   [Parte 3: criar recursos do Direct2D](#part-3-create-direct2d-resources)
-   [Parte 4: renderizar conteúdo Direct2D](#part-4-render-direct2d-content)
-   [Resumo](#summary)
-   [Tópicos relacionados](#related-topics)

Após a conclusão, a classe DemoApp produz a saída mostrada na ilustração a seguir.

![ilustração de dois retângulos em um plano de fundo de grade](images/drawrectangleexample-small.png)

## <a name="part-1-create-the-demoapp-header"></a>Parte 1: criar o cabeçalho DemoApp

Nesta etapa, você configura seu aplicativo para usar o Direct2D adicionando os cabeçalhos e macros necessários. Você também declara os métodos e membros de dados que serão usados nas partes posteriores deste tutorial.

1.  No arquivo de cabeçalho do aplicativo, inclua os seguintes cabeçalhos usados com frequência.
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

    

2.  Declare funções adicionais para liberar interfaces e macros para tratamento de erros e recuperar o endereço base do módulo.
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

    

3.  Declare métodos para inicializar a classe, criar e descartar recursos, manipular o loop de mensagem, renderizar conteúdo e o procedimento do Windows.
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



    

4.  Declare ponteiros para um objeto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) , um objeto [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) e dois objetos [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) como membros de classe.
```C++
    private:
    HWND m_hwnd;
    ID2D1Factory* m_pDirect2dFactory;
    ID2D1HwndRenderTarget* m_pRenderTarget;
    ID2D1SolidColorBrush* m_pLightSlateGrayBrush;
    ID2D1SolidColorBrush* m_pCornflowerBlueBrush;
```

    

## <a name="part-2-implement-the-class-infrastructure"></a>Parte 2: implementar a infraestrutura de classe

Nesta parte, você implementa o Construtor DemoApp e o destruidor, seus métodos de inicialização e loop de mensagem e a função WinMain. A maioria desses métodos tem a mesma aparência que aqueles encontrados em qualquer outro aplicativo Win32. A única exceção é o método Initialize, que chama o método CreateDeviceIndependentResources (que você define na próxima parte) que cria vários recursos do Direct2D.

1.  No arquivo de implementação de classe, implemente o construtor de classe e o destruidor. O construtor deve inicializar seus membros como **NULL**. O destruidor deve liberar qualquer interface armazenada como membros da classe.
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



    

2.  Implemente o método DemoApp:: RunMessageLoop que traduz e despacha mensagens.
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

    

3.  Implemente o método Initialize que cria a janela, mostra-o e chama o método DemoApp:: CreateDeviceIndependentResources. Você implementa o método CreateDeviceIndependentResources na próxima seção.
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

    

4.  Crie o método WinMain que serve como o ponto de entrada do aplicativo. Inicialize uma instância da classe DemoApp e inicie seu loop de mensagem.
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

    

## <a name="part-3-create-direct2d-resources"></a>Parte 3: criar recursos do Direct2D

Nesta parte, você cria os recursos de Direct2D que você usa para desenhar. O Direct2D fornece dois tipos de recursos: recursos independentes de dispositivo que podem durar pela duração do aplicativo e recursos dependentes do dispositivo. Os recursos dependentes do dispositivo são associados a um determinado dispositivo de renderização e deixarão de funcionar se o dispositivo for removido.

1.  Implemente o método DemoApp:: CreateDeviceIndependentResources. No método, crie um [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), um recurso independente de dispositivo, para criar outros recursos do Direct2D. Use o membro da classe **m \_ pDirect2DdFactory** para armazenar a fábrica.
```C++
    HRESULT DemoApp::CreateDeviceIndependentResources()
    {
        HRESULT hr = S_OK;

        // Create a Direct2D factory.
        hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

        return hr;
    }
```

    

2.  Implemente o método DemoApp:: CreateDeviceResources. Esse método cria os recursos dependentes do dispositivo da janela, um destino de renderização e dois pincéis. Recupere o tamanho da área do cliente e crie um [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) do mesmo tamanho que é processado para o **HWND** da janela. Armazene o destino de renderização no membro da classe **m \_ pRenderTarget** .
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

    

3.  Use o destino render para criar um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) cinza e um-centáurea azul **ID2D1SolidColorBrush**.
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

    

4.  Como esse método será chamado repetidamente, adicione uma instrução If para verificar se o destino de renderização (**m \_ pRenderTarget** ) já existe. O código a seguir mostra o método CreateDeviceResources completo.
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

    

5.  Implemente o método DemoApp::D iscardDeviceResources. Nesse método, libere o destino de renderização e os dois pincéis que você criou no método DemoApp:: CreateDeviceResources.
```C++
    void DemoApp::DiscardDeviceResources()
    {
        SafeRelease(&m_pRenderTarget);
        SafeRelease(&m_pLightSlateGrayBrush);
        SafeRelease(&m_pCornflowerBlueBrush);
    }
```

    

## <a name="part-4-render-direct2d-content"></a>Parte 4: renderizar conteúdo Direct2D

Nesta parte, você implementa o procedimento do Windows, o método OnRender que pinta o conteúdo e o método OnResize que ajusta o tamanho do destino de renderização quando a janela é redimensionada.

1.  Implemente o método DemoApp:: WndProc para lidar com mensagens de janela. Para a mensagem de [**\_ tamanho do WM**](../winmsg/wm-size.md) , chame o método demoApp:: OnResize e passe-o para a nova largura e altura. Para as mensagens do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) e do [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) , chame o método demoApp:: OnRender para pintar a janela. Você implementa os métodos OnRender e OnResize nas etapas a seguir.
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

    

2.  Implemente o método DemoApp:: OnRender. Primeiro, crie um **HRESULT**. Em seguida, chame o método CreateDeviceResource. Esse método é chamado toda vez que a janela é pintada. Lembre-se de que, na etapa 4 da parte 3, você adicionou uma instrução **If** para impedir que o método faça qualquer trabalho se o destino de renderização já existir.
```C++
    HRESULT DemoApp::OnRender()
    {
        HRESULT hr = S_OK;

        hr = CreateDeviceResources();
```

    

3.  Verifique se o método CreateDeviceResource foi bem-sucedido. Se não tiver, não realize nenhum desenho.
```C++
        if (SUCCEEDED(hr))
        {
```

    

4.  Dentro da instrução **If** que você acabou de criar, inicie o desenho chamando o método BeginDraw do destino de renderização. Defina a transformação do destino de renderização para a matriz de identidade e desmarque a janela.
```C++
            m_pRenderTarget->BeginDraw();

            m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

            m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));
    
```

    

5.  Recupere o tamanho da área de desenho.
```C++
            D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
```

    

6.  Desenhe um plano **de fundo de** grade usando um loop for e o método [**DrawLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawline) do destino render para desenhar uma série de linhas.
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

    

7.  Crie dois primitivos de retângulo que são centralizados na tela.
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

    

8.  Use o método [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) do destino de renderização para pintar o interior do primeiro retângulo com o pincel cinza.
```C++
            // Draw a filled rectangle.
            m_pRenderTarget->FillRectangle(&rectangle1, m_pLightSlateGrayBrush);
```

    

9.  Use o método [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) do destino de renderização para pintar o contorno do segundo retângulo com o pincel Azul-centáurea.
```C++
            // Draw the outline of a rectangle.
            m_pRenderTarget->DrawRectangle(&rectangle2, m_pCornflowerBlueBrush);
```

    

10. Chame o método [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) do destino de renderização. O método **EndDraw** retorna um **HRESULT** para indicar se as operações de desenho foram bem-sucedidas. Feche a instrução **If** que você iniciou na etapa 3.
```C++
            hr = m_pRenderTarget->EndDraw();
        }
```

    

11. Verifique o **HRESULT** retornado por [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw). Se ele indicar que o destino de renderização precisa ser recriado, chame o método DemoApp::D iscardDeviceResources para liberá-lo; Ela será recriada na próxima vez em que a janela receber uma mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) ou do [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) .
```C++
        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
```

    

12. Retorne o **HRESULT** e feche o método.
```C++
        return hr;
    }
```

    

13. Implemente o método DemoApp:: OnResize para redimensionar o destino de renderização para o novo tamanho da janela.
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

    

Você concluiu o tutorial.

> [!Note]  
> Para usar o Direct2D, verifique se o aplicativo inclui o arquivo de cabeçalho d2d1. h e se compila em relação à biblioteca d2d1. lib. Você pode encontrar d2d1. h e d2d1. lib no [SDK (Software Development Kit) do Windows para Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).

 

## <a name="summary"></a>Resumo

Neste tutorial, você aprendeu a criar recursos do Direct2D e a desenhar formas básicas. Você também aprendeu como estruturar seu aplicativo para melhorar o desempenho, minimizando a criação de recursos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral de API do Direct2D](the-direct2d-api.md)
</dt> <dt>

[Melhorando o desempenho do Direct2D](improving-direct2d-performance.md)
</dt> </dl>

 

 