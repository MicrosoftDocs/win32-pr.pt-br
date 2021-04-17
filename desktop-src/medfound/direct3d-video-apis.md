---
description: APIs de vídeo do Direct3D 9
ms.assetid: 2f5f46a0-f21f-4e57-9297-bad2b791da52
title: APIs de vídeo do Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7346741b5e78f052b7c895ca417735614930d35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501176"
---
# <a name="direct3d-9-video-apis"></a><span data-ttu-id="e304b-103">APIs de vídeo do Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="e304b-103">Direct3D 9 Video APIs</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e304b-104">Os aplicativos da Windows Store devem usar o Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="e304b-104">Windows Store apps must use Microsoft Direct3D 11.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="e304b-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="e304b-105">In this section</span></span>



| <span data-ttu-id="e304b-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="e304b-106">Topic</span></span>                                                                       | <span data-ttu-id="e304b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e304b-107">Description</span></span>                                                                                                                                 |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e304b-108">Proteção de Conteúdo baseado em GPU</span><span class="sxs-lookup"><span data-stu-id="e304b-108">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)<br/> | <span data-ttu-id="e304b-109">Descreve o conteúdo de vídeo – recursos de proteção que um driver de gráficos pode fornecer.</span><span class="sxs-lookup"><span data-stu-id="e304b-109">Describes video content–protection capabilities that a graphics driver can provide.</span></span><br/>                                              |
| [<span data-ttu-id="e304b-110">Suporte à sobreposição de hardware</span><span class="sxs-lookup"><span data-stu-id="e304b-110">Hardware Overlay Support</span></span>](hardware-overlay-support.md)<br/>         | <span data-ttu-id="e304b-111">Descreve como usar sobreposições de hardware no Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="e304b-111">Describes how to use hardware overlays in Direct3D 9.</span></span><br/>                                                                            |
| [<span data-ttu-id="e304b-112">Relatório de pressão de memória</span><span class="sxs-lookup"><span data-stu-id="e304b-112">Memory Pressure Reporting</span></span>](memory-pressure-reporting.md)<br/>       | <span data-ttu-id="e304b-113">O relatório de demanda de memória permite que um aplicativo do Direct3D determine quando seu conjunto de trabalho de memória de vídeo cresceu muito grande.</span><span class="sxs-lookup"><span data-stu-id="e304b-113">Memory pressure reporting enables a Direct3D application to determine when its video-memory working set has grown too large.</span></span><br/>     |
| [<span data-ttu-id="e304b-114">Interfaces de vídeo Direct3D</span><span class="sxs-lookup"><span data-stu-id="e304b-114">Direct3D Video Interfaces</span></span>](direct3d-video-interfaces.md)<br/>       | <span data-ttu-id="e304b-115">Descreve as interfaces de vídeo do Microsoft Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="e304b-115">Describes the Microsoft Direct3D 9 video interfaces.</span></span><br/>                                                                             |
| [<span data-ttu-id="e304b-116">Estruturas de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="e304b-116">Direct3D Video Structures</span></span>](direct3d-video-structures.md)<br/>       | <span data-ttu-id="e304b-117">Descreve as estruturas usadas pelas interfaces de vídeo do Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="e304b-117">Describes the structures used by the Direct3D 9 video interfaces.</span></span><br/>                                                                |
| [<span data-ttu-id="e304b-118">Enumerações de vídeo do Direct3D</span><span class="sxs-lookup"><span data-stu-id="e304b-118">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)<br/>   | <span data-ttu-id="e304b-119">Descreve as enumerações usadas pelas interfaces de vídeo do Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="e304b-119">Describes the enumerations used by the Direct3D 9 video interfaces.</span></span><br/>                                                              |
| [<span data-ttu-id="e304b-120">Comandos de Proteção de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="e304b-120">Content Protection Commands</span></span>](content-protection-commands.md)<br/>   | <span data-ttu-id="e304b-121">Lista os comandos para o método [**IDirect3DAuthenticatedChannel9:: Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .</span><span class="sxs-lookup"><span data-stu-id="e304b-121">Lists the commands for the [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) method.</span></span><br/> |
| [<span data-ttu-id="e304b-122">Consultas de Proteção de Conteúdo</span><span class="sxs-lookup"><span data-stu-id="e304b-122">Content Protection Queries</span></span>](content-protection-queries.md)<br/>     | <span data-ttu-id="e304b-123">Lista as consultas para o método [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .</span><span class="sxs-lookup"><span data-stu-id="e304b-123">Lists the queries for the [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) method.</span></span><br/>          |



 

## <a name="related-topics"></a><span data-ttu-id="e304b-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e304b-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e304b-125">Guia de programação Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e304b-125">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 




