---
description: Construindo uma linha do tempo
ms.assetid: 4909f797-d296-4c9f-83fb-543e48bbe75d
title: Construindo uma linha do tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c16b1134eb92b3e3ac5a0f1919d7c4a2736b206
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370252"
---
# <a name="constructing-a-timeline"></a><span data-ttu-id="91a0f-103">Construindo uma linha do tempo</span><span class="sxs-lookup"><span data-stu-id="91a0f-103">Constructing a Timeline</span></span>

<span data-ttu-id="91a0f-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="91a0f-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="91a0f-105">Este artigo descreve como construir uma linha do tempo em [serviços de edição do DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="91a0f-105">This article describes how to construct a timeline in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="91a0f-106">Ele apresenta um exemplo de aplicativo de console que cria uma linha do tempo e a renderiza.</span><span class="sxs-lookup"><span data-stu-id="91a0f-106">It presents an example console application that creates a timeline and renders it.</span></span> <span data-ttu-id="91a0f-107">A linha do tempo é mínima, consistindo em um único grupo de vídeos com um clipe de origem, mas demonstra a maioria dos conceitos necessários para criar linhas de tempo mais complexas.</span><span class="sxs-lookup"><span data-stu-id="91a0f-107">The timeline is minimal, consisting of a single video group with one source clip, but it demonstrates most of the concepts needed to create more complex timelines.</span></span>

<span data-ttu-id="91a0f-108">Este artigo contém os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="91a0f-108">This article contains the following topics.</span></span>

-   [<span data-ttu-id="91a0f-109">Criando objetos de linha do tempo</span><span class="sxs-lookup"><span data-stu-id="91a0f-109">Creating Timeline Objects</span></span>](creating-timeline-objects.md)
-   [<span data-ttu-id="91a0f-110">Criando grupos, composições e faixas</span><span class="sxs-lookup"><span data-stu-id="91a0f-110">Creating Groups, Compositions, and Tracks</span></span>](creating-groups-compositions-and-tracks.md)
-   [<span data-ttu-id="91a0f-111">Configurando o tipo de mídia do grupo</span><span class="sxs-lookup"><span data-stu-id="91a0f-111">Setting the Group Media Type</span></span>](setting-the-group-media-type.md)
-   [<span data-ttu-id="91a0f-112">Adicionando uma fonte</span><span class="sxs-lookup"><span data-stu-id="91a0f-112">Adding a Source</span></span>](adding-a-source.md)
-   [<span data-ttu-id="91a0f-113">Criando uma linha do tempo: código de exemplo</span><span class="sxs-lookup"><span data-stu-id="91a0f-113">Creating a Timeline: Example Code</span></span>](creating-a-timeline--example-code.md)

## <a name="related-topics"></a><span data-ttu-id="91a0f-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="91a0f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91a0f-115">Usando os serviços de edição do DirectShow</span><span class="sxs-lookup"><span data-stu-id="91a0f-115">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



