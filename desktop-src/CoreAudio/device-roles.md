---
description: Funções de dispositivo
ms.assetid: aa787004-0d3e-448b-80dd-92055f841aee
title: Funções de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b7182e3af6bf76af500588546a1b7c0db9eea97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089247"
---
# <a name="device-roles"></a><span data-ttu-id="a2c85-103">Funções de dispositivo</span><span class="sxs-lookup"><span data-stu-id="a2c85-103">Device Roles</span></span>

<span data-ttu-id="a2c85-104">Se um sistema contiver dois ou mais dispositivos de ponto de extremidade de renderização de áudio, um dispositivo poderá ser melhor para a execução de um tipo de conteúdo de áudio, e outro dispositivo poderá ser melhor para reproduzir outro tipo de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a2c85-104">If a system contains two or more audio-rendering endpoint devices, then one device might be best for playing one type of audio content, and another device might be best for playing another type of content.</span></span> <span data-ttu-id="a2c85-105">Por exemplo, se um sistema tiver dois dispositivos de renderização, o usuário poderá optar por reproduzir música em um dispositivo e reproduzir sons de notificação do sistema no outro.</span><span class="sxs-lookup"><span data-stu-id="a2c85-105">For example, if a system has two rendering devices, the user might choose to play music on one device and to play system notification sounds on the other.</span></span>

<span data-ttu-id="a2c85-106">Da mesma forma, se um sistema contiver dois ou mais dispositivos de ponto de extremidade de captura de áudio, um dispositivo poderá ser melhor para capturar um tipo de conteúdo de áudio e outro dispositivo poderá ser melhor para capturar outro tipo de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="a2c85-106">Similarly, if a system contains two or more audio-capture endpoint devices, then one device might be best for capturing one type of audio content, and another device might be best for capturing another type of content.</span></span> <span data-ttu-id="a2c85-107">Por exemplo, se um sistema tiver dois dispositivos de captura, o usuário poderá optar por gravar música ao vivo em um dispositivo e usar o outro dispositivo para comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="a2c85-107">For example, if a system has two capture devices, the user might choose to record live music on one device and to use the other device for voice commands.</span></span>

