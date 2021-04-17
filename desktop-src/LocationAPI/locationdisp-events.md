---
description: O modelo de objeto de API de localização fornece os seguintes eventos.
ms.assetid: c7ac0d81-ce36-4991-a0fb-6d3c6cc8efe8
title: Eventos de LocationDisp
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 55dae79305547bf4e41ee27c727ab9204eb561cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783380"
---
# <a name="locationdisp-events"></a><span data-ttu-id="c5dca-103">Eventos de LocationDisp</span><span class="sxs-lookup"><span data-stu-id="c5dca-103">LocationDisp Events</span></span>

<span data-ttu-id="c5dca-104">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="c5dca-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c5dca-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="c5dca-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="c5dca-106">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c5dca-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="c5dca-107">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="c5dca-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="c5dca-108">O modelo de objeto de API de localização fornece os seguintes eventos.</span><span class="sxs-lookup"><span data-stu-id="c5dca-108">The Location API object model provides the following events.</span></span>



| <span data-ttu-id="c5dca-109">Evento</span><span class="sxs-lookup"><span data-stu-id="c5dca-109">Event</span></span>                                                  | <span data-ttu-id="c5dca-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5dca-110">Description</span></span>                                               |
|--------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="c5dca-111">**NewCivicAddressReport**</span><span class="sxs-lookup"><span data-stu-id="c5dca-111">**NewCivicAddressReport**</span></span>](newcivicaddressreport.md) | <span data-ttu-id="c5dca-112">Ocorre quando um novo relatório de endereço cívico é gerado.</span><span class="sxs-lookup"><span data-stu-id="c5dca-112">Occurs when a new civic address report is generated.</span></span>      |
| [<span data-ttu-id="c5dca-113">**NewLatLongReport**</span><span class="sxs-lookup"><span data-stu-id="c5dca-113">**NewLatLongReport**</span></span>](newlatlongreport.md)           | <span data-ttu-id="c5dca-114">Ocorre quando um novo relatório de latitude/longitude é gerado.</span><span class="sxs-lookup"><span data-stu-id="c5dca-114">Occurs when a new latitude/longitude report is generated.</span></span> |
| [<span data-ttu-id="c5dca-115">**StatusChanged**</span><span class="sxs-lookup"><span data-stu-id="c5dca-115">**StatusChanged**</span></span>](statuschanged.md)                 | <span data-ttu-id="c5dca-116">Ocorre quando o status operacional de um relatório é alterado.</span><span class="sxs-lookup"><span data-stu-id="c5dca-116">Occurs when the operational status of a report changes.</span></span>   |



 

 

 
