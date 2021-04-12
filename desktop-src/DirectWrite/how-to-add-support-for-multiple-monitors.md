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
# <a name="how-to-add-support-for-multiple-monitors"></a><span data-ttu-id="b24b8-103">Como adicionar suporte para vários monitores</span><span class="sxs-lookup"><span data-stu-id="b24b8-103">How to Add Support for Multiple Monitors</span></span>

<span data-ttu-id="b24b8-104">O [DirectWrite](direct-write-portal.md) inclui suporte para sistemas com vários monitores.</span><span class="sxs-lookup"><span data-stu-id="b24b8-104">[DirectWrite](direct-write-portal.md) includes support for systems with multiple monitors.</span></span> <span data-ttu-id="b24b8-105">Monitores diferentes podem ter uma geometria de pixel diferente (RGB, BGR ou simples) ou outros atributos.</span><span class="sxs-lookup"><span data-stu-id="b24b8-105">Different monitors may have different pixel geometry (RGB, BGR, or FLAT) or other attributes.</span></span> <span data-ttu-id="b24b8-106">Para obter mais informações sobre a geometria de pixel, consulte o tópico de referência de [**\_ \_ geometria de pixel DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) .</span><span class="sxs-lookup"><span data-stu-id="b24b8-106">For more information about pixel geometry, see the [**DWRITE\_PIXEL\_GEOMETRY**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) reference topic.</span></span> <span data-ttu-id="b24b8-107">Este tópico mostrará como adicionar suporte para vários monitores ao aplicativo DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="b24b8-107">This topic will show you how to add support for multiple monitors to your DirectWrite application.</span></span>

<span data-ttu-id="b24b8-108">Para dar suporte a vários monitores, você deve manipular a mensagem da janela do **WM \_ WINDOWPOSCHANGED** .</span><span class="sxs-lookup"><span data-stu-id="b24b8-108">In order to support multiple monitors, you must handle the **WM\_WINDOWPOSCHANGED** window message.</span></span> <span data-ttu-id="b24b8-109">Essa mensagem é enviada quando a janela é movida, portanto, você deve verificar se a janela foi movida para um monitor diferente, conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="b24b8-109">This message is sent when the window is moved, so you must check if the window has moved to a different monitor as shown in the following code.</span></span>


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



<span data-ttu-id="b24b8-110">Se a janela estiver localizada em um novo monitor, você deverá criar parâmetros de renderização para o novo monitor usando o método [**IDWriteFactory:: CreateMonitorRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) .</span><span class="sxs-lookup"><span data-stu-id="b24b8-110">If the window is located on a new monitor, then you must create rendering parameters for the new monitor by using the [**IDWriteFactory::CreateMonitorRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) method.</span></span>

> [!Note]  
> <span data-ttu-id="b24b8-111">Não use o método [**IDWriteFactory:: CreateRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) para criar os parâmetros de renderização, pois ele sempre cria parâmetros para o monitor primário.</span><span class="sxs-lookup"><span data-stu-id="b24b8-111">Do not use the [**IDWriteFactory::CreateRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createrenderingparams) method to create the rendering parameters, because it always creates parameters for the primary monitor.</span></span>

 

<span data-ttu-id="b24b8-112">Quando você tiver um objeto [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) , defina os parâmetros de renderização para o destino de renderização usando o método [**ID2DRenderTarget:: SetTextRenderingParams**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams) .</span><span class="sxs-lookup"><span data-stu-id="b24b8-112">When you have an [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) object, set the rendering parameters for the render target by using the [**ID2DRenderTarget::SetTextRenderingParams**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settextrenderingparams) method.</span></span>

<span data-ttu-id="b24b8-113">Por fim, use a função [**InvalidateRect**](/windows/win32/api/winuser/nf-winuser-invalidaterect) para fazer com que a janela redesenhe com os novos parâmetros de renderização.</span><span class="sxs-lookup"><span data-stu-id="b24b8-113">Finally, use the [**InvalidateRect**](/windows/win32/api/winuser/nf-winuser-invalidaterect) function to cause the window to redraw with the new rendering parameters.</span></span>

 

 