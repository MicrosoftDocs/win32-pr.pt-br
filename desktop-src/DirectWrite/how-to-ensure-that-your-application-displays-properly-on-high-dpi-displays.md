---
title: Como garantir que seu aplicativo seja exibido corretamente em monitores de alto DPI (DirectWrite)
description: Descreve como criar uma janela que o exibe corretamente em monitores de alto DPI.
ms.assetid: d174a337-c98e-46c7-86d2-c208900882d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 317eb3379963cec600ab9bac7deb3778f0874e59
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294254"
---
# <a name="how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays"></a>Como garantir que seu aplicativo seja exibido corretamente em monitores de alto DPI

Embora [DirectWrite](direct-write-portal.md) atenda a muitos problemas de alto dpi, há duas etapas que você deve seguir para garantir que seu aplicativo funcione corretamente em monitores de alto dpi:

-   [Etapa 1: usar o DPI do sistema ao criar o Windows](#step-1-use-the-system-dpi-when-creating-windows)
    -   [Direct2D](#direct2d)
    -   [GRÁFICA](#gdi)
-   [Etapa 2: declarar que o aplicativo reconhece DPI](#step-2-declare-that-the-application-is-dpi-aware)
-   [Tópicos relacionados](#related-topics)

## <a name="step-1-use-the-system-dpi-when-creating-windows"></a>Etapa 1: usar o DPI do sistema ao criar o Windows

Isso pode ser feito usando o [Direct2D](../direct2d/direct2d-portal.md) ou o [GDI](../gdi/windows-gdi.md).

### <a name="direct2d"></a>Direct2D

A interface [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) fornece o método [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) para recuperar o DPI do sistema. Ele fornece as dimensões horizontal e vertical da exibição em pontos por polegada (DPI). Para usar esses valores para definir a largura de uma janela, use a seguinte fórmula:

<*dpi* >  \* horizontal  < *largura*, em pixels>/<*dpi horizontal padrão*>

... em que *dpi horizontal* é o valor recuperado por GetDpi e o *dpi horizontal padrão* é 96. A fórmula é semelhante ao tamanho vertical:

<*dpi* >  \* vertical  < *altura*, em pixels>/<*dpi vertical padrão*>

... em que *dpi vertical* é o valor recuperado pelo método [**GETDESKTOPDPI**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) e o *dpi vertical padrão* é 96.

O código a seguir usa o método [**GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) para criar uma janela 640 x 480, dimensionada para o DPI do sistema. (No código a seguir, *m \_ spD2DFactory* é um ponteiro inteligente para uma instância de [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) .)


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



### <a name="gdi"></a>GDI

O [GDI](interoperating-with-gdi.md) fornece a função [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) para recuperar informações do dispositivo. Você pode recuperar informações de DPI passando os valores de índice *LOGPIXELSX* e *LOGPIXELSY* . A fórmula para determinar o tamanho horizontal e vertical de uma janela é a mesma do exemplo [Direct2D](../direct2d/direct2d-portal.md) acima.

O código a seguir usa a função [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) para criar uma janela 640 x 480, dimensionada para o DPI do sistema.


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



## <a name="step-2-declare-that-the-application-is-dpi-aware"></a>Etapa 2: declarar que o aplicativo está DPI-Aware

Quando um aplicativo se declara para ser compatível com DPI, é uma instrução que especifica que o aplicativo se comporta bem em configurações de DPI até 200 DPI. No Windows Vista e no Windows 7, quando a virtualização de DPI está habilitada, os aplicativos que não têm reconhecimento de DPI são dimensionados e os aplicativos recebem dados virtualizados das APIs do sistema, como a função [**GetSystemMetric**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) . Para declarar que seu aplicativo reconhece DPI, conclua as etapas a seguir.

1.  Crie um arquivo chamado DeclareDPIAware. manifest.
2.  Copie o seguinte XML para o arquivo e salve-o:
    ```C++
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
      <asmv3:application>
        <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
          <dpiAware>true</dpiAware>
        </asmv3:windowsSettings>
      </asmv3:application>
    </assembly>
    ```

    

3.  No arquivo. vcproj do projeto, adicione a seguinte entrada dentro de cada elemento de configuração em VisualStudioProject/configurações:
    ```C++
    <Tool
        Name="VCManifestTool"
        AdditionalManifestFiles="DeclareDPIAware.manifest"
    />
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Direct2D e alto DPI](../direct2d/direct2d-and-high-dpi.md)
</dt> </dl>

 

 