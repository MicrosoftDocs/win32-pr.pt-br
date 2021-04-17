---
description: Representa um relatório de latitude/longitude.
ms.assetid: efa8d805-8546-4bab-95a0-69e1edc28753
title: Objeto LocationDisp. DispLatLongReport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1b9629f22aee33670463b2a0832c12d520a9b8e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784105"
---
# <a name="locationdispdisplatlongreport-object"></a><span data-ttu-id="88406-103">Objeto LocationDisp. DispLatLongReport</span><span class="sxs-lookup"><span data-stu-id="88406-103">LocationDisp.DispLatLongReport object</span></span>

<span data-ttu-id="88406-104">\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="88406-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="88406-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="88406-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="88406-106">Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="88406-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="88406-107">Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="88406-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="88406-108">Representa um relatório de latitude/longitude.</span><span class="sxs-lookup"><span data-stu-id="88406-108">Represents a latitude/longitude report.</span></span>

## <a name="members"></a><span data-ttu-id="88406-109">Membros</span><span class="sxs-lookup"><span data-stu-id="88406-109">Members</span></span>

<span data-ttu-id="88406-110">O objeto **LocationDisp. DispLatLongReport** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="88406-110">The **LocationDisp.DispLatLongReport** object has these types of members:</span></span>

-   [<span data-ttu-id="88406-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="88406-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="88406-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="88406-112">Properties</span></span>

<span data-ttu-id="88406-113">O objeto **LocationDisp. DispLatLongReport** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="88406-113">The **LocationDisp.DispLatLongReport** object has these properties.</span></span>



| <span data-ttu-id="88406-114">Propriedade</span><span class="sxs-lookup"><span data-stu-id="88406-114">Property</span></span>                                                                         | <span data-ttu-id="88406-115">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="88406-115">Access type</span></span>          | <span data-ttu-id="88406-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="88406-116">Description</span></span>                                                                                                                                                                                       |
|:---------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="88406-117">**Altitude**</span><span class="sxs-lookup"><span data-stu-id="88406-117">**Altitude**</span></span>](locationdisp-displatlongreport-altitude.md)<br/>           | <span data-ttu-id="88406-118">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="88406-118">Read-only</span></span><br/> | <span data-ttu-id="88406-119">Altitude atual, em metros.</span><span class="sxs-lookup"><span data-stu-id="88406-119">Current altitude, in meters.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="88406-120">**AltitudeError**</span><span class="sxs-lookup"><span data-stu-id="88406-120">**AltitudeError**</span></span>](locationdisp-displatlongreport-altitudeerror.md)<br/> | <span data-ttu-id="88406-121">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="88406-121">Read-only</span></span><br/> | <span data-ttu-id="88406-122">Erro de altitude, em metros.</span><span class="sxs-lookup"><span data-stu-id="88406-122">Altitude error, in meters.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="88406-123">**ErrorRadius**</span><span class="sxs-lookup"><span data-stu-id="88406-123">**ErrorRadius**</span></span>](locationdisp-displatlongreport-errorradius.md)<br/>     | <span data-ttu-id="88406-124">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="88406-124">Read-only</span></span><br/> | <span data-ttu-id="88406-125">Uma distância do local relatado, em metros.</span><span class="sxs-lookup"><span data-stu-id="88406-125">A distance from the reported location, in meters.</span></span> <span data-ttu-id="88406-126">Combinado com o local relatado como a origem, esse raio descreve o círculo no qual o local real é proably localizado.</span><span class="sxs-lookup"><span data-stu-id="88406-126">Combined with the reported location as the origin, this radius describes the circle in which the actual location is proably located.</span></span><br/> |
| [<span data-ttu-id="88406-127">**Latitude**</span><span class="sxs-lookup"><span data-stu-id="88406-127">**Latitude**</span></span>](locationdisp-displatlongreport-latitude.md)<br/>           | <span data-ttu-id="88406-128">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="88406-128">Read-only</span></span><br/> | <span data-ttu-id="88406-129">Latitude atual, em graus.</span><span class="sxs-lookup"><span data-stu-id="88406-129">Current latitude, in degrees.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="88406-130">**Longitude**</span><span class="sxs-lookup"><span data-stu-id="88406-130">**Longitude**</span></span>](locationdisp-displatlongreport-longitude.md)<br/>         | <span data-ttu-id="88406-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="88406-131">Read-only</span></span><br/> | <span data-ttu-id="88406-132">Longitude atual, em graus.</span><span class="sxs-lookup"><span data-stu-id="88406-132">Current longitude, in degrees.</span></span><br/>                                                                                                                                                         |
| [<span data-ttu-id="88406-133">**Timestamp**</span><span class="sxs-lookup"><span data-stu-id="88406-133">**Timestamp**</span></span>](locationdisp-displatlongreport-timestamp.md)<br/>         | <span data-ttu-id="88406-134">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="88406-134">Read-only</span></span><br/> | <span data-ttu-id="88406-135">A data e a hora em que o relatório foi gerado.</span><span class="sxs-lookup"><span data-stu-id="88406-135">The date and time when the report was generated.</span></span><br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="88406-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="88406-136">Remarks</span></span>

<span data-ttu-id="88406-137">Você pode recuperar esse objeto por meio da propriedade [**LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md) do objeto [**LatLongReportFactory**](locationdisp-latlongreportfactory.md) .</span><span class="sxs-lookup"><span data-stu-id="88406-137">You can retrieve this object through the [**LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md) property of the [**LatLongReportFactory**](locationdisp-latlongreportfactory.md) object.</span></span> <span data-ttu-id="88406-138">Você pode receber esse objeto por meio do evento [**NewLatLongReport**](newlatlongreport.md) .</span><span class="sxs-lookup"><span data-stu-id="88406-138">You can receive this object through the [**NewLatLongReport**](newlatlongreport.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="88406-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88406-139">Requirements</span></span>



| <span data-ttu-id="88406-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="88406-140">Requirement</span></span> | <span data-ttu-id="88406-141">Valor</span><span class="sxs-lookup"><span data-stu-id="88406-141">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="88406-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88406-142">Minimum supported client</span></span><br/> | <span data-ttu-id="88406-143">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="88406-143">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="88406-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88406-144">Minimum supported server</span></span><br/> | <span data-ttu-id="88406-145">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="88406-145">None supported</span></span><br/>                  |



 

