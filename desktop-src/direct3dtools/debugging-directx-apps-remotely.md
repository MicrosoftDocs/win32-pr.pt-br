---
title: Depuração remota de aplicativos DirectX
description: Você pode usar o Visual Studio e o SDK do Windows 8 para depurar aplicativos DirectX remotamente.
ms.assetid: CA471465-47C2-4706-B391-C9E6C2CD69D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55548cd282bf643e16f22177e46643c6e283a909
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366688"
---
# <a name="debugging-directx-apps-remotely"></a>Depuração remota de aplicativos DirectX

Você pode usar o Visual Studio e o SDK do Windows 8 para depurar aplicativos DirectX remotamente. O SDK do Windows 8 fornece um conjunto de componentes que dão suporte ao desenvolvimento do DirectX e fornecem verificação de erros e validação de parâmetros, além da depuração que o Visual Studio fornece. Esses componentes são D3D11 \_1SDKLayers.dll, D2D1Debug1.dll e Dxgidebug.dll.

Se você quiser depurar remotamente em um computador sem o SDK do Windows 8 instalado e desejar esse recurso de depuração adicional, deverá instalar o pacote de depuração remota apropriado para a arquitetura na qual você deseja depurar. Os pacotes Windows Installer no `C:\Program Files (x86)\Windows Kits\8.0\Remote\<arch>` instalam o suporte apropriado.

Para habilitar os recursos de depuração adicionais para aplicativos Direct2D, use este código:

```cpp
    D2D1_FACTORY_OPTIONS options;
    ZeroMemory(&options, sizeof(D2D1_FACTORY_OPTIONS));

#if defined(_DEBUG)
     // If the project is in a debug build, enable Direct2D debugging via SDK Layers.
    options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;
#endif

    DX::ThrowIfFailed(
        D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            __uuidof(ID2D1Factory1),
            &options,
            &m_d2dFactory
            )
        );         
```

Para habilitar os recursos adicionais de depuração para aplicativos do Direct3D, use este código:

```cpp
    // This flag supports surfaces with a different color channel ordering than the API default.
    // It is recommended usage, and is required for compatibility with Direct2D.
    UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
    ComPtr<IDXGIDevice> dxgiDevice;

#if defined(_DEBUG)
    // If the project is in a debug build, enable debugging via SDK Layers with this flag.
    creationFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif
    DX::ThrowIfFailed(
        D3D11CreateDevice(
            nullptr,                    // specify null to use the default adapter
            D3D_DRIVER_TYPE_HARDWARE,
            0,                          // leave as 0 unless software device
            creationFlags,              // optionally set debug and Direct2D compatibility flags
            featureLevels,              // list of feature levels this app can support
            ARRAYSIZE(featureLevels),   // number of entries in above list
            D3D11_SDK_VERSION,          // always set this to D3D11_SDK_VERSION for modern
            &device,                    // returns the Direct3D device created
            &m_featureLevel,            // returns feature level of device created
            &context                    // returns the device immediate context
            )
        );
```

Para obter mais informações sobre como depurar aplicativos Direct2D, consulte [camada de depuração do Direct2D](/windows/desktop/Direct2D/direct2ddebuglayer-portal).

Para obter mais informações sobre a depuração de aplicativos do Direct3D, consulte [camada de depuração do Direct3D](/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers).