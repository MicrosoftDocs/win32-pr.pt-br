---
description: a partir do Windows Vista, a tecnologia do tablet PC tem suporte para entrada por toque no Tablet pc com digitalizadores com capacidade de toque. esse suporte inclui uma interface do usuário aprimorada para auxiliar no direcionamento e na Windows de comando ao usar um dedo para entrada.
ms.assetid: 63f1d71f-03d8-4d83-a174-e3dc7c57bad0
title: suporte à entrada por toque no Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81b22130a7c731d49556db263d5c1d5565ef51aa103925969b35c98548a32d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119335066"
---
# <a name="touch-input-support-in-windows-vista"></a>suporte à entrada por toque no Windows Vista

a partir do Windows Vista, a tecnologia do tablet PC tem suporte para entrada por toque no Tablet pc com digitalizadores com capacidade de toque. esse suporte inclui uma interface do usuário aprimorada para auxiliar no direcionamento e na Windows de comando ao usar um dedo para entrada.

## <a name="touch-digitizer-support"></a>Suporte ao Touch digitalizador

### <a name="pen-and-touch-input-not-exclusive"></a>Entrada de caneta e toque não exclusiva

Não presuma que a entrada de caneta e toque sejam mutuamente exclusivas em aplicativos [**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)e [**RealTimeStylus**](realtimestylus-class.md) .

no Windows Vista, quando o sistema reconhece uma caneta, ele ignora a entrada por toque. Ou seja, o pressionamento de toque termina e o traço da caneta começa. Como isso poderia ser alterado no futuro, seu código não deve assumir que a entrada de caneta e toque seja mutuamente exclusiva.

### <a name="other-mouse-message-sources"></a>Outras fontes de mensagens do mouse

Há outras fontes de mensagens do mouse, mesmo quando o usuário está interagindo apenas usando o dedo ou a caneta. As fontes incluem touchpads, bem como o movimento destinado a permitir que um aplicativo por trás de uma janela em camadas esteja ciente de que o mouse está se movendo para cima do aplicativo.

### <a name="enabling-and-disabling-the-touch-input-user-interface"></a>Habilitando e desabilitando a interface do usuário de entrada por toque

Talvez você queira habilitar ou desabilitar a interface do usuário de entrada por toque, dependendo dos requisitos do seu aplicativo. para fazer isso, intercepte as mensagens da janela do sistema operacional em um procedimento de janela e modifique a mensagem de Windows. Substitua [WndProc](/dotnet/api/system.windows.forms.control.wndproc?view=netcore-3.1) em seu aplicativo para interceptar essas mensagens. O pseudocódigo C a seguir \# mostra como habilitar e desabilitar a interface do usuário de entrada por toque. O código também mostra o uso da mesma técnica para desabilitar o gesto de pressionar e manter pressionado. Esse método também funciona para desabilitar a caneta.


```C++
const int WM_TABLET_QUERY_SYSTEM_GESTURE_STATUS = 716;

const uint SYSTEM_GESTURE_STATUS_NOHOLD           = 0x00000001;
const uint SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEON  = 0x00000100;
const uint SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEOFF = 0x00000200;

protected override void WndProc(ref Message msg)
{
    switch (msg.Msg)
    {
        case WM_TABLET_QUERY_SYSTEM_GESTURE_STATUS:
        {
            uint result = 0;
            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_NOHOLD;
            }

            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEON;
            }

            if (...)
            {
                result |= SYSTEM_GESTURE_STATUS_TOUCHUI_FORCEOFF;
            }

            msg.Result = (IntPtr)result;
        }
        break;

        default:
            base.WndProc(ref msg);
            break;
    }
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Tom](../wintouch/windows-touch-portal.md)
</dt> </dl>

 

 
