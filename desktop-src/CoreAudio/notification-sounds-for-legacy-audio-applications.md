---
description: Sons de notificação para aplicativos de áudio herdados
ms.assetid: c5ad67d9-56fb-4bf0-aea4-5b49b0e5bf95
title: Sons de notificação para aplicativos de áudio herdados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e9ee2ef1155694e32a21779c55d290da6b3799c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500988"
---
# <a name="notification-sounds-for-legacy-audio-applications"></a><span data-ttu-id="2070a-103">Sons de notificação para aplicativos de áudio herdados</span><span class="sxs-lookup"><span data-stu-id="2070a-103">Notification Sounds for Legacy Audio Applications</span></span>

<span data-ttu-id="2070a-104">No Windows Vista, o sistema operacional atribui todos os seus sons de notificação do sistema a uma sessão de áudio de processo cruzado que é executada por meio do dispositivo de ponto de extremidade de renderização que está atualmente atribuído à [função de dispositivo](device-roles.md)eConsole.</span><span class="sxs-lookup"><span data-stu-id="2070a-104">In Windows Vista, the operating system assigns all of its system notification sounds to a cross-process audio session that plays through the rendering endpoint device that is currently assigned to the eConsole [device role](device-roles.md).</span></span> <span data-ttu-id="2070a-105">O programa de controle de volume do sistema, SNDVOL, exibe um controle deslizante de volume que é dedicado a sons de notificação do sistema.</span><span class="sxs-lookup"><span data-stu-id="2070a-105">The system volume-control program, Sndvol, displays a volume slider that is dedicated to system notification sounds.</span></span>

<span data-ttu-id="2070a-106">Alguns aplicativos reproduzem sons de notificação.</span><span class="sxs-lookup"><span data-stu-id="2070a-106">Some applications play notification sounds.</span></span> <span data-ttu-id="2070a-107">Em vez de exigir que o usuário gerencie a notificação de um aplicativo com um controle deslizante de volume separado no SNDVOL, o aplicativo pode atribuir seus sons de notificação à mesma sessão que os sons de notificação do sistema.</span><span class="sxs-lookup"><span data-stu-id="2070a-107">Instead of requiring the user to manage an application's notification sounds through a separate volume slider in Sndvol, the application can assign its notification sounds to the same session as the system notification sounds.</span></span> <span data-ttu-id="2070a-108">O controle deslizante de volume SNDVOL que controla os sons de notificação do sistema controla os sons de notificação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2070a-108">The Sndvol volume slider that controls the system notification sounds then controls the notification sounds from the application.</span></span>

<span data-ttu-id="2070a-109">Para habilitar esse comportamento, o Windows Vista define um \_ sinalizador de sistema de SND para a função de [**PlaySound**](/previous-versions//dd743680(v=vs.85)) herdada.</span><span class="sxs-lookup"><span data-stu-id="2070a-109">To enable this behavior, Windows Vista defines a SND\_SYSTEM flag for the legacy [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function.</span></span> <span data-ttu-id="2070a-110">(Esse sinalizador não tem suporte em versões anteriores do Windows, incluindo o Windows Server 2003, o Windows XP e o Windows 2000.) Se o chamador definir esse sinalizador, a função **PlaySound** atribuirá o som que ele toca à sessão de processo cruzado que o sistema operacional usa para seus sons de notificação.</span><span class="sxs-lookup"><span data-stu-id="2070a-110">(This flag is not supported in earlier versions of Windows, including Windows Server 2003, Windows XP, and Windows 2000.) If the caller sets this flag, then the **PlaySound** function assigns the sound that it plays to the cross-process session that the operating system uses for its notification sounds.</span></span> <span data-ttu-id="2070a-111">Se o chamador não definir o sinalizador, o **PlaySound** atribuirá o som que ele toca à sessão padrão — a sessão específica do processo que é identificada pelo valor GUID de sessão GUID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="2070a-111">If the caller does not set the flag, then **PlaySound** assigns the sound that it plays to the default session—the process-specific session that is identified by the session GUID value GUID\_NULL.</span></span> <span data-ttu-id="2070a-112">\_O sistema SND é definido no arquivo de cabeçalho mmsystem. h.</span><span class="sxs-lookup"><span data-stu-id="2070a-112">SND\_SYSTEM is defined in the header file Mmsystem.h.</span></span> <span data-ttu-id="2070a-113">Para obter mais informações sobre o **PlaySound**, consulte a documentação do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="2070a-113">For more information about **PlaySound**, see the Windows SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2070a-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2070a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2070a-115">Interoperabilidade com APIs de áudio herdadas</span><span class="sxs-lookup"><span data-stu-id="2070a-115">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
