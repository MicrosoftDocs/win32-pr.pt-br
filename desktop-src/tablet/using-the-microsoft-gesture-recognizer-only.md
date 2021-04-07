---
description: 'Você pode usar um coletor de tinta (InkCollector, InkOverlay ou InkPicture) para acessar diretamente o reconhecedor de gestos da Microsoft. Para usar um coletor de tinta para acessar o reconhecedor de gestos: defina a Propriedade CollectionMode do coletor de tinta para o modo InkAndGesture ou GestureOnly Mode. inkOverlay. CollectionMode = CollectionMode. GestureOnly; Escolha o gesto para o qual você deseja dar suporte. inkOverlay. SetGestureStatus (ApplicationGesture. algestos, true); implemente um manipulador de eventos que receba notificações de gesto. No manipulador de eventos, você precisa implementar a ação correspondente a cada evento recebido. Observação o modo misto dá suporte apenas a gestos de traço único. O modo de gesto dá suporte a vários gestos de traço. inkOverlay. gesto + = New InkCollectorGestureEventHandler (gesto de inkOverlay \_ ); no modo InkAndGesture, cada traço individual é enviado para o reconhecedor de gestos da Microsoft. Se for reconhecido como um gesto que você habilitou, uma notificação de evento será enviada. Se o aplicativo aceitar a notificação de eventos, o traço será apagado. Se o aplicativo não aceitar a notificação ou se o traço não for reconhecido como um gesto, o traço será armazenado no objeto de tinta. No modo GestureOnly, os traços são delimitados por tempos limite antes e depois dos traços. Os traços coletados no tempo limite são enviados para o reconhecedor. Se os traços forem reconhecidos como um gesto que você habilitou, uma notificação de evento será enviada. O aplicativo pode aceitar ou rejeitar o evento, afetando a ação correspondente ou não. No modo somente gesto, os traços nunca são salvos no objeto Ink.'
ms.assetid: 3f5f00a3-1f2c-4fa2-9738-bc5fb56e2208
title: Usando apenas o reconhecedor de gestos da Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80504e8b32c0b9596936bb4f07d029cd4ea8ddbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827075"
---
# <a name="using-the-microsoft-gesture-recognizer-only"></a>Usando apenas o reconhecedor de gestos da Microsoft

Você pode usar um coletor de tinta ([**InkCollector**](inkcollector-class.md), [**InkOverlay**](inkoverlay-class.md)ou [InkPicture](inkpicture-control-reference.md)) para acessar diretamente o reconhecedor de gestos da Microsoft.

Para usar um coletor de tinta para acessar o reconhecedor de gestos:

-   Defina a propriedade [**CollectionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkcollectionmode) do coletor de tinta para o modo **InkAndGesture** ou **GestureOnly** .

`inkOverlay.CollectionMode = CollectionMode.GestureOnly;`

-   Escolha o gesto para o qual você deseja dar suporte.

`inkOverlay.SetGestureStatus(ApplicationGesture.AllGestures, true);`

-   Implemente um manipulador de eventos que receba notificações de gestos. No manipulador de eventos, você precisa implementar a ação correspondente a cada evento recebido.
    > [!Note]  
    > O modo misto dá suporte apenas a gestos de traço único. O modo de gesto dá suporte a vários gestos de traço.

     

`inkOverlay.Gesture += new InkCollectorGestureEventHandler(inkOverlay_Gesture);`

No modo **InkAndGesture** , cada traço individual é enviado para o reconhecedor de gestos da Microsoft. Se for reconhecido como um gesto que você habilitou, uma notificação de evento será enviada. Se o aplicativo aceitar a notificação de eventos, o traço será apagado. Se o aplicativo não aceitar a notificação ou se o traço não for reconhecido como um gesto, o traço será armazenado no objeto de [**tinta**](inkdisp-class.md) .

No modo **GestureOnly** , os traços são delimitados por tempos limite antes e depois dos traços. Os traços coletados no tempo limite são enviados para o reconhecedor. Se os traços forem reconhecidos como um gesto que você habilitou, uma notificação de evento será enviada. O aplicativo pode aceitar ou rejeitar o evento, afetando a ação correspondente ou não. No modo somente gesto, os traços nunca são salvos no objeto [**Ink**](inkdisp-class.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Microsoft. Ink. InkCollector. CollectionMode](/previous-versions/ms836497(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkOverlay. CollectionMode](/previous-versions/ms833092(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkPicture. CollectionMode](/previous-versions/ms582182(v=vs.100))
</dt> </dl>

 

 
