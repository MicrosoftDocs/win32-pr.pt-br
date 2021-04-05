---
description: Os objetos WMContainer fornecem um controle de baixo nível sobre a análise e a gravação de um arquivo ASF (Advanced Systems Format).
ms.assetid: 258ea139-581f-4b94-9655-43ecf1e77f10
title: Componentes ASF WMContainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d7d1c1b76683cfe01dc0970ab1c077580215d2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921866"
---
# <a name="wmcontainer-asf-components"></a><span data-ttu-id="abdd3-103">Componentes ASF WMContainer</span><span class="sxs-lookup"><span data-stu-id="abdd3-103">WMContainer ASF Components</span></span>

<span data-ttu-id="abdd3-104">Os objetos WMContainer fornecem um controle de baixo nível sobre a análise e a gravação de um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="abdd3-104">The WMContainer objects provide low-level control over parsing and writing an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="abdd3-105">Os [componentes ASF da camada de pipeline](pipeline-layer-asf-components.md) usam os objetos WMContainer internamente.</span><span class="sxs-lookup"><span data-stu-id="abdd3-105">The [Pipeline Layer ASF Components](pipeline-layer-asf-components.md) use the WMContainer objects internally.</span></span> <span data-ttu-id="abdd3-106">A maioria dos aplicativos deve usar os componentes de pipeline, em vez de usar objetos WMContainer.</span><span class="sxs-lookup"><span data-stu-id="abdd3-106">Most applications should use the pipeline components, rather than using WMContainer objects.</span></span> <span data-ttu-id="abdd3-107">Use WMContainer somente se você precisar de controle de baixo nível sobre a análise e a gravação de um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="abdd3-107">Use WMContainer only if you require low-level control over parsing and writing an ASF file.</span></span>

<span data-ttu-id="abdd3-108">A camada WMContainer inclui os seguintes objetos:</span><span class="sxs-lookup"><span data-stu-id="abdd3-108">The WMContainer layer includes the following objects:</span></span>

-   [<span data-ttu-id="abdd3-109">Perfil ASF</span><span class="sxs-lookup"><span data-stu-id="abdd3-109">ASF Profile</span></span>](asf-profile.md)
-   [<span data-ttu-id="abdd3-110">Objeto ASF ContentInfo</span><span class="sxs-lookup"><span data-stu-id="abdd3-110">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
-   [<span data-ttu-id="abdd3-111">Divisor de ASF</span><span class="sxs-lookup"><span data-stu-id="abdd3-111">ASF Splitter</span></span>](asf-splitter.md)
-   [<span data-ttu-id="abdd3-112">Multiplexador ASF</span><span class="sxs-lookup"><span data-stu-id="abdd3-112">ASF Multiplexer</span></span>](asf-multiplexer.md)
-   [<span data-ttu-id="abdd3-113">Indexador ASF</span><span class="sxs-lookup"><span data-stu-id="abdd3-113">ASF Indexer</span></span>](asf-index-object.md)

<span data-ttu-id="abdd3-114">Os tópicos a seguir contêm instruções passo a passo sobre como usar o WMContainer para ler ou gravar arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="abdd3-114">The following topics contain step-by-step instructions about using WMContainer to read or write ASF files.</span></span>

-   [<span data-ttu-id="abdd3-115">Tutorial: lendo um arquivo ASF usando objetos WMContainer</span><span class="sxs-lookup"><span data-stu-id="abdd3-115">Tutorial: Reading an ASF File by Using WMContainer Objects</span></span>](tutorial--reading-an-asf-file.md)
-   [<span data-ttu-id="abdd3-116">Tutorial: copiando fluxos ASF usando objetos WMContainer</span><span class="sxs-lookup"><span data-stu-id="abdd3-116">Tutorial: Copying ASF Streams by Using WMContainer Objects</span></span>](tutorial--copying-asf-streams-from-one-file-to-another.md)
-   [<span data-ttu-id="abdd3-117">Tutorial: gravando um arquivo WMA usando objetos WMContainer</span><span class="sxs-lookup"><span data-stu-id="abdd3-117">Tutorial: Writing a WMA File by Using WMContainer Objects</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)

## <a name="about-wm-container"></a><span data-ttu-id="abdd3-118">Sobre o contêiner do WM</span><span class="sxs-lookup"><span data-stu-id="abdd3-118">About WM Container</span></span>

<span data-ttu-id="abdd3-119">Os objetos WMContainer interagem diretamente com objetos de arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="abdd3-119">The WMContainer objects interact directly with ASF file objects.</span></span> <span data-ttu-id="abdd3-120">O diagrama a seguir mostra a estrutura do arquivo ASF e os objetos WMContainer correspondentes.</span><span class="sxs-lookup"><span data-stu-id="abdd3-120">The following diagram shows the ASF file structure and the corresponding WMContainer objects.</span></span>

![diagrama mostrando a estrutura do arquivo ASF e os objetos do Media Foundation correspondentes](images/asf-components01.png)

<span data-ttu-id="abdd3-122">Exceto para o divisor e o multiplexador, cada um desses objetos dá suporte à análise (leitura) e à gravação de arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="abdd3-122">Except for the splitter and multiplexer, each of these objects supports both parsing (reading) and writing ASF files.</span></span> <span data-ttu-id="abdd3-123">O divisor é usado apenas para ler arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="abdd3-123">The splitter is used only for reading ASF files.</span></span> <span data-ttu-id="abdd3-124">O multiplexador é usado apenas para criar novos arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="abdd3-124">The multiplexer is used only for authoring new ASF files.</span></span>

<span data-ttu-id="abdd3-125">Todas as operações executadas por objetos WMContainer são síncronas, o que significa que elas bloqueiam o thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="abdd3-125">All operations performed by WMContainer objects are synchronous, meaning they block the calling thread.</span></span>

## <a name="related-topics"></a><span data-ttu-id="abdd3-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="abdd3-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abdd3-127">Suporte a ASF no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="abdd3-127">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



