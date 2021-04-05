---
description: Sobre as APIs de áudio do Windows Core
ms.assetid: 657cf75f-3d72-4a5f-ae29-299e826b2b86
title: Sobre as APIs de áudio do Windows Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30763d70bae4340436145a303763c0aad57171f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826677"
---
# <a name="about-the-windows-core-audio-apis"></a><span data-ttu-id="50f68-103">Sobre as APIs de áudio do Windows Core</span><span class="sxs-lookup"><span data-stu-id="50f68-103">About the Windows Core Audio APIs</span></span>

<span data-ttu-id="50f68-104">Esta documentação fornece informações sobre as principais APIs de áudio para a família Microsoft Windows de sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="50f68-104">This documentation provides information about Core Audio APIs for the Microsoft Windows family of operating systems.</span></span>

<span data-ttu-id="50f68-105">As principais APIs de áudio foram introduzidas no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="50f68-105">The Core Audio APIs were introduced in Windows Vista.</span></span> <span data-ttu-id="50f68-106">Este é um novo conjunto de componentes de áudio do modo de usuário que fornece aplicativos cliente com recursos de áudio aprimorados.</span><span class="sxs-lookup"><span data-stu-id="50f68-106">This is a new set of user-mode audio components provides client applications with improved audio capabilities.</span></span> <span data-ttu-id="50f68-107">Esses recursos incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="50f68-107">These capabilities include the following:</span></span>

-   <span data-ttu-id="50f68-108">Streaming de áudio de baixa latência e resistente a falhas.</span><span class="sxs-lookup"><span data-stu-id="50f68-108">Low-latency, glitch-resilient audio streaming.</span></span>
-   <span data-ttu-id="50f68-109">Confiabilidade aprimorada (muitas funções de áudio foram movidas do modo kernel para o modo de usuário).</span><span class="sxs-lookup"><span data-stu-id="50f68-109">Improved reliability (many audio functions have moved from kernel mode to user mode).</span></span>
-   <span data-ttu-id="50f68-110">Segurança aprimorada (o processamento de conteúdo de áudio protegido ocorre em um processo seguro e de baixo privilégio).</span><span class="sxs-lookup"><span data-stu-id="50f68-110">Improved security (processing of protected audio content takes place in a secure, lower-privilege process).</span></span>
-   <span data-ttu-id="50f68-111">Atribuição de funções específicas de todo o sistema (console, multimídia e comunicações) a dispositivos de áudio individuais.</span><span class="sxs-lookup"><span data-stu-id="50f68-111">Assignment of particular system-wide roles (console, multimedia, and communications) to individual audio devices.</span></span>
-   <span data-ttu-id="50f68-112">Abstração de software dos dispositivos de ponto de extremidade de áudio (por exemplo, alto-falantes, fones de ouvido e microfones) que o usuário manipula diretamente.</span><span class="sxs-lookup"><span data-stu-id="50f68-112">Software abstraction of the audio endpoint devices (for example, speakers, headphones, and microphones) that the user manipulates directly.</span></span>

