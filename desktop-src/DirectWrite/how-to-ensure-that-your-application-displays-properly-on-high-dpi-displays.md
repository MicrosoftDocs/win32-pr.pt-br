---
title: Como garantir que seu aplicativo seja exibido corretamente em monitores de alto DPI (DirectWrite)
description: Descreve como garantir que seu aplicativo crie uma janela que é exibida corretamente em monitores de alto DPI.
ms.assetid: d174a337-c98e-46c7-86d2-c208900882d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71166d312fe666644c683fe2ece7dd3ced59f765
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406419"
---
# <a name="how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays"></a><span data-ttu-id="18e03-103">Como garantir que seu aplicativo seja exibido corretamente em monitores de alto DPI</span><span class="sxs-lookup"><span data-stu-id="18e03-103">How to Ensure That Your Application Displays Properly on High-DPI Displays</span></span>

<span data-ttu-id="18e03-104">Embora [DirectWrite](direct-write-portal.md) atenda a muitos problemas de alto dpi, há duas etapas que você deve seguir para garantir que seu aplicativo funcione corretamente em monitores de alto dpi:</span><span class="sxs-lookup"><span data-stu-id="18e03-104">Although [DirectWrite](direct-write-portal.md) addresses many high-DPI issues for you, there are two steps you should take to ensure that your application works properly on high-DPI displays:</span></span>

