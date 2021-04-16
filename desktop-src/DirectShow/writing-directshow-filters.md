---
description: Gravando filtros do DirectShow
ms.assetid: ffbc92b2-4f45-439b-b140-49a66fc4d914
title: Gravando filtros do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2b266f3bbb9781dddcd2d0fb065b63d895a732
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757830"
---
# <a name="writing-directshow-filters"></a><span data-ttu-id="0947f-103">Gravando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="0947f-103">Writing DirectShow Filters</span></span>

<span data-ttu-id="0947f-104">Se você estiver desenvolvendo um filtro para uso em um grafo de filtro do Microsoft DirectShow, leia os artigos nesta seção.</span><span class="sxs-lookup"><span data-stu-id="0947f-104">If you are developing a filter for use in a Microsoft DirectShow filter graph, read the articles in this section.</span></span> <span data-ttu-id="0947f-105">Em geral, você não precisa ler esta seção se estiver escrevendo um aplicativo do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="0947f-105">In general, you do not have to read this section if you are writing a DirectShow application.</span></span> <span data-ttu-id="0947f-106">A maioria dos aplicativos não acessa filtros ou o grafo de filtro no nível discutido nesta seção.</span><span class="sxs-lookup"><span data-stu-id="0947f-106">Most applications do not access filters or the filter graph at the level discussed in this section.</span></span>

-   [<span data-ttu-id="0947f-107">Introdução ao desenvolvimento de filtro do DirectShow</span><span class="sxs-lookup"><span data-stu-id="0947f-107">Introduction to DirectShow Filter Development</span></span>](introduction-to-directshow-filter-development.md)
-   [<span data-ttu-id="0947f-108">Criando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="0947f-108">Building DirectShow Filters</span></span>](building-directshow-filters.md)
-   [<span data-ttu-id="0947f-109">Como os filtros se conectam</span><span class="sxs-lookup"><span data-stu-id="0947f-109">How Filters Connect</span></span>](how-filters-connect.md)
-   [<span data-ttu-id="0947f-110">Fluxo de dados para os desenvolvedores de filtro</span><span class="sxs-lookup"><span data-stu-id="0947f-110">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
-   [<span data-ttu-id="0947f-111">Threads e seções críticas</span><span class="sxs-lookup"><span data-stu-id="0947f-111">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
-   [<span data-ttu-id="0947f-112">Gerenciamento de controle de qualidade</span><span class="sxs-lookup"><span data-stu-id="0947f-112">Quality-Control Management</span></span>](quality-control-management.md)
-   [<span data-ttu-id="0947f-113">DirectShow e COM</span><span class="sxs-lookup"><span data-stu-id="0947f-113">DirectShow and COM</span></span>](directshow-and-com.md)
-   [<span data-ttu-id="0947f-114">Gravando filtros de origem</span><span class="sxs-lookup"><span data-stu-id="0947f-114">Writing Source Filters</span></span>](writing-source-filters.md)
-   [<span data-ttu-id="0947f-115">Gravando filtros de transformação</span><span class="sxs-lookup"><span data-stu-id="0947f-115">Writing Transform Filters</span></span>](writing-transform-filters.md)
-   [<span data-ttu-id="0947f-116">Escrevendo renderizadores de vídeo</span><span class="sxs-lookup"><span data-stu-id="0947f-116">Writing Video Renderers</span></span>](writing-video-renderers.md)
-   [<span data-ttu-id="0947f-117">Gravando filtros de captura</span><span class="sxs-lookup"><span data-stu-id="0947f-117">Writing Capture Filters</span></span>](writing-capture-filters.md)
-   [<span data-ttu-id="0947f-118">Expondo os formatos de captura e compactação</span><span class="sxs-lookup"><span data-stu-id="0947f-118">Exposing Capture and Compression Formats</span></span>](exposing-capture-and-compression-formats.md)
-   [<span data-ttu-id="0947f-119">Registrando um tipo de arquivo personalizado</span><span class="sxs-lookup"><span data-stu-id="0947f-119">Registering a Custom File Type</span></span>](registering-a-custom-file-type.md)
-   [<span data-ttu-id="0947f-120">Criando uma página de propriedades de filtro</span><span class="sxs-lookup"><span data-stu-id="0947f-120">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)

 

 



