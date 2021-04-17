---
description: A API de localização define os tipos de enumeração a seguir.
ms.assetid: a1d9d274-2861-4818-8fa1-d8d66edf27b3
title: Estruturas e tipos de enumeração (API de localização)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a73c27cb2ad6dc0dcd0c2b92f4e9ba52e98fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766255"
---
# <a name="structures-and-enumeration-types-location-api"></a><span data-ttu-id="8b0cd-103">Estruturas e tipos de enumeração (API de localização)</span><span class="sxs-lookup"><span data-stu-id="8b0cd-103">Structures and Enumeration Types (Location API)</span></span>

<span data-ttu-id="8b0cd-104">\[A API de localização Win32 está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="8b0cd-104">\[The Win32 Location API is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8b0cd-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="8b0cd-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="8b0cd-106">Em vez disso, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .</span><span class="sxs-lookup"><span data-stu-id="8b0cd-106">Instead, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.</span></span> <span data-ttu-id="8b0cd-107">\]</span><span class="sxs-lookup"><span data-stu-id="8b0cd-107">\]</span></span>

<span data-ttu-id="8b0cd-108">A API de localização define os tipos de enumeração a seguir.</span><span class="sxs-lookup"><span data-stu-id="8b0cd-108">The Location API defines the following enumeration types.</span></span>



| <span data-ttu-id="8b0cd-109">Enumeração</span><span class="sxs-lookup"><span data-stu-id="8b0cd-109">Enumeration</span></span>                                                                       | <span data-ttu-id="8b0cd-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="8b0cd-110">Description</span></span>                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="8b0cd-111">[**\_precisão desejada do local \_**](/previous-versions/windows/desktop/legacy/dd756639(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8b0cd-111">[**LOCATION\_DESIRED\_ACCURACY**](/previous-versions/windows/desktop/legacy/dd756639(v=vs.85))</span></span>                  | <span data-ttu-id="8b0cd-112">Define os tipos de precisão desejados possíveis.</span><span class="sxs-lookup"><span data-stu-id="8b0cd-112">Defines the possible desired accuracy types.</span></span>                         |
| [<span data-ttu-id="8b0cd-113">**\_status do relatório de localização \_**</span><span class="sxs-lookup"><span data-stu-id="8b0cd-113">**LOCATION\_REPORT\_STATUS**</span></span>](/windows/win32/api/locationapi/ne-locationapi-location_report_status) | <span data-ttu-id="8b0cd-114">Define o status possível para novos relatórios de um determinado tipo de relatório.</span><span class="sxs-lookup"><span data-stu-id="8b0cd-114">Defines possible status for new reports of a particular report type.</span></span> |



 

## <a name="location-constants-from-the-sensor-api"></a><span data-ttu-id="8b0cd-115">Constantes de localização da API do sensor</span><span class="sxs-lookup"><span data-stu-id="8b0cd-115">Location Constants from the Sensor API</span></span>

<span data-ttu-id="8b0cd-116">A API do sensor também define as chaves de propriedade e constantes relacionadas à localização.</span><span class="sxs-lookup"><span data-stu-id="8b0cd-116">The Sensor API also defines location-related property keys and constants.</span></span> <span data-ttu-id="8b0cd-117">As chaves de propriedade definidas em sensores. h podem ser usadas para recuperar dados de localização de um relatório chamando [**ILocationReport:: GetValue**](/windows/win32/api/locationapi/nf-locationapi-ilocationreport-getvalue).</span><span class="sxs-lookup"><span data-stu-id="8b0cd-117">The property keys defined in sensors.h can be used to retrieve location data from a report by calling [**ILocationReport::GetValue**](/windows/win32/api/locationapi/nf-locationapi-ilocationreport-getvalue).</span></span>

 

 
