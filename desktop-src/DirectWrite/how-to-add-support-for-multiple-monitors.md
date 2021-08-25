---
title: Como adicionar suporte para vários monitores
description: DirectWrite inclui suporte para sistemas com vários monitores.
ms.assetid: 62274126-49da-4166-8482-73aac2b29c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12bbfb2c803372e52128cd62dddeec407985e4180039d84f9aed66092149911b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048886"
---
# <a name="how-to-add-support-for-multiple-monitors"></a>Como adicionar suporte para vários monitores

[DirectWrite](direct-write-portal.md) inclui suporte para sistemas com vários monitores. Monitores diferentes podem ter geometria de pixel diferente (RGB, BGR ou FLAT) ou outros atributos. Para obter mais informações sobre geometria de pixel, consulte o [**tópico referência DWRITE \_ PIXEL \_ GEOMETRY.**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) Este tópico mostrará como adicionar suporte para vários monitores ao DirectWrite aplicativo.

Para dar suporte a vários monitores, você deve manipular a mensagem de janela **WM \_ WINDOWPOSCHANGED.** Essa mensagem é enviada quando a janela é movida, portanto, você deve verificar se a janela foi movida para um monitor diferente, conforme mostrado no código a seguir.


```C++
case WM_WINDOWPOSCHANGED:
    {
        HMONITOR monitor = MonitorFromWindow(hwnd, MONITOR_DEFAULTTONULL);
        if (monitor != g_monitor)
        {
            g_monitor = monitor;
            if (g_spRenderTarget != NULL)
            {
                IDWriteRenderingParams* pRenderingParams = NULL;
                g_spDWriteFactory->CreateMonitorRenderingParams(monitor, &pRenderingParams);

                g_spRenderTarget->SetTextRenderingParams(pRenderingParams);

                SafeRelease(&pRenderingParams);
            }

            InvalidateRect(hwnd, NULL, TRUE);
        }
    }
    break;
```



Se a janela estiver localizada em um novo monitor, você deverá criar parâmetros de renderização para o novo monitor usando o [**método IDWriteFactory::CreateMonitorRenderingParams.**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams)

> [!Note]  
> Não use o método [**IDWriteFactory::CreateRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) para criar os parâmetros de renderização, pois ele sempre cria parâmetros para o monitor primário.

 

Quando você tiver um [**objeto IDWriteRenderingParams,**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) de definir os parâmetros de renderização para o destino de renderização usando o [**método ID2DRenderTarget::SetTextRenderingParams.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams)

Por fim, use [**a função InvalidateRect**](/windows/win32/api/winuser/nf-winuser-invalidaterect) para fazer com que a janela seja redesenhada com os novos parâmetros de renderização.

 

 