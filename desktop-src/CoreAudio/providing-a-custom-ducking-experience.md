---
description: Um aplicativo pode recusar a experiência de pato padrão manipulada pelo sistema e substituí-la por uma implementação personalizada.
ms.assetid: 18290d05-b114-476b-8365-6bbb5fe6cffc
title: Fornecendo um comportamento personalizado de pato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4051dc7b79f698f10d007beaafa97e90d79f3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089509"
---
# <a name="providing-a-custom-ducking-behavior"></a>Fornecendo um comportamento personalizado de pato

Um aplicativo pode recusar a experiência de [pato padrão](stream-attenuation.md) manipulada pelo sistema e substituí-la por uma implementação personalizada.

Um aplicativo pode fornecer uma experiência personalizada de pato. Por exemplo, o Windows Media Player fornece sua própria experiência de pato pausando o fluxo de mídia atual durante uma sessão de comunicação e retomando a reprodução quando a sessão é fechada. Um aplicativo de mídia de exemplo que implementa o patoing está incluído em exemplos de SDK do Windows; para obter mais informações, consulte [DuckingMediaPlayer](duckingmediaplayer.md). Para simular a experiência de abrir e fechar fluxos de comunicação e gerar eventos de pato, consulte [DuckingCaptureSample](duckingcapturesample.md), que também está incluído com exemplos de SDK do Windows.

Um aplicativo de mídia que reproduz sons a serem atenuados deve estar ciente dos fluxos de comunicação, quando eles são abertos e fechados no sistema. A implementação personalizada pode ser fornecida usando MediaFoundation, DirectShow ou DirectSound, que usam as APIs de áudio principais. Um cliente WASAPI direto também pode substituir o tratamento padrão se ele sabe quando a sessão de comunicação começa e termina.

**Para fornecer uma experiência personalizada de pato, um cliente WASAPI deve executar as seguintes tarefas:**

1.  Registre-se para receber eventos de pato do *Gerenciador de pato*– um componente do sistema de áudio que manipula as notificações relacionadas às alterações de fluxo de comunicação. Para obter mais informações, [obter eventos de pato](handling-audio-ducking-events-from-communication-devices.md).
    > [!Note]  
    > Se o cliente for registrado para receber notificações de pato, o Gerenciador de patos desabilitará o comportamento padrão fornecido pelo sistema. Se o comportamento padrão for desabilitado explicitamente (consulte [desabilitando a experiência de pato padrão](disabling-the-ducking-experience.md)) e o cliente não fornecer um comportamento substituto, o aplicativo não experimentará nenhum comportamento de pato.

     

2.  Ouça as notificações de evento pato enviadas pelo Gerenciador de pato e execute o comportamento de pato desejado. Para obter mais informações sobre como implementar um comportamento de pato, consulte [considerações de implementação para notificações de pato](handling-audio-ducking-events-from-communication-devices.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando um dispositivo de comunicação](using-the-communication-device.md)
</dt> <dt>

[Experiência de pato padrão](stream-attenuation.md)
</dt> <dt>

[Desabilitando a experiência de pato padrão](disabling-the-ducking-experience.md)
</dt> <dt>

[Considerações de implementação para notificações de pato](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Obtendo eventos de pato](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



