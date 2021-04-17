---
description: Filtro do mixer de sobreposição 2
ms.assetid: 3d3871ac-518c-45a1-9e64-031f344f4527
title: Filtro do mixer de sobreposição 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22976a58b272cf04c098c102d32d154e361b8b9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105789827"
---
# <a name="overlay-mixer-2-filter"></a><span data-ttu-id="d310b-103">Filtro do mixer de sobreposição 2</span><span class="sxs-lookup"><span data-stu-id="d310b-103">Overlay Mixer 2 Filter</span></span>

<span data-ttu-id="d310b-104">O filtro Overlay Mixer 2 é idêntico ao filtro de [mixer de sobreposição](overlay-mixer-filter.md) , exceto:</span><span class="sxs-lookup"><span data-stu-id="d310b-104">The Overlay Mixer 2 filter is identical to the [Overlay Mixer](overlay-mixer-filter.md) filter, except:</span></span>

-   <span data-ttu-id="d310b-105">Ele dá suporte apenas a tipos de mídia com formatos [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="d310b-105">It supports only media types with [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats.</span></span>
-   <span data-ttu-id="d310b-106">Ele tem um mérito maior, o que permite que ele seja adicionado automaticamente a um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="d310b-106">It has a higher merit, which enables it to be added to a filter graph automatically.</span></span>

<span data-ttu-id="d310b-107">O mixer de sobreposição 2 é fornecido para que o Gerenciador do grafo de filtro o adicione ao grafo quando ele renderiza um vídeo MPEG-2 diferente de DVD.</span><span class="sxs-lookup"><span data-stu-id="d310b-107">The Overlay Mixer 2 is provided so that the Filter Graph Manager will add it to the graph when it renders non-DVD MPEG-2 video.</span></span> <span data-ttu-id="d310b-108">A opção de usar o mixer de sobreposição ou o mixer de sobreposição 2 é tratada pelo componente que cria o grafo, o Gerenciador de gráficos de filtro, o construtor de gráficos de captura ou o construtor de gráficos de DVD.</span><span class="sxs-lookup"><span data-stu-id="d310b-108">The choice of whether to use the Overlay Mixer or the Overlay Mixer 2 is handled by the component that builds the graph, either the Filter Graph Manager, the Capture Graph Builder, or the DVD Graph Builder.</span></span> <span data-ttu-id="d310b-109">Da perspectiva do aplicativo, eles são o mesmo filtro, com as mesmas interfaces e funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="d310b-109">From an application perspective, they are the same filter, with the same interfaces and functionality.</span></span>

<span data-ttu-id="d310b-110">A tabela a seguir contém informações específicas para o mixer de sobreposição 2.</span><span class="sxs-lookup"><span data-stu-id="d310b-110">The following table contains information specific to the Overlay Mixer 2.</span></span> <span data-ttu-id="d310b-111">Para todos os outros dados de filtro, consulte a documentação do mixer de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="d310b-111">For all other filter data, refer to the documentation for the Overlay Mixer.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d310b-112">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="d310b-112">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="d310b-113">Tipo de formato: Format_VIDEOINFO2</span><span class="sxs-lookup"><span data-stu-id="d310b-113">Format Type: Format_VIDEOINFO2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d310b-114">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="d310b-114">Filter CLSID</span></span></td>
<td><span data-ttu-id="d310b-115">CLSID_OverlayMixer2</span><span class="sxs-lookup"><span data-stu-id="d310b-115">CLSID_OverlayMixer2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d310b-116"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="d310b-116"><a href="merit.md">Merit</a></span></span></td>
<td><ul>
<li><span data-ttu-id="d310b-117">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="d310b-117">MERIT_UNLIKELY</span></span></li>
<li><span data-ttu-id="d310b-118">Windows Vista ou posterior: MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="d310b-118">Windows Vista or later: MERIT_DO_NOT_USE</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d310b-119">No Windows Vista ou posterior, o mérito do filtro Overlay Mixer 2 é um mérito \_ \_ não \_ usado, pois os renderizadores de vídeo mais recentes (VMR-7, VMR-9 e EVR) dão suporte a formatos **VIDEOINFOHEADER2** e, portanto, não é necessário usar o mixer de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="d310b-119">In Windows Vista or later, the merit of the Overlay Mixer 2 filter is MERIT\_DO\_NOT\_USE, because the newer video renderers (VMR-7, VMR-9, and EVR) all support **VIDEOINFOHEADER2** formats, and therefore it is not necessary to use the Overlay Mixer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d310b-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d310b-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d310b-121">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="d310b-121">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



