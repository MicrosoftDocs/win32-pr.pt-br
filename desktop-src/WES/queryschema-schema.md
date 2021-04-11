---
title: Esquema de consulta
ms.assetid: 5710231b-5195-413e-8953-e47a411897a6
description: 'Saiba mais sobre: esquema de consulta'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aa9b6c842ff7acd874e8e467d07c31e298a63564
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170904"
---
# <a name="query-schema"></a><span data-ttu-id="8dd7c-103">Esquema de consulta</span><span class="sxs-lookup"><span data-stu-id="8dd7c-103">Query Schema</span></span>

<span data-ttu-id="8dd7c-104">O esquema de consulta define os seguintes elementos e tipos que você pode usar para escrever uma consulta XML estruturada para recuperar eventos de um canal ou arquivo de log:</span><span class="sxs-lookup"><span data-stu-id="8dd7c-104">The Query Schema defines the following elements and types that you can use to write a structured XML query to retrieve events from a channel or log file:</span></span>

-   [<span data-ttu-id="8dd7c-105">Elementos QuerySchema</span><span class="sxs-lookup"><span data-stu-id="8dd7c-105">QuerySchema Elements</span></span>](queryschema-elements.md)
-   [<span data-ttu-id="8dd7c-106">Tipos complexos QuerySchema</span><span class="sxs-lookup"><span data-stu-id="8dd7c-106">QuerySchema Complex Types</span></span>](queryschema-complex-types.md)

<span data-ttu-id="8dd7c-107">A seção elementos contém os nomes dos elementos que você usa em sua consulta; no entanto, para obter os detalhes de cada elemento, consulte o tipo complexo que contém o elemento.</span><span class="sxs-lookup"><span data-stu-id="8dd7c-107">The elements section contains the names of the elements that you use in your query; however, to get the details for each element, see the complex type that contains the element.</span></span>

<span data-ttu-id="8dd7c-108">Uma consulta pode conter uma ou mais expressões XPath que são usadas para incluir ou excluir o evento no conjunto de resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="8dd7c-108">A query can contain one or more XPath expressions that are used to include or exclude event in the query result set.</span></span> <span data-ttu-id="8dd7c-109">Você pode consultar eventos de vários canais ou arquivos de log, mas não pode misturar canais e arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="8dd7c-109">You can query for events from multiple channels or log files but you cannot mix channels and log files.</span></span> <span data-ttu-id="8dd7c-110">Você pode usar uma consulta em qualquer função que usa um XPath (por exemplo, as funções [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) ou [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) ).</span><span class="sxs-lookup"><span data-stu-id="8dd7c-110">You can use a query in any function that takes an XPath (for example, the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) or [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) functions).</span></span> <span data-ttu-id="8dd7c-111">Cada XPath especificado é limitado a 32 expressões.</span><span class="sxs-lookup"><span data-stu-id="8dd7c-111">Each XPath that you specify is limited to 32 expressions.</span></span> <span data-ttu-id="8dd7c-112">Para obter um exemplo, consulte [consumindo eventos](consuming-events.md).</span><span class="sxs-lookup"><span data-stu-id="8dd7c-112">For an example, see [Consuming Events](consuming-events.md).</span></span>

<span data-ttu-id="8dd7c-113">O SDK do Windows inclui o esquema no \\ arquivo include \\ Query. xsd.</span><span class="sxs-lookup"><span data-stu-id="8dd7c-113">The Windows SDK includes the schema in the \\Include\\Query.xsd file.</span></span>

<span data-ttu-id="8dd7c-114">Além do esquema de consulta, o log de eventos do Windows também define os seguintes esquemas:</span><span class="sxs-lookup"><span data-stu-id="8dd7c-114">In addition to the Query schema, Windows Event Log also defines the following schemas:</span></span>

-   <span data-ttu-id="8dd7c-115">[Esquema EventManifest](eventmanifestschema-schema.md)— define os elementos e tipos usados para escrever um manifesto de instrumentação.</span><span class="sxs-lookup"><span data-stu-id="8dd7c-115">[EventManifest Schema](eventmanifestschema-schema.md)—defines the elements and types used to write an instrumentation manifest.</span></span>
-   <span data-ttu-id="8dd7c-116">[Esquema de evento](eventschema-schema.md)— define os elementos e tipos usados para renderizar um evento.</span><span class="sxs-lookup"><span data-stu-id="8dd7c-116">[Event Schema](eventschema-schema.md)—defines the elements and types used to render an event.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8dd7c-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8dd7c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8dd7c-118">Consumindo eventos</span><span class="sxs-lookup"><span data-stu-id="8dd7c-118">Consuming Events</span></span>](consuming-events.md)
</dt> </dl>

 

 




