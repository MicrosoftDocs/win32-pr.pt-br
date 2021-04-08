---
description: Modo de reprodução do VMR (alocador personalizado-apresentadores)
ms.assetid: 0381f862-2f16-4b4d-be48-40f7fe151585
title: Modo de reprodução do VMR (alocador personalizado-apresentadores)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad9cd4dcb5e5b2f1965d49c7f31b4ef8c9ebd78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662544"
---
# <a name="vmr-renderless-playback-mode-custom-allocator-presenters"></a><span data-ttu-id="cd3a5-103">Modo de reprodução do VMR (alocador personalizado-apresentadores)</span><span class="sxs-lookup"><span data-stu-id="cd3a5-103">VMR Renderless Playback Mode (Custom Allocator-Presenters)</span></span>

<span data-ttu-id="cd3a5-104">No modo de reprodução de renderização, o VMR não executa a renderização.</span><span class="sxs-lookup"><span data-stu-id="cd3a5-104">In renderless playback mode, the VMR does not perform the rendering.</span></span> <span data-ttu-id="cd3a5-105">Em vez disso, ele usa um apresentador de alocador personalizado fornecido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cd3a5-105">Instead, it uses a custom allocator-presenter supplied by the application.</span></span> <span data-ttu-id="cd3a5-106">Esse modo é útil para jogos e outros tipos de aplicativos que têm efeitos de vídeo sofisticados.</span><span class="sxs-lookup"><span data-stu-id="cd3a5-106">This mode is useful for games and other types of applications that have sophisticated video effects.</span></span> <span data-ttu-id="cd3a5-107">O modo de reprodução sem renderização permite que os aplicativos criem e controlem sua própria superfície do DirectDraw (VMR-7) ou a superfície do Direct3D (VMR-9) e acessem os bits de vídeo no momento da apresentação.</span><span class="sxs-lookup"><span data-stu-id="cd3a5-107">Renderless playback mode enables the applications to create and control its own DirectDraw surface (VMR-7) or Direct3D surface (VMR-9), and to access the video bits at presentation time.</span></span>

<span data-ttu-id="cd3a5-108">No modo de processamento, o VMR-9 não carrega automaticamente seu componente de mixer.</span><span class="sxs-lookup"><span data-stu-id="cd3a5-108">In renderless mode, the VMR-9 does not automatically load its mixer component.</span></span>

<span data-ttu-id="cd3a5-109">No modo de reprodução de renderização, o aplicativo executa as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="cd3a5-109">In renderless playback mode, the application does the following tasks:</span></span>

-   <span data-ttu-id="cd3a5-110">Gerencia a janela de reprodução.</span><span class="sxs-lookup"><span data-stu-id="cd3a5-110">Manages the playback window.</span></span>
-   <span data-ttu-id="cd3a5-111">Aloca o objeto DirectDraw ou Direct3D e o buffer de quadro final.</span><span class="sxs-lookup"><span data-stu-id="cd3a5-111">Allocates the DirectDraw or Direct3D object and the final frame buffer.</span></span>
-   <span data-ttu-id="cd3a5-112">Notifica o restante do sistema de reprodução do objeto que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="cd3a5-112">Notifies the rest of the playback system of the object being used.</span></span>
-   <span data-ttu-id="cd3a5-113">Apresenta o buffer de quadro no horário correto.</span><span class="sxs-lookup"><span data-stu-id="cd3a5-113">Presents the frame buffer at the correct time.</span></span>
-   <span data-ttu-id="cd3a5-114">Lida com todas as alterações no modo de resolução, monitore alterações e perdas de superfície.</span><span class="sxs-lookup"><span data-stu-id="cd3a5-114">Handles all resolution-mode changes, monitor changes, and surface losses.</span></span> <span data-ttu-id="cd3a5-115">Ele deve aconselhar o restante do sistema de reprodução desses eventos.</span><span class="sxs-lookup"><span data-stu-id="cd3a5-115">It must advise the rest of the playback system of these events.</span></span>

<span data-ttu-id="cd3a5-116">O VMR faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cd3a5-116">The VMR does the following:</span></span>

-   <span data-ttu-id="cd3a5-117">Manipula todo o tempo relacionado à apresentação do quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="cd3a5-117">Handles all timing related to presenting the video frame.</span></span>
-   <span data-ttu-id="cd3a5-118">Fornece informações de controle de qualidade para o aplicativo e o restante do sistema de reprodução.</span><span class="sxs-lookup"><span data-stu-id="cd3a5-118">Provides quality-control information to the application and the rest of the playback system.</span></span>
-   <span data-ttu-id="cd3a5-119">Apresenta uma interface consistente para os componentes upstream do sistema de reprodução, que não sabem que o aplicativo está fornecendo a alocação de buffer de quadro e realizando a renderização.</span><span class="sxs-lookup"><span data-stu-id="cd3a5-119">Presents a consistent interface to the upstream components of the playback system, which are not aware that the application is providing the frame buffer allocation and performing the rendering.</span></span>
-   <span data-ttu-id="cd3a5-120">Fornece qualquer combinação de fluxos de vídeo que podem ser necessários antes da renderização.</span><span class="sxs-lookup"><span data-stu-id="cd3a5-120">Provides any mixing of video streams that may be required prior to rendering.</span></span>

<span data-ttu-id="cd3a5-121">Como o desentrelaçamento é executado pelo mixer, o apresentador de alocador sempre recebe quadros desentrelaçados.</span><span class="sxs-lookup"><span data-stu-id="cd3a5-121">Because deinterlacing is performed by the mixer, the allocator-presenter always received deinterlaced frames.</span></span> <span data-ttu-id="cd3a5-122">Para obter mais informações, consulte [definindo preferências de desentrelaçamento](setting-deinterlace-preferences.md).</span><span class="sxs-lookup"><span data-stu-id="cd3a5-122">For more information, see [Setting Deinterlace Preferences](setting-deinterlace-preferences.md).</span></span>

<span data-ttu-id="cd3a5-123">Para obter mais informações sobre como fornecer um apresentador de alocador personalizado, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="cd3a5-123">For more information about providing a custom allocator-presenter, see the following topics:</span></span>

-   [<span data-ttu-id="cd3a5-124">Fornecendo um Allocator-Presenter personalizado para o VMR-7</span><span class="sxs-lookup"><span data-stu-id="cd3a5-124">Supplying a Custom Allocator-Presenter for VMR-7</span></span>](supplying-a-custom-allocator-presenter-for-vmr-7.md)
-   [<span data-ttu-id="cd3a5-125">Fornecendo um Allocator-Presenter personalizado para o VMR-9</span><span class="sxs-lookup"><span data-stu-id="cd3a5-125">Supplying a Custom Allocator-Presenter for VMR-9</span></span>](supplying-a-custom-allocator-presenter-for-vmr-9.md)
-   [<span data-ttu-id="cd3a5-126">Sincronizando o VMR com a taxa de atualização do monitor</span><span class="sxs-lookup"><span data-stu-id="cd3a5-126">Synchronizing the VMR to the Monitor's Refresh Rate</span></span>](synchronizing-the-vmr-to-the-monitors-refresh-rate.md)

 

 