<span data-ttu-id="50f68-113">As principais APIs de áudio foram aprimoradas no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="50f68-113">The Core Audio APIs have been improved in Windows 7.</span></span> <span data-ttu-id="50f68-114">Para obter mais informações sobre os aprimoramentos e novos recursos adicionados, consulte [novidades para APIs de áudio de núcleo no Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md).</span><span class="sxs-lookup"><span data-stu-id="50f68-114">For more information about the improvements and new features added, see [What's New for Core Audio APIs in Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md).</span></span>

<span data-ttu-id="50f68-115">Esta documentação descreve as principais APIs de áudio.</span><span class="sxs-lookup"><span data-stu-id="50f68-115">This documentation describes the Core Audio APIs.</span></span> <span data-ttu-id="50f68-116">Essas APIs servem como base para as seguintes APIs de nível superior:</span><span class="sxs-lookup"><span data-stu-id="50f68-116">These APIs serve as the foundation for the following higher-level APIs:</span></span>

-   <span data-ttu-id="50f68-117">DirectSound</span><span class="sxs-lookup"><span data-stu-id="50f68-117">DirectSound</span></span>
-   <span data-ttu-id="50f68-118">DirectMusic</span><span class="sxs-lookup"><span data-stu-id="50f68-118">DirectMusic</span></span>
-   <span data-ttu-id="50f68-119">Funções de **waveXxx** e **mixerXxx** multimídia do Windows</span><span class="sxs-lookup"><span data-stu-id="50f68-119">Windows multimedia **waveXxx** and **mixerXxx** functions</span></span>
-   <span data-ttu-id="50f68-120">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="50f68-120">Media Foundation</span></span>

<span data-ttu-id="50f68-121">Essas APIs de nível superior usam as principais APIs de áudio para compartilhar o acesso a dispositivos de áudio.</span><span class="sxs-lookup"><span data-stu-id="50f68-121">These higher-level APIs use the Core Audio APIs to share access to audio devices.</span></span> <span data-ttu-id="50f68-122">Media Foundation é novo no Windows Vista, enquanto o DirectSound, o DirectMusic e as funções **waveXxx** e **mixerXxx** têm suporte no Windows 98, no Windows Millennium Edition e no Windows 2000 e posterior.</span><span class="sxs-lookup"><span data-stu-id="50f68-122">Media Foundation is new with Windows Vista, whereas DirectSound, DirectMusic, and the **waveXxx** and **mixerXxx** functions are supported in Windows 98, Windows Millennium Edition, and in Windows 2000 and later.</span></span>

<span data-ttu-id="50f68-123">A maioria dos aplicativos de áudio se comunica com as APIs de nível superior em vez de se comunicar diretamente com as APIs de áudio principais.</span><span class="sxs-lookup"><span data-stu-id="50f68-123">Most audio applications communicate with the higher-level APIs instead of communicating directly with the Core Audio APIs.</span></span> <span data-ttu-id="50f68-124">Alguns exemplos de aplicativos que usam APIs de nível superior são:</span><span class="sxs-lookup"><span data-stu-id="50f68-124">Some examples of applications that use higher-level APIs are:</span></span>

-   <span data-ttu-id="50f68-125">Players de mídia</span><span class="sxs-lookup"><span data-stu-id="50f68-125">Media players</span></span>
-   <span data-ttu-id="50f68-126">Players de DVD</span><span class="sxs-lookup"><span data-stu-id="50f68-126">DVD players</span></span>
-   <span data-ttu-id="50f68-127">Jogos</span><span class="sxs-lookup"><span data-stu-id="50f68-127">Games</span></span>
-   <span data-ttu-id="50f68-128">Aplicativos de negócios, como Microsoft Office PowerPoint, que reproduzem arquivos de som</span><span class="sxs-lookup"><span data-stu-id="50f68-128">Business applications, such as Microsoft Office PowerPoint, that play sound files</span></span>

<span data-ttu-id="50f68-129">Normalmente, esses aplicativos se comunicam com as APIs DirectSound ou Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="50f68-129">Typically, these applications communicate with the DirectSound or Media Foundation APIs.</span></span>

<span data-ttu-id="50f68-130">A comunicação direta com as APIs de áudio principais pode não ser adequada para muitos aplicativos de áudio de uso geral.</span><span class="sxs-lookup"><span data-stu-id="50f68-130">Direct communication with the Core Audio APIs might not be suitable for many general-purpose audio applications.</span></span> <span data-ttu-id="50f68-131">Por exemplo, as APIs de áudio principais exigem fluxos de áudio para usar os formatos de dados nativos de um dispositivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="50f68-131">For example, the Core Audio APIs require audio streams to use an audio device's native data formats.</span></span> <span data-ttu-id="50f68-132">No entanto, os desenvolvedores de software de terceiros que estão desenvolvendo os seguintes tipos de produtos podem exigir os recursos especiais das APIs de áudio principal:</span><span class="sxs-lookup"><span data-stu-id="50f68-132">However, third-party software developers who are developing the following types of products might require the special capabilities of the Core Audio APIs:</span></span>

-   <span data-ttu-id="50f68-133">Aplicativos de áudio profissional ("áudio pro")</span><span class="sxs-lookup"><span data-stu-id="50f68-133">Professional audio ("pro audio") applications</span></span>
-   <span data-ttu-id="50f68-134">Aplicativos de comunicação em tempo real (RTC)</span><span class="sxs-lookup"><span data-stu-id="50f68-134">Real-time communication (RTC) applications</span></span>
-   <span data-ttu-id="50f68-135">APIs de áudio de terceiros</span><span class="sxs-lookup"><span data-stu-id="50f68-135">Third-party audio APIs</span></span>

<span data-ttu-id="50f68-136">Um aplicativo de "áudio pro" ou RTC pode precisar de acesso direto aos recursos de baixo nível das APIs de áudio principal para obter a latência mínima ao obter acesso exclusivo ao hardware de áudio.</span><span class="sxs-lookup"><span data-stu-id="50f68-136">A "pro audio" or RTC application might need direct access to the low-level features of the Core Audio APIs to achieve minimum latency by obtaining exclusive access to audio hardware.</span></span> <span data-ttu-id="50f68-137">Uma API de áudio de terceiros pode exigir acesso direto às APIs de áudio principais para implementar um conjunto de recursos que podem não ser totalmente suportados por qualquer API de áudio de alto nível fornecida com o Windows.</span><span class="sxs-lookup"><span data-stu-id="50f68-137">A third-party audio API might require direct access to the Core Audio APIs to implement a set of features that might not be entirely supported by any single high-level audio API that is supplied with Windows.</span></span>

<span data-ttu-id="50f68-138">Um aplicativo que usa uma API de áudio herdada para reproduzir ou gravar áudio pode exigir recursos adicionais que não têm suporte da API de áudio herdada, mas que têm suporte das APIs de áudio de núcleo.</span><span class="sxs-lookup"><span data-stu-id="50f68-138">An application that uses a legacy audio API to play or record audio might require additional capabilities that are not supported by the legacy audio API, but that are supported by the Core Audio APIs.</span></span> <span data-ttu-id="50f68-139">Em muitos casos, o aplicativo pode acessar esses recursos diretamente por meio das APIs de áudio principais, que podem ser usadas em conjunto com a API de áudio herdada.</span><span class="sxs-lookup"><span data-stu-id="50f68-139">In many cases, the application can access these capabilities directly through the Core Audio APIs, which can be used in conjunction with the legacy audio API.</span></span>

<span data-ttu-id="50f68-140">As principais APIs de áudio são:</span><span class="sxs-lookup"><span data-stu-id="50f68-140">The Core Audio APIs are:</span></span>

-   <span data-ttu-id="50f68-141">[API do dispositivo de multimídia (MMDevice)](mmdevice-api.md).</span><span class="sxs-lookup"><span data-stu-id="50f68-141">[Multimedia Device (MMDevice) API](mmdevice-api.md).</span></span> <span data-ttu-id="50f68-142">Os clientes usam essa API para enumerar os dispositivos de ponto de extremidade de áudio no sistema.</span><span class="sxs-lookup"><span data-stu-id="50f68-142">Clients use this API to enumerate the audio endpoint devices in the system.</span></span>
-   <span data-ttu-id="50f68-143">[API de sessão de áudio do Windows (WASAPI)](wasapi.md).</span><span class="sxs-lookup"><span data-stu-id="50f68-143">[Windows Audio Session API (WASAPI)](wasapi.md).</span></span> <span data-ttu-id="50f68-144">Os clientes usam essa API para criar e gerenciar fluxos de áudio de e para dispositivos de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="50f68-144">Clients use this API to create and manage audio streams to and from audio endpoint devices.</span></span>
-   <span data-ttu-id="50f68-145">[API DeviceTopology](devicetopology-api.md).</span><span class="sxs-lookup"><span data-stu-id="50f68-145">[DeviceTopology API](devicetopology-api.md).</span></span> <span data-ttu-id="50f68-146">Os clientes usam essa API para acessar diretamente os recursos do topológica (por exemplo, controles de volume e multiplexadores) que se encontram nos caminhos de dados dentro de dispositivos de hardware em adaptadores de áudio.</span><span class="sxs-lookup"><span data-stu-id="50f68-146">Clients use this API to directly access the topological features (for example, volume controls and multiplexers) that lie along the data paths inside hardware devices in audio adapters.</span></span>
-   <span data-ttu-id="50f68-147">[API EndpointVolume](endpointvolume-api.md).</span><span class="sxs-lookup"><span data-stu-id="50f68-147">[EndpointVolume API](endpointvolume-api.md).</span></span> <span data-ttu-id="50f68-148">Os clientes usam essa API para acessar diretamente os controles de volume em dispositivos de ponto de extremidade de áudio.</span><span class="sxs-lookup"><span data-stu-id="50f68-148">Clients use this API to directly access the volume controls on audio endpoint devices.</span></span> <span data-ttu-id="50f68-149">Essa API é usada principalmente por aplicativos que gerenciam fluxos de áudio de modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="50f68-149">This API is primarily used by applications that manage exclusive-mode audio streams.</span></span>

<span data-ttu-id="50f68-150">Essas APIs oferecem suporte à noção amigável de um dispositivo de ponto de extremidade, que é descrita em [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md).</span><span class="sxs-lookup"><span data-stu-id="50f68-150">These APIs support the user-friendly notion of an endpoint device, which is described in [Audio Endpoint Devices](audio-endpoint-devices.md).</span></span>

<span data-ttu-id="50f68-151">A Microsoft não planeja fazer as APIs de áudio principal descritas aqui disponíveis para uso com versões anteriores do Windows, incluindo Microsoft Windows Server 2003, Windows XP, Windows Millennium Edition, Windows 2000 e Windows 98.</span><span class="sxs-lookup"><span data-stu-id="50f68-151">Microsoft does not plan to make the Core Audio APIs that are described here available for use with earlier versions of Windows, including Microsoft Windows Server 2003, Windows XP, Windows Millennium Edition, Windows 2000, and Windows 98.</span></span>

<span data-ttu-id="50f68-152">Esta visão geral contém os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="50f68-152">This overview contains the following topics.</span></span>



| <span data-ttu-id="50f68-153">**Tópico**</span><span class="sxs-lookup"><span data-stu-id="50f68-153">**Topic**</span></span>                                                                                      | <span data-ttu-id="50f68-154">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="50f68-154">**Description**</span></span>                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50f68-155">O que há de novo para as APIs de áudio de núcleo no Windows 7</span><span class="sxs-lookup"><span data-stu-id="50f68-155">What's New for Core Audio APIs in Windows 7</span></span>](what-s-new-for-core-audio-apis-in-windows-7.md) | <span data-ttu-id="50f68-156">Resume os novos recursos e as melhorias nas APIs de áudio principais</span><span class="sxs-lookup"><span data-stu-id="50f68-156">Summarizes the new features and the improvements to the Core Audio APIs</span></span>                   |
| [<span data-ttu-id="50f68-157">Arquivos de cabeçalho e componentes do sistema</span><span class="sxs-lookup"><span data-stu-id="50f68-157">Header Files and System Components</span></span>](header-files-and-system-components.md)                   | <span data-ttu-id="50f68-158">Descreve os arquivos de cabeçalho e componentes do sistema para as APIs de áudio principal.</span><span class="sxs-lookup"><span data-stu-id="50f68-158">Describes the header files and system components for the Core Audio APIs.</span></span>                 |
| [<span data-ttu-id="50f68-159">Exemplos de SDK que usam as APIs de áudio principal</span><span class="sxs-lookup"><span data-stu-id="50f68-159">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)       | <span data-ttu-id="50f68-160">Lista os exemplos no SDK do Windows que usam as APIs de áudio principal.</span><span class="sxs-lookup"><span data-stu-id="50f68-160">Lists the samples in the Windows SDK that use the Core Audio APIs.</span></span>                        |




 

## <a name="related-topics"></a><span data-ttu-id="50f68-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="50f68-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50f68-162">APIs de áudio de núcleo</span><span class="sxs-lookup"><span data-stu-id="50f68-162">Core Audio APIs</span></span>](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



