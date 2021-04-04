---
title: Visão geral da interface de programação do Microsoft Agent
description: Visão geral da interface de programação do Microsoft Agent
ms.assetid: 8709441b-9739-4f11-a2de-40a5f5eefb72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad89249e064eb89d37f497fb79cb8982c79cb83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822667"
---
# <a name="microsoft-agent-programming-interface-overview"></a><span data-ttu-id="3259b-103">Visão geral da interface de programação do Microsoft Agent</span><span class="sxs-lookup"><span data-stu-id="3259b-103">Microsoft Agent Programming Interface Overview</span></span>

<span data-ttu-id="3259b-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3259b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="3259b-105">A API do Microsoft Agent fornece serviços que dão suporte à exibição e animação de caracteres animados.</span><span class="sxs-lookup"><span data-stu-id="3259b-105">The Microsoft Agent API provides services that support the display and animation of animated characters.</span></span> <span data-ttu-id="3259b-106">Implementado como um servidor de automação OLE (Component Object Model \[ com \] ), o Microsoft Agent permite que vários aplicativos, chamados de clientes ou aplicativos cliente, hospedem e acessem seus serviços de animação, entrada e saída ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="3259b-106">Implemented as an OLE Automation (Component Object Model \[COM\]) server, Microsoft Agent enables multiple applications, called clients or client applications, to host and access its animation, input, and output services at the same time.</span></span> <span data-ttu-id="3259b-107">Um cliente pode ser qualquer aplicativo que se conecta às interfaces COM do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="3259b-107">A client can be any application that connects to the Microsoft Agent's COM interfaces.</span></span>

<span data-ttu-id="3259b-108">Como um servidor COM, o Microsoft Agent é iniciado automaticamente somente quando um aplicativo cliente usa as interfaces COM e as solicitações para se conectar a ele.</span><span class="sxs-lookup"><span data-stu-id="3259b-108">As a COM server, Microsoft Agent automatically starts up only when a client application uses the COM interfaces and requests to connect to it.</span></span> <span data-ttu-id="3259b-109">Ele permanece em execução até que todos os clientes fechem suas conexões.</span><span class="sxs-lookup"><span data-stu-id="3259b-109">It remains running until all clients close their connections.</span></span> <span data-ttu-id="3259b-110">Quando nenhum cliente conectado permanece, o Microsoft Agent é encerrado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3259b-110">When no connected clients remain, Microsoft Agent automatically exits.</span></span>

<span data-ttu-id="3259b-111">Embora você possa chamar as interfaces COM do Microsoft Agent diretamente, o Microsoft Agent também inclui um controle Microsoft ActiveX.</span><span class="sxs-lookup"><span data-stu-id="3259b-111">Although you can call Microsoft Agent's COM interfaces directly, Microsoft Agent also includes a Microsoft ActiveX control.</span></span> <span data-ttu-id="3259b-112">Esse controle facilita o acesso aos serviços do Microsoft Agent a partir de linguagens de programação que dão suporte à interface do controle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="3259b-112">This control makes it easy to access Microsoft Agent's services from programming languages that support the ActiveX control interface.</span></span>

<span data-ttu-id="3259b-113">Além de dar suporte a programas autônomos escritos para o Windows, o Agent pode ser inserido no script para dar suporte a páginas da Web, desde que o navegador dê suporte à interface do ActiveX.</span><span class="sxs-lookup"><span data-stu-id="3259b-113">In addition to supporting stand-alone programs written for Windows, Agent can be scripted to support webpages, provided that the browser supports the ActiveX interface.</span></span> <span data-ttu-id="3259b-114">O Microsoft Internet Explorer inclui suporte para ActiveX, bem como linguagens de script que você pode usar para programar o agente.</span><span class="sxs-lookup"><span data-stu-id="3259b-114">Microsoft Internet Explorer includes support for ActiveX as well as scripting languages that you can use to program Agent.</span></span> <span data-ttu-id="3259b-115">Se você não estiver usando o Internet Explorer, consulte seu fornecedor ou fornecedor sobre o suporte do navegador para ActiveX.</span><span class="sxs-lookup"><span data-stu-id="3259b-115">If you are not using Internet Explorer, consult with your vendor or supplier about the browser's support for ActiveX.</span></span>

<span data-ttu-id="3259b-116">As informações a seguir fornecem uma breve visão geral das interfaces de programação para o software Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="3259b-116">The following information provides a brief overview of the programming interfaces for the Microsoft Agent software.</span></span>

-   [<span data-ttu-id="3259b-117">Serviços de animação</span><span class="sxs-lookup"><span data-stu-id="3259b-117">Animation Services</span></span>](animation-services.md)
-   [<span data-ttu-id="3259b-118">Serviços de entrada</span><span class="sxs-lookup"><span data-stu-id="3259b-118">Input Services</span></span>](input-services.md)
-   [<span data-ttu-id="3259b-119">A janela comandos de voz</span><span class="sxs-lookup"><span data-stu-id="3259b-119">The Voice Commands Window</span></span>](the-voice-commands-window.md)
-   [<span data-ttu-id="3259b-120">Serviços de saída</span><span class="sxs-lookup"><span data-stu-id="3259b-120">Output Services</span></span>](output-services.md)

 

 




