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
# <a name="step-4-draw-the-bitmap-on-the-client-area"></a>Etapa 4: desenhar o bitmap na área do cliente

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Este tópico é a etapa 4 da [captura de um quadro de cartaz](grabbing-a-poster-frame.md).

A etapa final é desenhar o bitmap na área do cliente da janela do aplicativo, usando a função [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) . Este exemplo simplesmente pinta o bitmap no canto superior esquerdo da área do cliente, sem considerar o tamanho da janela:


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



As variáveis *pBuffer* e *pbmi* são declaradas na [etapa 1: criar o Windows Framework](step-1--create-the-windows-framework.md)e seus valores são obtidos na [etapa 3: implementar a função Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Capturando um quadro de cartaz](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
