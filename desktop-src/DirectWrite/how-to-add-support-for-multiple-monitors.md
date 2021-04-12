---
title: Como adicionar suporte para vários monitores
description: O DirectWrite inclui suporte para sistemas com vários monitores.
ms.assetid: 62274126-49da-4166-8482-73aac2b29c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c5d95d0e727b4184a2dcce1720379231ce22a8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366299"
---
# <a name="how-to-add-support-for-multiple-monitors"></a>Como adicionar suporte para vários monitores

O [DirectWrite](direct-write-portal.md) inclui suporte para sistemas com vários monitores. Monitores diferentes podem ter uma geometria de pixel diferente (RGB, BGR ou simples) ou outros atributos. Para obter mais informações sobre a geometria de pixel, consulte o tópico de referência de [**\_ \_ geometria de pixel DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) . Este tópico mostrará como adicionar suporte para vários monitores ao aplicativo DirectWrite.

Para dar suporte a vários monitores, você deve manipular a mensagem da janela do **WM \_ WINDOWPOSCHANGED** . Essa mensagem é enviada quando a janela é movida, portanto, você deve verificar se a janela foi movida para um monitor diferente, conforme mostrado no código a seguir.


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



Se a janela estiver localizada em um novo monitor, você deverá criar parâmetros de renderização para o novo monitor usando o método [**IDWriteFactory:: CreateMonitorRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) .

> [!Note]  
> Não use o método [**IDWriteFactory:: CreateRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) para criar os parâmetros de renderização, pois ele sempre cria parâmetros para o monitor primário.

 

Quando você tiver um objeto [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) , defina os parâmetros de renderização para o destino de renderização usando o método [**ID2DRenderTarget:: SetTextRenderingParams**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams) .

Por fim, use a função [**InvalidateRect**](/windows/win32/api/winuser/nf-winuser-invalidaterect) para fazer com que a janela redesenhe com os novos parâmetros de renderização.

 

 