<span data-ttu-id="a2c85-108">Os dispositivos podem ter três funções: console, comunicações e multimídia. a tabela a seguir descreve as funções de dispositivo identificadas pelas três constantes — eConsole, eCommunications e eMultimedia — na enumeração [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) .</span><span class="sxs-lookup"><span data-stu-id="a2c85-108">Devices can have three roles: Console, Communications, and Multimedia.The following table describes the device roles identified by the three constants—eConsole, eCommunications, and eMultimedia—in the [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration.</span></span>



| <span data-ttu-id="a2c85-109">Constante ERole</span><span class="sxs-lookup"><span data-stu-id="a2c85-109">ERole constant</span></span>  | <span data-ttu-id="a2c85-110">Função do dispositivo</span><span class="sxs-lookup"><span data-stu-id="a2c85-110">Device role</span></span>                              | <span data-ttu-id="a2c85-111">Exemplos de renderização</span><span class="sxs-lookup"><span data-stu-id="a2c85-111">Rendering examples</span></span>             | <span data-ttu-id="a2c85-112">Exemplos de captura</span><span class="sxs-lookup"><span data-stu-id="a2c85-112">Capture examples</span></span>                   |
|-----------------|------------------------------------------|--------------------------------|------------------------------------|
| <span data-ttu-id="a2c85-113">eConsole</span><span class="sxs-lookup"><span data-stu-id="a2c85-113">eConsole</span></span>        | <span data-ttu-id="a2c85-114">Interação com o computador</span><span class="sxs-lookup"><span data-stu-id="a2c85-114">Interaction with the computer</span></span>            | <span data-ttu-id="a2c85-115">Jogos e notificações do sistema</span><span class="sxs-lookup"><span data-stu-id="a2c85-115">Games and system notifications</span></span> | <span data-ttu-id="a2c85-116">Comandos de voz</span><span class="sxs-lookup"><span data-stu-id="a2c85-116">Voice commands</span></span>                     |
| <span data-ttu-id="a2c85-117">eCommunications</span><span class="sxs-lookup"><span data-stu-id="a2c85-117">eCommunications</span></span> | <span data-ttu-id="a2c85-118">Comunicações de voz com outra pessoa</span><span class="sxs-lookup"><span data-stu-id="a2c85-118">Voice communications with another person</span></span> | <span data-ttu-id="a2c85-119">Bate-papo e VoIP</span><span class="sxs-lookup"><span data-stu-id="a2c85-119">Chat and VoIP</span></span>                  | <span data-ttu-id="a2c85-120">Bate-papo e VoIP</span><span class="sxs-lookup"><span data-stu-id="a2c85-120">Chat and VoIP</span></span>                      |
| <span data-ttu-id="a2c85-121">eMultimedia</span><span class="sxs-lookup"><span data-stu-id="a2c85-121">eMultimedia</span></span>     | <span data-ttu-id="a2c85-122">Reprodução ou gravação de conteúdo de áudio</span><span class="sxs-lookup"><span data-stu-id="a2c85-122">Playing or recording audio content</span></span>       | <span data-ttu-id="a2c85-123">Música e filmes</span><span class="sxs-lookup"><span data-stu-id="a2c85-123">Music and movies</span></span>               | <span data-ttu-id="a2c85-124">Narração e gravação de música ao vivo</span><span class="sxs-lookup"><span data-stu-id="a2c85-124">Narration and live music recording</span></span> |



 

<span data-ttu-id="a2c85-125">Um dispositivo de renderização ou de captura específico pode ser atribuído a nenhuma, uma, algumas ou todas as funções na tabela anterior.</span><span class="sxs-lookup"><span data-stu-id="a2c85-125">A particular rendering or capture device might be assigned none, one, some, or all of the roles in the preceding table.</span></span> <span data-ttu-id="a2c85-126">A qualquer momento, cada função na tabela é atribuída a um dispositivo de renderização (e apenas um) e a um (e apenas um) dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="a2c85-126">At any time, each role in the table is assigned to one (and only one) rendering device and to one (and only one) capture device.</span></span> <span data-ttu-id="a2c85-127">Ou seja, a atribuição de funções para processar dispositivos é independente da atribuição de funções para capturar dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a2c85-127">That is, the assignment of roles to rendering devices is independent of the assignment of roles to capture devices.</span></span>

<span data-ttu-id="a2c85-128">Um aplicativo pode optar por reproduzir todos os seus fluxos de saída por meio de um único dispositivo de ponto de extremidade de renderização e registrar todos os seus fluxos de entrada de um único dispositivo de ponto de extremidade de captura.</span><span class="sxs-lookup"><span data-stu-id="a2c85-128">An application might choose to play all of its output streams through a single rendering endpoint device, and to record all of its input streams from a single capture endpoint device.</span></span> <span data-ttu-id="a2c85-129">Como alternativa, um aplicativo pode optar por reproduzir alguns dos fluxos de saída por meio de um dispositivo de renderização e reproduzir outros fluxos de saída por meio de outro dispositivo de renderização.</span><span class="sxs-lookup"><span data-stu-id="a2c85-129">Alternatively, an application might choose to play some of its output streams through one rendering device and to play other output streams through another rendering device.</span></span> <span data-ttu-id="a2c85-130">Da mesma forma, ele pode optar por registrar alguns de seus fluxos de entrada por meio de um dispositivo de captura e registrar outros fluxos de entrada por meio de outro dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="a2c85-130">Similarly, it might choose to record some of its input streams through one capture device and to record other input streams through another capture device.</span></span> <span data-ttu-id="a2c85-131">Em todos os casos, o aplicativo pode atribuir cada fluxo ao dispositivo cuja função é mais apropriada para esse fluxo.</span><span class="sxs-lookup"><span data-stu-id="a2c85-131">In all cases, the application can assign each stream to the device whose role is most appropriate for that stream.</span></span>

<span data-ttu-id="a2c85-132">Por exemplo, um aplicativo VoIP pode atribuir o fluxo de saída que contém a notificação de toque para o dispositivo de ponto de extremidade de renderização com a função eConsole.</span><span class="sxs-lookup"><span data-stu-id="a2c85-132">For example, a VoIP application might assign the output stream that contains the ring-in notification to the rendering endpoint device with the eConsole role.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2c85-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a2c85-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2c85-134">Dispositivos de ponto de extremidade de áudio</span><span class="sxs-lookup"><span data-stu-id="a2c85-134">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> <dt>

[<span data-ttu-id="a2c85-135">Trabalhando com funções de dispositivo</span><span class="sxs-lookup"><span data-stu-id="a2c85-135">Working with Device Roles</span></span>](device-roles-in-windows-vista.md)
</dt> <dt>

[<span data-ttu-id="a2c85-136">Interoperabilidade com APIs de áudio herdadas</span><span class="sxs-lookup"><span data-stu-id="a2c85-136">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



