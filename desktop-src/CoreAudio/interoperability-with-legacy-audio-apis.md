---
description: Interoperabilidade com APIs de áudio herdadas
ms.assetid: 34939f6d-a6e4-4f7a-afa3-b1fed52b471f
title: Interoperabilidade com APIs de áudio herdadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6b9a80b55695ffcfd3ac54e871f00ea27744d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920486"
---
# <a name="interoperability-with-legacy-audio-apis"></a><span data-ttu-id="25abe-103">Interoperabilidade com APIs de áudio herdadas</span><span class="sxs-lookup"><span data-stu-id="25abe-103">Interoperability with Legacy Audio APIs</span></span>

<span data-ttu-id="25abe-104">Muitos aplicativos existentes usam APIs de áudio herdadas, como DirectSound, DirectShow e as funções de multimídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="25abe-104">Many existing applications use legacy audio APIs such as DirectSound, DirectShow, and the Windows multimedia functions.</span></span> <span data-ttu-id="25abe-105">Com apenas pequenas modificações, esses aplicativos podem ser aumentados para fazer uso de [funções de dispositivo](device-roles.md), [controles de volume de sessão](session-volume-controls.md)e outros recursos das principais APIs de áudio no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="25abe-105">With only minor modifications, these applications can be augmented to make use of [device roles](device-roles.md), [session volume controls](session-volume-controls.md), and other features of the core audio APIs in Windows Vista.</span></span>

<span data-ttu-id="25abe-106">Conforme discutido nos [componentes de áudio do modo de usuário](user-mode-audio-components.md), as principais APIs de áudio servem como base na qual as APIs de áudio de nível superior são criadas.</span><span class="sxs-lookup"><span data-stu-id="25abe-106">As discussed in [User-Mode Audio Components](user-mode-audio-components.md), the core audio APIs serve as the foundation on which higher-level audio APIs are built.</span></span> <span data-ttu-id="25abe-107">No Windows Vista, os dispositivos de áudio que os aplicativos acessam por meio de APIs de áudio herdadas como DirectSound e as funções **waveOutXxx** e **waveInXxx** do Windows Media são, de fato, [dispositivos de ponto de extremidade de áudio](audio-endpoint-devices.md) implementados pelas APIs de áudio principal.</span><span class="sxs-lookup"><span data-stu-id="25abe-107">In Windows Vista, the audio devices that applications access through legacy audio APIs such as DirectSound and the Windows media **waveOutXxx** and **waveInXxx** functions are, in fact, [audio endpoint devices](audio-endpoint-devices.md) that are implemented by the core audio APIs.</span></span> <span data-ttu-id="25abe-108">Devido a limitações inerentes nas interfaces de APIs de áudio herdadas, um aplicativo pode acessar alguns, mas não todos os recursos de dispositivos de ponto de extremidade de áudio por meio dessas interfaces.</span><span class="sxs-lookup"><span data-stu-id="25abe-108">Because of inherent limitations in the interfaces of legacy audio APIs, an application can access some but not all of the capabilities of audio endpoint devices through these interfaces.</span></span> <span data-ttu-id="25abe-109">As seções a seguir descrevem as técnicas para aprimorar os aplicativos existentes, acessando recursos adicionais dos dispositivos de ponto de extremidade de áudio diretamente por meio das APIs de áudio principal.</span><span class="sxs-lookup"><span data-stu-id="25abe-109">The following sections describe techniques for enhancing existing applications by accessing additional capabilities of audio endpoint devices directly through the core audio APIs.</span></span> <span data-ttu-id="25abe-110">Esses aprimoramentos normalmente exigem apenas pequenas alterações no código do aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="25abe-110">These enhancements typically require only minor changes to the existing application code.</span></span>

<span data-ttu-id="25abe-111">As seções a seguir descrevem como incorporar recursos das APIs de áudio principais em aplicativos existentes que usam APIs de áudio herdadas:</span><span class="sxs-lookup"><span data-stu-id="25abe-111">The following sections describe how to incorporate features of the core audio APIs into existing applications that use legacy audio APIs:</span></span>

-   [<span data-ttu-id="25abe-112">Funções de dispositivo para aplicativos DirectSound</span><span class="sxs-lookup"><span data-stu-id="25abe-112">Device Roles for DirectSound Applications</span></span>](device-roles-for-directsound-applications.md)
-   [<span data-ttu-id="25abe-113">Funções de dispositivo para aplicativos do DirectShow</span><span class="sxs-lookup"><span data-stu-id="25abe-113">Device Roles for DirectShow Applications</span></span>](device-roles-for-directshow-applications.md)
-   [<span data-ttu-id="25abe-114">Funções de dispositivo para aplicativos multimídia herdados do Windows</span><span class="sxs-lookup"><span data-stu-id="25abe-114">Device Roles for Legacy Windows Multimedia Applications</span></span>](device-roles-for-legacy-windows-multimedia-applications.md)
-   [<span data-ttu-id="25abe-115">Eventos de áudio para aplicativos de áudio herdados</span><span class="sxs-lookup"><span data-stu-id="25abe-115">Audio Events for Legacy Audio Applications</span></span>](audio-events-for-legacy-audio-applications.md)
-   [<span data-ttu-id="25abe-116">Sons de notificação para aplicativos de áudio herdados</span><span class="sxs-lookup"><span data-stu-id="25abe-116">Notification Sounds for Legacy Audio Applications</span></span>](notification-sounds-for-legacy-audio-applications.md)

## <a name="related-topics"></a><span data-ttu-id="25abe-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="25abe-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25abe-118">Funções de dispositivo</span><span class="sxs-lookup"><span data-stu-id="25abe-118">Device Roles</span></span>](device-roles.md)
</dt> </dl>

 

 



