---
title: Exibindo corretamente em uma exibição de alto DPI
description: Descreve as etapas para criar uma janela para seu aplicativo que é exibida corretamente em exibições de alto DPI.
ms.assetid: 72a4b076-1cf0-4dc9-bd75-43b5173fc2a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd45b4b654556fc251575410cc11f9b66961263
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406149"
---
# <a name="displaying-properly-on-a-high-dpi-display"></a><span data-ttu-id="f2cd1-103">Exibindo corretamente em uma exibição de alto DPI</span><span class="sxs-lookup"><span data-stu-id="f2cd1-103">Displaying properly on a high-DPI display</span></span>

<span data-ttu-id="f2cd1-104">Embora o Direct2D aborda muitos problemas de DPI alto para você, há duas etapas que você deve seguir para garantir que seu aplicativo funcione corretamente em exibições de alto DPI:</span><span class="sxs-lookup"><span data-stu-id="f2cd1-104">Although Direct2D addresses many high-DPI issues for you, there are two steps you should take to ensure that your application works properly on high-DPI displays:</span></span>

-   [<span data-ttu-id="f2cd1-105">Etapa 1: Usar o DPI do sistema ao criar o Windows</span><span class="sxs-lookup"><span data-stu-id="f2cd1-105">Step 1: Use the System DPI When Creating Windows</span></span>](#step-1-use-the-system-dpi-when-creating-windows)
-   [<span data-ttu-id="f2cd1-106">Etapa 2: Declarar que o aplicativo tem conhecimento de DPI</span><span class="sxs-lookup"><span data-stu-id="f2cd1-106">Step 2: Declare That the Application is DPI-Aware</span></span>](#step-2-declare-that-the-application-is-dpi-aware)
-   [<span data-ttu-id="f2cd1-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f2cd1-107">Related topics</span></span>](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a><span data-ttu-id="f2cd1-108">Etapa 1: Usar o DPI do sistema ao criar o Windows</span><span class="sxs-lookup"><span data-stu-id="f2cd1-108">Step 1: Use the System DPI When Creating Windows</span></span>

<span data-ttu-id="f2cd1-109">A interface [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) fornece o [**método GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) para recuperar o DPI do sistema.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-109">The [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface provides the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method for retrieving the system DPI.</span></span> <span data-ttu-id="f2cd1-110">Ele fornece as dimensões horizontal e vertical da exibição em DPI (pontos por polegada).</span><span class="sxs-lookup"><span data-stu-id="f2cd1-110">It provides the horizontal and vertical dimensions of the display in dots per inch (DPI).</span></span> <span data-ttu-id="f2cd1-111">Para usar esses valores para definir a largura de uma janela, use a seguinte fórmula:</span><span class="sxs-lookup"><span data-stu-id="f2cd1-111">To use these values to set the width of a window, use the following formula:</span></span>

<span data-ttu-id="f2cd1-112"><DPI horizontal  >  \*  < *width*, em pixels>/<*DPI horizontal padrão*></span><span class="sxs-lookup"><span data-stu-id="f2cd1-112"><*horizontal DPI*> \* <*width*, in pixels> / <*default horizontal DPI*></span></span>

<span data-ttu-id="f2cd1-113">... em *que dPI* horizontal é o valor derivado por [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) e o *DPI horizontal* padrão é 96.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-113">...where *horizontal DPI* is the value retrived by [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) and *default horizontal DPI* is 96.</span></span> <span data-ttu-id="f2cd1-114">A fórmula é semelhante ao tamanho vertical:</span><span class="sxs-lookup"><span data-stu-id="f2cd1-114">The formula is similar for the vertical size:</span></span>

<span data-ttu-id="f2cd1-115"><DPI vertical  >  \*  < *height*, em pixels>/<*DPI vertical padrão*></span><span class="sxs-lookup"><span data-stu-id="f2cd1-115"><*vertical DPI*> \* <*height*, in pixels> / <*default vertical DPI*></span></span>

<span data-ttu-id="f2cd1-116">... em *que dPI* vertical é o valor recuperado pelo [**método GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) e o *DPI vertical padrão* é 96.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-116">...where *vertical DPI* is the value retrieved by the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method and *default vertical DPI* is 96.</span></span>

<span data-ttu-id="f2cd1-117">O código a seguir usa o [**método GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) para recuperar o DPI do sistema e cria uma janela 640 × 480, dimensionada para o DPI do sistema.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-117">The following code uses the [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method to retrieve the system DPI and then creates a 640 × 480 window, scaled to the system DPI.</span></span>


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



> [!Note]
>
> <span data-ttu-id="f2cd1-118">Começando com Windows 8, você pode usar a classe [**Windows::Graphics::D isplay::D isplayProperties**](/uwp/api/Windows.Graphics.Display.DisplayProperties) para obter o DPI do sistema.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-118">Starting with Windows 8, you can use the [**Windows::Graphics::Display::DisplayProperties**](/uwp/api/Windows.Graphics.Display.DisplayProperties) class to get the system DPI.</span></span>

 

## <a name="step-2-declare-that-the-application-is-dpi-aware"></a><span data-ttu-id="f2cd1-119">Etapa 2: Declarar que o aplicativo está DPI-Aware</span><span class="sxs-lookup"><span data-stu-id="f2cd1-119">Step 2: Declare That the Application is DPI-Aware</span></span>

<span data-ttu-id="f2cd1-120">Quando um aplicativo se declara com conhecimento de DPI, é uma instrução que especifica que o aplicativo se comporta bem em configurações de DPI até 200 DPI.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-120">When an application declares itself to be DPI-aware, it is a statement specifying that the application behaves well at DPI settings up to 200 DPI.</span></span> <span data-ttu-id="f2cd1-121">No Windows Vista e no Windows 7, quando a virtualização de DPI está habilitada, os aplicativos que não têm suporte para DPI são dimensionados e os aplicativos recebem dados virtualizados das APIs do sistema, como a [**função GetSystemMetric.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)</span><span class="sxs-lookup"><span data-stu-id="f2cd1-121">In Windows Vista and Windows 7, when DPI virtualization is enabled, applications that are not DPI-aware are scaled, and applications receive virtualized data from the system APIs, such as the [**GetSystemMetric**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function.</span></span> <span data-ttu-id="f2cd1-122">Para declarar que seu aplicativo tem conhecimento de DPI, conclua as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-122">To declare that your application is DPI-aware, complete the following steps.</span></span>

1.  <span data-ttu-id="f2cd1-123">Crie um arquivo chamado DeclareDPIAware.manifest.</span><span class="sxs-lookup"><span data-stu-id="f2cd1-123">Create a file called DeclareDPIAware.manifest.</span></span>
2.  <span data-ttu-id="f2cd1-124">Copie o xml a seguir no arquivo e salve-o:</span><span class="sxs-lookup"><span data-stu-id="f2cd1-124">Copy the following xml into the file and save it:</span></span>
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  <span data-ttu-id="f2cd1-125">No arquivo .vcproj do projeto, adicione a seguinte entrada dentro de cada elemento Configuration em VisualStudioProject/Configurations:</span><span class="sxs-lookup"><span data-stu-id="f2cd1-125">In the project's .vcproj file, add the following entry inside each Configuration element under VisualStudioProject/Configurations:</span></span>
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a><span data-ttu-id="f2cd1-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f2cd1-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2cd1-127">Direct2D e Alto DPI</span><span class="sxs-lookup"><span data-stu-id="f2cd1-127">Direct2D and High-DPI</span></span>](direct2d-and-high-dpi.md)
</dt> </dl>

 

 