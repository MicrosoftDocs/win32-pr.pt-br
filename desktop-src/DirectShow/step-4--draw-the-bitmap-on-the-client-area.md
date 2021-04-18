---
description: 'Etapa 4: desenhar o bitmap na área do cliente'
ms.assetid: fb22468c-9113-46ff-a576-8dee30c458be
title: 'Etapa 4: desenhar o bitmap na área do cliente'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4975215e5d75de9909f029a3378bd6cc8bc60916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370798"
---
# <a name="step-4-draw-the-bitmap-on-the-client-area"></a><span data-ttu-id="2df19-103">Etapa 4: desenhar o bitmap na área do cliente</span><span class="sxs-lookup"><span data-stu-id="2df19-103">Step 4: Draw the Bitmap on the Client Area</span></span>

<span data-ttu-id="2df19-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="2df19-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="2df19-105">Este tópico é a etapa 4 da [captura de um quadro de cartaz](grabbing-a-poster-frame.md).</span><span class="sxs-lookup"><span data-stu-id="2df19-105">This topic is Step 4 of [Grabbing a Poster Frame](grabbing-a-poster-frame.md).</span></span>

<span data-ttu-id="2df19-106">A etapa final é desenhar o bitmap na área do cliente da janela do aplicativo, usando a função [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) .</span><span class="sxs-lookup"><span data-stu-id="2df19-106">The final step is to draw the bitmap onto the client area of the application window, using the [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) function.</span></span> <span data-ttu-id="2df19-107">Este exemplo simplesmente pinta o bitmap no canto superior esquerdo da área do cliente, sem considerar o tamanho da janela:</span><span class="sxs-lookup"><span data-stu-id="2df19-107">This example simply paints the bitmap in the upper-left corner of the client area, without regard to the window size:</span></span>


```C++
case WM_PAINT:
    {
        PAINTSTRUCT ps;
        HDC hdc = BeginPaint(hwnd, &ps);
        if (pbmi)
        {
            int result = SetDIBitsToDevice(hdc, 0, 0, 
                pbmi->biWidth,
                pbmi->biHeight,
                0, 0, 0,
                pbmi->biHeight,
                pBuffer,
                reinterpret_cast<BITMAPINFO*>(pbmi),
                DIB_RGB_COLORS);
        }
        EndPaint(hwnd, &ps);
    }
    break;
```



<span data-ttu-id="2df19-108">As variáveis *pBuffer* e *pbmi* são declaradas na [etapa 1: criar o Windows Framework](step-1--create-the-windows-framework.md)e seus valores são obtidos na [etapa 3: implementar a função Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md).</span><span class="sxs-lookup"><span data-stu-id="2df19-108">The *pBuffer* and *pbmi* variables are declared in [Step 1: Create the Windows Framework](step-1--create-the-windows-framework.md), and their values are obtained in [Step 3: Implement the Frame-Grabbing Function](step-3--implement-the-frame-grabbing-function.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2df19-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2df19-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2df19-110">Capturando um quadro de cartaz</span><span class="sxs-lookup"><span data-stu-id="2df19-110">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
