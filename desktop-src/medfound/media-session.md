---
description: A sessão de mídia é um objeto que gerencia o fluxo de dados no pipeline. Ele pode ser usado para executar e codificar arquivos.
ms.assetid: dac99908-be90-415d-8837-2f97d573feb5
title: Sessão de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3df4597e5461788f990f620875bce946570ab97
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105798471"
---
# <a name="media-session"></a><span data-ttu-id="ab118-104">Sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="ab118-104">Media Session</span></span>

<span data-ttu-id="ab118-105">A sessão de mídia é um objeto que gerencia o fluxo de dados no pipeline.</span><span class="sxs-lookup"><span data-stu-id="ab118-105">The Media Session is an object that manages data flow in the pipeline.</span></span> <span data-ttu-id="ab118-106">Ele pode ser usado para executar e codificar arquivos.</span><span class="sxs-lookup"><span data-stu-id="ab118-106">It can be used for both playing and encoding files.</span></span>

<span data-ttu-id="ab118-107">Esta seção descreve a sessão de mídia do ponto de vista da arquitetura.</span><span class="sxs-lookup"><span data-stu-id="ab118-107">This section describes the Media Session from an architectural standpoint.</span></span> <span data-ttu-id="ab118-108">Ele contém as seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="ab118-108">It contains the following sections:</span></span>



| <span data-ttu-id="ab118-109">Tópico</span><span class="sxs-lookup"><span data-stu-id="ab118-109">Topic</span></span>                                                                                        | <span data-ttu-id="ab118-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab118-110">Description</span></span>                                                                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab118-111">Sobre a sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="ab118-111">About the Media Session</span></span>](about-the-media-session.md)                                       | <span data-ttu-id="ab118-112">Fornece uma visão geral da sessão de mídia, como um aplicativo pode criar a sessão de mídia e como a sessão de mídia gerencia o tempo de apresentação.</span><span class="sxs-lookup"><span data-stu-id="ab118-112">Provides an overview of the Media Session, how an application can create the Media Session, and how the Media Session manages presentation time.</span></span> |
| [<span data-ttu-id="ab118-113">Topologias</span><span class="sxs-lookup"><span data-stu-id="ab118-113">Topologies</span></span>](topologies.md)                                                                 | <span data-ttu-id="ab118-114">Uma topologia é um objeto que representa o fluxo de dados no pipeline.</span><span class="sxs-lookup"><span data-stu-id="ab118-114">A topology is an object that represents the flow of data in the pipeline.</span></span>                                                                        |
| [<span data-ttu-id="ab118-115">Eventos de sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="ab118-115">Media Session Events</span></span>](media-session-events.md)                                             | <span data-ttu-id="ab118-116">Descreve os eventos que um aplicativo pode receber da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="ab118-116">Describes the events that an application might receive from the Media Session.</span></span>                                                                   |
| [<span data-ttu-id="ab118-117">Como controlar os Estados de apresentação</span><span class="sxs-lookup"><span data-stu-id="ab118-117">How to Control Presentation States</span></span>](how-to-control-presentation-states.md)                 | <span data-ttu-id="ab118-118">Descreve os controles de transporte de sessão de mídia: reproduzir, pausar e parar.</span><span class="sxs-lookup"><span data-stu-id="ab118-118">Describes the Media Session transport controls: Play, Pause, and Stop.</span></span>                                                                           |
| [<span data-ttu-id="ab118-119">Usando fontes de mídia com a sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="ab118-119">Using Media Sources with the Media Session</span></span>](using-media-sources-with-the-media-session.md) | <span data-ttu-id="ab118-120">Como usar as fontes de mídia com a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="ab118-120">How to use media sources with the Media Session.</span></span>                                                                                                 |
| [<span data-ttu-id="ab118-121">Controle de taxa</span><span class="sxs-lookup"><span data-stu-id="ab118-121">Rate Control</span></span>](rate-control.md)                                                             | <span data-ttu-id="ab118-122">Descreve como controlar a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="ab118-122">Describes how to control playback rate.</span></span>                                                                                                          |
| [<span data-ttu-id="ab118-123">Gerenciamento de qualidade de vídeo</span><span class="sxs-lookup"><span data-stu-id="ab118-123">Video Quality Management</span></span>](video-quality-management.md)                                     | <span data-ttu-id="ab118-124">Descreve melhorias no pipeline de vídeo no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ab118-124">Describes improvements to the video pipeline in Windows 7.</span></span>                                                                                       |
| [<span data-ttu-id="ab118-125">Sessão de mídia do PMP</span><span class="sxs-lookup"><span data-stu-id="ab118-125">PMP Media Session</span></span>](pmp-media-session.md)                                                   | <span data-ttu-id="ab118-126">Descreve como criar a sessão de mídia dentro de um processo de caminho de mídia protegido (PMP).</span><span class="sxs-lookup"><span data-stu-id="ab118-126">Describes how to create the Media Session inside a Protected Media Path (PMP) process.</span></span>                                                           |



 

<span data-ttu-id="ab118-127">Os tópicos a seguir descrevem como usar a sessão de mídia em cenários de aplicativo específicos:</span><span class="sxs-lookup"><span data-stu-id="ab118-127">The following topics describe how to use the Media Session in specific application scenarios:</span></span>

-   [<span data-ttu-id="ab118-128">Reprodução de áudio/vídeo</span><span class="sxs-lookup"><span data-stu-id="ab118-128">Audio/Video Playback</span></span>](audio-video-playback.md)
-   [<span data-ttu-id="ab118-129">Codificando e criando arquivos</span><span class="sxs-lookup"><span data-stu-id="ab118-129">Encoding and File Authoring</span></span>](encoding-and-file-authoring.md)

## <a name="related-topics"></a><span data-ttu-id="ab118-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ab118-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab118-131">Arquitetura Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ab118-131">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="ab118-132">**IMFMediaSession**</span><span class="sxs-lookup"><span data-stu-id="ab118-132">**IMFMediaSession**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> </dl>

 

 



