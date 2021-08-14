---
title: Depuração remota de aplicativos DirectX
description: você pode usar Visual Studio e o SDK do Windows 8 para depurar aplicativos DirectX remotamente.
ms.assetid: CA471465-47C2-4706-B391-C9E6C2CD69D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30f9fd97519bb88a0a89206e5a8c3aa43cf990948cb9aa8c9dd40379c53ed1a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118505671"
---
# <a name="debugging-directx-apps-remotely"></a>Depuração remota de aplicativos DirectX

você pode usar Visual Studio e o SDK do Windows 8 para depurar aplicativos DirectX remotamente. o SDK do Windows 8 fornece um conjunto de componentes que dão suporte ao desenvolvimento do DirectX e fornecem verificação de erros e validação de parâmetros, além da depuração que o Visual Studio fornece. Esses componentes são D3D11 \_1SDKLayers.dll, D2D1Debug1.dll e Dxgidebug.dll.

se você quiser depurar remotamente em um computador sem o SDK do Windows 8 instalado e desejar esse recurso de depuração adicional, deverá instalar o pacote de depuração remota apropriado para a arquitetura na qual você deseja depurar. os pacotes Windows Installer no `C:\Program Files (x86)\Windows Kits\8.0\Remote\<arch>` instalam o suporte apropriado.

para habilitar os recursos adicionais de depuração para Direct2D aplicativos, use este código:

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

para obter mais informações sobre como depurar Direct2D aplicativos, consulte [Direct2D camada de depuração](/windows/desktop/Direct2D/direct2ddebuglayer-portal).

Para obter mais informações sobre a depuração de aplicativos do Direct3D, consulte [camada de depuração do Direct3D](/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers).