---
description: Experiência de pato padrão
ms.assetid: 2ad9482f-1888-4f19-bc41-9d47a8e0ed15
title: Experiência de pato padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d81aa22254ab33ee7396fd4a22d83cc7f5a58041
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646407"
---
# <a name="default-ducking-experience"></a><span data-ttu-id="2722e-103">Experiência de pato padrão</span><span class="sxs-lookup"><span data-stu-id="2722e-103">Default Ducking Experience</span></span>

<span data-ttu-id="2722e-104">Considere um cenário em que um usuário recebe uma chamada telefônica ao ouvir música no computador.</span><span class="sxs-lookup"><span data-stu-id="2722e-104">Consider a scenario where a user receives a phone call while listening to music on the computer.</span></span> <span data-ttu-id="2722e-105">Durante a chamada telefônica, o usuário deseja reduzir o nível de volume da música ao participar da chamada telefônica e retomar o volume original após o término da chamada telefônica.</span><span class="sxs-lookup"><span data-stu-id="2722e-105">During the phone call, the user wants to reduce the volume level of the music while attending to the phone call, and resume the original volume after the phone call has ended.</span></span> <span data-ttu-id="2722e-106">Dependendo das opções especificadas pelo usuário no painel de controle de **sons** , o sistema operacional fornece automaticamente essa funcionalidade por meio da *atenuação* do *pato* ou do fluxo — redução na intensidade de um fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="2722e-106">Depending on the options specified by the user in the **Sounds** control panel, the operating system automatically provides this functionality through *ducking* or *stream attenuation*—reduction in the intensity of an audio stream.</span></span>

<span data-ttu-id="2722e-107">A experiência de atenuação padrão depende da preferência do usuário, conforme especificado na opção de **som** do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="2722e-107">The default attenuation experience depends on the user's preference, as specified in the control panel's **Sound** option.</span></span> <span data-ttu-id="2722e-108">Na guia **comunicações** , o usuário pode escolher um nível de atenuação (o valor padrão é 80%), ativar mudo de todos os fluxos de não comunicação ou desabilitar a experiência de atenuação do fluxo padrão.</span><span class="sxs-lookup"><span data-stu-id="2722e-108">On the **Communications** tab, the user can choose an attenuation level (default value is 80%), mute all non-communication streams, or disable the default stream attenuation experience.</span></span> <span data-ttu-id="2722e-109">O sistema permite que novos fluxos de não comunicação (exceto para novos sons do sistema) sejam abertos durante a sessão de comunicação, mas os novos fluxos não são automaticamente atenuados.</span><span class="sxs-lookup"><span data-stu-id="2722e-109">The system allows new non-communication streams (except for new system sounds) to be opened during the communication session but the new streams are not automatically attenuated.</span></span> <span data-ttu-id="2722e-110">Quando todos os fluxos de comunicação são fechados, o sistema encerra a sessão de comunicação e restaura o volume dos fluxos que foram atenuados durante a sessão de comunicação.</span><span class="sxs-lookup"><span data-stu-id="2722e-110">When all of the communication streams are closed, the system ends the communication session and restores the volume of the streams that were attenuated during the communication session.</span></span>

<span data-ttu-id="2722e-111">Para indicar visualmente a atenuação do fluxo, o sistema altera as configurações do mixer de volume dependendo da preferência do usuário.</span><span class="sxs-lookup"><span data-stu-id="2722e-111">To indicate stream attenuation visually, the system changes the volume mixer settings depending on the user's preference.</span></span> <span data-ttu-id="2722e-112">Por exemplo, se o usuário especificar um nível de atenuação, o mixer de volume diminuirá o controle deslizante, exibirá o novo volume atenuado e exibirá o nível de volume original.</span><span class="sxs-lookup"><span data-stu-id="2722e-112">For example, if the user specifies an attenuation level, the volume mixer lowers the slider, displays the new attenuated volume, and displays the original volume level.</span></span> <span data-ttu-id="2722e-113">A imagem a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="2722e-113">The following image illustrates this process.</span></span>

![diagrama de comportamento de atenuação de fluxo padrão fornecido no Windows 7](images/stream-aatenuation.jpg)

<span data-ttu-id="2722e-115">Um aplicativo pode substituir a atenuação de fluxo e implementar uma experiência personalizada de pato se souber quando a sessão de comunicação começa e termina.</span><span class="sxs-lookup"><span data-stu-id="2722e-115">An application can override stream attenuation and implement a custom ducking experience if it knows when the communication session starts and ends.</span></span> <span data-ttu-id="2722e-116">Para obter mais informações, consulte [fornecendo um comportamento de pato personalizado](providing-a-custom-ducking-experience.md).</span><span class="sxs-lookup"><span data-stu-id="2722e-116">For more information, see [Providing a Custom Ducking Behavior](providing-a-custom-ducking-experience.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2722e-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2722e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2722e-118">Usando um dispositivo de comunicação</span><span class="sxs-lookup"><span data-stu-id="2722e-118">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="2722e-119">Desabilitando a experiência de pato padrão</span><span class="sxs-lookup"><span data-stu-id="2722e-119">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="2722e-120">Fornecendo um comportamento personalizado de pato</span><span class="sxs-lookup"><span data-stu-id="2722e-120">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="2722e-121">Considerações de implementação para notificações de pato</span><span class="sxs-lookup"><span data-stu-id="2722e-121">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[<span data-ttu-id="2722e-122">Obtendo eventos de pato</span><span class="sxs-lookup"><span data-stu-id="2722e-122">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