-   [<span data-ttu-id="18e03-105">Etapa 1: usar o DPI do sistema ao criar o Windows</span><span class="sxs-lookup"><span data-stu-id="18e03-105">Step 1: Use the System DPI When Creating Windows</span></span>](#step-1-use-the-system-dpi-when-creating-windows)
    -   [<span data-ttu-id="18e03-106">Direct2D</span><span class="sxs-lookup"><span data-stu-id="18e03-106">Direct2D</span></span>](#direct2d)
    -   [<span data-ttu-id="18e03-107">GRÁFICA</span><span class="sxs-lookup"><span data-stu-id="18e03-107">GDI</span></span>](#gdi)
-   [<span data-ttu-id="18e03-108">Etapa 2: declarar que o aplicativo reconhece DPI</span><span class="sxs-lookup"><span data-stu-id="18e03-108">Step 2: Declare That the Application is DPI-Aware</span></span>](#step-2-declare-that-the-application-is-dpi-aware)
-   [<span data-ttu-id="18e03-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="18e03-109">Related topics</span></span>](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a><span data-ttu-id="18e03-110">Etapa 1: usar o DPI do sistema ao criar o Windows</span><span class="sxs-lookup"><span data-stu-id="18e03-110">Step 1: Use the System DPI When Creating Windows</span></span>

<span data-ttu-id="18e03-111">Isso pode ser feito usando o [Direct2D](../direct2d/direct2d-portal.md) ou o [GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="18e03-111">This can be done by using [Direct2D](../direct2d/direct2d-portal.md) or by using [GDI](../gdi/windows-gdi.md).</span></span>

### <a name="direct2d"></a><span data-ttu-id="18e03-112">Direct2D</span><span class="sxs-lookup"><span data-stu-id="18e03-112">Direct2D</span></span>

<span data-ttu-id="18e03-113">A interface [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) fornece o método [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) para recuperar o DPI do sistema.</span><span class="sxs-lookup"><span data-stu-id="18e03-113">The [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface provides the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method for retrieving the system DPI.</span></span> <span data-ttu-id="18e03-114">Ele fornece as dimensões horizontal e vertical da exibição em pontos por polegada (DPI).</span><span class="sxs-lookup"><span data-stu-id="18e03-114">It provides the horizontal and vertical dimensions of the display in dots per inch (DPI).</span></span> <span data-ttu-id="18e03-115">Para usar esses valores para definir a largura de uma janela, use a seguinte fórmula:</span><span class="sxs-lookup"><span data-stu-id="18e03-115">To use these values to set the width of a window, use the following formula:</span></span>

<span data-ttu-id="18e03-116"><*dpi* >  \* horizontal  < *largura*, em pixels>/<*dpi horizontal padrão*></span><span class="sxs-lookup"><span data-stu-id="18e03-116"><*horizontal DPI*> \* <*width*, in pixels> / <*default horizontal DPI*></span></span>

<span data-ttu-id="18e03-117">... em que *dpi horizontal* é o valor recuperado por GetDpi e o *dpi horizontal padrão* é 96.</span><span class="sxs-lookup"><span data-stu-id="18e03-117">...where *horizontal DPI* is the value retrived by GetDpi and *default horizontal DPI* is 96.</span></span> <span data-ttu-id="18e03-118">A fórmula é semelhante ao tamanho vertical:</span><span class="sxs-lookup"><span data-stu-id="18e03-118">The formula is similar for the vertical size:</span></span>

<span data-ttu-id="18e03-119"><*dpi* >  \* vertical  < *altura*, em pixels>/<*dpi vertical padrão*></span><span class="sxs-lookup"><span data-stu-id="18e03-119"><*vertical DPI*> \* <*height*, in pixels> / <*default vertical DPI*></span></span>

<span data-ttu-id="18e03-120">... em que *dpi vertical* é o valor recuperado pelo método [**GETDESKTOPDPI**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) e o *dpi vertical padrão* é 96.</span><span class="sxs-lookup"><span data-stu-id="18e03-120">...where *vertical DPI* is the value retrieved by the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method and *default vertical DPI* is 96.</span></span>

<span data-ttu-id="18e03-121">O código a seguir usa o método [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) para criar uma janela 640 x 480, dimensionada para o DPI do sistema.</span><span class="sxs-lookup"><span data-stu-id="18e03-121">The following code uses the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method to create a 640 x 480 window, scaled to the system DPI.</span></span> <span data-ttu-id="18e03-122">(No código a seguir, *m \_ spD2DFactory* é um ponteiro inteligente para uma instância de [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) .)</span><span class="sxs-lookup"><span data-stu-id="18e03-122">(In the following code, *m\_spD2DFactory* is a smart pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) instance.)</span></span>


```C++
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
```



### <a name="gdi"></a><span data-ttu-id="18e03-123">GDI</span><span class="sxs-lookup"><span data-stu-id="18e03-123">GDI</span></span>

<span data-ttu-id="18e03-124">O [GDI](interoperating-with-gdi.md) fornece a função [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) para recuperar informações do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18e03-124">[GDI](interoperating-with-gdi.md) provides the [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) function for retrieving device information.</span></span> <span data-ttu-id="18e03-125">Você pode recuperar informações de DPI passando os valores de índice *LOGPIXELSX* e *LOGPIXELSY* .</span><span class="sxs-lookup"><span data-stu-id="18e03-125">You can retrieve DPI information by passing the *LOGPIXELSX* and *LOGPIXELSY* index values.</span></span> <span data-ttu-id="18e03-126">A fórmula para determinar o tamanho horizontal e vertical de uma janela é a mesma do exemplo [Direct2D](../direct2d/direct2d-portal.md) acima.</span><span class="sxs-lookup"><span data-stu-id="18e03-126">The formula for determining the horizontal and vertical size of a window is the same as with the [Direct2D](../direct2d/direct2d-portal.md) example above.</span></span>

<span data-ttu-id="18e03-127">O código a seguir usa a função [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) para criar uma janela 640 x 480, dimensionada para o DPI do sistema.</span><span class="sxs-lookup"><span data-stu-id="18e03-127">The following code uses the [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) function to create a 640 x 480 window, scaled to the system DPI.</span></span>


```C++
FLOAT dpiX, dpiY;

HDC screen = GetDC(0);
dpiX = static_cast<FLOAT>(GetDeviceCaps(screen, LOGPIXELSX));
dpiY = static_cast<FLOAT>(GetDeviceCaps(screen, LOGPIXELSY));
ReleaseDC(0, screen);

hWnd = CreateWindow(
         TEXT("DirectWriteApp"),
         TEXT("DirectWrite Demo App"),
         WS_OVERLAPPEDWINDOW,
         CW_USEDEFAULT,
         CW_USEDEFAULT,
         static_cast<INT>(dpiX * 640.f / 96.f),
         static_cast<INT>(dpiY * 480.f / 96.f),
         NULL,
         NULL,
         hInstance,
         NULL
         );
```



## <a name="step-2-declare-that-the-application-is-dpi-aware"></a><span data-ttu-id="18e03-128">Etapa 2: declarar que o aplicativo está DPI-Aware</span><span class="sxs-lookup"><span data-stu-id="18e03-128">Step 2: Declare That the Application is DPI-Aware</span></span>

<span data-ttu-id="18e03-129">Quando um aplicativo se declara para ser compatível com DPI, é uma instrução que especifica que o aplicativo se comporta bem em configurações de DPI até 200 DPI.</span><span class="sxs-lookup"><span data-stu-id="18e03-129">When an application declares itself to be DPI-aware, it is a statement specifying that the application behaves well at DPI settings up to 200 DPI.</span></span> <span data-ttu-id="18e03-130">No Windows Vista e no Windows 7, quando a virtualização de DPI está habilitada, os aplicativos que não têm reconhecimento de DPI são dimensionados e os aplicativos recebem dados virtualizados das APIs do sistema, como a função [**GetSystemMetric**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) .</span><span class="sxs-lookup"><span data-stu-id="18e03-130">In Windows Vista and Windows 7, when DPI virtualization is enabled, applications that are not DPI-aware are scaled, and applications receive virtualized data from the system APIs, such as the [**GetSystemMetric**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function.</span></span> <span data-ttu-id="18e03-131">Para declarar que seu aplicativo reconhece DPI, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="18e03-131">To declare that your application is DPI-aware, complete the following steps.</span></span>

1.  <span data-ttu-id="18e03-132">Crie um arquivo chamado DeclareDPIAware. manifest.</span><span class="sxs-lookup"><span data-stu-id="18e03-132">Create a file called DeclareDPIAware.manifest.</span></span>
2.  <span data-ttu-id="18e03-133">Copie o seguinte XML para o arquivo e salve-o:</span><span class="sxs-lookup"><span data-stu-id="18e03-133">Copy the following xml into the file and save it:</span></span>
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  <span data-ttu-id="18e03-134">No arquivo. vcproj do projeto, adicione a seguinte entrada dentro de cada elemento de configuração em VisualStudioProject/configurações:</span><span class="sxs-lookup"><span data-stu-id="18e03-134">In the project's .vcproj file, add the following entry inside each Configuration element under VisualStudioProject/Configurations:</span></span>
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a><span data-ttu-id="18e03-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="18e03-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18e03-136">Direct2D e alto DPI</span><span class="sxs-lookup"><span data-stu-id="18e03-136">Direct2D and High-DPI</span></span>](../direct2d/direct2d-and-high-dpi.md)
</dt> </dl>

 

 