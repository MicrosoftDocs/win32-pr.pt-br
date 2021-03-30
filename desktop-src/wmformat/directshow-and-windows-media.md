---
title: DirectShow e Windows Media
description: DirectShow e Windows Media
ms.assetid: e2ddc781-9f56-4f77-a191-015018755eff
keywords:
- SDK do Windows Media Format, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- DirectShow, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4ca8eb4b1051d6685efa0bf73052ad9e7b31fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637140"
---
# <a name="directshow-and-windows-media"></a><span data-ttu-id="887d2-107">DirectShow e Windows Media</span><span class="sxs-lookup"><span data-stu-id="887d2-107">DirectShow and Windows Media</span></span>

<span data-ttu-id="887d2-108">Como alternativa ao uso exclusivo do Windows Media Format SDK, os aplicativos também podem ler e gravar o conteúdo baseado no Windows Media usando a arquitetura de streaming do Microsoft® DirectShow®, conforme descrito nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="887d2-108">As an alternative to using the Windows Media Format SDK exclusively, applications can also read and write Windows Media-based content by using the Microsoft® DirectShow® streaming architecture, as described in the following sections.</span></span>



| <span data-ttu-id="887d2-109">Seção</span><span class="sxs-lookup"><span data-stu-id="887d2-109">Section</span></span>                                                                                   | <span data-ttu-id="887d2-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="887d2-110">Description</span></span>                                                                                                                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="887d2-111">Sobre o DirectShow</span><span class="sxs-lookup"><span data-stu-id="887d2-111">About DirectShow</span></span>](about-directshow.md)                                                  | <span data-ttu-id="887d2-112">Descreve o DirectShow em termos gerais e informa onde obter mais informações sobre ele.</span><span class="sxs-lookup"><span data-stu-id="887d2-112">Describes DirectShow in general terms and tells where to get more information about it.</span></span>                                                     |
| [<span data-ttu-id="887d2-113">Por que usar o DirectShow?</span><span class="sxs-lookup"><span data-stu-id="887d2-113">Why Use DirectShow?</span></span>](why-use-directshow.md)                                             | <span data-ttu-id="887d2-114">Descreve como o DirectShow simplifica determinadas tarefas na criação e na reprodução de conteúdo baseado no Windows Media.</span><span class="sxs-lookup"><span data-stu-id="887d2-114">Describes how DirectShow simplifies certain tasks in the creation and playback of Windows Media–based content.</span></span>                              |
| [<span data-ttu-id="887d2-115">Lendo arquivos ASF no DirectShow</span><span class="sxs-lookup"><span data-stu-id="887d2-115">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)                    | <span data-ttu-id="887d2-116">Descreve como reproduzir arquivos ASF usando o DirectShow.</span><span class="sxs-lookup"><span data-stu-id="887d2-116">Describes how to play ASF files using DirectShow.</span></span>                                                                                           |
| [<span data-ttu-id="887d2-117">Criando arquivos ASF no DirectShow</span><span class="sxs-lookup"><span data-stu-id="887d2-117">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)                  | <span data-ttu-id="887d2-118">Descreve como criar arquivos ASF usando o DirectShow.</span><span class="sxs-lookup"><span data-stu-id="887d2-118">Describes how to create ASF files using DirectShow.</span></span>                                                                                         |
| [<span data-ttu-id="887d2-119">\_Notificação de eventos de status do WMT no DirectShow</span><span class="sxs-lookup"><span data-stu-id="887d2-119">WMT\_STATUS Event Notification in DirectShow</span></span>](wmt-status-notification-in-directshow.md) | <span data-ttu-id="887d2-120">Descreve quais eventos de **\_ status de WMT** são tratados pelo leitor de ASF e filtros do gravador ASF e como os aplicativos podem receber esses eventos.</span><span class="sxs-lookup"><span data-stu-id="887d2-120">Describes which **WMT\_STATUS** events are handled by the ASF Reader and ASF Writer filters, and how applications can receive those events.</span></span> |
| [<span data-ttu-id="887d2-121">Suporte a DRM no DirectShow</span><span class="sxs-lookup"><span data-stu-id="887d2-121">DRM Support in DirectShow</span></span>](drm-support-in-directshow.md)                                | <span data-ttu-id="887d2-122">Descreve como ler e gravar arquivos protegidos por DRM por meio do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="887d2-122">Describes how to read and write DRM-protected files through DirectShow.</span></span>                                                                     |
| [<span data-ttu-id="887d2-123">Referência do QASF do DirectShow</span><span class="sxs-lookup"><span data-stu-id="887d2-123">DirectShow QASF Reference</span></span>](directshow-qasf-reference.md)                                | <span data-ttu-id="887d2-124">Contém a documentação de referência para os componentes do DirectShow que dão suporte ao Windows Media.</span><span class="sxs-lookup"><span data-stu-id="887d2-124">Contains the reference documentation for the DirectShow components that support Windows Media.</span></span>                                              |



 

<span data-ttu-id="887d2-125">Três aplicativos de exemplo no SDK ilustram o uso do DirectShow: DSCopy, DSPlay e DSSeekFM.</span><span class="sxs-lookup"><span data-stu-id="887d2-125">Three sample applications in the SDK illustrate the use of DirectShow: DSCopy, DSPlay, and DSSeekFM.</span></span> <span data-ttu-id="887d2-126">Para obter mais informações, consulte [aplicativos de exemplo](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="887d2-126">For more information, see [Sample Applications](sample-applications.md).</span></span>

> [!Note]  
> <span data-ttu-id="887d2-127">Os aplicativos que usam os componentes QASF incluídos neste SDK exigem que o Microsoft DirectX® 8,1 ou o tempo de execução do SDK posterior seja instalado nos sistemas Windows® 2000, Windows 98 e Windows 95.</span><span class="sxs-lookup"><span data-stu-id="887d2-127">Applications that use the QASF components included in this SDK require the Microsoft DirectX® 8.1 or later SDK runtime to be installed on Windows® 2000, Windows 98, and Windows 95 systems.</span></span> <span data-ttu-id="887d2-128">Especificamente, esse tempo de execução é exigido pelo filtro de invólucro do DMO que hospeda os codecs de mídia do Windows em um grafo de filtro do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="887d2-128">Specifically, this runtime is required by the DMO Wrapper filter which hosts the Windows Media codecs in a DirectShow filter graph.</span></span>

 

 

 




