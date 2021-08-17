---
description: Um aplicativo pode ressumentar a Experiência de Replicação Padrão manipulada pelo sistema e substituí-la por uma implementação personalizada.
ms.assetid: 18290d05-b114-476b-8365-6bbb5fe6cffc
title: Fornecendo um comportamento de desaqueamento personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72cf4bb254b97a6a9d6b5c9d415d48a2c95f528f20efbf2ffbe4782ae5980400
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406364"
---
# <a name="providing-a-custom-ducking-behavior"></a>Fornecendo um comportamento de desaqueamento personalizado

Um aplicativo pode ressumentar a [Experiência de Replicação Padrão](stream-attenuation.md) manipulada pelo sistema e substituí-la por uma implementação personalizada.

Um aplicativo pode fornecer uma experiência de replicação personalizada. Por exemplo, Windows Media Player fornece sua própria experiência de ressalvação pausando o fluxo de mídia atual durante uma sessão de comunicação e retomando a reprodução quando a sessão é fechada. Um aplicativo de mídia de exemplo que implementa a replicação de dados está incluído Windows exemplos do SDK; Para obter mais informações, [consulte DuckingMediaPlayer](duckingmediaplayer.md). Para simular a experiência de abertura e fechamento de fluxos de comunicação e a geração de eventos de ressarma, consulte [OIngCaptureSample](duckingcapturesample.md), que também está incluído com exemplos Windows SDK.

Um aplicativo de mídia que reproduz sons a serem atenuados deve estar ciente dos fluxos de comunicação, quando eles são abertos e fechados no sistema. A implementação personalizada pode ser fornecida usando MediaFoundation, DirectShow ou DirectSound, que usam as APIs de Áudio Principal. Um cliente WASAPI direto também poderá substituir o tratamento padrão se souber quando a sessão de comunicação é iniciada e termina.

**Para fornecer uma experiência de desaqueamento personalizada, um cliente WASAPI deve executar as seguintes tarefas:**

1.  Registre-se para receber eventos de 10000001 do gerenciador *de* alvos – um componente do sistema de áudio que lida com notificações relacionadas a alterações de fluxo de comunicação. Para obter mais informações, [Obter eventos de desaqueamento.](handling-audio-ducking-events-from-communication-devices.md)
    > [!Note]  
    > Se o cliente for registrado para receber notificações de ressalvação, o gerenciador de defesa desabilitará o comportamento padrão fornecido pelo sistema. Se o comportamento padrão for desabilitado explictly (consulte Desabilitando a experiência de redução padrão [)](disabling-the-ducking-experience.md)e o cliente não fornecer um comportamento substituto, o aplicativo não enfrentará nenhum comportamento de redução.

     

2.  Escutar as notificações de evento de patinho enviadas pelo gerente de patinho e executar o comportamento desejado de desaqueamento. Para obter mais informações sobre como implementar um comportamento de replicação, consulte [Considerações de implementação para notificações de ressalvação.](handling-audio-ducking-events-from-communication-devices.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando um dispositivo de comunicação](using-the-communication-device.md)
</dt> <dt>

[Experiência padrão de ressalvamento](stream-attenuation.md)
</dt> <dt>

[Desabilitando a experiência de ressalvamento padrão](disabling-the-ducking-experience.md)
</dt> <dt>

[Considerações de implementação para notificações de replicação](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Obter eventos de desaqueamento](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



