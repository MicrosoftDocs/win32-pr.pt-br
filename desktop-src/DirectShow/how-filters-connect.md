---
description: Como os filtros se conectam
ms.assetid: 6a126dd5-00fa-4ea6-b00a-09b7e1246874
title: Como os filtros se conectam
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a72b2540133e84e473e3e82896a6427b923319
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105747999"
---
# <a name="how-filters-connect"></a><span data-ttu-id="a87e0-103">Como os filtros se conectam</span><span class="sxs-lookup"><span data-stu-id="a87e0-103">How Filters Connect</span></span>

<span data-ttu-id="a87e0-104">Este artigo descreve como os filtros se conectam no DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a87e0-104">This article describes how filters connect in DirectShow.</span></span> <span data-ttu-id="a87e0-105">O artigo destina-se a desenvolvedores de filtro.</span><span class="sxs-lookup"><span data-stu-id="a87e0-105">The article is intended for filter developers.</span></span> <span data-ttu-id="a87e0-106">Se você estiver escrevendo um aplicativo DirectShow, provavelmente poderá ignorar os detalhes apresentados aqui.</span><span class="sxs-lookup"><span data-stu-id="a87e0-106">If you are writing a DirectShow application, you can probably ignore the details presented here.</span></span>

<span data-ttu-id="a87e0-107">Este artigo contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="a87e0-107">This article contains the following topics:</span></span>

-   [<span data-ttu-id="a87e0-108">Fixar conexões</span><span class="sxs-lookup"><span data-stu-id="a87e0-108">Pin Connections</span></span>](pin-connections.md)
-   [<span data-ttu-id="a87e0-109">Negociando tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="a87e0-109">Negotiating Media Types</span></span>](negotiating-media-types.md)
-   [<span data-ttu-id="a87e0-110">Negociando alocadores</span><span class="sxs-lookup"><span data-stu-id="a87e0-110">Negotiating Allocators</span></span>](negotiating-allocators.md)
-   [<span data-ttu-id="a87e0-111">Fornecendo um alocador personalizado</span><span class="sxs-lookup"><span data-stu-id="a87e0-111">Providing a Custom Allocator</span></span>](providing-a-custom-allocator.md)
-   [<span data-ttu-id="a87e0-112">Reconectando Pins</span><span class="sxs-lookup"><span data-stu-id="a87e0-112">Reconnecting Pins</span></span>](reconnecting-pins.md)

## <a name="related-topics"></a><span data-ttu-id="a87e0-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a87e0-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a87e0-114">Processo de conexão do CBasePin</span><span class="sxs-lookup"><span data-stu-id="a87e0-114">CBasePin Connection Process</span></span>](cbasepin-connection-process.md)
</dt> <dt>

[<span data-ttu-id="a87e0-115">Gravando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="a87e0-115">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



