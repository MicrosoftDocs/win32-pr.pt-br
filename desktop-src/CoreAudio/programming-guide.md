---
description: Saiba mais sobre os conceitos e recursos das PRINCIPAIS APIs de áudio do Windows Vista e como usá-los na programação de aplicativos.
ms.assetid: 825c7cd7-dc66-47b6-a1b6-d10101daebb3
title: Guia de programação de áudio principal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f02e27206c70cca69abf263cfa49dfd439c480
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405869"
---
# <a name="core-audio-programming-guide"></a><span data-ttu-id="5f681-103">Guia de programação de áudio principal</span><span class="sxs-lookup"><span data-stu-id="5f681-103">Core Audio Programming Guide</span></span>

<span data-ttu-id="5f681-104">Esta seção de guia explica os conceitos e os recursos das PRINCIPAIS APIs de áudio do Windows Vista e descreve como usá-los na programação de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="5f681-104">This guide section explains the concepts and features of the core audio APIs of Windows Vista, and describes how to use them in application programming.</span></span>

<span data-ttu-id="5f681-105">Esta seção contém os seguintes tópicos.</span><span class="sxs-lookup"><span data-stu-id="5f681-105">This section contains the following topics.</span></span>



| <span data-ttu-id="5f681-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="5f681-106">Topic</span></span>                                                                                                                      | <span data-ttu-id="5f681-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f681-107">Description</span></span>                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f681-108">Componentes de áudio do modo de usuário</span><span class="sxs-lookup"><span data-stu-id="5f681-108">User-Mode Audio Components</span></span>](user-mode-audio-components.md)                                                               | <span data-ttu-id="5f681-109">Por meio das interfaces de baixo nível nas APIs de áudio principais, um cliente pode acessar os componentes do sistema que gerenciam e combinam fluxos de áudio.</span><span class="sxs-lookup"><span data-stu-id="5f681-109">Through the low-level interfaces in the core audio APIs, a client can access the system components that manage and mix audio streams.</span></span>                                                                        |
| [<span data-ttu-id="5f681-110">Áudio de modo de usuário protegido (MOTION)</span><span class="sxs-lookup"><span data-stu-id="5f681-110">Protected User Mode Audio (PUMA)</span></span>](protected-user-mode-audio--puma-.md)                                                   | <span data-ttu-id="5f681-111">Descreve as atualizações do AUDIO (Modo de Usuário Protegido), o mecanismo de áudio de modo de usuário no PE (Ambiente Protegido), que fornece um ambiente mais seguro para processamento e renderização de áudio.</span><span class="sxs-lookup"><span data-stu-id="5f681-111">Describes the updates to Protected User Mode Audio (PUMA), the user-mode audio engine in the Protected Environment (PE), which provides a safer environment for audio processing and rendering.</span></span>              |
| [<span data-ttu-id="5f681-112">Dispositivos de ponto de extremidade de áudio</span><span class="sxs-lookup"><span data-stu-id="5f681-112">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)                                                                       | <span data-ttu-id="5f681-113">Um dispositivo de ponto de extremidade de áudio é uma abstração de software que permite interações amigáveis com dispositivos de áudio, como microfones e alto-falantes.</span><span class="sxs-lookup"><span data-stu-id="5f681-113">An audio endpoint device is a software abstraction that enables user-friendly interactions with audio devices such as microphones and speakers.</span></span>                                                              |
| [<span data-ttu-id="5f681-114">Sessões de áudio</span><span class="sxs-lookup"><span data-stu-id="5f681-114">Audio Sessions</span></span>](audio-sessions.md)                                                                                       | <span data-ttu-id="5f681-115">Uma sessão de áudio é uma abstração de software que permite que um cliente gerencie uma coleção de fluxos de áudio relacionados como uma única unidade.</span><span class="sxs-lookup"><span data-stu-id="5f681-115">An audio session is a software abstraction that enables a client to manage a collection of related audio streams as a single unit.</span></span>                                                                           |
| [<span data-ttu-id="5f681-116">Controles de volume</span><span class="sxs-lookup"><span data-stu-id="5f681-116">Volume Controls</span></span>](volume-controls.md)                                                                                     | <span data-ttu-id="5f681-117">O sistema integra suas configurações de volume baseadas em políticas com as configurações de volume do usuário de maneira lógica e consistente.</span><span class="sxs-lookup"><span data-stu-id="5f681-117">The system integrates its policy-based volume settings with the user's volume settings in a logical and consistent way.</span></span>                                                                                      |
| [<span data-ttu-id="5f681-118">Gerenciamento de Fluxo</span><span class="sxs-lookup"><span data-stu-id="5f681-118">Stream Management</span></span>](stream-management.md)                                                                                 | <span data-ttu-id="5f681-119">A API de Sessão de Áudio do Windows (WASAPI) fornece a um cliente um conjunto completo de métodos para criar e gerenciar fluxos de áudio.</span><span class="sxs-lookup"><span data-stu-id="5f681-119">The Windows Audio Session API (WASAPI) provides a client with a complete set of methods for creating and managing audio streams.</span></span>                                                                             |
| [<span data-ttu-id="5f681-120">Topologias de dispositivo</span><span class="sxs-lookup"><span data-stu-id="5f681-120">Device Topologies</span></span>](device-topologies.md)                                                                                 | <span data-ttu-id="5f681-121">A API DeviceTopology permite que um cliente descubra os controles de áudio que estão ao longo dos vários caminhos de dados no hardware de áudio.</span><span class="sxs-lookup"><span data-stu-id="5f681-121">The DeviceTopology API enables a client to discover the audio controls that lie along the various data paths in the audio hardware.</span></span>                                                                          |
| [<span data-ttu-id="5f681-122">Usando a interface IKsControl para acessar propriedades de áudio</span><span class="sxs-lookup"><span data-stu-id="5f681-122">Using the IKsControl Interface to Access Audio Properties</span></span>](using-the-ikscontrol-interface-to-access-audio-properties.md) | <span data-ttu-id="5f681-123">Um aplicativo de áudio especializado pode precisar usar a interface IKsControl para acessar as propriedades de um adaptador de áudio.</span><span class="sxs-lookup"><span data-stu-id="5f681-123">A specialized audio application might need to use the IKsControl interface to access the properties of an audio adapter.</span></span>                                                                                     |
| [<span data-ttu-id="5f681-124">Interoperabilidade com APIs de áudio herdado</span><span class="sxs-lookup"><span data-stu-id="5f681-124">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)                                     | <span data-ttu-id="5f681-125">Os principais recursos das PRINCIPAIS APIs de áudio no Windows Vista podem ser incorporados em aplicativos existentes que usam DirectSound, DirectShow e as funções de multimídia do Windows **waveOutXxx** e **waveInXxx.**</span><span class="sxs-lookup"><span data-stu-id="5f681-125">Key features of the core audio APIs in Windows Vista can be incorporated into existing applications that use DirectSound, DirectShow, and the Windows multimedia **waveOutXxx** and **waveInXxx** functions.</span></span> |
| [<span data-ttu-id="5f681-126">Som espacial</span><span class="sxs-lookup"><span data-stu-id="5f681-126">Spatial Sound</span></span>](spatial-sound.md)                                                                                         | <span data-ttu-id="5f681-127">Fornece diretrizes para usar o Windows Sonic, a solução de nível de plataforma da Microsoft para suporte a som espacial no Xbox e no Windows, permitindo versões de áudio surround e elevação (acima ou abaixo do ouvinte).</span><span class="sxs-lookup"><span data-stu-id="5f681-127">Provides guidance for using Windows Sonic, Microsoft’s platform-level solution for spatial sound support on Xbox and Windows, enabling both surround and elevation (above or below the listener) audio cues.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5f681-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5f681-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f681-129">APIs de áudio principais</span><span class="sxs-lookup"><span data-stu-id="5f681-129">Core Audio APIs</span></span>](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



