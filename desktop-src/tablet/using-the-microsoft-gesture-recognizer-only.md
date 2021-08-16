---
description: Você pode usar um coletor de tinta (InkCollector, InkOverlay ou InkPicture) para acessar diretamente o reconhecedor de gestos padrão da Microsoft. Para usar um coletor de tintas para acessar o reconhecedor de gestos:de definir a propriedade CollectionMode do coletor de tinta para o modo InkAndGesture ou o modo GestureOnly.inkOverlay.CollectionMode = CollectionMode.GestureOnly; Escolha o gesto que você deseja dar suporte a.inkOverlay.SetGestureStatus(ApplicationGesture.AllGestures, true);Implementar um manipulador de eventos que recebe notificações de gesto. No manipulador de eventos, você precisa implementar a ação correspondente a cada evento recebido. Observação O modo misto dá suporte apenas a gestos de traço único. O modo de gesto dá suporte a vários gestos de traço. inkOverlay.Gesture += new InkCollectorGestureEventHandler(inkOverlay Gesture);No modo InkAndGesture, cada traço individual é enviado para o reconhecedor de gestos da \_ Microsoft. Se ele for reconhecido como um gesto que você habilitar, uma notificação de evento será enviada. Se o aplicativo aceitar a notificação de evento, o traço será apagado. Se o aplicativo não aceitar a notificação ou se o traço não for reconhecido como um gesto, o traço será armazenado no objeto Ink. No modo GestureOnly, os traços são delimitados por tempos limite antes e depois dos traços. Os traços coletados dentro do tempoout são enviados para o reconhecedor. Se os traços são reconhecidos como um gesto que você habilitar, uma notificação de evento é enviada. O aplicativo pode aceitar ou rejeitar o evento, a ação correspondente ou não. No modo somente gesto, os traços nunca são salvos no objeto Ink.
ms.assetid: 3f5f00a3-1f2c-4fa2-9738-bc5fb56e2208
title: Usando somente o Reconhecedor de Gestos da Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d7b27ae30e0bba98ee2c9db57cc0da2d6491932d0137cc5cd4d2b6f86420ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715173"
---
# <a name="using-the-microsoft-gesture-recognizer-only"></a>Usando somente o Reconhecedor de Gestos da Microsoft

Você pode usar um coletor de tinta ([**InkCollector,**](inkcollector-class.md) [**InkOverlay**](inkoverlay-class.md)ou [InkPicture](inkpicture-control-reference.md)) para acessar diretamente o reconhecedor de gestos padrão da Microsoft.

Para usar um coletor de tinta para acessar o reconhecedor de gestos:

-   De definir [**a propriedade CollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) do coletor de tinta para **o modo InkAndGesture** ou **o modo GestureOnly.**

`inkOverlay.CollectionMode = CollectionMode.GestureOnly;`

-   Escolha o gesto que você deseja dar suporte.

`inkOverlay.SetGestureStatus(ApplicationGesture.AllGestures, true);`

-   Implemente um manipulador de eventos que recebe notificações de gesto. No manipulador de eventos, você precisa implementar a ação correspondente a cada evento recebido.
    > [!Note]  
    > O modo misto dá suporte apenas a gestos de traço único. O modo de gesto dá suporte a vários gestos de traço.

     

`inkOverlay.Gesture += new InkCollectorGestureEventHandler(inkOverlay_Gesture);`

No **modo InkAndGesture,** cada traço individual é enviado para o reconhecedor de gestos da Microsoft. Se ele for reconhecido como um gesto que você habilitar, uma notificação de evento será enviada. Se o aplicativo aceitar a notificação de evento, o traço será apagado. Se o aplicativo não aceitar a notificação ou se o traço não for reconhecido como um gesto, o traço será armazenado no [**objeto Ink.**](inkdisp-class.md)

No **modo GestureOnly,** os traços são delimitados por tempos limite antes e depois dos traços. Os traços coletados dentro do tempoout são enviados para o reconhecedor. Se os traços são reconhecidos como um gesto que você habilitar, uma notificação de evento é enviada. O aplicativo pode aceitar ou rejeitar o evento, a ação correspondente ou não. No modo somente gesto, os traços nunca são salvos no [**objeto Ink.**](inkdisp-class.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Microsoft.Ink.InkCollector.CollectionMode](/previous-versions/ms836497(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkOverlay.CollectionMode](/previous-versions/ms833092(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkPicture.CollectionMode](/previous-versions/ms582182(v=vs.100))
</dt> </dl>

 

 
