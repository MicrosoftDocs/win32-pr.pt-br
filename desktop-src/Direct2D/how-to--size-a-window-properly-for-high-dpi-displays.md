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
# <a name="displaying-properly-on-a-high-dpi-display"></a>Exibindo corretamente em uma exibição de alto DPI

Embora o Direct2D aborda muitos problemas de DPI alto para você, há duas etapas que você deve seguir para garantir que seu aplicativo funcione corretamente em exibições de alto DPI:

-   [Etapa 1: Usar o DPI do sistema ao criar o Windows](#step-1-use-the-system-dpi-when-creating-windows)
-   [Etapa 2: Declarar que o aplicativo tem conhecimento de DPI](#step-2-declare-that-the-application-is-dpi-aware)
-   [Tópicos relacionados](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a>Etapa 1: Usar o DPI do sistema ao criar o Windows

A interface [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) fornece o [**método GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) para recuperar o DPI do sistema. Ele fornece as dimensões horizontal e vertical da exibição em DPI (pontos por polegada). Para usar esses valores para definir a largura de uma janela, use a seguinte fórmula:

<DPI horizontal  >  \*  < *width*, em pixels>/<*DPI horizontal padrão*>

... em *que dPI* horizontal é o valor derivado por [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) e o *DPI horizontal* padrão é 96. A fórmula é semelhante ao tamanho vertical:

<DPI vertical  >  \*  < *height*, em pixels>/<*DPI vertical padrão*>

... em *que dPI* vertical é o valor recuperado pelo [**método GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) e o *DPI vertical padrão* é 96.

O código a seguir usa o [**método GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) para recuperar o DPI do sistema e cria uma janela 640 × 480, dimensionada para o DPI do sistema.


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
> Começando com Windows 8, você pode usar a classe [**Windows::Graphics::D isplay::D isplayProperties**](/uwp/api/Windows.Graphics.Display.DisplayProperties) para obter o DPI do sistema.

 

## <a name="step-2-declare-that-the-application-is-dpi-aware"></a>Etapa 2: Declarar que o aplicativo está DPI-Aware

Quando um aplicativo se declara com conhecimento de DPI, é uma instrução que especifica que o aplicativo se comporta bem em configurações de DPI até 200 DPI. No Windows Vista e no Windows 7, quando a virtualização de DPI está habilitada, os aplicativos que não têm suporte para DPI são dimensionados e os aplicativos recebem dados virtualizados das APIs do sistema, como a [**função GetSystemMetric.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) Para declarar que seu aplicativo tem conhecimento de DPI, conclua as etapas a seguir.

1.  Crie um arquivo chamado DeclareDPIAware.manifest.
2.  Copie o xml a seguir no arquivo e salve-o:
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  No arquivo .vcproj do projeto, adicione a seguinte entrada dentro de cada elemento Configuration em VisualStudioProject/Configurations:
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Direct2D e Alto DPI](direct2d-and-high-dpi.md)
</dt> </dl>

 

 