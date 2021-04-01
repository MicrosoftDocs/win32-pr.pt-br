---
description: O fragmento de código a seguir ilustra como solicitar e definir um endereço de multicast para uma conferência.
ms.assetid: faff57a9-88b3-45ce-bf9e-3f7087dfd1fd
title: Adquirindo um endereço multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffb451bb403002a4b2dc347abf51e587d8ea02a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090161"
---
# <a name="acquiring-a-multicast-address"></a><span data-ttu-id="cafdf-103">Adquirindo um endereço multicast</span><span class="sxs-lookup"><span data-stu-id="cafdf-103">Acquiring a Multicast Address</span></span>

<span data-ttu-id="cafdf-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="cafdf-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cafdf-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="cafdf-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="cafdf-106">O fragmento de código a seguir ilustra como solicitar e definir um endereço de multicast para uma conferência.</span><span class="sxs-lookup"><span data-stu-id="cafdf-106">The following code fragment illustrates how to request and set a multicast address for a conference.</span></span>

<span data-ttu-id="cafdf-107">Para simplificar, esse fragmento mostra a atribuição de um endereço de multicast a um item de mídia.</span><span class="sxs-lookup"><span data-stu-id="cafdf-107">For the sake of simplicity, this fragment shows the assignment of one multicast address to one media item.</span></span> <span data-ttu-id="cafdf-108">Na realidade, a seleção de um escopo, a solicitação de endereço multicast e a atribuição serão executadas para cada item de mídia envolvido na conferência.</span><span class="sxs-lookup"><span data-stu-id="cafdf-108">In actuality, the selection of a scope, the multicast address request, and the assignment will be performed for every media item involved in the conference.</span></span>

<span data-ttu-id="cafdf-109">Este fragmento pressupõe que [a conexão com um servidor ILS](connecting-to-an-ils-server.md) já foi executada.</span><span class="sxs-lookup"><span data-stu-id="cafdf-109">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed.</span></span> <span data-ttu-id="cafdf-110">As operações mostradas aqui seriam executadas na seção "modificar as configurações, se necessário", de [criar um comunicado de conferência](creating-a-conference-announcement.md).</span><span class="sxs-lookup"><span data-stu-id="cafdf-110">The operations shown here would be performed in the "Modify the settings if necessary" section of [Creating a Conference Announcement](creating-a-conference-announcement.md).</span></span>


```C++
// If ( hr != S_OK ) process the error here.
```



## <a name="related-topics"></a><span data-ttu-id="cafdf-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cafdf-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cafdf-112">Interfaces COM multicast</span><span class="sxs-lookup"><span data-stu-id="cafdf-112">Multicast COM Interfaces</span></span>](multicast-com-interfaces.md)
</dt> <dt>

[<span data-ttu-id="cafdf-113">**IMcastAddressAllocation**</span><span class="sxs-lookup"><span data-stu-id="cafdf-113">**IMcastAddressAllocation**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation)
</dt> <dt>

[<span data-ttu-id="cafdf-114">**IMcastScope**</span><span class="sxs-lookup"><span data-stu-id="cafdf-114">**IMcastScope**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope)
</dt> <dt>

[<span data-ttu-id="cafdf-115">**IMcastLeaseInfo**</span><span class="sxs-lookup"><span data-stu-id="cafdf-115">**IMcastLeaseInfo**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo)
</dt> <dt>

[<span data-ttu-id="cafdf-116">**IEnumMcastScope**</span><span class="sxs-lookup"><span data-stu-id="cafdf-116">**IEnumMcastScope**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-ienummcastscope)
</dt> <dt>

[<span data-ttu-id="cafdf-117">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="cafdf-117">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="cafdf-118">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="cafdf-118">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="cafdf-119">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="cafdf-119">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> <dt>

[<span data-ttu-id="cafdf-120">**IEnumBstr**</span><span class="sxs-lookup"><span data-stu-id="cafdf-120">**IEnumBstr**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumbstr)
</dt> <dt>

[<span data-ttu-id="cafdf-121">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="cafdf-121">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="cafdf-122">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="cafdf-122">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 



