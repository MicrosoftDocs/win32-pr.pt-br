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
# <a name="providing-a-custom-ducking-behavior"></a><span data-ttu-id="f9132-103">Fornecendo um comportamento personalizado de pato</span><span class="sxs-lookup"><span data-stu-id="f9132-103">Providing a Custom Ducking Behavior</span></span>

<span data-ttu-id="f9132-104">Um aplicativo pode recusar a experiência de [pato padrão](stream-attenuation.md) manipulada pelo sistema e substituí-la por uma implementação personalizada.</span><span class="sxs-lookup"><span data-stu-id="f9132-104">An application can opt out of the [Default Ducking Experience](stream-attenuation.md) handled by the system and replace it with a custom implementation.</span></span>

<span data-ttu-id="f9132-105">Um aplicativo pode fornecer uma experiência personalizada de pato.</span><span class="sxs-lookup"><span data-stu-id="f9132-105">An application can provide a custom ducking experience.</span></span> <span data-ttu-id="f9132-106">Por exemplo, o Windows Media Player fornece sua própria experiência de pato pausando o fluxo de mídia atual durante uma sessão de comunicação e retomando a reprodução quando a sessão é fechada.</span><span class="sxs-lookup"><span data-stu-id="f9132-106">For example, Windows Media Player provides its own ducking experience by pausing the current media stream during a communication session and resuming playback when the session is closed.</span></span> <span data-ttu-id="f9132-107">Um aplicativo de mídia de exemplo que implementa o patoing está incluído em exemplos de SDK do Windows; para obter mais informações, consulte [DuckingMediaPlayer](duckingmediaplayer.md).</span><span class="sxs-lookup"><span data-stu-id="f9132-107">A sample media application that implements ducking is included with Windows SDK samples; for more information, see [DuckingMediaPlayer](duckingmediaplayer.md).</span></span> <span data-ttu-id="f9132-108">Para simular a experiência de abrir e fechar fluxos de comunicação e gerar eventos de pato, consulte [DuckingCaptureSample](duckingcapturesample.md), que também está incluído com exemplos de SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="f9132-108">To simulate the experience of opening and closing communication streams, and generating ducking events, see [DuckingCaptureSample](duckingcapturesample.md), which is also included with Windows SDK samples.</span></span>

<span data-ttu-id="f9132-109">Um aplicativo de mídia que reproduz sons a serem atenuados deve estar ciente dos fluxos de comunicação, quando eles são abertos e fechados no sistema.</span><span class="sxs-lookup"><span data-stu-id="f9132-109">A media application that plays sounds to be attenuated must be aware of the communication streams, when they are opened and closed in the system.</span></span> <span data-ttu-id="f9132-110">A implementação personalizada pode ser fornecida usando MediaFoundation, DirectShow ou DirectSound, que usam as APIs de áudio principais.</span><span class="sxs-lookup"><span data-stu-id="f9132-110">The custom implementation can be provided by using MediaFoundation, DirectShow, or DirectSound, which use the Core Audio APIs.</span></span> <span data-ttu-id="f9132-111">Um cliente WASAPI direto também pode substituir o tratamento padrão se ele sabe quando a sessão de comunicação começa e termina.</span><span class="sxs-lookup"><span data-stu-id="f9132-111">A direct WASAPI client can also override the default handling if it knows when the communication session starts and ends.</span></span>

<span data-ttu-id="f9132-112">**Para fornecer uma experiência personalizada de pato, um cliente WASAPI deve executar as seguintes tarefas:**</span><span class="sxs-lookup"><span data-stu-id="f9132-112">**To provide a custom ducking experience, a WASAPI client must perform the following tasks:**</span></span>

1.  <span data-ttu-id="f9132-113">Registre-se para receber eventos de pato do *Gerenciador de pato*– um componente do sistema de áudio que manipula as notificações relacionadas às alterações de fluxo de comunicação.</span><span class="sxs-lookup"><span data-stu-id="f9132-113">Register to receive ducking events from the *ducking manager*—a component of the audio system that handles notifications related to communication stream changes.</span></span> <span data-ttu-id="f9132-114">Para obter mais informações, [obter eventos de pato](handling-audio-ducking-events-from-communication-devices.md).</span><span class="sxs-lookup"><span data-stu-id="f9132-114">For more information, [Getting Ducking Events](handling-audio-ducking-events-from-communication-devices.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="f9132-115">Se o cliente for registrado para receber notificações de pato, o Gerenciador de patos desabilitará o comportamento padrão fornecido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="f9132-115">If the client is gets registered to receive ducking notifications, the ducking manager disables the default behavior provided by the system.</span></span> <span data-ttu-id="f9132-116">Se o comportamento padrão for desabilitado explicitamente (consulte [desabilitando a experiência de pato padrão](disabling-the-ducking-experience.md)) e o cliente não fornecer um comportamento substituto, o aplicativo não experimentará nenhum comportamento de pato.</span><span class="sxs-lookup"><span data-stu-id="f9132-116">If the default behavior is disabled explictly (see [Disabling the Default Ducking Experience](disabling-the-ducking-experience.md)) and the client does not provide a substitute behavior, the application does not experience any ducking behavior.</span></span>

     

2.  <span data-ttu-id="f9132-117">Ouça as notificações de evento pato enviadas pelo Gerenciador de pato e execute o comportamento de pato desejado.</span><span class="sxs-lookup"><span data-stu-id="f9132-117">Listen for the duck event notifications sent by the ducking manager and perform the desired ducking behavior.</span></span> <span data-ttu-id="f9132-118">Para obter mais informações sobre como implementar um comportamento de pato, consulte [considerações de implementação para notificações de pato](handling-audio-ducking-events-from-communication-devices.md).</span><span class="sxs-lookup"><span data-stu-id="f9132-118">For more information about implementing a ducking behavior, see [Implementation Considerations for Ducking Notifications](handling-audio-ducking-events-from-communication-devices.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9132-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f9132-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9132-120">Usando um dispositivo de comunicação</span><span class="sxs-lookup"><span data-stu-id="f9132-120">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="f9132-121">Experiência de pato padrão</span><span class="sxs-lookup"><span data-stu-id="f9132-121">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="f9132-122">Desabilitando a experiência de pato padrão</span><span class="sxs-lookup"><span data-stu-id="f9132-122">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="f9132-123">Considerações de implementação para notificações de pato</span><span class="sxs-lookup"><span data-stu-id="f9132-123">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[<span data-ttu-id="f9132-124">Obtendo eventos de pato</span><span class="sxs-lookup"><span data-stu-id="f9132-124">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



